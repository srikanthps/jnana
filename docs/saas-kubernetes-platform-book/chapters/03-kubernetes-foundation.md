# Chapter 3: Kubernetes Platform Foundation

Kubernetes provides a common control plane for workloads, networking, scaling, deployment, and multi-cloud consistency.

## Managed Kubernetes Options

| Cloud | Service |
| --- | --- |
| AWS | EKS |
| Azure | AKS |
| Google Cloud | GKE |
| Oracle Cloud | OKE |
| DigitalOcean | DOKS |
| On-premises | OpenShift, Rancher, Talos, k0s, kubeadm |

## Core Add-ons

A production platform normally includes:

- Ingress or Gateway API controller
- CNI with network policy support such as Cilium or Calico
- cert-manager for TLS certificates
- ExternalDNS for DNS automation
- External Secrets Operator or Secrets Store CSI Driver
- Metrics Server
- Cluster Autoscaler or Karpenter
- OpenTelemetry Collector
- Policy controller such as Kyverno or OPA Gatekeeper
- Runtime security such as Falco or Tetragon

## Workload Standards

Every workload should define:

- Resource requests and limits
- Readiness, liveness, and startup probes
- Pod security context
- Non-root user
- Read-only root filesystem where possible
- Labels for service, owner, tenant, environment, and version
- Pod disruption budget
- Topology spread constraints for high availability

## Scaling

Use:

- Horizontal Pod Autoscaler for CPU, memory, and custom metrics
- Vertical Pod Autoscaler for recommendations or selected workloads
- KEDA for event-driven autoscaling
- Cluster Autoscaler or Karpenter for node capacity

## Network Foundation

Adopt default-deny network policy and explicitly allow only required service paths. Use dedicated node pools for sensitive, noisy, or enterprise workloads.
