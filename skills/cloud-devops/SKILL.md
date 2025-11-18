---
name: cloud-devops
description: Master cloud platforms (AWS, Cloudflare), containerization (Docker, Kubernetes), infrastructure automation (Terraform), and DevOps practices. Build scalable, reliable infrastructure with modern tools. Use when deploying applications, managing infrastructure, or implementing CI/CD pipelines.
---

# Cloud & DevOps Skill

## Quick Start

### Docker Containerization
```dockerfile
# Dockerfile for Node.js application
FROM node:18-alpine

WORKDIR /app

COPY package*.json ./
RUN npm ci --only=production

COPY . .

EXPOSE 3000

CMD ["node", "index.js"]
```

```bash
# Build & run image
docker build -t my-app:1.0 .
docker run -p 3000:3000 my-app:1.0
docker push registry/my-app:1.0
```

### Kubernetes Deployment
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: my-app
        image: my-app:1.0
        ports:
        - containerPort: 3000
        env:
        - name: NODE_ENV
          value: "production"
        resources:
          requests:
            memory: "256Mi"
            cpu: "250m"
          limits:
            memory: "512Mi"
            cpu: "500m"
---
apiVersion: v1
kind: Service
metadata:
  name: my-app-service
spec:
  selector:
    app: my-app
  ports:
  - port: 80
    targetPort: 3000
  type: LoadBalancer
```

### Terraform Infrastructure
```hcl
# AWS VPC with EC2 instances
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 5.0"
    }
  }
}

provider "aws" {
  region = "us-east-1"
}

resource "aws_vpc" "main" {
  cidr_block           = "10.0.0.0/16"
  enable_dns_hostnames = true

  tags = {
    Name = "main-vpc"
  }
}

resource "aws_instance" "web" {
  count           = 3
  ami             = "ami-0c55b159cbfafe1f0"
  instance_type   = "t2.micro"
  subnet_id       = aws_subnet.main.id
  security_groups = [aws_security_group.web.id]

  tags = {
    Name = "web-server-${count.index + 1}"
  }
}

output "instance_ips" {
  value = aws_instance.web[*].public_ip
}
```

### GitHub Actions CI/CD
```yaml
name: Deploy Application

on:
  push:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3

      - name: Build Docker image
        run: docker build -t my-app:${{ github.sha }} .

      - name: Run tests
        run: npm test

      - name: Deploy
        run: |
          docker push my-app:${{ github.sha }}
          kubectl set image deployment/my-app my-app=my-app:${{ github.sha }}
```

## Docker & Containerization

### Docker Concepts
- **Images:** Read-only templates with application
- **Containers:** Running instances of images
- **Registries:** Central repositories (Docker Hub, ECR, GCR)
- **Volumes:** Persistent data storage
- **Networks:** Container communication
- **Compose:** Multi-container applications

### Docker Best Practices
- Use alpine base images (smaller)
- Multi-stage builds (reduce image size)
- Layer caching optimization
- Security scanning (Trivy)
- Non-root user execution
- Health checks

## Kubernetes Orchestration

### Core K8s Concepts
- **Pods:** Smallest deployable units
- **Deployments:** Desired state management
- **Services:** Network abstraction
- **ConfigMaps:** Configuration management
- **Secrets:** Sensitive data
- **PersistentVolumes:** Storage abstraction
- **StatefulSets:** Stateful applications
- **DaemonSets:** Per-node deployments

### Kubernetes Resource Management
- **Requests:** Guaranteed minimum resources
- **Limits:** Maximum resource usage
- **HPA:** Horizontal Pod Autoscaling
- **VPA:** Vertical Pod Autoscaling
- **Resource Quotas:** Namespace limits

### Kubernetes Best Practices
- Resource requests & limits
- Health checks (liveness, readiness)
- Pod disruption budgets
- Network policies
- RBAC (Role-Based Access Control)
- Service meshes (Istio, Linkerd)

## Terraform & Infrastructure as Code

### Terraform Fundamentals
- **Resources:** Infrastructure components
- **Data Sources:** Query existing infrastructure
- **Variables:** Input parameterization
- **Outputs:** Export values
- **Modules:** Reusable components
- **State:** Current infrastructure state
- **Backends:** Remote state storage

### Terraform Best Practices
- Module structure & reusability
- Variable validation
- Output documentation
- State management & locking
- Version pinning
- Workspaces for environments
- Testing (Terratest)

### Terraform Modules
```hcl
# Example: Reusable module
module "web_server" {
  source = "./modules/web-server"

  instance_count = var.instance_count
  instance_type  = var.instance_type
  ami_id        = data.aws_ami.ubuntu.id

