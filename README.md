# Deploy Tailscale

Create an auth key in Tailscale
Then set it on the Fly app with
`flyctl secrets set TAILSCALE_AUTHKEY="tskey-<key>"`

To deploy a Tailscale Fly app,

1. Run `flyctl launch`.
2. Choose the country (this will be used as the Tailscale machine name).
3. Go to the monitoring view of the new app.
4. Click on the login link to authenticate the app with Tailscale.
5. Enable it as exit node and authenticate it.
