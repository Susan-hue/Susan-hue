# Hi, I'm Susan Amechi 👋

**Junior DevOps & Cloud Engineer · Backend Developer**
Owerri, Nigeria · Open to internships, SIWES placements and junior roles

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/susan-amechi-2b1302231/)
[![Blog](https://img.shields.io/badge/Blog-2962FF?style=for-the-badge&logo=hashnode&logoColor=white)](https://susan-amechi.hashnode.dev)
[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:amechisusanogechi@gmail.com)

---

## About me

I like the part of software that happens after `git push`: pipelines, containers, servers, monitoring, and the security around them. I work mostly on Linux with Docker, GitHub Actions, Terraform and AWS, and I write Django and Node.js backends so that I understand what I am shipping.

What you can expect from me:

- **I ship things that run.** My projects get deployed, wired into pipelines and monitored, not left as code in a repo.
- **I think about security early.** Hardened SSH, firewalls, least privilege, and secret scanning and security linting in CI.
- **I write things down.** I document how my systems work and blog about what I learn on [Hashnode](https://susan-amechi.hashnode.dev).

---

## Featured projects

### 🎓 Senet — academic operations platform for universities
**[Live demo](https://senet-pi.vercel.app)** · [Code](https://github.com/Susan-hue/senet)

A multi-tenant platform covering results approval, GPA/CGPA grading, continuous assessment and computer-based tests.

- Results move through a five-state approval chain, from a lecturer's draft through HOD and Dean approval to Senate ratification, with PostgreSQL triggers that keep submitted scores and the audit log append-only
- CI on every pull request: Ruff linting, Bandit security scan, Gitleaks secret scanning and 500+ Django tests against a PostgreSQL 16 service
- When CI passes on `main`, GitHub Actions deploys the API and a Celery worker to Fly.io, with the React frontend on Vercel

`Django REST Framework` `PostgreSQL` `Celery` `React` `TypeScript` `GitHub Actions` `Docker` `Fly.io`

### 🛡️ Sentinel — real-time DDoS detection engine
[Code](https://github.com/Susan-hue/DDos-Detector)

A Python daemon that tails Nginx logs in real time, learns what normal traffic looks like, and blocks attackers on its own.

- Sliding-window rate tracking per IP against a rolling baseline, flagging anomalies by z-score and rate multiplier
- Bans offending IPs with `iptables` within seconds, then releases them on a backoff schedule (10 min → 30 min → 2 hrs → permanent)
- Slack alerts, a structured audit log and a live metrics dashboard, with the detection logic written from scratch and no rate-limiting libraries

`Python` `Docker Compose` `Nginx` `iptables` `Slack webhooks` `Linux`

### 🏢 RoomSync — room booking platform with full observability
[Code](https://github.com/Susan-hue/roomsync)

A booking system for study rooms and labs with conflict detection and round-robin fairness, deployed as a monitored container stack.

- Docker Compose stack of Django, Nginx, PostgreSQL and Redis, monitored by Prometheus and Grafana with exporters for each service
- GitHub Actions pipeline that redeploys the backend to AWS EC2 over SSH whenever backend code is pushed to `main`
- JWT authentication with three roles, transactional bookings and an admin analytics dashboard

`Django REST Framework` `React` `TypeScript` `Docker Compose` `Nginx` `Prometheus` `Grafana` `AWS EC2`

### ☁️ Cloud Cost Tracker — serverless AWS billing alerts
[Code](https://github.com/Susan-hue/cloud-cost-tracker)

A serverless system that watches AWS spend, alerts when it crosses a threshold, and shows the history on a dashboard. Every resource is defined in Terraform.

- CloudWatch billing alarm → SNS → Lambda → DynamoDB, plus scheduled sampling with EventBridge
- Static dashboard on S3 and CloudFront, fed by an API Gateway and Lambda read endpoint
- Documented with an architecture diagram that traces each data path end to end

`Terraform` `AWS Lambda` `DynamoDB` `SNS` `CloudWatch` `EventBridge` `API Gateway` `S3` `CloudFront`

### 📬 SIWES Outreach Tracker — a CRM I built for my own placement search
[Code](https://github.com/Susan-hue/SIWES-TRACKER) · [Live app](https://siwes-tracker-woad.vercel.app) (private: it holds my real outreach data, so it asks for an access key)

An installable web app (PWA) for tracking outreach to cloud and DevOps companies.

- Pipeline board, interaction timeline and response analytics computed from the interaction log
- A scheduled GitHub Actions job checks daily for companies that have gone quiet and prepares an AI-drafted follow-up for me to review and send
- Django REST API on Render with Supabase PostgreSQL, React frontend on Vercel

`Django REST Framework` `React` `PostgreSQL` `GitHub Actions` `PWA`

### More work

| Project | What it is | Stack |
| --- | --- | --- |
| [go-web-app](https://github.com/Susan-hue/go-web-app) | Go web app with a GitOps delivery pipeline: CI runs tests and linting, CD builds a distroless image, pushes it to Docker Hub and updates the Helm chart | Go, Docker, Helm, Argo CD, GitHub Actions |
| [ENT312 CBT](https://github.com/Susan-hue/ENT312) · [live](https://ent312.vercel.app) | Exam practice app for a 300-level entrepreneurship course, with chapter filters, score breakdowns and retry-incorrect mode | Next.js, TypeScript, Tailwind CSS |
| [profile-api](https://github.com/Susan-hue/profile-api) | Profile management app with token authentication and validated avatar uploads | Django REST Framework, React, Vite |

---

## Toolbox

| Area | Tools |
| --- | --- |
| **Cloud** | AWS (EC2, Lambda, S3, CloudFront, DynamoDB, SNS, CloudWatch, EventBridge, API Gateway), Oracle Cloud, Fly.io, Render, Vercel |
| **Infrastructure as Code** | Terraform |
| **Containers** | Docker, Docker Compose, Helm |
| **CI/CD** | GitHub Actions, Argo CD, Git |
| **Monitoring** | Prometheus, Grafana, Slack alerting |
| **Linux & networking** | Ubuntu, Nginx, systemd, SSH hardening, UFW, iptables, DNS, TLS with Certbot |
| **Backend** | Python (Django, Django REST Framework, Celery), Node.js (Express) |
| **Databases** | PostgreSQL, Redis, MySQL, MongoDB, DynamoDB |
| **Languages** | Python, Bash, JavaScript, TypeScript |

---

## Experience

- **HNG Internship 14, DevOps track.** Shipped staged tasks against real deadlines, including an API deployed behind Nginx with systemd and the Sentinel detection engine above.
- **Self-directed cloud projects.** Deployed and hardened servers on AWS and Oracle Cloud with key-only SSH, UFW, least-privilege sudo, managed DNS and auto-renewing TLS.

---

## Let's talk

I'm looking for a team where I can take real ownership of pipelines and infrastructure and keep growing as an engineer. If you have an internship, a SIWES placement or a junior DevOps, cloud or backend role, I'd love to hear from you.

📧 [amechisusanogechi@gmail.com](mailto:amechisusanogechi@gmail.com) · 💼 [LinkedIn](https://www.linkedin.com/in/susan-amechi-2b1302231/) · ✍️ [Blog](https://susan-amechi.hashnode.dev)
