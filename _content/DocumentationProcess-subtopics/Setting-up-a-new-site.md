---
title: "Setting up a new site"
author: Reuben Evans
---

## A quick summary

1. Login to GitHub as intuitivedocs. Currently this is tied to reuben@intuitivesystems.com
2. Make a new repository. Its name will be the site's name
3. Make a new branch called "gh-pages" (this is where all the files need to go)
4. Copy all the files across from another repository
  - Delete the _content files (but not the folder)
  - Edit index.markdown in the root if you want to modify it - this is the landing page for the site
  - Edit _config.yml and change the following to match the new site URL/name:
    - maintitle
    - title
    - description
    - baseurl
    - url 
5. Edit Jekyll/_includes/sidebar.html to reflect the new site pages
6. Add anyone who will be adding to the site as a collaborator