---
title: List and Delete All Docker Containers
type: howto
blog-post: https://lmika.org/2022/06/27/a-useful-command.html
---

This will list all Docker containers, and delete each one regardless of whether it's running or not. Good if you use Docker for dev containers and need to reset your state.

```
docker ps -a --format '{{.ID}}' | xargs -I{} docker rm -v {}
```

EDIT: thanks to [@sonicrocketman](https://micro.blog/sonicrocketman) for suggesting another way to do this.  Works just as well:

```
docker ps -aq | xargs -I{} docker rm -vf {}
```