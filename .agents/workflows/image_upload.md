---
description: How to quickly upload an image to the Discord repository
---

This workflow ensures images are uploaded to the `discord10xc/Discord` repository efficiently.

1.  **Preparation**:
    - Identify the source image path provided by the user.
    - Confirm the destination folder (default: `new_message` if not specified).
    - Choose a descriptive English name for the image.

2.  **Environment Check**:
    - Ensure the working directory is `c:\AIDev\画像アップロード`.
    - // turbo
    - Run `gh auth switch --hostname github.com --user discord10xc` to ensure correct permissions.
    - // turbo
    - Run `gh auth setup-git` if needed.

3.  **File Operations**:
    - Create the destination folder if it doesn't exist.
    - Copy the image to the destination folder with the English name.

4.  **Git Operations**:
    - // turbo
    - Execute the following:
      ```powershell
      git add .
      git commit -m "Add <filename> to <folder>"
      git push origin main
      ```

5.  **Verification**:
    - Confirm the upload via browser or `git log`.
