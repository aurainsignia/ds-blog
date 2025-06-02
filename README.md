# Dead Reckoning Development Blog Documentation

The Dead Reckoning Development Blog website is build with __Hugo__, a static website generator built in Go.

Hugo was chosen for its fast compilation times, feature support, and native asset pipelines.
Hugo also has a wide variety of public themes as well as offering support for custom themes.

__PaperMod__ is the Hugo theme the website uses.

## Testing
__Local deployments__ can be viewed at [http://localhost:1313/](http://localhost:1313/) after running `hugo server -D` to start a local instance.
Any changes to Markdown, templates, or config will auto-refresh on this instance.



## Hosting and Deployment
The development blog is hosted on __GitHub Pages__ and uses __Github Actions workflows__ to enable repository pushes to automatically
update the live website.

Every push to `master` will rebuild the website and redeploy it to a GitHub Pages instance.