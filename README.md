Memo
---
A place where I store all my useful cmd.

---

Pulsar
---

create msgs : `bin/pulsar-client produce -m "Hello World !" persistent://my-tenant/my-namespace/my-topic`

consume msgs : `bin/pulsar-client consume -n 0 -s debug-subscription persistent://my-tenant/my-namespace/my-topic`

Cockroach
---
Start mononode server (dev only)
```
podman run \
  -d \
  --name=roach1 \
  --hostname=roach1 \
  -p 26257:26257 \
  -p 8080:8080 \
  -v "roach1:$HOME/cockroach-dev-volume" \
  cockroachdb/cockroach:v22.1.10 start --insecure --join roach1
```
once exec in the container:
```
./cockroach init --insecure
```
