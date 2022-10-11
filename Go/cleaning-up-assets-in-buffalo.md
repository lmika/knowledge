---
title: Cleaning Up Assets in Buffalo
type: howto
blog-post: https://lmika.org/2022/03/21/the.html
---

Buffalo doesn't clean up old versions of bundled JavaScript files.
This means that the `public/asset` directory can grow to gigabytes in size, eventually reaching the point where Go will simply refuse to embed that much data.

The tell-tail sign is this error message when you try to run the application:

    too much data in section SDWARFSECT (over 2e+09 bytes)

If you see that, deleting `public/assets` should solve your problem.