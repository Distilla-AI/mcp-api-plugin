# Security policy

## Supported versions

| Version | Supported |
| --- | --- |
| 1.0.x | Yes |

The version is the `version` field in `.claude-plugin/plugin.json`.

## Report a vulnerability

Send a security report to [support@distilla.ai](mailto:support@distilla.ai).

Do not open a public GitHub issue for a security problem. Include the plugin version, the Claude product you use, and the steps that show the problem.

This repository holds the public plugin files only. The hosted Distilla backend is proprietary and is not in this repository. Report a problem in that service to the same address.

## What this plugin can access

The plugin connects Claude to `https://api.distilla.ai/mcp` over HTTPS. It does not ship local executables, hooks, or credentials. Do not commit tokens, keys, or customer data to this repository.
