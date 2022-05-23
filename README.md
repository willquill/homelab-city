# How I built this

`pip3 install --upgrade pip`

`sudo pip3 install mkdocs`

`sudo pip3 install mkdocs-material`

`mkdocs homelab-city`

`cd homelab-city`

From there, you can do the following:

To test your new website locally:

```mkdocs serve```

To make changes to your website:

- Edit docs/index.md

- Edit mkdocs.yml

- Add your own directories and md files

### Add a CNAME if you want a custom domain

`echo 'homelab.city' >> docs/CNAME`

More info on custom domain [here](https://medium.com/@hossainkhan/using-custom-domain-for-github-pages-86b303d3918a)

### Push to your main branch for good measure

`git add -A`

`git commit -m "initial commit"`

`git push -u origin main`

### Deploy

`mkdocs gh-deploy`

## Notes about updating site after initial deployment

Never modify files directly within the `site` directory.

To make changes to your website after the initial deploy:

- Modify your yml and md files as needed.

- `mkdocs gh-deploy`

Breakdown of what `mkdocs gh-deploy` does:

- Repopulates the `site` directory with a static site generated from your md and yml files.

- Pushes the contents of the `site` directory into the gh-pages branch on Github.