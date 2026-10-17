# Self-Hosting

Run the app on a machine you control, and give the internet a way to reach it.

## A home server

- TODO: Run the process on a machine in the house, and publish the app you intend to share.
- TODO: Leave administration on the local network.

## CGNAT

- TODO: The carrier may assign no public address you can forward to.
- TODO: An inbound connection from the internet then has nowhere to land. A port forward on the home router does not create that address.

## Tunnels

- TODO: An agent on the home machine opens an outbound connection to a public endpoint and keeps it open.
- TODO: Visitors use that public name, and the traffic comes back down the tunnel to the app.
- TODO: Put authentication on the public name. The tunnel is the path, and access is a separate decision.

## Practical Examples

- See [Building a SaaS: Deployment](/building-a-saas/11-deployment/overview) - The hosted path for this kind of app

## Related Topics

- See [App Service](/devops/azure/app-service)
- See [HTTP and the Web](/fundamentals/networking/http)

---

**Next:** [App Service](/devops/azure/app-service)
