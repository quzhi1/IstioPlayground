# IstioPlayground
Playground for Istio

## Installation
1. Download Istio
```bash
curl -L https://istio.io/downloadIstio | sh -
# Add this to .zshrc
export PATH=$HOME/istio-1.13.2/bin:$PATH
```
2. Install Istio:
```bash
istioctl install --set profile=demo -y
kubectl label namespace default istio-injection=enabled
```
3. Deploy services
```bash
tilt up
```

## Troubleshooting
### Init problem
```bash
kubectl logs reviews-v1-745bcc464d-qtbdr -n default -c istio-init
```
Right now, Apple M1 chip still can't run Istio locally.
