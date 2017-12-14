# uv-app-starter

Get started building a [IIIF](http://iiif.io)-enabled website using the [Universal Viewer](http://universalviewer.io) and host it for free on [Github Pages](https://pages.github.com/).

### Examples

- https://sophiedixon.github.io/3d-portfolio/

### Setup

 - Fork this repo on github to your personal account.

 - Rename the repo, e.g. "my-collection"

 - Clone the repo to your desktop

 - Run `npm install`

 - Organise your files and folders in `/collection` using the [biiif conventions](https://github.com/edsilv/biiif/#examples)

 - Run `npm start` to preview on `http://localhost:8888`

 - When ready to publish to [Github Pages](https://pages.github.com/), in the `package.json` scripts section, assuming your Github username is for example `@edsilv`, change:

    ```
     "dist": "biiif collection -u https://username.github.io/uv-app-starter/collection"
    ```

    to:

    ```
     "dist": "biiif collection -u https://edsilv.github.io/my-collection/collection"
    ```

- In `index.html`, replace:

    ```
    <iiif-gallery manifest="/collection/index.json"></iiif-gallery>
    ```

    with: 

    ```
    <iiif-gallery manifest="/my-collection/collection/index.json"></iiif-gallery>
    ```

- Publish to github by running:

    `npm run publish`

- Your site should now be available at `https://edsilv.github.io/my-collection/` (may take a few seconds)
