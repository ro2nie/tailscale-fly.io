# Deploy Tailscale

To deploy a Tailscale Fly app,

1. First ensure ENV TSFILE in Dockerfile is using the latest tailscale binary.
2. Log your terminal in with `flyctl auth login`
3. Run `flyctl launch --name <app name>` ie: madrid-tailscale 
4. Choose the country (this will be used as the Tailscale machine name).
5. Create an auth key in Tailscale from https://login.tailscale.com/admin/settings/keys
6. Create an OAuth key in Tailscale admin console (https://login.tailscale.com/admin/settings/keys) with `Devices read and write` and add the tag `tag:xyz`. This should match the `--advertise-tags=tag:xyz` in start.sh
7. Then set it on the Fly app with `flyctl secrets set TAILSCALE_AUTHKEY="tskey-<key>?ephemeral=false"`. If ephemeral=false not set, then if machine goes offline, it won't re-connect as it cannot re-authenticate.
8. The app will update
9. It should now appear in Tailscale console.
10. Approve it in tailscale dashboard
11. Approve it as exit node and authenticate it.
