# Dead Reckoning Development Blog Documentation

The Dead Reckoning Development Blog website is build with __Hugo__, a static website generator built in Go.

Hugo was chosen for its fast compilation times, feature support, and native asset pipelines.
Hugo also has a wide variety of public themes as well as offering support for custom themes.

__PaperMod__ is the Hugo theme the website uses.

## Adding Articles
*Assuming you are in the repository root directory*

1. Running `hugo new --kind default articles/article-name.md` will create a markdown file for the new article in `content/articles`based on `archetypes/default.md`.

2. Populate and edit the `content/articles/article-name.md` generated with the article's content.

3. Preview renders on [port 1313 of localhost](http://localhost:1313/ds-blog/) after running `hugo server -D` to start a local instance. 
Any changes to Markdown, templates, or config will auto-refresh on this instance, so no need to rerun this command at any point.

4. Mark the article ready for publishing by changing the `draft` value to `false` in the front matter (`draft: false`).

5. Stage, commit, and push all repository changes. The custom Github Actions Workflow `Build & Deploy Hugo` will rebuild the site and deploy it automatically.

## Hosting and Deployment
The development blog is hosted on __GitHub Pages__ and uses __Github Actions workflows__ to enable repository pushes to automatically
update the live website.

Every push to `master` will rebuild the website and redeploy it to a GitHub Pages instance.