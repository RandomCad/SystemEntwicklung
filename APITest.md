# API Test
The use of the REST API is possible with curl, the GitHub CLI and JavaScript.  
Most of the operations of the API need authentication. If u wont too use plain http request you will need a personal access token. Throw this it is possible to set what actions a specific script has.  

## The GitHub Command Line Interface (CLI) Use Cases

The GitHub Command Line Interface (CLI), often referred to as `gh`, offers a variety of use cases that streamline interactions with GitHub directly from the terminal. Here are some common use cases:

### 1. **Repository Management**
   - **Creating Repositories**: `gh repo create` allows for quick repository creation directly from the terminal.
   - **Cloning Repositories**: `gh repo clone` helps in cloning repositories without visiting GitHub in the browser.
   - **Viewing Repository Information**: Retrieve details about repositories using commands like `gh repo view`.

### 2. **Issue and Pull Request Management**
   - **Creating Issues and Pull Requests**: Create issues or pull requests with `gh issue create` or `gh pr create`.
   - **Listing and Viewing Issues/PRs**: Get a list of issues or pull requests and view details directly in the terminal.

### 3. **Workflow Automation**
   - **Interacting with Actions**: Trigger workflows, list runs, and view logs using `gh workflow`.

### 4. **Collaboration**
   - **Managing Collaborators**: Add or remove collaborators from repositories with `gh repo collaborator`.

### 5. **Reviewing and Merging**
   - **Review Pull Requests**: Review and comment on pull requests using `gh pr review`.
   - **Merging Pull Requests**: Merge pull requests via the CLI with commands like `gh pr merge`.

### 6. **GitHub Gists**
   - **Creating and Managing Gists**: Create, view, edit, and delete gists using commands like `gh gist create` or `gh gist list`.

### 7. **Authentication and Configuration**
   - **Authentication**: Authenticate with GitHub via the CLI using `gh auth login`.
   - **Configuration**: Adjust various settings and configurations for the CLI itself or specific repositories.

The GitHub CLI provides a comprehensive set of commands to perform many of the common GitHub operations directly from the terminal, offering convenience, efficiency, and automation for developers and users who prefer command-line interactions.

