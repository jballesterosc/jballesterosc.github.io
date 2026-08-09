# writing/

to publish a post, add a markdown file here named:

    YYYY-MM-DD-a-short-title.md

with this front matter at the top:

    ---
    layout: post
    title: your post title
    date: YYYY-MM-DD
    ---

    your content, in markdown, starts here.

that's it — push it and it shows up on the [writing page](/writing/).

the writing page only shows the title and the month/year, so no need for
a description, image, or tags.

unfinished posts: save them in `_drafts/` instead of `_posts/` (same
format, minus the date in the filename) and they won't be published.
see [jekyllrb.com/docs/posts](https://jekyllrb.com/docs/posts/) for more
options (categories, excerpts, etc.) if you ever want them.
