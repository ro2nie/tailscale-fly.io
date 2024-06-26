# Deploy Tailscale

To deploy a Tailscale Fly app,

1. First ensure ENV TSFILE in Dockerfile is using the latest tailscale binary.
2. Log your terminal in with `flyct auth login`
3. Run `flyctl launch --name <app name>` ie: madrid-tailscale 
4. Choose the country (this will be used as the Tailscale machine name).
5. Create an auth key in Tailscale from https://login.tailscale.com/admin/settings/keys
6. Then set it on the Fly app with `flyctl secrets set TAILSCALE_AUTHKEY="tskey-<key>"`
7. The app will update
8. It should now appear in Tailscale console.
9. Approve it in tailscale dashboard
10. Approve it as exit node and authenticate it.

