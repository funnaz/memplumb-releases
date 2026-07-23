# MemPlumb releases

Official Preview downloads, checksums, and release notes for
[MemPlumb](https://memplumb.com), a local-first Agent MemoryOps control plane.

## Current Preview

MemPlumb v0.13.0 is an unsigned Preview release for Windows x64.

- [Release notes and all assets](https://github.com/funnaz/memplumb-releases/releases/tag/v0.13.0)
- [Windows x64 ZIP](https://github.com/funnaz/memplumb-releases/releases/download/v0.13.0/memplumb-0.13.0-windows-x64.zip)
- [Python SDK wheel](https://github.com/funnaz/memplumb-releases/releases/download/v0.13.0/memplumb-0.13.0-py3-none-any.whl)
- [TypeScript SDK package](https://github.com/funnaz/memplumb-releases/releases/download/v0.13.0/memplumb-sdk-0.13.0.tgz)

The Windows artifact is not Authenticode signed. Verify its SHA-256 digest
against the published `SHA256SUMS` before running it. Windows may show a
reputation warning for this Preview.

## Five-minute local evaluation

1. Download and extract the Windows ZIP.
2. Verify the executable:

   ```powershell
   Get-FileHash .\memplumb.exe -Algorithm SHA256
   Get-Content .\SHA256SUMS
   ```

3. Start the local Runtime and Console:

   ```powershell
   .\memplumb.exe
   ```

4. In another PowerShell window, write and retrieve one Memory:

   ```powershell
   .\memplumb.exe init
   .\memplumb.exe ingest --actor user_123 --facts '[{"kind":"profile","key":"city","value":"Hangzhou"}]'
   .\memplumb.exe context --actor user_123 --query "recommend a restaurant" --budget 1200
   ```

Success means the local Console opens and the Event, current Memory, and
Context evidence are visible for `user_123`.

## SDK installation

```bash
npm install https://github.com/funnaz/memplumb-releases/releases/download/v0.13.0/memplumb-sdk-0.13.0.tgz
pip install https://github.com/funnaz/memplumb-releases/releases/download/v0.13.0/memplumb-0.13.0-py3-none-any.whl
```

## Repository boundary

This public repository is a binary-only release channel. GitHub-generated
"Source code" archives contain only this release-channel repository, not the
private MemPlumb product source.

Preview use is governed by [EULA.md](./EULA.md). Report vulnerabilities through
[SECURITY.md](./SECURITY.md).
