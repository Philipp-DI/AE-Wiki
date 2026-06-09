# LF5.3: Development Tools & Version Control

<details>
<summary>Briefing</summary>

## 👥 Epic User Story

> As IT Consultants,  
> we want to set up a professional, collaborative development environment and establish strict version control workflows,  
> so that we can securely build, track, and deploy the software prototype for our chosen scenario without chaotic file conflicts.

## 🎉 Celebration Criteria (Core Competencies)

- We can **differentiate** between basic text editors, Integrated Development Environments (IDEs), compilers, and interpreters. (K4)
- We **know how to initialize** a Git repository and execute fundamental commands (add, commit, push, pull). (K3)
- We can **evaluate** and establish a branching strategy (like Git Flow or Trunk-based) suitable for our team size. (K5)
- We can **set up** a shared GitHub repository and document our setup process in Docmost. (K4)

## 🧩 Comprehensive Task: The Workshop Setup (8 SP)

**The Mission:** Your architectural blueprint is complete. Now, before writing the actual code for the Neustadt Museum, Mutti's Bakery, or the Metropolis Library, you must prepare your digital workshop. You will configure your IDE, establish a Git repository on GitHub, and agree on a branching workflow to avoid merge conflicts.

### **Tasks**

1. **Tool Selection & Setup:** Open your Ubuntu 24.04 environment. Start VSCode. Install necessary extensions for your upcoming work (e.g., Python, MarkdownLint, GitLens). Document why you chose VSCode over a simple text editor like `nano` in your Docmost instance.
2. **Analog Workflow Planning:** On a whiteboard, sketch the Git workflow your team will use (e.g., Feature Branch Workflow). Draw the `main` branch and show how a team member branches off, commits, and merges back. Take a photo of this agreement.
3. **Repository Initialization:** One team member creates a new public repository on GitHub named after your chosen scenario (e.g., `metropolis-library-prototype`). Initialize it with a `README.md` and a `.gitignore` file suitable for Python.
4. **Team Collaboration:** The creator invites the other team members as collaborators to the GitHub repository. Every team member must successfully `git clone` the repository to their local Ubuntu machine.
5. **The First Commit:** Every team member creates their own feature branch (e.g., `feature/docs-setup`). Everyone creates a simple markdown file with their name in a specific folder, commits the change, pushes the branch, and creates a Pull Request (PR) on GitHub. Review and merge all PRs into `main`.

## **📦 Result Artifact**

A fully functional, shared GitHub repository containing the first merged files, alongside a Docmost page detailing your team's Git workflow and IDE setup, including the analog workflow sketch.

</details>

### T1: Tools Selection & Setup

**Why VSCode instead of Nano?**

|     |     |     |
| --- | --- | --- |
| **Merkmal** | **Nano** | **VS Code** |
| **Learning Curve** | Flat (easy) | Steep (complex) |
| **Functionality** | Basic Text-Editor | Fully-fledged IDE |
| **Ressource Demand** | Minimal | Higher |
| **Main Usage** | Quick changes (e.g. Console) | Extensive Software-Engineering |
| **Extensibility** | None | Expansive library of extensions |

For instance, Nano is an excellent tool for a simple, quick-to-edit file. However, for more complex tasks, it becomes—comparatively speaking—a chore. Even without extensions, VSCode offers a multitude of features that significantly streamline the process of working with code and similar content. In particular, the ability to maintain an overview of an entire project structure directly within VSCode is invaluable for a focused and efficient workflow.

**Recommended Basic Extensions**

|     |     |     |
| --- | --- | --- |
| **Extension** | **Type** | **Why?** |
| **Python (Microsoft)** | Language | Mandatory Language Support for Python and its Debugging. |
| **Pylance** | Analysis | Checks for errors—live, before the code runs and includes some guidance. |
| **Ruff** | Formatting & Linting | Automatically formats code and resolves minor errors, such as flawed syntax and typos—helps to create a homogenous code structure, even within teams where everyone has their own coding style. |
| **GitLens** | Workflow | Shows changes within the line—helps to find errors. |
| **Error Lens** | Feedback | Puts error notifications in the line instead of just within the console’s output. |