# LF5.4.5: Containerization with Docker CE

<details>
<summary>Briefing</summary>

## User Story

As a DevOps Engineer, **I** want to containerize an application using Docker CE, so that **I** can package my software with all its dependencies into an isolated, universally runnable unit.

## Celebration Criteria

- **I can contrast** a Docker Container with a traditional Virtual Machine (VM). (K2)
- **I know how to define** the instructions within a Dockerfile. (K3)
- **I can build** a Docker Image and run it as a Container. (K3)

## Knowledge Briefing

"It works on my machine" is the oldest excuse in IT. Docker solves this by packaging code, runtime, and libraries into a standard unit called a container.

**1\. VMs vs. Containers:**

- **Virtual Machine (VM):** Simulates entire hardware. Runs a full, heavy "Guest OS" on top of a Hypervisor.
- **Container:** Shares the Host OS kernel. It is extremely lightweight, fast to start, and only contains the app and its exact dependencies.

**2\. The Docker Trinity:**

- **Dockerfile:** The recipe (a simple text file). Contains instructions like `FROM ubuntu`, `COPY code.py /app`, `CMD ["python", "code.py"]`.
- **Image:** The baked cake. An immutable, read-only template created by running `docker build` on the Dockerfile.
- **Container:** The running instance. Created by executing `docker run` on an Image.

## Common Pitfalls

- Confusing an Image with a Container. You _build_ an Image (the static template), and you _run_ a Container (the active process).

## Mandatory Tasks

1. Explain the primary architectural difference between a Docker Container and a Virtual Machine regarding the Operating System kernel. (K2)
2. Define the terms "Dockerfile", "Docker Image", and "Docker Container". (K1)
3. State the purpose of the `FROM` instruction at the very beginning of a Dockerfile. (K2)
4. Write down the exact terminal command used to build an image named "my-app" from a Dockerfile in the current directory. (K3)
5. Write down the exact terminal command used to start a container from the "my-app" image. (K3)

## Optional Tasks

1. Analyze why stateless design is considered a best practice for applications running inside Docker containers. (K4)
2. Evaluate the security risks of running a Docker container in `--privileged` mode. (K5)
3. Design a Dockerfile for a Python application that uses a lightweight "Alpine Linux" base image and installs required packages via a `requirements.txt` file. (K6)

## 📺 Web Search Term Liste

| Topic / Term | Recommended Platform | Exact Search Term |
| --- | --- | --- |
| Docker Basics | YouTube | "Docker in 100 Seconds" |
| Containers vs VMs | Studyflix / YouTube | "Docker Container vs Virtual Machine" |
| Dockerfile Instructions | Google | "Dockerfile reference guide" |

</details>

## Answers

### M1: Explain the primary architectural difference between a Docker Container and a Virtual Machine regarding the Operating System kernel. (K2)

A **Virtual Machine** emulates complete hardware and runs its own full emulated **Guest OS** - meaning every VM carries an **entire operating system** (kernel, system libraries, init process, the works) regardless of how small the actual application inside it is. A **Windows Server VM** weighs several **gigabytes** before your application even starts.

A **Docker Container** takes a fundamentally different approach: it **shares the Host OS kernel** directly. The container only contains the application itself plus its exact runtime dependencies - no duplicate kernel, no duplicate OS layer.

|     | Virtual Machine | Docker Container |
| --- | --- | --- |
| OS kernel | Own Guest OS kernel per VM | Shared Host OS kernel |
| Managed by | Hypervisor (Type 1 or 2) | Container runtime (Docker Engine) |
| Startup time | Minutes (OS boot sequence) | Seconds (process start) |
| Typical size | Gigabytes | Megabytes |
| Isolation level | Strong (hardware emulation) | Process-level isolation |

**Analogy:**  
A VM is like renting an entire apartment - you get your own kitchen, bathroom, and entrance, but you're also paying for all that infrastructure even if you only need a desk. A container is like renting a desk in a co-working space - shared building, shared infrastructure, but your work is isolated and you only bring what you actually need.

---

### M2: Define the terms "Dockerfile", "Docker Image", and "Docker Container". (K1)

- **Dockerfile** - a plain text file containing the **build instructions** for an image. Line by line, it tells Docker what base to start from, which files to copy in, which commands to run, and how to start the application. Think of it as the recipe/blueprint.
- **Docker Image** - the read-only, **immutable artifact** produced by running `docker build` on a Dockerfile. It is a layered snapshot of the filesystem at build time - the baked result of following the recipe. Images are what you store, share, and push to registries like DockerHub.
- **Docker Container** - a running instance of an image. When you execute `docker run`, Docker takes an image and starts it as a live process with its own isolated filesystem, network interface, and process space. Multiple containers can run from the same image simultaneously, each completely **independent**.

