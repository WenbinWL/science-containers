# CANFAR Webterm

This contributed-session image runs `ttyd` on port 5000 over the standard
`skaha/terminal` image.  Its browser tab title uses the Skaha session name.

Build it after publishing the corresponding terminal image:

```sh
docker buildx build \
  --platform linux/amd64 \
  --build-arg BASE_IMAGE=images.canfar.net/skaha/terminal:<terminal-tag> \
  --tag images.canfar.net/skaha/webterm:<version> \
  --push \
  .
```
