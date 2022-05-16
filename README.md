Memo
---
A place where I store all my useful cmd.

---

Pulsar
---

create msgs : `bin/pulsar-client produce -m "Hello World !" persistent://my-tenant/my-namespace/my-topic`

consume msgs : `bin/pulsar-client consume -n 0 -s debug-subscription persistent://my-tenant/my-namespace/my-topic`
