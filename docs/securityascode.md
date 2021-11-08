# Security Policy as Code 
- [Introduction](#introduction)
- [Open Policy Agent (OPA)](#open-policy-agent-opa)
    - [Open Policy Agent in Kubernetes](#open-policy-agent-in-kubernetes)
    - [Open Policy Agent in OpenShift](#open-policy-agent-in-openshift)
    - [Open Policy Agent in Cloudflare Workers](#open-policy-agent-in-cloudflare-workers)
    - [Policy as Code in Terraform Cloud](#policy-as-code-in-terraform-cloud)
    - [Other OPA based solutions](#other-opa-based-solutions)
- [Other Policy as Code Scanning Tools](#other-policy-as-code-scanning-tools)
- [Kyverno](#kyverno)
- [Cloud Custodian](#cloud-custodian)
- [Apolicy](#apolicy)

## Introduction
- [Dzone: DevOps Security at Scale - Security Policy as Code](https://dzone.com/articles/devops-security-at-scale)
- [searchitoperations.techtarget.com: Kubernetes policy project takes enterprise IT by storm](https://searchitoperations.techtarget.com/news/252467102/Kubernetes-policy-project-takes-enterprise-IT-by-storm) A Kubernetes-friendly compliance as code project hosted by the CNCF has caught on among large enterprises in the first half of 2019, largely through word of mouth.
- [amazon.com: Policy-based countermeasures for Kubernetes – Part 1](https://aws.amazon.com/blogs/containers/policy-based-countermeasures-for-kubernetes-part-1/)
- [medium: Automate policies enforcement with Policy-as-Code 🌟](https://medium.com/airwalk/automate-policies-enforcement-with-policy-as-code-2f20aac9e2b0)

## Open Policy Agent (OPA)
- [OPA Open Policy Agent 🌟](https://www.openpolicyagent.org/) 
- OPA is most often used as an admission controller in Kubernetes. An admission controller is where all the semantic validation of Kubernetes resources occur before resources are persisted to etcd and controllers go off and start doing work.
- [magalix.com: Integrating Open Policy Agent (OPA) With Kubernetes 🌟](https://www.magalix.com/blog/integrating-open-policy-agent-opa-with-kubernetes-a-deep-dive-tutorial)
- [fugue.co: 5 tips for using the Rego language for Open Policy Agent (OPA)](https://www.fugue.co/blog/5-tips-for-using-the-rego-language-for-open-policy-agent-opa)
- [PolicyHub CLI, a CLI tool that makes Rego policies searchable 🌟](https://github.com/policy-hub/policy-hub-cli) a list of community OPA policies
- [blog.styra.com: Integrating Identity: OAUTH2 and OPENID CONNECT in Open Policy Agent](https://blog.styra.com/blog/integrating-identity-oauth2-and-openid-connect-in-open-policy-agent)
- [blog.styra.com: Rego Unit Testing](https://blog.styra.com/blog/rego-unit-testing)
- [github.com/instrumenta/policies: A set of shared policies for use with Conftest and other Open Policy Agent tools](https://github.com/instrumenta/policies)
- [itprotoday.com: Who Needs Open Policy Agent?](https://www.itprotoday.com/devops-and-software-development/who-needs-open-policy-agent) Open Policy Agent makes it possible to create a single set of configuration rules and deploy them automatically across a large-scale environment.
- [blog.styra.com: Dynamic Policy Composition for OPA](https://blog.styra.com/blog/dynamic-policy-composition-for-opa)
- [blog.styra.com: 5 OPA Deployment Performance Models for Microservices](https://blog.styra.com/blog/5-opa-deployment-performance-models-for-microservices)
- [blog.styra.com: Open Policy Agent: The Top 5 Kubernetes Admission Control Policies](https://blog.styra.com/blog/open-policy-agent-the-top-5-kubernetes-admission-control-policies) 
    - Trusted Repo
    - Label Safety
    - Privileged Mode
    - Ingress
    - Egress
- [thenewstack.io: Getting Open Policy Agent Up and Running](https://thenewstack.io/getting-open-policy-agent-up-and-running/)
- [siegert-maximilian.medium.com: Ensure Content Trust on Kubernetes using Notary and Open Policy Agent](https://siegert-maximilian.medium.com/ensure-content-trust-on-kubernetes-using-notary-and-open-policy-agent-485ab3a9423c) A detailed guide to help you to ensure that only signed images can get deployed on the cluster
- [blog.styra.com: Policy-based infrastructure guardrails with Terraform and OPA 🌟](https://blog.styra.com/blog/policy-based-infrastructure-guardrails-with-terraform-and-opa)
- [spacelift.io: What is Open Policy Agent (OPA) and how it works](https://spacelift.io/blog/what-is-open-policy-agent-and-how-it-works)

### Open Policy Agent in Kubernetes
- [infracloud.io: Kubernetes Pod Security Policies with Open Policy Agent](https://www.infracloud.io/kubernetes-pod-security-policies-opa/)
- [banzaicloud.com: Istio and Kubernetes ft. OPA policies](https://banzaicloud.com/blog/istio-opa/)
- [fugue.co: 5 tips for using the Rego language for Open Policy Agent (OPA)](https://www.fugue.co/blog/5-tips-for-using-the-rego-language-for-open-policy-agent-opa)
- [medium: Ensure Content Trust on Kubernetes using Notary and Open Policy Agent](https://medium.com/@siegert.maximilian/ensure-content-trust-on-kubernetes-using-notary-and-open-policy-agent-485ab3a9423c) A detailed guide to help you to ensure that only signed images can get deployed on the cluster. In this blog post you will learn how to enforce image trust on your Kubernetes Cluster by fully relying on two well known CNCF hosted open source solutions: Notary and Open Policy Agent (OPA).
- [kubermatic.com: Using Open Policy Agent With Kubermatic Kubernetes Platform](https://www.kubermatic.com/blog/using-open-policy-agent-with-kubermatic/)
- [k8s-security-policies](https://github.com/raspbernetes/k8s-security-policies) This repository provides a security policies library that is used for securing Kubernetes clusters configurations. The security policies are created based on CIS Kubernetes benchmark and rules defined in Kubesec.io. The policies are written in Rego, a high-level declarative language, its purpose-built for expressing policies over complex hierarchical data structures. For detailed information on Rego see the Policy Language documentation.
- [medium: Deploying Open Policy Agent (OPA) on a GKE cluster — Step by Step](https://medium.com/linkbynet/deploying-opa-on-a-gke-cluster-da4d3d77812c)
- [github.com/instrumenta/policies: A set of shared policies for use with Conftest and other Open Policy Agent tools 🌟](https://github.com/instrumenta/policies)
- [blog.styra.com: Using OPA with GitOps to speed Cloud-Native development](https://blog.styra.com/blog/using-opa-with-gitops-to-speed-cloud-native-development)

### Open Policy Agent in OpenShift
- [blog.openshift.com: Fine-Grained Policy Enforcement in OpenShift with Open Policy Agent 🌟](https://blog.openshift.com/fine-grained-policy-enforcement-in-openshift-with-open-policy-agent/)

### Open Policy Agent in Cloudflare Workers
* [compile OpenPolicyAgent policies into WebAssembly and run them on the edge](https://github.com/open-policy-agent/contrib/tree/master/wasm/cloudflare-worker)

### Policy as Code in Terraform Cloud
- [hashicorp.com: Securing Infrastructure In Application Pipelines](https://www.hashicorp.com/resources/securing-infrastructure-in-application-pipelines/) Learn how to use policy as code in Terraform Cloud to securely deliver applications.

### Other OPA based solutions
- [Fugue: Container and Kubernetes. Runtime infrastructure security](https://www.fugue.co/container-kubernetes) - [darkreading.com: Fugue Adds Kubernetes Security Checks to Secure Infrastructure-as-Code](https://www.darkreading.com/dr-tech/fugue-adds-kubernetes-security-checks-to-secure-infrastructure-as-code) Developers can apply proper security controls as they programmatically deploy Kubernetes clusters.

## Other Policy as Code Scanning Tools
- [thenewstack.io: Yor Automates Tagging for Infrastructure as Code](https://thenewstack.io/yor-automates-tagging-for-infrastructure-as-code/)
- [yor.io](https://yor.io/) Automated IaC tag and trace. Yor is an open-source tool that automatically tags infrastructure as code (IaC) templates with attribution and ownership details, unique IDs that get carried across to cloud resources, and any other need-to-know information. Run Yor as a pre-commit hook or in your CI/CD pipeline for code to cloud traceability and auditability.
- [checkov.io](https://www.checkov.io/) policy as code scanning tool
- [aws.amazon.com: Policy-based countermeasures for Kubernetes – Part 1](https://aws.amazon.com/es/blogs/containers/policy-based-countermeasures-for-kubernetes-part-1/) Choosing the right policy-as-code solution for your Kubernetes cluster:
    - OPA
    - Gatekeeper
    - Kyverno
    - k-rail
    - [MagTape](https://github.com/tmobile/magtape) Policy as code for kubernetes

## Kyverno
- [Kyverno 🌟](https://kyverno.io/) Kubernetes Native Policy Management. Open Policy Agent? That’s old school. Securely manage workloads on your kubernetesio clusters with this handy new tool, Kyverno.Kyverno is a policy engine designed for Kubernetes. With Kyverno, policies are managed as Kubernetes resources and no new language is required to write policies. This allows using familiar tools such as kubectl, git, and kustomize to manage policies. Kyverno policies can validate, mutate, and generate Kubernetes resources. The Kyverno CLI can be used to test policies and validate resources as part of a CI/CD pipeline. [youtube: The Way of the Future | Kubernetes Policy Management with Kyverno](https://www.youtube.com/watch?v=8fgrjBnxqi0&t=270s&ab_channel=AppSecEngineer)
- [venturebeat.com: How Nirmata plans to ‘conquer Kubernetes complexity’ with open source Kyverno](https://venturebeat.com/2021/08/10/how-nirmata-plans-to-conquer-kubernetes-complexity-with-open-source-kyverno/)
- [neonmirrors.net: Kubernetes Policy Comparison: OPA/Gatekeeper vs Kyverno 🌟](https://neonmirrors.net/post/2021-02/kubernetes-policy-comparison-opa-gatekeeper-vs-kyverno/)
- [kyverno.io: 56 sample policies 🌟](https://kyverno.io/policies/)
- [dev.to: Using Kyverno To Enforce EKS Best Practices](https://dev.to/rinkiyakedad/using-kyverno-to-enforce-eks-best-practices-cad)
- Tip: Use kyverno to monitor for usage of deprecated resources ahead of the Kubernetes 1.22 release (validation check to scan and report usage of deprecated resources) - [ref](https://github.com/kyverno/policies/issues/80#issuecomment-882332198) - [ref2](https://twitter.com/Marcus_Noble_/status/1417007780888825856)
- [aws.amazon.com: Easy as one-two-three policy management with Kyverno on Amazon EKS 🌟](https://aws.amazon.com/blogs/containers/easy-as-one-two-three-policy-management-with-kyverno-on-amazon-eks/)
- [kyverno.io: Mutating Resources](https://kyverno.io/docs/writing-policies/mutate/) Modify resources during admission control (Kyverno supports mutating resources).
- [squadcast.com: Kyverno - Policy Management in Kubernetes 🌟](https://www.squadcast.com/blog/kyverno-policy-management-in-kubernetes)
- [neonmirrors.net: Exploring Kyverno: Part 3, Generation](https://neonmirrors.net/post/2020-12/exploring-kyverno-part3/)
- [kyverno.io: Check deprecated APIs 🌟](https://kyverno.io/policies/best-practices/check_deprecated_apis/) Kubernetes APIs are sometimes deprecated and removed after a few releases. As a best practice, older API versions should be replaced with newer versions. This policy validates for APIs that are deprecated or scheduled for removal. Note that checking for some of these resources may require modifying the Kyverno ConfigMap to remove filters.
- [kyverno.io: Generating resources into existing namespaces](https://kyverno.io/docs/writing-policies/generate/#generating-resources-into-existing-namespaces)
- [kyverno.io: Add Pod Proxies](https://kyverno.io/policies/other/add-pod-proxies/) A kyverno policy to inject K8s Pod proxy env variables.
- [kyverno.io: Auto-Gen Rules for Pod Controllers](https://kyverno.io/docs/writing-policies/autogen/) Automatically generate rules for Pod controllers. 
- [kyverno.io: Require PodDisruptionBudget](https://kyverno.io/policies/other/require_pdb/) Use this kyverno sample to prevent app downtime by requiring all kubernetesio Deployments have a corresponding PodDisruptionBudget.
- [nirmata.com: Kubernetes Supply Chain Policy Management with Cosign and Kyverno](https://nirmata.com/2021/08/12/kubernetes-supply-chain-policy-management-with-cosign-and-kyverno/)
- [neonmirrors.net: Exploring Kyverno: Introduction 🌟](https://neonmirrors.net/post/2020-11/exploring-kyverno-intro/)
- [nirmata.com: Introducing Kyverno 1.4.2: Trusted And More Efficient!](https://nirmata.com/2021/08/18/introducing-kyverno-1-4-2-trusted-and-more-efficient/)
- [searchitoperations.techtarget.com: CNCF policy-as-code project bridges Kubernetes security gaps](https://searchitoperations.techtarget.com/news/252505548/CNCF-policy-as-code-project-bridges-Kubernetes-security-gaps) Kyverno, a CNCF policy-as-code sandbox project, can help platform engineers navigate the transition toward the successor to Kubernetes pod security policies.
- [Policy Reporter 🌟](https://github.com/kyverno/policy-reporter) Creates Prometheus Metrics for PolicyReports and ClusterPolicyReports. Ships with an optional Web UI and can send new Results to different Clients like Loki and Elasticsearch. Provides a optional Monitoring Subchart with a ServiceMonitor and Grafana Dashboards for the Prometheus Operator.
- [sesin.at: Securing Kubernetes with Kyverno: How to Protect Your Users From Themselves by Ritesh Patel](https://www.sesin.at/2021/08/28/securing-kubernetes-with-kyverno-how-to-protect-your-users-from-themselves-by-ritesh-patel/)
- [movi.hashnode.dev: Simplify Kubernetes Cluster Management with Kyverno](https://movi.hashnode.dev/simplify-kubernetes-cluster-management-with-kyverno-ckt6yxjqy0duy95s14groe7h4) Kyverno, a policy engine designed specifically for Kubernetes.
- [arun-sisodiya.medium.com: Kyverno — A Kubernetes native policy manager (Policy as Code)](https://arun-sisodiya.medium.com/kyverno-a-policy-manager-for-kubernetes-286f6e082062)
- [dev.to: Default Kyverno Policies for OpenEBS](https://dev.to/niveditacoder/default-kyverno-policies-for-openebs-4abf)
- [cloud.redhat.com: Automate Your Security Practices and Policies on OpenShift With Kyverno 🌟](https://cloud.redhat.com/blog/automate-your-security-practices-and-policies-on-openshift-with-kyverno)
- [A Kyverno policy to block custom snippet configurations for Kubernetes Nginx ingress (CVE-2021-25742](https://github.com/kubernetes/ingress-nginx/issues/7837)

## Cloud Custodian
- [Cloud Custodian](https://github.com/cloud-custodian/cloud-custodian) is a rules engine for managing public cloud accounts and resources. It allows users to define policies to enable a well managed cloud infrastructure, that's both secure and cost optimized.

## Apolicy
- [Apolicy](https://apolicy.io/)
- [sysdig.com: Sysdig and Apolicy join forces to help customers secure Infrastructure As Code and automate remediation](https://sysdig.com/blog/sysdig-and-apolicy-join-forces-to-help-customer-secure-infrastructure-as-code/)
