# hoverloader
A tiny library which tries to improve user experience on websites by reducing time for resources to be loaded after clicking on any link.

## How it works
When you hover an `<a href="URL">` you probably click on it, too. Wouldn't it be great to have the resource loaded right away in the background?
Sure, because after clicking on the link, the resource is already in cache and can be shown very fast by your browser.

This is where `<link rel="preload">` comes in handy:
"Using <link rel="preload">, browsers can be informed to prefetch resources without having to execute them, allowing fine-grained control over when and how resources are loaded." (from caniuse.com)

Right after page load hoverloader adds `<link rel="preload">` for all `a` elements to your `body` on `mouseenter` event. It is removed safely on `mouseleave`.

It works for image (gif|jpg|jpeg|tiff|png) and html links.

## Demo
Right now hoverloader is used on https://feuerwehr-eisolzried.de/media/

## How to add
Simply include `<script src="/js/hoverloader.min.js" async></script>` right before the `</body>` tag.

## Browser support
Right now only Chrome > 55 and Opera > 43.
For recent support check https://caniuse.com/#search=preload
