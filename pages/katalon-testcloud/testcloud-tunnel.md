---
title: "TestCloud Tunnel"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/testcloud-overview.html
description: Introducing TestCloud and Beta Testing program for Katalon users
---

## TestCloud Tunnel

A tunnel is used to secure the movement of data from one network to another.

A TestCloud Tunnel enables a secure connection to local resources so that users can test their software/application in a restricted environment, avoiding unwanted external access from the global network.

A TestCloud Tunnel can:

* Scale up in accordance with the team size and user's needs.
* Offer latency by deploying a state-of-the-art technology QUIC.
* Prevent overload and crashes with multiple tunnel clients at the user's disposal.
* Provide a top-notch security by limiting access to authorized users with API keys only.
* Optimize performance by enabling the usage of multiple Edge-servers for running multiple concurrent tests.

### How does TestCloud Tunnel work?

Once TestCloud clients have installed the tunnels in the machines which have access to their private network (tunnel clients), the TestCloud tunnels spin up a fresh virtual machine (VM) that is used only for your testing.

By default, the TestCloud Tunnel is closed after 30 minutes if there is no request or traffic (i.e. the tunnel is idle for 30 minutes). Consequently, the VM is shut down.

To start the tunnels again, you run a command line in the machine where tunnel clients are installed.

> Notes:
>
> You can also run the command line in your CLI for shortcut.

After running the command line, the tunnel client connects you to TestCloud Tunnel's server inside it.

## Utilize TestCloud Tunnel

We recommend the following practices to optimize your tunnel usage:

* Use a single TestCloud Tunnel or tunnel pool for each test suite or build, then tear it down at the end of your test.

    > Notes:
    >
    > You should launch the tunnel client before the test suite is triggered, then shut the tunnel client down once the test suite is finished.

* Use a machine with stable Internet connection and large bandwidth to connect the tunnel client. This would prevent test failure.

* Use a machine with high specs (e.g., RAM, CPU) when you run many concurrent tests.

    > Notes:
    >
    > We will provide recommended specs requirements soon.

* Run one tunnel client on one machine to utilize the machine's resources. This would avoid test failure due to timeout or bandwidth running out.

    If test failure occurs and you change your machine, you need to copy the current tunnel configuration to a new machine. Then you delete the `client_id` in CLI to run a new one.

* Force quit by entering Ctrl+C in CLI after you finish running tests. This would avoid wasting your machine’s bandwidth and resources.

## Configure TestCloud Tunnel

### For Katalon TestOps

See: [Integrate TestCloud with TestOps](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#integrate-testcloud-with-testops).

### For Katalon Studio

See: [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html).


> Notes:
>
> * The tunnel-sharing feature is only available in TestOps.
> * The tunnel created in Studio is separate from the one in TestOps. You cannot use tunnels from TestOps and Studio interchangeably.
> * The tunnel is automatically terminated after 30 minutes of idleness.
