# Instalación

```bash
helm repo add wireguard https://bryopsida.github.io/wireguard-chart
helm repo update

 #helm show values wireguard/wireguard --version 0.26.0 > values-default.yaml
 kubectl create namespace wireguard
 helm upgrade --install wireguard wireguard/wireguard --version 0.26.0 -n wireguard 
 


 kubectl create secret generic pihole-admin-secret --from-literal=password=your-admin-password -n pihole
 helm upgrade --install pihole mojo2600/pihole -f values-modified.yaml --version 2.26.1 -n pihole
```

### Comandos

```bash
    kubectl cp pihole-56bb9845f6-ctd7n:/etc/pihole/custom.list ./custom.list -c pihole -n pihole
    kubectl cp pihole-56bb9845f6-ctd7n:/etc/pihole/setupVars.conf ./setupVars.conf -c pihole -n pihole
    
```