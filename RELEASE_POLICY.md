# Captain Sapphire — Desktop Release Policy

Status: PRE-RELEASE / NO DISTRIBUTION AUTHORIZED

This public repository is dedicated to distributing approved Captain Sapphire macOS desktop releases. It is not a source-code or development-data repository.

## Release admission requirements

1. Use a release version greater than the version already installed when testing an actual update. Keep `package.json`, Tauri configuration, application Info.plist, tag, and manifest version aligned.
2. Build the release application, sign it with the approved Apple Developer ID identity, notarize it, staple where applicable, and verify the code signature and Gatekeeper acceptance.
3. Create the Tauri updater archive from the exact approved application bundle. Verify the extracted bundle against the approved source and check platform compatibility.
4. Sign the exact archive bytes with the existing authorized Tauri updater private key. Verify the archive/signature pair independently; reject any modified archive or mismatched signature.
5. Generate `latest.json` using the verified signature, matching version, supported platform, and real immutable release asset URL. Verify the manifest and asset availability before activating an update.
6. Test download and update installation in an isolated environment, including data preservation and rollback planning, before production activation.
7. Obtain explicit approval before publishing release assets, exposing a production manifest, or enabling automatic update delivery.

## Prohibited materials

Never commit or attach private signing keys, passwords, tokens, developer credentials, local user databases, personal files, production secrets, or unapproved internal source code.

## Security boundaries

Release engineering must not change Founder authority, action grants, execution grants, provider writes, or M6-R4 security gates. Founder authentication and execution remain blocked until separately certified and approved.

## Current baseline

Captain Sapphire 0.14.0 is the notarized local packaging-validation baseline. Its staging manifest and updater archive are not authorized for public distribution. No published releases or live automatic-update delivery are approved by this policy.

## Repository role

Public release assets only after approval. Development, governance, and private engineering work stay in their existing separate repositories.
