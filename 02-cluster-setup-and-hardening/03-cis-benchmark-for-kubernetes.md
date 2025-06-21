# CIS benchmark for Kubernetes
- The CIS Kubernetes Benchmark provides security best practices for Kubernetes clusters, targeting versions 1.16 to 1.18 in its v1.6.0 release. It is intended for:
    - System & application administrators
    - Security specialists
    - Auditors
    - DevOps/SRE teams securing Kubernetes environments

---

## What the Benchmark Covers
- Recommendations for both control plane and worker node components.
- File permissions, process arguments, and security settings.

#### Example: Securing Master Node Files
- kube-apiserver.yaml file should have 644 permissions
- Check with:
```bash
stat -c %a /etc/kubernetes/manifests/kube-apiserver.yaml
```
- Fix with:
```bash
chmod 644 /etc/kubernetes/manifests/kube-apiserver.yaml
```

---

## Tools for CIS Assessment
- CIS CAT (CIS Configuration Assessment Tool):
    - Free Lite version supports only a few platforms (Windows, Ubuntu, macOS, Chrome)
    - Does not support Kubernetes
- Open-source alternative for Kubernetes:
    - Kube bench
    - Designed for CIS Benchmark checks on Kubernetes
