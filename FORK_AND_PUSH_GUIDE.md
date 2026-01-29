# Step-by-step: Fork ComfyUI-fal-API and push your changes

You already have the code (with the Flux 2 Flex Edit node) in this folder. Follow these steps to get it into **your own** GitHub repo.

---

## Step 1: Create a fork on GitHub

1. Open: **https://github.com/gokayfem/ComfyUI-fal-API**
2. Log in to your GitHub account.
3. Click the **Fork** button (top right).
4. Choose your account as the destination.  
   - Optionally change the repo name (e.g. `ComfyUI-fal-API` or `my-comfyui-fal`).
5. Click **Create fork**.  
   You’ll be on: `https://github.com/YOUR_USERNAME/ComfyUI-fal-API`

---

## Step 2: Turn this folder into a git repo and push (recommended)

Because this folder was not cloned with `git clone`, we’ll initialize git here and push everything (including your new node) to your fork.

### 2a. Initialize git and make the first commit

In a terminal, from **this project folder** (where `config.ini` and `nodes/` are):

```bash
cd /path/to/ComfyUI-fal-API-main   # or wherever this folder is

git init
git add .
git commit -m "Add Flux 2 Flex Edit node (fal-ai/flux-2-flex/edit)"
```

### 2b. Connect to your fork and push

Replace `YOUR_USERNAME` with your GitHub username:

```bash
git remote add origin https://github.com/YOUR_USERNAME/ComfyUI-fal-API.git
git branch -M main
git push -u origin main
```

If your fork uses a different default branch (e.g. `master`), use that instead of `main`.

---

## Step 3: Optional – sync with the original repo later

To pull future updates from the original repo:

```bash
git remote add upstream https://github.com/gokayfem/ComfyUI-fal-API.git
git fetch upstream
git merge upstream/main   # or upstream/master
git push origin main
```

---

## Alternative: Start from a fresh clone of your fork

If you prefer a repo that has the **full commit history** from the original project:

1. **Create the fork** (Step 1 above).
2. **Clone your fork** (not the original):
   ```bash
   git clone https://github.com/YOUR_USERNAME/ComfyUI-fal-API.git
   cd ComfyUI-fal-API
   ```
3. **Copy your modified file** into the clone:
   - Replace `nodes/image_node.py` in the clone with your current `nodes/image_node.py` (the one that has the Flux 2 Flex Edit node).
4. **Commit and push**:
   ```bash
   git add nodes/image_node.py
   git commit -m "Add Flux 2 Flex Edit node (fal-ai/flux-2-flex/edit)"
   git push origin main
   ```

---

## Summary

| Step | Action |
|------|--------|
| 1 | Fork https://github.com/gokayfem/ComfyUI-fal-API on GitHub |
| 2 | In this folder: `git init`, `git add .`, `git commit -m "Add Flux 2 Flex Edit node"` |
| 3 | `git remote add origin https://github.com/YOUR_USERNAME/ComfyUI-fal-API.git` |
| 4 | `git branch -M main` then `git push -u origin main` |

After this, your fork will contain the new **Flux 2 Flex Edit (fal)** node.