**Analogy:**  
_Dockerfile_ = recipe card. _Image_ = the sealed, packaged meal ready to reheat. _Container_ = the meal actually on your plate, being eaten.

---

### M3: State the purpose of the `FROM` instruction at the very beginning of a Dockerfile. (K2)

`FROM` defines the **base image** - the _starting point_ that all subsequent instructions build on top of. Every Dockerfile must begin with it.

```dockerfile
FROM ubuntu:24.04
```

Rather than building from absolute zero (which would mean manually configuring a kernel, filesystem, package manager, and runtime from scratch), you start from an existing, maintained image and add only what your application needs. **Common base choices:**

- `ubuntu:24.04` - a full general-purpose Linux environment
- `python:3.12-slim` - minimal Debian with Python pre-installed
- `alpine:3.20` - a ~5 MB minimal Linux, preferred when size matters

The base image determines what tools, libraries, and package managers are available to every instruction that follows. Choosing the wrong base is one of the most _common sources of bloated_ _images_ and _unexpected security vulnerabilities_.

---

### M4: Write down the exact terminal command used to build an image named "my-app" from a Dockerfile in the current directory. (K3)

```bash
docker build -t my-app .
```

- `docker build` - invokes the build process
- `-t my-app` - tags the resulting image with the name `my-app` (short for `--tag`). Without `-t`, Docker creates what is known as an unnamed or dangling image, resulting in a non-human readable name (ID).
- `.` - the **build context**: the current directory. Docker sends everything in this directory to the Docker Engine and looks for the `Dockerfile` there

The full tag format is `name:version`, so in practice you'd often write `-t my-app:1.0` or `-t my-app:latest`. Without a version tag, Docker defaults to `:latest`.

---

### M5: Write down the exact terminal command used to start a container from the "my-app" image. (K3)

```bash
docker run my-app
```

In practice, you'll almost always add flags and/or options:

```bash
docker run -d -p 8080:5000 --name my-running-app my-app
```

