# doooohun. — Instagram-style fictional profile with comments

Each of the 9 post modals has its own shared comment thread powered by **Giscus** (GitHub Discussions).

## Enable shared comments

GitHub Pages by itself cannot store comments shared between visitors. Giscus is a free comments widget backed by GitHub Discussions.

1. Push `index.html` to a GitHub repository.
2. In that repository, open **Settings → General → Features** and enable **Discussions**.
3. Create a Discussions category named **Comments** (or update the category in `index.html` to match the category you use).
4. Open https://giscus.app/ and enter your repository (`YOUR_GITHUB_USERNAME/YOUR_REPOSITORY`). Follow its setup checks and copy its `data-repo-id` and `data-category-id` values.
5. In `index.html`, find `function loadComments(postIndex)` and replace:
   - `YOUR_GITHUB_USERNAME/YOUR_REPOSITORY` with your repository, e.g. `myname/dohun-instagram`
   - `YOUR_GISCUS_REPO_ID` with the `data-repo-id` value from giscus.app
   - `YOUR_GISCUS_CATEGORY_ID` with the `data-category-id` value from giscus.app
6. Make sure the repository is public and meets the requirements shown on giscus.app.
7. In **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/(root)`, then save.

Visitors can comment and react using GitHub Discussions. They may need to sign in with a GitHub account. Comments are public and persistent. Each post has its own thread (post 1 through post 9).

## Notes
- This is a fictional demo profile, not affiliated with Instagram.
- Photos are loaded from Unsplash and need an internet connection.
