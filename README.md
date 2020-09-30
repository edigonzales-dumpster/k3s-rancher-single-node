# k3s-rancher-single-node

```
docker run -d -v ~/rancher-server/var/lib/rancher/:/var/lib/rancher/ --restart=unless-stopped -p 8080:8080 rancher/server
```
----

```
curl -fsSL get.docker.com | sh
```

```
url -fsL https://get.k3s.io | sh -
```

```
vi /etc/systemd/system/multi-user.target.wants/k3s.service
ExecStart=/usr/local/bin/k3s server --docker --no-deploy traefik
sudo systemctl daemon-reload
sudo service k3s restart
k3s kubectl get node
```