- `-d` - detached mode: runs in the background, returns the terminal immediately
- `-p 8080:5000` - maps port 5000 inside the container to port 8080 on the host (without this, the container's network is invisible from outside)
- `--name my-running-app` - gives the container a human-readable name instead of a random auto-generated one

The **distinction from M2** matters here: `docker run` doesn't modify the image. The **image stays immutable**. The container is a new, separate running instance layered on top of it.

---

### O1: Analyze why stateless design is considered a best practice for applications running inside Docker containers. (K4)

A container's filesystem is **ephemeral (non-persistent) by default** - when a container is stopped and removed, everything written inside it since it started is gone. Stateless design turns this from a liability into a strength by ensuring the application itself generates no persistent state that lives inside the container.

**What "stateless" means in practice:** The application processes requests purely based on what comes in and what it can read from external services - it doesn't write anything to its local disk that the next request will depend on. User sessions go in Redis (Remote Dictionary Server). Files go in S3 (Simple Storage Service → see also: “buckets”) or a mounted volume. Database records go in an external database. The container itself stays clean.

**Why this matters for containers specifically:**

1. **Horizontal scaling becomes trivial.** If a container holds no local state, you can start 10 identical containers behind a load balancer and any request can go to any container. With stateful containers, a user's session might only exist on container 3 - and suddenly you need sticky routing, which defeats the purpose of scaling.
2. **Crash recovery is automatic.** Orchestrators like Kubernetes monitor containers and restart failed ones. If the replacement container starts fresh with no local state, it's immediately operational. If it had local state, that state is lost on crash and the new container starts broken.
3. **Immutable deployments.** A new version of the app means building a new image and swapping out containers. If no state lives in the container, the swap is clean and reversible - just run the old image again if something breaks.
4. **Container interchangeability.** The core promise of Docker is "runs the same everywhere." Local state breaks this: a container that has been running for two weeks has accumulated two weeks of local history that a freshly started container doesn't have. They're no longer equivalent.

The trade-off is architectural complexity: stateless containers require external services for everything that would otherwise be trivially stored locally. A database, a cache, an object store, and a session backend are all now required dependencies. This is a deliberate exchange - you're trading local simplicity for distributed resilience. Of course, this also means that there might be external dependencies that might cause trouble, especially if those change and/or update.

---

### O2: Evaluate the security risks of running a Docker container in `--privileged` mode. (K5)

By **default**, Docker runs containers with a **restricted capability set** - a container process cannot load kernel modules, modify network interfaces on the host, access raw hardware devices, or call most privileged system calls. This is the isolation that makes containers safe to co-locate.

`--privileged` removes almost all of those restrictions in one flag:

```bash
docker run --privileged my-app # pretty much disables container isolation
```

This creates a high-risk scenario.

**Concrete attack surfaces opened by** `--privileged`**:**

1. **Full host filesystem access.** A privileged container can mount the host's root filesystem: `mount /dev/sda1 /mnt` gives read/write access to every file on the physical disk - including `/etc/shadow`, SSH keys, and TLS certificates.
2. **Kernel module loading.** `insmod` works inside a privileged container. An attacker can load a malicious kernel module that operates at the highest privilege level on the host machine, completely outside the container abstraction.
3. **Container escape via** `nsenter`**.** The `nsenter` tool can be used to enter the host's network or process namespace from a privileged container. At that point, the "container" boundary is purely nominal.
4. **Host network manipulation.** iptables rules, routing tables, and network interfaces on the host become modifiable. An attacker could reroute or intercept all network traffic passing through the host.
5. **Multi-tenant risk multiplication.** On a shared Kubernetes cluster, a single privileged container can potentially affect every other workload on the same node - what starts as a compromised container becomes a compromised node.

**When** `--privileged` **is legitimately used:**

- Running _Docker-in-Docker (DinD)_ for CI pipelines - though rootless alternatives exist
- Certain _hardware access scenarios_ (GPU passthrough, custom device drivers)
- _Kubernetes node-level agents_ that need to interact with the host

:::warning
In **all cases**, the correct question before using `--privileged` is: **can this be achieved with a targeted capability grant instead**? E.g. `--cap-add SYS_PTRACE` is far safer than `--privileged` if that's the only capability you actually need.
:::

_Source(s): docs.docker.com/engine/reference/run/#runtime-privilege-and-linux-capabilities; bsi.bund.de/IT-Grundschutz (SYS.1.6)._

---

### O3: Design a Dockerfile for a Python application that uses a lightweight "Alpine Linux" base image and installs required packages via a `requirements.txt` file. (K6)

**This example is auto-generated and manually verified:**

```dockerfile
# Stage: runtime image
FROM python:3.12-alpine

# Metadata - good practice for maintainability
LABEL maintainer="devops@example.com"
LABEL version="1.0"

# Set working directory inside the container
WORKDIR /app

# Copy dependency list first - Docker layer caching means this layer
# is only rebuilt when requirements.txt changes, not on every code change
COPY requirements.txt .

# Install dependencies
# --no-cache: don't store the apk index on disk (keeps image smaller)
# gcc musl-dev: common build dependencies some Python packages need on Alpine
RUN apk add --no-cache gcc musl-dev \
    && pip install --no-cache-dir -r requirements.txt \
    && apk del gcc musl-dev

# Copy the application source code
COPY . .

# Run as a non-root user - security best practice
RUN adduser -D appuser
USER appuser

# Document which port the app listens on (informational, does not publish it)
EXPOSE 8000

# Default command to start the application
CMD ["python", "app.py"]
```

A matching `requirements.txt` might look like:

```
flask==3.1.0
gunicorn==22.0.0
requests==2.32.3
```

**Design decisions worth noting:**

- `python:3.12-alpine` **vs** `python:3.12` - the Alpine-based image is roughly 50 MB vs 900+ MB for the Debian-based default. Smaller image = faster pulls, less disk use, and a reduced attack surface (fewer pre-installed packages that could contain vulnerabilities). Westermann's Kap. 4.8 notes this philosophy directly: "Betriebssysteme müssen so schlank wie möglich und nur so groß wie nötig sein."
- `COPY requirements.txt .` **before** `COPY . .` - Docker builds images in layers. Each instruction creates a new layer, and layers are cached. By copying and installing dependencies _before_ copying the source code, you ensure that the expensive `pip install` layer is reused on every subsequent build - unless `requirements.txt` itself changes. Copying everything first would invalidate the cache on every single code change.
- **Build dependency cleanup** (`apk del gcc musl-dev`) - some Python packages with C extensions (e.g. `cryptography`, `psycopg2`) need a compiler at build time but not at runtime. Installing, building, then deleting the compiler tools keeps the final image clean.
- **Non-root user (**`USER appuser`**)** - containers run as root by default, which means a successful exploit inside the container immediately has root. Running as an unprivileged user limits the blast radius considerably - one of the explicit protective measures from Westermann LF1-5, Kap. 5.4.6.
- `--no-cache-dir` **for pip** - prevents pip from storing downloaded wheel files in the image, saving space.