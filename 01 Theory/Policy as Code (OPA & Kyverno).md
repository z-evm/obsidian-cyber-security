**Policy as Code (PaC)** is the practice of defining and enforcing policies—such as security, compliance, and operational rules—using code. In Kubernetes and cloud-native environments, PaC ensures **automated, consistent, and auditable** enforcement of best practices.

> 🧠 *If you can define it, you can enforce it—automatically.*

---

## 🧱 Benefits of Policy as Code

- ✅ Continuous enforcement across environments (dev, test, prod)
- 🧪 Testable policies integrated into CI/CD
- 🧾 Auditable and version-controlled in Git
- 🔁 Self-documenting infrastructure governance

---

## 🧰 Tools: OPA vs Kyverno

| Feature               | **Open Policy Agent (OPA)**        | **Kyverno**                          |
|------------------------|------------------------------------|--------------------------------------|
| Language               | Rego (custom policy language)      | YAML (Kubernetes-native syntax)      |
| Kubernetes Integration | OPA-Gatekeeper or OPA standalone   | Native Kubernetes admission controller |
| Policy Scope           | Cloud, APIs, microservices, K8s    | Kubernetes only                      |
| Complexity             | Powerful, but steep learning curve | Easy for K8s admins, readable syntax |
| External Use           | Can be used with Terraform, APIs   | Kubernetes only                      |

---

## 🔐 Common Policy Use Cases

| Use Case                          | Enforcement Goal                              |
|----------------------------------|-----------------------------------------------|
| Image source control             | Only allow signed/trusted container registries |
| Disallow privilege escalation    | No `runAsRoot`, no privileged containers       |
| Label enforcement                | Ensure labels for ownership, environment, etc. |
| Resource quotas & limits         | Enforce CPU/memory requests on all pods       |
| Secrets management               | Disallow secrets in environment variables     |
| Namespace isolation              | Prevent cross-namespace access                |

---

## 📜 OPA Example (Rego)

```rego
package kubernetes.admission

deny[msg] {
  input.request.kind.kind == "Pod"
  input.request.object.spec.containers[_].securityContext.privileged == true
  msg := "Privileged containers are not allowed."
}
```
> Deployed using **OPA Gatekeeper** as a `ConstraintTemplate`.

---

## 📜 Kyverno Example (YAML)

```
apiVersion: kyverno.io/v1
kind: ClusterPolicy
metadata:
  name: disallow-privileged
spec:
  validationFailureAction: enforce
  rules:
    - name: check-privileged
      match:
        resources:
          kinds:
            - Pod
      validate:
        message: "Privileged mode is not allowed"
        pattern:
          spec:
            containers:
              - securityContext:
                  privileged: false
```

> Kyverno rules can **mutate**, **validate**, and **generate** Kubernetes resources.

---

## 🔧 Policy Deployment & Testing

- **OPA**
    - Deploy with Gatekeeper (`ConstraintTemplate` + `Constraint`)
    - Validate with `conftest`, `opa test`
- **Kyverno**
    - Use `kubectl apply -f policy.yaml`
    - Test policies with `kyverno test` and `kyverno apply --resource`

---

## 🛠 Recommended Policies to Enforce

- ✅ Disallow privileged containers
- ✅ Require `readOnlyRootFilesystem: true`
- ✅ Block public container registries (e.g., DockerHub)
- ✅ Require specific annotations or labels
- ✅ Enforce TLS-only ingress traffic
- ✅ Restrict hostPath volumes

---

## 🔁 Integration into DevSecOps

- Run policy checks in CI pipelines:
    - `conftest` for OPA
    - `kyverno test` in GitHub Actions/GitLab CI
- Validate Helm charts and Kustomize overlays pre-deployment
- Monitor violations post-deployment with admission audit logs

---

## 🧩 Related Topics

- [[Kubernetes Security]]
- [[Infrastructure as Code (IaC) Security]]
- [[DevSecOps Pipeline]]
- [[Container Security]]
- [[Role Based Access Control (RBAC)]]

---

## 🏷 Tags

#policyascode #opa #kyverno #devsecops #kubernetes #rego #admissioncontroller #securitypolicy #automation #cloudnative #paccicd