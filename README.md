# 🚀 KubeSense AI

**KubeSense AI** is an AI-powered Kubernetes Troubleshooting Assistant built using **Google Gemma 4**. It helps developers and DevOps engineers diagnose Kubernetes issues by analyzing logs, manifests, and cluster information, then provides actionable recommendations, explanations, and troubleshooting steps.

---

## 📖 Overview

Troubleshooting Kubernetes can be time-consuming, especially for developers who are not Kubernetes experts. KubeSense AI acts like a senior Site Reliability Engineer (SRE), guiding users through diagnosing issues instead of simply answering questions.

The application can analyze Kubernetes logs, YAML manifests, and cluster events to identify problems, explain why they occurred, recommend fixes, and suggest the next commands to run.

---

## 🎯 Features

### ✅ Kubernetes Log Analyzer
Analyze pod logs and identify:

- CrashLoopBackOff
- ImagePullBackOff
- OOMKilled
- ContainerCreating
- Pending Pods
- FailedScheduling
- Networking Errors
- DNS Issues
- Database Connection Failures
- TLS Errors

---

### ✅ YAML Manifest Analyzer

Analyze Kubernetes manifests including:

- Deployment
- Service
- Ingress
- ConfigMap
- Secret
- StatefulSet
- DaemonSet
- Job
- CronJob

Detects:

- Missing resource limits
- Missing readiness/liveness probes
- Security risks
- Incorrect selectors
- Bad practices
- Configuration mistakes

---

### ✅ Interactive Troubleshooting

Instead of guessing, KubeSense AI asks for additional information when needed.

Example workflow:

```
User:
My pod is crashing.

↓

AI:
Please share:

kubectl describe pod <pod-name>

kubectl logs <pod-name> --previous

kubectl get events

↓

AI analyzes all information before providing recommendations.
```

---

### ✅ AI-Powered Recommendations

Every analysis includes:

- Problem Summary
- Root Cause
- Evidence
- Severity
- Recommended kubectl Commands
- Suggested Fix
- Preventive Measures
- Confidence Score

---

### ✅ Beginner-Friendly Explanations

Every issue is also explained in simple language for users who are new to Kubernetes.

---

## 🛠 Tech Stack

### Frontend

- Next.js
- TypeScript
- Tailwind CSS
- Shadcn UI
- Monaco Editor

### Backend

- FastAPI
- Python
- Pydantic

### AI

- Google Gemma 4

### Deployment

- Docker
- Kubernetes

---

## 📂 Project Structure

```
kubesense-ai/
│
├── frontend/
│   ├── app/
│   ├── components/
│   ├── lib/
│   └── package.json
│
├── backend/
│   ├── app/
│   │   ├── api/
│   │   ├── prompts/
│   │   ├── services/
│   │   ├── models/
│   │   ├── utils/
│   │   └── main.py
│   │
│   ├── requirements.txt
│   └── Dockerfile
│
├── docs/
│
├── docker-compose.yml
│
└── README.md
```

---

## ⚙️ How It Works

```
User Input
      │
      ▼
Paste Logs / YAML
      │
      ▼
FastAPI Backend
      │
      ▼
Prompt Builder
      │
      ▼
Google Gemma 4
      │
      ▼
AI Analysis
      │
      ▼
Structured Report
```

---

## 📋 Example Input

### Kubernetes Logs

```text
Back-off restarting failed container

CrashLoopBackOff

Error: failed to connect to database
```

---

## 📊 Example Output

```
Problem Summary

The application is repeatedly crashing after startup.

Root Cause

Unable to connect to the PostgreSQL database.

Evidence

failed to connect to database

Recommended Commands

kubectl describe pod

kubectl logs --previous

kubectl get secret

Suggested Fix

Verify database credentials and connectivity.

Prevention

Implement startup probes and validate configuration before deployment.

Confidence

94%
```

---

## 🔍 Supported Kubernetes Issues

| Category | Examples |
|----------|----------|
| Pod Issues | CrashLoopBackOff, Pending, OOMKilled |
| Image Issues | ImagePullBackOff, ErrImagePull |
| Scheduling | FailedScheduling, Node Affinity |
| Networking | DNS, Services, Ingress |
| Storage | PVC Pending, Volume Mount |
| Security | Secrets, RBAC |
| Application | Database, Redis, TLS |
| Configuration | ConfigMaps, Environment Variables |

---

## 🚀 Future Enhancements

- RAG using official Kubernetes documentation
- Incident Report Generator
- Cluster Health Dashboard
- kubectl Command Generator
- AI Chat Mode
- Multi-cluster Support
- Authentication
- Saved Analysis History
- Export Reports as PDF

---

## 💡 Why KubeSense AI?

KubeSense AI is designed to behave like a Kubernetes expert rather than a generic chatbot.

Instead of immediately producing an answer, it:

- Understands the context
- Asks follow-up questions
- Explains Kubernetes concepts
- Suggests practical debugging steps
- Provides actionable recommendations

This makes it useful for both experienced DevOps engineers and beginners learning Kubernetes.

---

## 🤝 Contributing

Contributions, feature requests, and bug reports are welcome.

Feel free to fork the repository and submit a pull request.

---

## 📄 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

Developed as a Google Gemma 4 AI project to simplify Kubernetes troubleshooting using Generative AI.
