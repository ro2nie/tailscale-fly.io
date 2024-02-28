# Deploy Tailscale

Create an auth key in Tailscale
Then set it on the Fly app with
`flyctl secrets set TAILSCALE_AUTHKEY="tskey-<key>"`

To deploy a Tailscale Fly app,

1. Run `flyctl launch --name <app name>`.
2. Choose the country (this will be used as the Tailscale machine name).
3. It should appear in Tailscale console.
4. Enable it as exit node and authenticate it.
