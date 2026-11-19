# AZ-104 Day 01 — Interview Q&A (English)

> Questions are derived from lecture themes. Answers include additional technical clarification and are not direct instructor quotes.

## Q1. What is AZ-104 primarily about?

**Answer:** Managing Azure identity/governance, storage, compute, networking, and monitoring/maintenance of Azure environments.

## Q2. How does AZ-900 differ from AZ-104?

**Answer:** AZ-900 tests broad fundamentals; AZ-104 focuses on hands-on administration and implementation decisions.

## Q3. What is the purpose of AZ-305?

**Answer:** It addresses designing Azure infrastructure solutions; it is a separate exam/certification pathway.

## Q4. Why should a cloud admin understand on-premises data centers?

**Answer:** Networking, availability, power/failure domains, access, and workload requirements still shape cloud architecture.

## Q5. What is a business workload?

**Answer:** A set of applications, services, data, and dependencies that delivers a business capability.

## Q6. What should you ask before sizing 15 servers?

**Answer:** Identify services, performance baselines, peak load, growth, high availability, compliance, and ownership; validate whether 15 is justified.

## Q7. How do you estimate CPU and RAM?

**Answer:** Use measured application usage, peak concurrency, performance targets, headroom, and vendor requirements.

## Q8. What is a colocation facility?

**Answer:** A provider-operated site where customers place their equipment and purchase space, power, connectivity, and optional support.

## Q9. Is colocation the same as public cloud?

**Answer:** No. Colocation generally exposes customer-owned equipment; public cloud offers abstracted on-demand services and provider-managed layers.

## Q10. What is a private data center?

**Answer:** A facility dedicated to one organization’s own infrastructure and operational needs.

## Q11. Why check geographic location?

**Answer:** Site risks, legal requirements, latency, access, resilience and disaster-recovery planning depend on location.

## Q12. Why does cooling matter?

**Answer:** Hardware reliability depends on proper intake temperature, airflow, humidity and monitoring.

## Q13. What is a rack PDU?

**Answer:** A power distribution unit supplying electrical power to equipment in a rack.

## Q14. How do dual PSUs improve availability?

**Answer:** They can protect against a PSU or power-path failure when connected to independent, correctly provisioned feeds.

## Q15. Why spread servers across racks?

**Answer:** To reduce the impact of a single rack, PDU, networking, or power-domain failure.

## Q16. What is remote-hands support?

**Answer:** On-site provider staff perform agreed physical tasks on behalf of remote customers.

## Q17. Who may enter a shared data center?

**Answer:** Only authorized people under the provider’s security, escort, and access procedures.

## Q18. What is CAPEX?

**Answer:** Capital expenditure for acquiring or improving long-lived assets such as servers and infrastructure.

## Q19. What is OPEX?

**Answer:** Ongoing costs to operate services: energy, labor, support, subscriptions, and similar expenses.

## Q20. Is every expense after startup OPEX?

**Answer:** No. Buying more physical servers may remain CAPEX; classification depends on accounting treatment.

## Q21. What is an SLA?

**Answer:** A documented agreement defining service levels, measurements, and responsibilities.

## Q22. How is response SLA different from resolution SLA?

**Answer:** Response measures acknowledgement or engagement; resolution measures restoration or fix time.

## Q23. What do P1–P5 mean?

**Answer:** Priority labels used by some organizations; definitions and response targets differ by contract.

## Q24. How would you handle a P1 incident?

**Answer:** Acknowledge, confirm impact, engage on-call teams, communicate, mitigate, escalate, document, and restore within agreed objectives.

## Q25. Should high CPU alone always be P1?

**Answer:** No. Prioritize based on actual service impact, urgency, customer exposure and agreed incident criteria.

## Q26. Why ask customers about ownership of servers?

**Answer:** It changes procurement, licensing, maintenance, remote access, contracts, and support boundaries.

## Q27. What is a failure domain?

**Answer:** A group of components likely to fail together after one incident, such as one rack or power feed.

## Q28. What is a virtual network?

**Answer:** A logically isolated network defined through cloud software for connecting workloads.

## Q29. What is Azure Virtual Desktop?

**Answer:** Microsoft’s desktop/application virtualization service in Azure for delivering remote user sessions.

## Q30. What metrics should an administrator monitor?

**Answer:** Resource health, CPU/memory/disk, latency, failures, utilization, and cost/budget signals.
