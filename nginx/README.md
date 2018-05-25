# Nginx proxypass

This configuration is for Nginx and require at least 1.9.13 version.

Configuration fields that needs to be updated:

* uid-name:
  * uid: the uid given by MySocialApp
  * name: the name you wish
* your-fqdn: your FQDN dns name

Note: Do not forget to setup your SSL certificates

# FAQ

## Why is there multiple time the same field in upstream backends?

The dns name is load balanced via round robin. To avoid to maintain a list of endpoints by hands, we're using the same endpoint entry multiple times. If an endpoint is dead, it is automatically removed in a few seconds/minutes from the round robin and retry won't be necessary anymore.
