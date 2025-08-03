# DevSecOps Security Review – {{PROJECT_NAME}}

**Date**: {{DATE}}  
**Reviewer**:  
**Pipeline Tool**: (e.g., GitHub Actions, GitLab CI, Jenkins)

---

## 🛠 CI/CD Environment Overview

- Languages/Frameworks:
- Deployment target:
- Cloud/Infra stack:

---

## 🔍 Security Tooling In Use

| Stage     | Tool        | Status   | Notes                        |
|-----------|-------------|----------|------------------------------|
| Code Scan | SonarQube   | ✅       | Only Java scanned            |
| Secrets   | TruffleHog  | ✅       |                             |
| Container | Grype       | ❌       | Not yet implemented          |
| IaC       | Checkov     | ✅       | Terraform checked, no CDK   |

---

## 🧩 Risks Identified

- Hardcoded secrets
- Lack of SBOM
- Missing artifact validation

---

## 🛡 Recommendations

- Implement Grype or Snyk in build stage
- Use OPA/Gatekeeper for deployment gating
- Add DAST to staging pipeline

---

## ✅ Summary

> Status of DevSecOps maturity & next actions

---

## 📎 References

- [CIS CI/CD Benchmark]()
- [GitHub Actions Hardening Guide]()
