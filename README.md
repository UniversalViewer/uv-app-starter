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

    `npm run publish-gh`

- Your site should now be available at `https://edsilv.github.io/my-collection/` (may take a few seconds)

### Publishing using dat

You can use [Beaker Browser](https://beakerbrowser.com/) to publish your portfolio using the [dat protocol](https://datproject.org/).

- In Beaker, click on the menu button and select "New Site".

- Give it a name and click Create Site.

- Next to the Share button, click the drop down and select Change Folder.

- Set the folder to the location of your current uv-app-starter project.

- Now click the Share button and copy your dat address (`dat://<hash>`).

- In `index.html`, replace:

    ```
    <iiif-gallery manifest="/collection/index.json"></iiif-gallery>
    ```

    with: 

    ```
    <iiif-gallery manifest="dat://<hash>/collection/index.json"></iiif-gallery>
    ```

- In `package.json` under the `dist-dat` script, replace the dat address with your site's address.

- Run `npm run publish-dat`. This will generate your IIIF using your dat address as the root.

- Refresh your site in Beaker. 
