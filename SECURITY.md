# Security policy

## Reporting a vulnerability

Please do not open a public issue for a vulnerability. Report it privately through GitHub instead: open the **Security** tab of the repository it affects, and choose **Report a vulnerability**. If you are unsure which repository it belongs to, report it on the generator whose output or command shows it.

Say which generator and version you used (`go tool kanna-<name> -version`), the declaration or input that triggers it, and what an attacker can do with it. You will get an answer in the advisory, and the fix and the advisory are published together once a release carries the fix.

## Supported versions

kanna is before v1, and fixes go into the next release of each module. Please update to the latest release before reporting.
