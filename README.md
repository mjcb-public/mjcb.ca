# mjcb.ca #

This is the Git repository for the **mjcb.ca** website, which is currently using the Hugo CMS platform and is deployed using the Netlify platform.

This website was migrated from the **mjcb.io** domain in early 2025.

## Theme ##

This website uses the [Hugo Clarity](https://github.com/chipzoller/hugo-clarity) theme.

## License ##

[![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg

See the [LICENSE](https://github.com/matthew-tfs/mjcb.ca/blob/main/LICENSE) file for details.

## Netlify Status ##

[![Netlify Status](https://api.netlify.com/api/v1/badges/7c471c8a-2c89-4556-93c0-95b78d5bc9e0/deploy-status)](https://app.netlify.com/sites/mjcbca/deploys)

## File and Folder Structure ##

```
.
├── /
│   ├── content/
│   │   ├── blog/
│   │   │   └── 00000-blog.md
│   │   ├── publications/
│   │   │   └── 00000-publication.md
│   │   ├── about.md
│   │   ├── archives.md
│   │   ├── cookie-policy.md
│   │   ├── guides.md
│   │   ├── privacy-policy.md
│   │   └── search.md
│   ├── layouts/
│   │   ├── partials/
│   │   │   └── gdpr-notice.html
│   │   └── shortcodes/
│   │       ├── archive.html
│   │       └── toc.html
│   ├── static/
│   │   ├── docs/
|   |   |   └── blog/
|   |   ├── gdpr-notice/
│   │   │   ├── gdpr-notice.css
│   │   │   └── gdpr-notice.js
|   |   ├── images/
│   │   │   ├── author/
│   │   │   ├── blog/
│   │   │   │   └── 00000/
│   │   │   ├── logos/
│   │   │   └── publications/
│   │   │       └── publication-name/
|   |   ├── videos/
|   |   └── robots.txt
│   └── themes/
|       └── hugo-clarity/
├── config.toml
├── LICENSE
├── mjcb.ca-blog.txt
├── mjcb.ca-pages.txt
├── mjcb.ca-publications.txt
├── netlify.toml
└── README.md
```

### Important Files ###

* **/config.toml** - Primary configuration file for Hugo. It is in TOML format.
* **/LICENSE** - License information for this website.
* **/mjcb.ca-blog.txt** - List of all individual blog posts. Manually updated.
* **/mjcb.ca-pages.txt** - List of all individual pages. Manually updated.
* **/mjcb.ca-publications.txt** - List of all publication pages. Manually updated.
* **/netlify.toml** - Primary configuration file for Hugo deployment on the Netlify platform. It is in TOML format.
* **/README.md** - This README file.

### Important Folders ###

* **/content/blog/** - Contains all blog posts. Blog posts are sequentially ordered with the slug name of the post.
* **/layouts/partials/** - Contains all partial templates which are added to the existing theme.
* **/layouts/shortcodes/** - Contains all custom shortcodes that can be used.
* **/static/** - Contains all content that is placed in the root of the website when rendered by Hugo.
* **/static/docs/blog/** - Contains all linked documents for blog posts. Directories are numbered to match the blog post.
* **/static/gdpr-notice/** - Contains the necessary files for the GDPR notice for the website.
* **/static/images/** - Contains all images.
* **/static/images/blog/** - Contains all images for blog posts. Directories are numbered to match the blog post.
