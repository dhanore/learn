
# Azure Integration – Senior Developer & Architect Interview Guide

This guide is curated for **5–15 years experience** covering **C#, .NET, SQL, Azure, Azure PaaS, Microservices, Security, MongoDB, Terraform, CI/CD, SOLID, Design Patterns, Caching, and Entra ID (Azure AD B2C)**.

---

## 1. C# (Senior–Architect Level)

### Q1. Explain value types vs reference types and real-world impact.
**Answer:** Value types store data directly on the stack (or inline in objects), while reference types store references pointing to heap memory. This affects performance, memory pressure, and behavior when passed to methods. In high-throughput systems, misuse of reference types can cause GC pressure.

### Q2. What is immutability and why is it important?
**Answer:** Immutable objects cannot change state after creation. They improve thread safety, reduce side effects, and simplify reasoning in concurrent systems.

### Q3. async/await internals?
**Answer:** async/await compiles into a state machine. Await releases the thread while the task runs, improving scalability in I/O-bound workloads.

### Q4. Explain Span<T> and Memory<T>.
**Answer:** They provide safe, allocation-free access to memory, improving performance in high-load systems.

### Q5. How do you implement thread safety?
**Answer:** Use immutability, locks, Monitor, SemaphoreSlim, or concurrent collections. Prefer lock-free designs where possible.

(Additional curated advanced questions continue…)

---

## 2. .NET Runtime & Framework

### Q1. CLR vs .NET Runtime?
**Answer:** CLR manages memory, threading, JIT compilation, and security. .NET Runtime includes CLR plus base libraries.

### Q2. Garbage Collection modes?
**Answer:** Workstation vs Server GC. Server GC is optimized for throughput in server environments like ASP.NET Core.

### Q3. Dependency Injection lifetime?
**Answer:** Transient, Scoped, Singleton. Incorrect lifetime usage causes memory leaks or concurrency issues.

---

## 3. SQL Server

### Q1. Clustered vs Non-clustered index?
**Answer:** Clustered defines physical order. Non-clustered is a separate structure referencing rows.

### Q2. Deadlocks and resolution?
**Answer:** Occur due to cyclic locks. Resolve using proper indexing, shorter transactions, and retry logic.

### Q3. Query optimization approach?
**Answer:** Execution plans, index tuning, statistics updates, and avoiding RBAR patterns.

---

## 4. Azure Core

### Q1. Azure Resource Manager?
**Answer:** ARM provides declarative infrastructure management with idempotent deployments.

### Q2. Azure networking integration?
**Answer:** VNETs, subnets, private endpoints, service endpoints, and NSGs ensure secure communication.

### Q3. Identity & access in Azure?
**Answer:** Managed Identity + RBAC removes secrets and enforces least privilege.

---

## 5. Azure PaaS

### Q1. App Service vs AKS?
**Answer:** App Service is managed hosting; AKS offers container orchestration and flexibility.

### Q2. Azure Functions scaling?
**Answer:** Event-driven auto-scaling with Consumption or Premium plans.

### Q3. Service Bus vs Event Grid?
**Answer:** Service Bus is message-based; Event Grid is event-based reactive integration.

---

## 6. Microservices

### Q1. Monolith vs Microservices?
**Answer:** Microservices enable independent scaling and deployment at cost of complexity.

### Q2. Inter-service communication?
**Answer:** REST, gRPC, async messaging. Prefer async for resilience.

### Q3. Distributed transactions?
**Answer:** Avoid 2PC; use Saga pattern.

---

## 7. Application Security

### Q1. OAuth2 vs OpenID Connect?
**Answer:** OAuth handles authorization; OIDC adds authentication layer.

### Q2. Securing secrets?
**Answer:** Azure Key Vault + Managed Identity.

### Q3. OWASP Top 10 mitigation?
**Answer:** Input validation, auth, logging, least privilege, secure headers.

---

## 8. MongoDB

### Q1. Document vs relational modeling?
**Answer:** Embed for read performance, reference for normalization.

### Q2. Indexing strategy?
**Answer:** Compound indexes aligned to query patterns.

### Q3. Transactions in MongoDB?
**Answer:** Supported for replica sets but should be used sparingly.

---

## 9. Terraform

### Q1. State management?
**Answer:** Remote backend (Azure Storage) enables locking and collaboration.

### Q2. Modules?
**Answer:** Promote reuse, standardization, and governance.

---

## 10. CI/CD (Azure DevOps / GitHub Actions)

### Q1. Build vs Release pipeline?
**Answer:** Build produces artifacts; Release deploys them.

### Q2. Blue-Green deployment?
**Answer:** Zero-downtime deployment by switching traffic.

---

## 11. SOLID Principles

### Single Responsibility Principle
**Answer:** One reason to change. Improves maintainability.

### Open/Closed Principle
**Answer:** Open for extension, closed for modification.

(Other principles covered similarly)

---

## 12. Design Patterns

### Factory Pattern
**Answer:** Encapsulates object creation.

### Strategy Pattern
**Answer:** Enables runtime behavior selection.

### Circuit Breaker
**Answer:** Prevents cascading failures in distributed systems.

---

## 13. Caching

### Q1. In-memory vs Distributed cache?
**Answer:** In-memory is fast but local; Redis enables shared caching.

### Q2. Cache invalidation strategies?
**Answer:** TTL, write-through, cache-aside.

---

## 14. Entra ID / Azure AD B2C

### Q1. B2C vs Entra ID?
**Answer:** B2C is for customer identity; Entra ID is for enterprise identity.

### Q2. Custom policies?
**Answer:** Enable advanced identity workflows using XML-based definitions.

---

## Final Tip

Architect-level interviews focus on **trade-offs, scalability, security, and real-world decisions**, not just syntax.
