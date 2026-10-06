# nsq-docker

[![ci](https://github.com/golang-queue/nsq-docker/actions/workflows/ci.yml/badge.svg)](https://github.com/golang-queue/nsq-docker/actions/workflows/ci.yml)

NSQ docker for GitHub Actions which [doesn't support entrypoint args in Docker service](https://github.community/t/how-do-i-properly-override-a-service-entrypoint/17435/4).

The container runs as UID/GID `65532:65532` and stores data in `/data` by
default. If you bind-mount a data directory or provide a custom `--data-path`,
make sure it is writable by this UID/GID. Mounted TLS certificates and keys
must also be readable by this user.
