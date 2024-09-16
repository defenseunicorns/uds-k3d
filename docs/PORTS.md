## Port Configuration

By default, `uds-k3d` will only expose ports `80` and `443` through `k3d` with a redirect from `80` to `443` within the Nginx configuration. The works for most packages however some may require additional TCP ports to be opened in order to provide / test all of their functionality.  To do so you can override the following:

### K3d Override

First set (or add to) `K3D_EXTRA_ARGS` to include all of the ports that you would like to expose:

```
--set K3D_EXTRA_ARGS="-p <port>:<port>@server:* -p 9999:9999@server:*"
```

### Nginx Configuration

Then allow the ports to pass through Nginx by setting `NGINX_EXTRA_PORTS`:

```
--set NGINX_EXTRA_PORTS="[<port>,9999]"
```

> [!IMPORTANT]
> This configuration only supports forwarding traffic exposed over the `tenant` gateway in `uds-core` - if you need to expose traffic over another gateway this configuration will not work.
