# haolinMA.github.io

Haolin MA's personal website

## How to build

1. Create a repository in Github and name it `username.github.io`. You can replace `username`, but it’s best to use your Github account name and keep it lowercase.

- Set the repository to public
- In the repository's **Settings/Pages** section, set the branch to main/(root)

2. Use `git clone` locally to download the repository and add a file named `index.html` (the website will load from `index.html`).

3. In `index.html`, write the website content using HTML. For more details, see [Basic HTML Content](./files/HTML).
4. Use git commands to upload the files. Afterward, you should see the updated website content.

## Architecture Explanation

If you set up a /docs folder in GitHub, all subsequent files should use this folder as the root directory.

In this document, the root folder is set to /root.

### /css

This folder contains stylesheets used in the website.

### /files

This folder is for storing files.

### /images

This folder contains images used on the website.

#### /base

This folder stores some basic elements of the website.

#### /README.assets

This folder contains some image files used in README.md.
