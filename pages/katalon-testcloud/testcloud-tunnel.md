---
title: "TestCloud Tunnel"
sidebar: katalon_studio_docs_sidebar
permalink: katalon-testcloud/docs/testcloud-tunnel.html
description: Introducing TestCloud Tunnel
---

## TestCloud Tunnel

A tunnel is used to secure the movement of data from one network to another.

TestCloud Tunnel enables a secure connection to local resources so that users can test their software/application in a restricted environment, avoiding unwanted external access from the global network.

TestCloud tunnel services can:

* Scale up with team size and work requirements.
* Reduce latency to a minimum by deploying the QUIC technology.
* Prevent overload and crashes when running many tunnel clients.
* Provide security by limiting access to authorized users with API keys.
* Save time by running multiple concurrent tests using multiple Edge servers.

## Configure TestCloud Tunnel

> Recommended specs:
>
> Recommended specs are still under evaluation during the trial period.

TestCloud tunnel can be configured to be used with Katalon TestOps or Katalon Studio. See: 
* [Integrate TestCloud with TestOps](https://docs.katalon.com/katalon-testcloud/docs/integrate-testcloud-with-testops.html#configure-the-testcloud-tunnel)
* [Integrate TestCloud with Studio](https://docs.katalon.com/katalon-studio/docs/testcloud-integration.html)

The tunnel-sharing feature is only available in TestOps. The tunnel created in Studio is separate from the one created in TestOps. You cannot use tunnels from TestOps and Studio interchangeably.

> Known limitations:
> 
> We currently do not support using tunnel connections behind a proxy.
> If you cannot load your app after correctly setting up local testing, you are probably behind a proxy.

## Some key information

TestCloud clients are distinct from tunnel clients. But setting up a TestCloud client in your machines on your private networks also sets up the tunnel client.

After starting the run command, the tunnel client does two things: 
- Spin up a fresh virtual machine (VM) that is used only for testing.
- Connect you to the TestCloud Tunnel server.

By default, the tunnel is closed after 30 minutes if there is no request or traffic (i.e. the tunnel is idle for 30 minutes). Consequently, the VM is shut down.

To start the tunnel again, enter the run command in the tunnel client.

## TestCloud Tunnel usage recommendations

We recommend the following practices to optimize your tunnel usage:

* Use a single tunnel or tunnel pool for each test suite or build, then tear it down at the end of your test.

    > Notes:
    >
    > You should launch the tunnel client before the test suite is triggered, then shut the tunnel client down once the test suite is finished.

* Use a machine with stable internet connection and large bandwidth to connect the tunnel client. This is to prevent test failure.

* Use a machine with high specs (e.g., RAM, CPU) when you run many concurrent tests.

* Run one tunnel client on one machine to avoid timeout and bandwidth issues that could cause test failure.

* To save your machine's bandwidth and resources, you can quickly close the tunnel using the shortcut Ctrl+C in the command-line interface (CLI) after you finish running tests.

## Reuse your Testcloud Tunnel configuration in a new machine

In the case that you encounter a test failure and decide to change your machine, first copy the current tunnel configuration to a new machine. Then delete the `client_id` in the command-line interface. You can then run the tests on the new machine.
