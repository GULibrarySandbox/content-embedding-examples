---
title: Articulate Rise
nav_order: 3
layout: default
---

# Embedding Articulate Rise content in GitHub
{: .no_toc }

Articulate can host Rise content on their own servers, but there are downsides to doing it that way.
{: .fs-6 .fw-300 }
<!-- You can style the preceding line using .fs for font size and .fw for font weight -->

To embed and Articulate Rise module into GitHub:

1. Create your GitHub repository. 
2. Optionally choose a template that allows for Markdown editing, like Evan Williams' Workshop-B or Just The Docs.
3. Turn on Pages in the repository settings (use the new actions option)
4. Log in to rise.articulate.com and find the module you want to publish.
5. Click the Publish button.
6. Choose 'Web'. A .zip file should start to download.
7. Find the .zip file in your downloads folder and decompress it.
9. Return to your GitHub repository and create a new folder (unless you are going to place the Rise content in the root directory of the repository).
10. Copy the contents of the decompressed folder into the new folder in your repository. Don't copy the folder, just its contents!
11. Commit your changes and wait for the publish Action to run.

If you want to display Articulate Rise content in a GitHub page, you have two options:

### Embedding a rise module inside an existing page

Using the follwing code snippet, you can make the Rise object appear within your GitHub page.

```
<div style="margin: 0 auto; width:100%; height:400px;">
    <object type="text/html" data="*** your URL here ***"
            style="width:100%; height:100%; margin:1%;">
    </object>
</div>
```

Here's an example:

<div style="margin: 0 auto; width:100%; height:400px;">
    <object type="text/html" data="rise/index.html"
            style="width:100%; height:100%; margin:1%;">
    </object>
</div>

### Displaying a Rise module in its own page

Alternatively, you can simply upload the page and link directly to it, in which can it will appear in its own page at full screen.

[Link to rise content](rise/index.html)