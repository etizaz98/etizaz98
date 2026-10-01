# Etizaz Ahsan

**Lead Solutions Architect** at [Operanex](https://operanex.com) · DevOps & Cloud · Islamabad, Pakistan · [LinkedIn](https://www.linkedin.com/in/etizaz7)

I've spent 10+ years building and running production systems, from Node.js backends to AWS and Kubernetes infrastructure. Today I lead architecture and infrastructure for client platforms and still ship backend code. I'm also the main technical contact on those projects: requirements, scoping, estimates and delivery plans.

## Stack

- **Cloud & IaC:** AWS (EKS, RDS, EC2, S3, ECR, SQS, IAM) · OpenTofu · Pulumi · Ansible
- **Containers & CI/CD:** Kubernetes · Docker · Helm · GitHub Actions · Argo CD (GitOps)
- **Backend:** Node.js · TypeScript · Bun · NestJS · Express · tRPC · Socket.IO
- **Data & streaming:** PostgreSQL/PostGIS · Redis · Cassandra · MongoDB · MySQL · Kafka · Redpanda · MQTT
- **Frontend:** SvelteKit · React · Next.js

## Highlights

- **Pulumi → OpenTofu:** migrated all dev and prod infrastructure (EKS, ECR, networking, IAM, Kubernetes deployments) and retired the Pulumi stacks.
- **CI/CD:** built GitHub Actions pipelines (build, test, deploy) with OIDC auth to AWS; OpenTofu applies deploy to dev on merge and to prod on release.
- **GitOps on bare metal:** automated provisioning with Ansible and deployed an on-prem EKS cluster running Argo CD and Mattermost, plus the Kafka broker the dev environment uses.
- **Reliability:** recovered EKS clusters from node failures and tuned node sizing, memory limits and replica counts to stop thrashing; set up monitoring and alerting.
- **Cost & tooling:** moved RDS storage from gp2 to gp3; evaluated Redpanda vs. Confluent for Kafka on cost, scalability and operational fit.
- **Database tuning (earlier work):** indexing cut query times on Cassandra (30 s → 5 s) and MongoDB Atlas (1 min → 15 s); added a Lambda function for 30-day data retention, with a daily cron job moving older data to a backup database.

## Selected work

**Kimax Digital** — multi-tenant fleet telematics for heavy vehicles (Operanex, 2024–present). Architecture and DevOps lead. Provisioned the production Redpanda cluster and worked on backend route/trip state machines and Teltonika device integration.

```text
MQTT devices + Teltonika trackers
  → Kafka (Redpanda)
  → ~25 workers
  → live map · trips · REST API
```

**Turing Insights** — real-time vehicle telemetry (glasc.io, 2020–2024). Built the backend and owned its DevOps on Kubernetes; kept leading it after being promoted to technical lead.

```text
Vehicle position (every 5 s)
  → Cassandra
  → events (PostgreSQL) + state (Redis)
  → clients via Socket.IO
```

**Leza** — centralised identity service (glasc.io, 2019–2024). Led backend and architecture (Express proxy, Passport OAuth2, Ory Hydra for tokens, MongoDB audit logs); deployed and operated it on AWS.

**Visum** — manufacturing analytics and cost-cutting recommendations for a Unilever factory (glasc.io, 2020). Built the KPI analytics APIs on PostgreSQL (Sequelize + raw SQL), with Socket.IO live updates.

**[pipelinedemo](https://github.com/etizaz98/pipelinedemo)** — CI/CD demo repo: GitHub Actions → versioned images → Amazon ECR → deploy.

## Career

- **Oct 2024 – present** · Lead Software Solution Architect · [Operanex](https://operanex.com) (remote)
- **Jan 2022 – Oct 2024** · Technical Lead · glasc.io — led the development team
- **Jan 2019 – Dec 2021** · Senior Software Engineer · glasc.io — mentored junior engineers
- **Feb – Dec 2018** · MEAN Stack Developer · Aristostar, UAE
- **Sep 2015 – Jan 2018** · Frontend Developer (trainee) → Node.js Developer · uExel

**Education:** BS Computer Software Engineering, University of Engineering and Technology, Taxila (2011–2015)
