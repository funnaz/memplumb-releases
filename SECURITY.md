# Security policy

## Supported releases

MemPlumb is currently a Preview product. Security fixes are applied to the
latest published v0.x release only.

## Report a vulnerability

Send vulnerability reports privately to `andowang0310@gmail.com` with the
subject `MemPlumb security report`.

Include the affected version, deployment surface, reproduction steps, impact,
and any suggested mitigation. Do not include production credentials, raw
Memory content, personal data, or private database snapshots.

Please allow 7 calendar days for an initial response. Do not publish an
unresolved vulnerability before coordinated disclosure terms are agreed.

## Artifact verification

Preview Windows artifacts are unsigned until their manifest says otherwise.
Verify both `manifest.json` and `SHA256SUMS` before execution. A published hash
proves byte integrity; it does not establish publisher identity.
