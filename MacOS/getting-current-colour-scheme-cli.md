---
title: Getting the Current Colour Scheme from the CLI
type: post
blog-post: https://lmika.org/2022/10/04/the-annoying-way.html
---

To get the current colour scheme from the CLI, use the following command:

```
defaults read -g AppleInterfaceStyle
```

If MacOS is in dark mode, this will print `Dark`.  But if MacOS is in light mode, this key won't be set at all, and the command will print return an error of the form:

```
2022-10-04 09:15:18.058 defaults[35844:466643] 
The domain/default pair of (kCFPreferencesAnyApplication, AppleInterfaceStyle) does not exist
```

As such, in order to confirm that the colour scheme is light, you'll need to parse for this error.