ARG K3S_TAG="v1.30.2-k3s1"

FROM rancher/k3s:$K3S_TAG as k3s

COPY config.toml.tmpl /var/lib/rancher/k3s/agent/etc/containerd/config.toml.tmpl