  tags = {
    Environment = var.environment
  }
}
```

## AWS Cloud Services

### Compute Services
- **EC2:** Virtual machines with full control
- **ECS:** Container orchestration (Docker)
- **Lambda:** Serverless functions
- **Elastic Beanstalk:** PaaS for apps
- **AppRunner:** Container deployment

### Storage Services
- **S3:** Object storage (files, backups)
- **EBS:** Block storage for EC2
- **EFS:** Network file system
- **Glacier:** Archive storage

### Database Services
- **RDS:** Managed relational databases
- **DynamoDB:** NoSQL database
- **ElastiCache:** Caching layer
- **Redshift:** Data warehouse

### Networking Services
- **VPC:** Virtual network
- **ELB/ALB/NLB:** Load balancers
- **Route 53:** DNS service
- **CloudFront:** CDN service
- **API Gateway:** API management

### Monitoring & Logging
- **CloudWatch:** Metrics & logs
- **CloudTrail:** Audit logging
- **X-Ray:** Distributed tracing
- **EventBridge:** Event routing

## Cloudflare Services

### Performance & Security
- **CDN:** Content delivery network
- **DDoS Protection:** Attack mitigation
- **WAF:** Web Application Firewall
- **SSL/TLS:** Certificate management
- **Page Rules:** Caching rules

### Developer Services
- **Workers:** Serverless edge computing
- **Durable Objects:** Persistent state
- **D1:** Edge database
- **KV Storage:** Key-value store
- **Pages:** Static site hosting

## CI/CD & DevOps

### CI/CD Pipeline Stages
1. **Source:** Version control trigger
2. **Build:** Compile & package
3. **Test:** Automated testing
4. **Deploy:** Staging/production deployment
5. **Monitor:** Health & performance tracking

### Popular CI/CD Tools
- **GitHub Actions:** GitHub-integrated
- **GitLab CI:** GitLab-integrated
- **Jenkins:** Self-hosted, flexible
- **CircleCI:** Cloud-based
- **ArgoCD:** GitOps for Kubernetes

### Deployment Strategies
- **Blue-Green:** Two environments swap
- **Canary:** Gradual rollout
- **Rolling:** Sequential pod updates
- **Feature Flags:** Gradual enablement

## Monitoring & Observability

### Metrics & Dashboards
- **Prometheus:** Metrics collection
- **Grafana:** Dashboard visualization
- **CloudWatch:** AWS metrics
- **Datadog:** APM & monitoring

### Logging & Tracing
- **ELK Stack:** Elasticsearch, Logstash, Kibana
- **CloudWatch Logs:** AWS logging
- **Splunk:** Enterprise logging
- **Jaeger:** Distributed tracing
- **OpenTelemetry:** Observability standard

### Alerting
- **Alert Rules:** Threshold-based
- **Webhooks:** Integration endpoints
- **PagerDuty:** Incident management
- **Slack:** Notification channels

## Linux Administration

### Essential Commands
```bash
# File management
ls, cd, cp, mv, rm, mkdir, chmod, chown

# Process management
ps, top, kill, systemctl, journalctl

# Package management
apt/yum, npm, pip, brew

# Networking
ifconfig, netstat, curl, wget, ssh

# System monitoring
df, du, free, iostat, vmstat

# User management
useradd, userdel, passwd, sudo

# Network troubleshooting
ping, traceroute, dig, nslookup
```

### System Administration
- User & permission management
- Package management
- Cron jobs & scheduling
- Log management
- Security hardening
- Firewall configuration (iptables, firewalld)
- SSH key management

## Cloud Security

### Security Best Practices
- **Encryption:** At rest and in transit
- **Secrets Management:** Vault, AWS Secrets Manager
- **IAM:** Principle of least privilege
- **Network Security:** VPC, security groups, NACLs
- **Compliance:** SOC2, HIPAA, GDPR
- **Scanning:** Vulnerability scanning, code scanning

### Compliance Frameworks
- **SOC2:** Security controls for service providers
- **HIPAA:** Healthcare data protection
- **GDPR:** EU data privacy
- **PCI-DSS:** Payment card security
- **CIS Benchmarks:** Security configuration standards

## DevOps Culture & Practices

### Key Principles
- **Collaboration:** Developers & operations
- **Automation:** Reduce manual work
- **Measurement:** Metrics & feedback
- **Sharing:** Knowledge & responsibility
- **Continuous Improvement:** Iterate & optimize

### Metrics (DORA)
- Deployment Frequency
- Lead Time for Changes
- Mean Time to Recovery (MTTR)
- Change Failure Rate

## When to Use This Skill

### Cloud & DevOps Scenarios
- Deploying applications
- Managing infrastructure
- Setting up CI/CD
- Container orchestration
- Infrastructure automation
- Monitoring & logging
- Performance optimization
- Security hardening

## Resources

- **Docker:** Docker docs, Docker Hub
- **Kubernetes:** Kubernetes docs, CNCF resources
- **Terraform:** Terraform docs, Module registry
- **AWS:** AWS documentation, AWS Training
- **Cloudflare:** Cloudflare docs, Learning Center
- **CI/CD:** Tool-specific documentation
- **DevOps:** DevOps Handbook, DORA metrics
