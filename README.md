# Distilla

Distilla is a Claude plugin for fundamental equity research. It connects Claude to the hosted Distilla MCP server at `https://api.distilla.ai/mcp`.

The hosted backend is proprietary. It is not in this repository. This repository contains the plugin manifest, the MCP connection file, and these documents. It does not contain secrets or private application code.

The MIT license applies to the files in this repository. It does not apply to the hosted Distilla service.

## Requirements

- Claude Code, or Claude Cowork
- A Distilla account that can use the hosted server

## Install for a local test

Clone this repository and load the plugin directory:

```bash
git clone https://github.com/Distilla-AI/mcp-api-plugin.git
cd mcp-api-plugin
claude --plugin-dir .
```

`--plugin-dir` loads the plugin for that session. It does not publish the plugin.

## Install from the plugin directory

After Anthropic lists this plugin, add the community marketplace and install Distilla:

```text
/plugin marketplace add anthropics/claude-plugins-community
/plugin install distilla@claude-community
```

Submit the public GitHub repository from the Claude.ai or Console plugin form. Run `claude plugin validate .` on the commit you submit. See [Submitting your plugin](https://claude.com/docs/plugins/submit).

## Enable and sign in

The plugin stays off until you enable it. Turn it on in `/plugin`, or run:

```bash
claude plugin enable distilla@claude-community
```

Use the marketplace name that applies to your install. For a local `--plugin-dir` session, enable `distilla` in `/plugin` if Claude shows it as off.

This repository does not store credentials. When the hosted server asks you to sign in, complete that step in Claude. Do not add tokens or keys to these files.

## Example prompts

Ask Claude in plain language after the server is connected. The tools you can call depend on your Distilla account.

1. Prepare a meeting brief for a company on my watchlist. Include the current thesis, recent results, and the main risks.
2. Write a short earnings review for a company I follow. State what changed and what I should track next.
3. Compare two companies in the same industry. Explain the drivers that matter for a fundamental thesis.

## Permissions

The plugin opens one remote MCP connection:

| Server | Transport | URL |
| --- | --- | --- |
| `distilla` | HTTP | `https://api.distilla.ai/mcp` |

Review the tool list in Claude before you approve a call. The plugin does not run local software.

## Version

The plugin version is `1.0.0` in `.claude-plugin/plugin.json`. Bump that field when you want installed copies to receive a change.

## Security

Report a vulnerability as described in [SECURITY.md](SECURITY.md).

## Maintainer

Distilla, Inc.

- Website: [https://www.distilla.ai](https://www.distilla.ai)
- Email: [support@distilla.ai](mailto:support@distilla.ai)
- Repository: [https://github.com/Distilla-AI/mcp-api-plugin](https://github.com/Distilla-AI/mcp-api-plugin)
