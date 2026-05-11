# Spatio Python SDK

The official Python client for the [SpatioAPI](https://www.spatio.app/developers). Notes, sheets, slides, tasks, mail, calendar, channels, DMs, files, contacts, repos, agents, and federated search.

```bash
pip install spatio-sdk
```

```python
from spatio import ApiClient, Configuration
from spatio.api import NotesApi

client = ApiClient(Configuration(
    host="https://api.spatio.app",
    access_token="pat_...",
))

envelope = NotesApi(client).list_notes()
print(envelope.items)
```

## Authentication

Two paths.

**Personal Access Token.** Mint one at *Settings → Tokens* in [Spatio Desktop](https://www.spatio.app) and pass it as `access_token`. The right choice for scripts, automations, and your own backend services.

**OAuth 2.1 + OpenID Connect.** Build a "Sign in with Spatio" flow for your own product. The OIDC discovery document at [`/.well-known/openid-configuration`](https://api.spatio.app/.well-known/openid-configuration) drops into Authlib, oidcrp, and every other conformant RP library.

## What you can build

Spatio's API is designed to be the substrate someone could build their own Spatio Desktop on top of: realtime collaboration via Yjs, federated cross-platform search, OAuth 2.1 dynamic client registration, OpenID Connect sign-in, and a self-hosted agent runtime. The OpenAPI spec is the canonical reference.

## Links

- [SpatioAPI reference](https://www.spatio.app/developers/docs/api)
- [OpenAPI spec](https://api.spatio.app/openapi.json)
- [Spatio on the web](https://www.spatio.app)

## About this package

Generated from the SpatioAPI OpenAPI spec on every release. PRs against generated files will be overwritten on the next release; file issues here for bugs in the SDK shape, or report API problems through Spatio Support.

Licensed under [MIT](LICENSE).
