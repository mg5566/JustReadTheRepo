# JustReadTheRepo

This is the main project repository containing client and server as submodules.

## Project Structure

- `client/`: Client-side application (submodule)
- `server/`: Server-side application (submodule)

## Getting Started

1. Clone the repository with submodules:
   ```bash
   git clone --recurse-submodules <repository-url>
   ```

2. Or, if you already cloned the repository, initialize and update submodules:
   ```bash
   git submodule init
   git submodule update
   ```

## Updating Submodules

To update all submodules to their latest master branch:

```bash
git submodule update --remote --merge
```

This will fetch and merge the latest changes from each submodule's remote repository.

If you want to update to a specific commit or tag in a submodule:

```bash
# Navigate to the submodule directory
cd client  # or server

# Checkout the desired branch/commit/tag
git checkout <branch-name>  # or <commit-hash> or <tag-name>

# Go back to the parent directory
cd ..

# Commit the submodule update
git add client  # or server
git commit -m "Update submodule to specific version"
```

## Working with Submodules

- To see the status of all submodules:
  ```bash
  git submodule status
  ```

- To initialize and update all submodules (including nested ones):
  ```bash
  git submodule update --init --recursive
  ```

- To pull all changes in the repository including submodules:
  ```bash
  git pull --recurse-submodules
  ```
