# Entalio HQ plugin

Entalio HQ in Claude Code and Codex: HQ's hosted MCP server and the skills for working with it
(`hq`, `hq-status`, `hq-pages`). It holds no secrets: HQ's address is public, and every app signs in
with a person's own HQ login on HQ's Allow page.

## Install

The easiest is HQ's setup line, which installs this plugin and signs each app in:

```sh
curl -fsSL https://hq-86189444959.europe-west2.run.app/connect | sh
```

Or by hand:

```sh
claude plugin marketplace add arashlabafian/entalio-hq-plugin
claude plugin install entalio-hq@entalio
claude mcp login plugin:entalio-hq:hq

codex plugin marketplace add arashlabafian/entalio-hq-plugin
codex plugin add entalio-hq@entalio
codex mcp login hq
```

This repository is a copy of `plugins/` in Entalio's own repository, published by
`scripts/plugin-publish.sh`. Changes are made there.
