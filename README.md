## Code-LS Utility

A simple bash utility designed to quickly open all subfolders within a specified parent directory using VS Code (`code`).

### Usage

The `code-ls` script requires one argument: the path to the parent directory containing the folders you wish to open. It will open each detected subdirectory in a new instance of Visual Studio Code, allowing you to navigate multiple parts of your project simultaneously.

**Syntax:**
```bash
./code-ls <path_to_parent_directory>
```

**Examples:**

*   **Open subfolders in the current directory:**
    ```bash
    ./code-ls . 
    ```
*   **Open subfolders within a specific project path:**
    ```bash
    ./code-ls /path/to/my/project
    ```

---

### Installation

To make `code-ls` accessible from anywhere on your system, follow these steps:

**1. Save the scripts:**
Ensure you have the `code-ls` and the `install` script in a known location (e.g., your project root).

**2. Run the Install Script:**
Execute the helper script to copy the main binary to your user's local bin directory (`~/.local/bin`).
```bash
./install
```
*This copies `code-ls` to `~/.local/bin/*`.*

**3. Update Your PATH (Crucial Step):**
For the system to recognize this new command, you **must** ensure that `~/.local/bin` is included in your system's `$PATH`. The installation script provides specific suggestions for common shell profiles (`.bashrc`, `.zshrc`).

After modifying your profile file by adding the necessary export line, remember to source it or restart your terminal:
```bash
source ~/.bashrc  # Use the appropriate source command for your shell (e.g., .zshrc)
```