# Priyank Pandey

**Site Reliability / DevOps Engineer.** I keep production systems available and I build the infrastructure underneath them.

4.5 years at Capgemini, promoted four times from Analyst to Consultant. I own production reliability for an enterprise platform processing 10M+ transactions a year against a 99.5% availability target — 24x7 on-call, P1/P2 major incident command, and the SLO and alerting model that catches failures before they become outages.

Alongside that I build and run [Jobingen](https://ai.jobingen.com), a live AI platform on AWS where the infrastructure work is entirely hands-on: the estate codified in Terraform on remote state with locking, keyless CI/CD through OIDC federation, deploys that are smoke-test gated with automatic rollback, and backups that are actually restore-tested.

Most interested in reliability problems where the fix is permanent rather than procedural.

---

### What I work with

**Cloud** &nbsp;AWS (EC2, EKS, ECS Fargate, Lambda, S3, IAM, VPC, ALB/NLB, Auto Scaling, ECR, SSM, CloudWatch) · Microsoft Azure

**Infrastructure** &nbsp;Terraform · CloudFormation · Docker · Kubernetes · Helm · Ansible

**CI/CD** &nbsp;GitHub Actions (OIDC) · Jenkins · Trivy · gitleaks · AWS SSM Run Command

**Observability** &nbsp;Prometheus · PromQL · Grafana · Alertmanager · OpenTelemetry · Splunk

**SRE** &nbsp;SLI/SLO · error budgets · burn-rate alerting · incident command · postmortems · capacity planning

**Languages** &nbsp;Python · Bash · SQL · PowerShell · Ruby · TypeScript

---

### Things I have built

**[eks-self-healing-platform](https://github.com/PriyankP2/eks-self-healing-platform)** — A six-service application on AWS EKS with a Python controller that watches the Kubernetes API and auto-remediates OOMKilled, Evicted and crash-looping pods, with a cooldown and structured audit logging. Helm across two availability zones, nginx Ingress behind an NLB, HPA to 8 replicas at a 65% CPU target, PodDisruptionBudgets, least-privilege RBAC per ServiceAccount. Jenkins pipeline with parallel builds, SHA-tagged ECR pushes and `helm upgrade --atomic` so a failed release rolls itself back. Prometheus, Grafana and Alertmanager with five custom alert rules.

**[LiveInfra](https://github.com/PriyankP2/LiveInfra)** — Continuously reads an AWS account and builds a live dependency graph, so teams know what depends on what *before* an incident rather than during one. Ranks blast radius through a variable-length graph traversal with per-resource-type severity weighting. PostgreSQL with Row-Level Security for tenant isolation; cross-account access through STS AssumeRole with an ExternalId on short-lived, strictly read-only sessions.

**AWS automation and compliance** — Detective and preventive controls in Python and boto3 that run without manual review: an [S3 encryption monitor](https://github.com/PriyankP2/S3-Encryption-Monitor) flagging unencrypted buckets, [EventBridge-triggered EC2 auto-tagging](https://github.com/PriyankP2/Auto-Tagging-EC2-Instances-on-Launch) at launch for cost attribution, and [tag-driven instance lifecycle control](https://github.com/PriyankP2/EC2-automation).

**[AWS-SAA03-questionbank](https://github.com/PriyankP2/AWS-SAA03-questionbank)** — A free, open, community-built bank of scenario-based practice questions for the AWS Solutions Architect Associate exam, with worked explanations.

---

### Certifications

AWS Certified Solutions Architect – Associate &nbsp;·&nbsp; Microsoft Certified: Azure Administrator Associate (AZ-104)

---

### Reach me

[LinkedIn](https://linkedin.com/in/priyankpandey-devops) &nbsp;·&nbsp; [ai.jobingen.com](https://ai.jobingen.com) &nbsp;·&nbsp; priyankpandey02@gmail.com

Open to Site Reliability, DevOps, Platform and Cloud Infrastructure roles.
