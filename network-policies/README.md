# Network Policies

# Links

Network Policies
https://kubernetes.io/docs/concepts/services-networking/network-policies/

Kubernetes — Debugging NetworkPolicy (Part 1)
https://faun.pub/debugging-networkpolicy-part-1-249921cdba37

Kubernetes — Debugging NetworkPolicy (Part 2)
https://pauldally.medium.com/debugging-networkpolicy-part-2-2d5c42d8465c

Kubernetes — Debugging NetworkPolicy (Part 3)
https://pauldally.medium.com/debugging-networkpolicy-part-3-83658d26747e

# Procedure

- [ ] Always create a namespace to insert your application. Don't use the default namespace as best practice

kubectl create -f https://raw.githubusercontent.com/andrelomonaco/SpringBoot/main/Namespace.yaml

- [ ] Create a deny-all-expect-DNS for all namespaces you create. In this example springboot namespace

kubectl create -f https://raw.githubusercontent.com/andrelomonaco/kubernetes/main/network-policies/default-deny-allow-dns.yaml
    
- [ ] Create the necessary ingress and egress network policies as your application requires
