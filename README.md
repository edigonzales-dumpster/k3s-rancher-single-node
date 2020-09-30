# k3s-rancher-single-node

```
docker run -d -v ~/rancher-server/var/lib/rancher/:/var/lib/rancher/ --restart=unless-stopped -p 8080:8080 rancher/rancher:stable
docker run --restart=unless-stopped -p 80:80 -p 443:443 rancher/rancher:stable
```
----

```
curl -fsSL get.docker.com | sh
```

```
curl -fsL https://get.k3s.io | sh -
```

```
vi /etc/systemd/system/multi-user.target.wants/k3s.service
ExecStart=/usr/local/bin/k3s server --docker --no-deploy traefik
systemctl daemon-reload
service k3s restart
k3s kubectl get node
```

admin / admin

https://stackoverflow.com/questions/31037918/vagrant-ping-or-curl-from-guest-to-host-machine

```
curl --insecure -sfL https://172.42.42.1/v3/import/kqn6jw6mgdz7jzwfj8hjkzk2rrq49kgc8llt5t4n8hdjwkd7vj59jm.yaml | kubectl apply -f -

-> Fehlermeldung

curl --insecure -sfL https://172.42.42.1/v3/import/kqn6jw6mgdz7jzwfj8hjkzk2rrq49kgc8llt5t4n8hdjwkd7vj59jm.yaml
curl --insecure -sfL https://172.42.42.1/v3/import/kqn6jw6mgdz7jzwfj8hjkzk2rrq49kgc8llt5t4n8hdjwkd7vj59jm.yaml | kubectl apply -f -


```