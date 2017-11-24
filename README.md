# cato-accept-vm
vagrant config to setup the VM for HMRC CATO acceptance tests to be run

HMRC VPN required.

After installation check if chrome works and mongo also. Mongo is in old version ~2.8.
The sync folders needs to be adjusted and copy the last lines of .bashrc to the guest.

If you need swap use the moreSwap.sh

From Final version a box should be created and shared.
Useful vagrant commands: up, halt, reload, ssh, destroy.

Before starting `vagrant up` (from the cloned repo) you need to install vagrant and virtualbox.
To start the CATO set of microservices run: `sm --start CATO`. Probably less of those services are required.

If you want only run the test against the host you may lower the memomry to 3-4 GB. At ngnix.conf you'll find a ready config to set up the reverse proxy.
