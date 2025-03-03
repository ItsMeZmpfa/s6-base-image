# S6-Overlay-BaseImage
This repo providing a s6-overlay base image

For more info for S6-overlay
[a link] (https://github.com/just-containers/s6-overlay)
## Usage

```Dockerfile
FROM itsmezmpfa/s6-base-image AS s6-overlay
FROM alpine3

COPY --from=s6-overlay /s6/root /

ENTRYPOINT ["/init"]
```