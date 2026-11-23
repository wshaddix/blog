---
title: Self-Hosting
order: 1
---

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

## A rented VPS

- TODO: A rented virtual server is a machine you administer. Patch the operating system, restrict the firewall, keep backups, and serve the site over TLS.
- TODO: Put a reverse proxy in front, and run one container for each app behind it.
- TODO: A self-hosted dashboard can build and deploy those containers. Dokploy is one option. See [A VPS instead of Azure](/building-a-saas/11-deployment/overview#a-vps-instead-of-azure).

### Staging and production on separate machines

- TODO: Run each environment on its own machine. Staging and production do not share a host.
- TODO: Store secrets for each environment separately, and run a restore drill so a backup is known to work. See [Restore drills](#restore-drills).

## Database on the app server

- TODO: Keeping the database on the application machine removes a network hop, and one failure takes the app and the data together.
- TODO: The two processes share CPU, memory, and disk. Size the machine for both, not for the app alone.

## Backups off the box

- TODO: On a schedule, dump the database to object storage. Keep a retention window, and encrypt the dump.
- TODO: Alert when an expected dump does not arrive.

## Restore drills

- TODO: On a schedule, restore a dump into an empty database and record how long it took.
- TODO: A dump you have not restored is an untested file.

## Practical Examples

- See [Building a SaaS: Deployment](/building-a-saas/11-deployment/overview) - The hosted path for this kind of app

## Related Topics

- See [App Service](/devops/azure/app-service)
- See [HTTP and the Web](/fundamentals/networking/http)

---

**Next:** [App Service](/devops/azure/app-service)
