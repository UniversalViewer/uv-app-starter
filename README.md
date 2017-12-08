# uv-app-starter

### Setup

 - Fork this repo on github to your personal account.

 - Rename the repo, e.g. "my-portfolio"

 - Clone the repo to your desktop.

 - Check out the `gh-pages` branch.

 - Organise your files and folders in `/content` using the [biiif conventions](https://github.com/edsilv/biiif/#examples)

 - Run `npm start` to preview on `http://localhost:8888`

 - When ready to publish to [Github Pages](https://pages.github.com/), in the `package.json` scripts section, assuming your Github username is for example `@edsilv`, change:

    ```
     "dist": "biiif content -u https://username.github.io/uv-app-starter-fork/content"
    ```

    to:

    ```
     "dist": "biiif content -u https://edsilv.github.io/my-portfolio/content"
    ```

- Now run `npm run dist`

- Add your changes to the `gh-pages` branch, and `git push origin gh-pages`

- Your site should now be available at `https://edsilv.github.io/my-portfolio/`

