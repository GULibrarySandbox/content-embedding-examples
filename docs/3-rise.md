---
title: Articulate Rise
nav_order: 3
layout: default
---

# Articulate Rise
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

Rise courses can be viewed on Articulate's servers or they can be exported and embedded on a GitHub page.
{: .fs-6 .fw-300 }
<!-- You can style the preceding line using .fs for font size and .fw for font weight -->

'Articulate' is [pronounced with a long 'a' at the end](https://community.articulate.com/discussions/articulate-storyline/articulate-pronunciation), like 'late'!
{:. .note }

Although it's less work to simply leave your Rise course on the Articulate website, there are significant downsides to that approach: 

- You can't incorporate the content into an existing course or page.
- Branding options are limited.
- **Important**: You can't make draft edits to your work without it being seen immediately by students.

Thus, it's better to export your Rise content and host it somewhere that you control, for example on a GitHub site. 

If you want to display Articulate Rise content on a GitHub site, you have two options. The most common approach is to create a repository dedicated solely to the Rise course. Alternatively, you can embed the Rise course inside a page on an existing repository. This might be a good option if the Rise course forms only a part of what you want to present to the student.

## Creating a dedicated repository for your Rise course

1. Create your GitHub repository
2. Log in to rise.articulate.com and find the module you want to publish.
3. Click the Publish button.
4. Choose 'Web'. A .zip file should start to download.
5. Find the .zip file in your downloads folder and decompress it.
6. Upload the contents of the decompressed folder into the root directory of your repository. Don't copy the folder, just its contents! You should see `index.html` in the root directory, along with two folders called `assets` and `lib`.
7. Optionally add the Google Analytics code (below) to `index.html`.
8. Turn on Pages in the repository settings (use the new actions option)
9. Commit your changes and wait for the publish Action to run.

Here's a short video illustrating the process:

<iframe src="https://player.vimeo.com/video/774945468?h=cd1b35bb2c" width="640" height="564" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>

> Here's an example of how a Rise lesson looks in a dedicated repository:

[Finding Cases](https://griffithunilibrary.github.io/finding-cases/)
{: .btn }

### Google Analytics

To connect your site to Griffith Library's Google Analytics account, you need to add the following code snippet to the `<head>` section of `index.html`.

```
    <!-- Global site tag (gtag.js) - Google Analytics -->
    <!-- Google tag (gtag.js) -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=G-NC3PPY2JZB">
    </script> 
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag(){dataLayer.push(arguments);}
      gtag('js', new Date());
      gtag('config', 'G-NC3PPY2JZB');
    </script>
```

---

## Displaying a Rise course in its own page

1. Create your GitHub repository.
2. Optionally choose a template that allows for Markdown editing, like Evan Williams' [Workshop-B](https://github.com/evanwill/workshop-template-b), [Learn-Static](https://github.com/learn-static/lesson-template) or [Just The Docs](https://github.com/just-the-docs/just-the-docs).
3. Turn on Pages in the repository settings (use the new actions option)
4. Log in to rise.articulate.com and find the module you want to publish.
5. Click the Publish button.
6. Choose 'Web'. A .zip file should start to download.
7. Find the .zip file in your downloads folder and decompress it.
8. Return to your GitHub repository and create a new folder (don't put it in the root directory).
9. Copy the contents of the decompressed folder into the new folder in your repository. Don't copy the folder, just its contents!
10. Commit your changes and wait for the publish Action to run.

Once you've done that, you can either link directly to it, in which can it will appear in its own page at full screen, or you can embed it 

[Link to rise content](rise/index.html)

[Launch lesson](rise/index.html){: .btn }

### Embedding a Rise module inside an existing page

Using the following code snippet, you can make the Rise object appear within your GitHub page.

```
<div style="margin: 0 auto; width:100%; height:400px;">
    <object type="text/html" data="*** your URL here ***"
            style="width:100%; height:100%; margin:1%;">
    </object>
</div>
```

1. Create your repository as explained above and add a page to your site.


> Here's how a Rise course looks when it's embedded in a page:

<div style="margin: 0 auto; width:100%; height:400px;">
    <object type="text/html" data="rise/index.html"
            style="width:100%; height:100%; margin:1%;">
    </object>
</div>