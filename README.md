# GGC STaRS Website 

Produces the [website](https://ggc-stars.github.io/) for the yearly
Science Technology and Reseach Symposium (STaRS) symposium event at
Georgia Gwinnett College. It holds blog-style posts and can also
generate individual pages for each poster submission from a CSV file
(see
[2021 poster archive](https://ggc-stars.github.io/archive-stars2021/posters/)).

## Instructions for updating content for a new STaRS event:

You can change all the files on the Github site, you don't need to
clone the repository to your computer. Once you commit a change, click
on the [Actions tab](/GGC-STaRS/GGC-STaRS.github.io/actions) on the
top of this page to watch the process to update the published
website. It should take 3-5 minutes. If it succeeds, you can refresh
the [website](https://ggc-stars.github.io/) to see your changes. If
somehow you broke it, look at your changes
under [Commits](/GGC-STaRS/GGC-STaRS.github.io/commits/master) and
revert some of your changes to recover the site.

Steps:

1. Edit the `_config.yml` file:
    - Update the fields: `title` (window/tab title), `label` (folder
    from where all posts are read), `email` (if necessary), and
    `copyright` (shows at the bottom of page).
    - Under `header_pages` you will find the list of top menu
    pages. If you want to remove the _Submissions_ and _Program_ links
    until they are ready, comment them out by putting a pound sign
    (`#`) at the beginning of their lines.
    - Further below, under the `defaults:` and `stars:` lines, change
    the `heading` and `subheading` lines as needed. You can change the
    background image with the `banner` line.
1. Create a new folder with the same content you used for `label` (e.g., "stars2024").
    - Under this folder, create a second folder called `_posts`.
    - Copy and rename selected posts (e.g., "_Welcome message_" and
      "_Dean's message_") from the previous years' folder.
    - Make sure to update the file names of the posts to reflect
      current dates since posts dated on the site based on file names.
    - Post files are formatted using Markdown and the pair of `---`
      signs at the top delineate its metadata.
1. When ready, make new posts to remind about submissions. Update the
   `submissions.md` and `schedule.md` files to reflect the submission
   instructions and program details, respectively. Download files must
   be uploaded to `/assets/` folders.
   
And you should be done!
Contact [@cengique](https://github.com/cengique) (or cgunay AT
ggc.edu) for questions or create
an [Issue](/GGC-STaRS/GGC-STaRS.github.io/issues).

## Other details

This site generated via the [Jekyll](https://jekyllrb.com/) static
side building system, using
the [YAT Theme](https://github.com/jeffreytse/jekyll-theme-yat). It
was originally modified and customized by Cengiz Gunay for the STaRS
website.

`_config.yml` contains is meant for settings that affect your whole
blog, values which you are expected to set up once and rarely edit
after that. If you find yourself editing this file very often,
consider using Jekyll's data files feature for the data you need to
update frequently.

You don't need to edit `index.md`, which simply invokes the layout
`_layouts/stars.html`). The layout HTML file reads all the necessary
information from the config file, but could be further edited if
necessary.

`posters.md` contains the posters and layouts, as of now it interfaces
with 2021 posters (site.data.stars2021.posters).

`archives.md` lists past year's versions of the site.

To test locally: 

```bash
bundle exec jekyll serve
```

and open on same computer: http://127.0.0.1:4000/
