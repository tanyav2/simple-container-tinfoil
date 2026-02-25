# Simple Tinfoil Container Example

A minimal working example of a [Tinfoil Container](https://docs.tinfoil.sh/containers/overview) deployment with a private Docker image, secrets, environment variables, and routing.

Referenced in the [Quickstart](https://docs.tinfoil.sh/containers/quickstart) and [Overview](https://docs.tinfoil.sh/containers/overview) docs.

## What's in this repo

- **`tinfoil-config.yml`** — the only file needed. It defines the container image, environment variables, secrets, and exposed paths.

## Details

- **Private image**: The container image (`ghcr.io/tanyav2/simple-container-private`) is hosted in a private GitHub Container Registry. Tinfoil pulls private images using registry credentials configured in the dashboard.
- **Secrets**: `TINFOIL_API_KEY` is created in the Tinfoil dashboard. Secret values are never visible in the config.
- **Paths**: Only `/health` and `/chat` are exposed. All other paths will return a 403.
