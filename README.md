# uv-app-starter

Get started building a [IIIF](http://iiif.io)-enabled website using the [Universal Viewer](http://universalviewer.io) and host it for free on [Github Pages](https://pages.github.com/).

### Setup

 - Fork this repo on github to your personal account.

 - Rename the repo, e.g. "my-collection"

 - Clone the repo to your desktop

 - Check out the `gh-pages` branch `git checkout gh-pages`

 - Run `npm install`

 - Organise your files and folders in `/collection` using the [biiif conventions](https://github.com/edsilv/biiif/#examples)

 - Run `npm start` to preview on `http://localhost:8888`

 - When ready to publish to [Github Pages](https://pages.github.com/), in the `package.json` scripts section, assuming your Github username is for example `@edsilv`, change:

    ```
     "dist": "biiif collection -u https://username.github.io/uv-app-starter-fork/collection"
    ```

    to:

    ```
     "dist": "biiif collection -u https://edsilv.github.io/my-collection/collection"
    ```

- Now run `npm run dist`

- Delete the line with `collection/**` from the `.gitignore` file

- In `index.html`, replace:

    ```
    <iiif-gallery manifest="http://localhost:8888/collection/index.json"></iiif-gallery>
    ```

    with: 

    ```
    <iiif-gallery manifest="https://edsilv.github.io/my-collection/collection/index.json"></iiif-gallery>
    ```

- Add your changes to the `gh-pages` branch with `git add -A`, then `git commit -m "added collection"`, and `git push origin gh-pages`

- Your site should now be available at `https://edsilv.github.io/my-collection/`

