**Serverless architecture** is a cloud computing model where developers focus on writing code without managing servers or infrastructure. The cloud provider handles the provisioning, scaling, and management of backend resources.

---

## 🚀 What Is Serverless?

In serverless computing:
- Developers deploy **functions**, not entire applications.
- Resources are **dynamically allocated** and **ephemeral**.
- You only pay for **actual execution time** (no idle cost).

> ⚠️ "Serverless" does not mean *no servers*, but rather *abstracted infrastructure*.

---

## 🔧 Key Components

| Component         | Description                                          | Examples                              |
|------------------|------------------------------------------------------|---------------------------------------|
| **FaaS** *(Function-as-a-Service)* | Event-driven functions in the cloud          | AWS Lambda, Azure Functions, GCP Cloud Functions |
| **BaaS** *(Backend-as-a-Service)* | Cloud-hosted backend services (e.g., auth, DB) | Firebase, AWS Cognito, Hasura         |
| **API Gateways**  | Interface for invoking functions via HTTP            | Amazon API Gateway, Azure API Mgmt    |
| **Triggers**      | Events that invoke functions (e.g., file upload, API call) | S3 event, Pub/Sub, HTTP request        |

---

## 🌐 How It Works

1. Developer writes a **function** (e.g., Python, Node.js).
2. Function is **uploaded** to the provider.
3. An **event** triggers the function.
4. Cloud **executes**, **scales**, and **terminates** the instance as needed.
5. Logs and metrics are handled via **monitoring tools**.

---

## ✅ Benefits

- **No server management**
- **Automatic scaling**
- **Cost-efficient** (pay-per-execution)
- **Faster deployment cycles**
- **Event-driven** flexibility

---

## ⚠️ Risks & Challenges

| Risk                     | Description                                         |
|--------------------------|-----------------------------------------------------|
| **Cold Starts**          | Delay in initial function execution after idle      |
| **Limited execution time** | Function run-time caps (e.g., 15 min in Lambda)   |
| **Vendor Lock-in**       | Tightly coupled to provider-specific APIs           |
| **Observability**        | Harder to trace/debug across ephemeral instances    |
| **Complex security model** | Surface area increases with more APIs & services |

---

## 🔐 Security Considerations

| Control Area            | Best Practices                                      |
|-------------------------|-----------------------------------------------------|
| **Authentication & AuthZ** | Enforce least privilege using IAM roles          |
| **Input Validation**     | Sanitize inputs to prevent injection attacks       |
| **Secrets Management**   | Use services like AWS Secrets Manager, Azure Key Vault |
| **Logging & Monitoring** | Enable CloudWatch, Azure Monitor, etc.             |
| **Dependency Management**| Keep packages updated, use SBOMs                   |
| **API Security**         | Protect endpoints with throttling, tokens, CORS    |

---

## 🔄 Use Cases

- RESTful APIs
- File processing (e.g., image resize on upload)
- Real-time analytics
- Event-driven automation
- Chatbots and voice skills (e.g., Alexa)

---

## 🧠 Serverless vs Traditional vs Containers

| Feature              | Serverless              | Containers               | Traditional VMs           |
|----------------------|-------------------------|--------------------------|---------------------------|
| **Management**       | None                    | Partial (via orchestration) | Full stack               |
| **Scalability**      | Auto                    | Manual or auto           | Manual                    |
| **Cost Efficiency**  | Per-invocation          | Per-runtime              | Always-on billing         |
| **Start Time**       | High (cold starts)      | Medium                   | Low                       |
| **Use Case Fit**     | Event-driven            | Microservices            | Monolithic apps           |

---

## 📎 Related Notes

- [[Cloud Infrastructure]]
- [[Cloud Security Posture Management (CSPM)]]
- [[Zero Trust Architecture]]
- [[Identity & Access Management (IAM)]]
- [[API Gateway]]

---

## 🏷 Tags

#serverless #cloud #faas #baas #api_security #event_driven #cloud_security

