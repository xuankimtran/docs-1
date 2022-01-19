---
title: "TestCloud Tunnel"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/testcloud-tunnel.html
description: Introducing TestCloud Tunnel and how to utilize it
---

> Notice:
>
> We currently do not support using the tunnel connections behind a proxy.
>
> If you cannot load your app after setting up the local testing correctly, you are probably behind a proxy.

## TestCloud Tunnel

A tunnel is used to secure the movement of data from one network to another.

TestCloud Tunnel enables a secure connection to local resources so that users can test their software/application in a restricted environment, avoiding unwanted external access from the global network.

TestCloud tunnel services can:

* Scale up with team size and work requirements.
* Reduce latency to a minimum by deploying the QUIC technology.
* Prevent overload and crashes when running many tunnel clients.
* Provide security by limiting access to authorized users with API keys.
* Save time by running multiple concurrent tests using multiple Edge servers.

### How does TestCloud Tunnel work?

Once TestCloud clients have installed the tunnels in the machines which have access to their private network, they have set up the tunnel clients.

A tunnel client spins up a fresh virtual machine (VM) that is used only for testing.

By default, the tunnel is closed after 30 minutes if there is no request or traffic (i.e. the tunnel is idle for 30 minutes). Consequently, the VM is shut down.

To start the tunnel again, you enter the run command in the tunnel client.

After starting the run command, the tunnel client connects you to the TestCloud Tunnel server.

## Utilize TestCloud Tunnel

We recommend the following practices to optimize your tunnel usage:

* Use a single tunnel or tunnel pool for each test suite or build, then tear it down at the end of your test.

    > Notes:
    >
    > You should launch the tunnel client before the test suite is triggered, then shut the tunnel client down once the test suite is finished.

* Use a machine with stable internet connection and large bandwidth to connect the tunnel client. This would prevent test failure.

* Use a machine with high specs (e.g., RAM, CPU) when you run many concurrent tests.

    > Notes:
    >
    > We will provide recommended specs requirements soon.

* Run one tunnel client on one machine to avoid timeout and bandwidth issues that could cause test failure.

* To save your machine's bandwidth and resources, you can quickly close the tunnel using the shortcut Ctrl+C in the command-line interface (CLI) after you finish running tests.

## Configure TestCloud Tunnel

> Notes:
>
> * The tunnel-sharing feature is only available in TestOps.
> * The tunnel created in Studio is separate from the one created in TestOps. You cannot use tunnels from TestOps and Studio interchangeably.
> * The tunnel is automatically terminated after 30 minutes of idleness.

### For Katalon TestOps

See: [Integrate TestCloud with TestOps](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#configure-the-testcloud-tunnel).

### For Katalon Studio

See: [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html).

### Configure Testcloud Tunnel in a new machine

If test failure occurs and you change your machine, you need to copy the current tunnel configuration to a new machine. Then you delete the `client_id` in the CLI to run a new one.
