# Wintel Training Class — English Translation
## Part 3: Enterprise Project Planning, Data Centers, Hardware Support, and Disaster Recovery

**Original transcript:** `wintel.txt`, lines **254–496** (inclusive).  
**Translation approach:** Detailed, readable classroom translation, preserving questions, examples, numerical scenarios, and discussion order rather than reducing the lecture to a summary. The source transcription occasionally merges speakers and contains unclear names/dates; such details are retained cautiously.

---

### 1. How Does an IT Support Company Earn Revenue?

**Instructor (Speaker 1):** We have been discussing how a company provides infrastructure for its own employees. But how does the company earn revenue? We have said that our company, System SLA Technologies, is an IT technical support company. How will that company actually make money? Does anyone have an idea?

**Participant (Speaker 2):** We should publish our services. We should tell potential customers, “We provide this service, we provide that service,” and explain the things we can offer.

**Instructor:** Correct. We can publish the information on our website. Suppose a customer is also starting a new business. We can say, “We can build a website for you.” If that customer needs storage, we can provide storage. If they need servers, we can provide servers. If they need networking infrastructure, we can provide that too.

Maybe another company needs a technical support team but does not have the authorization, resources, or budget to hire and maintain a complete team itself. We already have a technical team. We can provide support using that team.

You have probably come across third-party employment arrangements. Someone may say, “I work for IBM, but my primary employer is another company.” Or someone may say, “HCL pays my salary, but I work on an IBM assignment on behalf of HCL.” This kind of arrangement is very common in IT support projects.

### 2. The Meaning of a Resource in an IT Project

**Instructor:** Remember one important term: *resource*. Almost everything we discuss in a project may be referred to as a resource. Employees are also resources in the company’s project-planning language.

For example, Nadeem is a resource on the storage team. Khalid is a resource on the virtualization team. Sarfraz is a resource for physical server infrastructure, and Anil is a resource for the operating-system team—Windows and Linux servers.

In this discussion, a resource means something or someone that can be used to deliver a service or complete project work. We will keep using this word.

Today I am deliberately not going into the core technical details of Windows Server. First, we need to understand these fundamentals and how companies operate in real environments.

### 3. Marketing, Project Acquisition, and Professional Certifications

**Instructor:** System SLA Technologies can advertise its offerings through its website, Facebook/Meta, Google, and other platforms. We may also employ a marketing team to approach other businesses and bring back projects.

Those employees may have MBA qualifications, or they may come from technical backgrounds such as BTech or MTech and have additional certifications. Certifications that may come up in this discussion include **PMP**, **ITIL**, and **PRINCE2**. The source also mentions a name that sounds like “AZIL”; its precise identity is unclear in the recording.

As I am explaining it in this class, PRINCE2 is connected with learning a structured approach to projects and working with clients. PMP is connected with project management: when the project is obtained, how do we plan and manage it? With ITIL, we discuss how services and project work are made transparent and visible to the client.

We will discuss these frameworks in more detail later. For now, understand that a company has to win projects, organize its people, and then deliver the agreed services.

### 4. A Sample Banking Project Received from IBM

**Instructor:** Now let us assume our marketing colleague returns with a project. For this example, the project comes through IBM and is connected with a bank. We will refer to it as the IBM bank project, just to make the scenario easy to follow.

The colleague says, “Vargank, we have obtained a project. We need to set up infrastructure for a bank.”

In the IT industry, projects may belong to clients in the United States, the United Kingdom, or another country. Domestic projects exist as well, but many service teams work for clients who are geographically far away. I have also worked on a domestic Delhi Police project while employed at Tech Mahindra; the date range is unclear in the recorded transcript.

A person based in Delhi may support a data center in Bengaluru. Someone in Bengaluru may support infrastructure in Chennai, and someone in Chennai may support projects in Pune. The servers at those locations may ultimately be serving a completely different client company.

For our example, we need to implement a **data center** for a bank in the United States.

### 5. Think Beyond a Single Windows Server

**Instructor:** When you work on Active Directory, DNS, DHCP, or any other server role, do not think only about the single server assigned to you. Ask yourself where that server is actually hosted. It is inside a data center.

Your responsibility as an engineer should include understanding the broader environment. I do not know what access or responsibilities your managers have given you today. But I recommend exploring as many related systems as possible. Coordinate with other teams and learn what they do.

The more you understand about the physical infrastructure, virtualization, storage, networking, and other team activities, the better you will understand your own server. That is where the real server-build process starts—not merely at the Windows installation screen.

**Instructor:** Gautam, I forgot to ask you earlier: have you ever had the chance to build a new server? Are you there? Okay, no problem. Let us continue.

### 6. The Customer Requests 1,500 Servers

**Instructor:** IBM tells us: “Vargank, we need approximately **1,500 servers**.” How many?

**Participant:** Fifteen hundred.

**Instructor:** Yes, fifteen hundred. When I was new in IT, I wondered whether companies really had so many servers and why they would need them. If you have the same question, we will discuss the reasons later. Windows Server has multiple roles, but the number of roles alone does not explain why a company may require hundreds or thousands of servers.

Now forget your current job title for a moment. Think like a **data center architect**. IBM has given you the number 1,500. What questions will you ask next?

**Instructor:** I will ask Sarfraz first, because he already operates a data center.

### 7. The Questions a Data Center Architect Should Ask

**Participant (responding to the instructor's question):** Sir, if we are starting from scratch, I would ask many questions. What network devices will be required? What are the hardware requirements? What is the purpose of the data center? Are we building a disaster recovery site, an availability zone, or something else?

If the requirement is 1,500 servers, perhaps only 100 of them are physical servers and the rest are virtual. We must find out what physical hardware we are buying, how many CPU cores the machines have, how much RAM they need, and the other specifications. The answer to one question creates several more questions.

**Instructor:** Correct, correct. Those are all useful points. For now, we are not going deeply into the networking side. Our course is focused on server technology, so let us keep the discussion on physical servers and operating-system-level servers. However, we must at least be aware of the other infrastructure areas.

### 8. Physical, Virtual, and Cloud Server Distribution

**Instructor:** Not all 1,500 servers need to be physical. Some are physical servers, others are virtual machines, and some will be hosted in the cloud.

Sarfraz suggested approximately 100 physical servers. Let us expand the example a little. Suppose our requirements are:

| Deployment category | Example quantity | Where it runs |
|---|---:|---|
| Physical servers | 200 | In our physical data center |
| Virtual servers / VMs | 800 | Hosted on the on-premises physical infrastructure |
| Cloud servers | 500 | In a cloud environment |
| **Total** | **1,500** | Hybrid infrastructure |

These are illustrative numbers chosen during the lesson, not a final capacity plan. We would need hardware sizing before knowing whether 200 hosts are appropriate.

**Instructor:** Nadeem, in the cloud class earlier today, you gave a good answer: some systems could be in our physical data center and others in the cloud. That is exactly the idea here.

**Participant:** Oh, I see. Wonderful.

**Instructor:** For teaching purposes, we are discussing physical infrastructure first, then virtualization, and then cloud. This helps us build the understanding step by step.

### 9. Decide Where the Data Center Will Be Located

**Instructor:** IBM has told us how many servers it needs, but we still have not asked where the physical infrastructure should be located. Even the network manufacturers have not yet been selected. We may eventually use Cisco, Juniper, Aruba, Arista, or another vendor, but we are not finalizing those details today.

The next question to IBM is: “Where do you want the data center? Do you already have a location where we should install the servers?”

If IBM owns a suitable facility, we may deploy there. If IBM says, “We do not have a location; please recommend one,” then we must investigate and propose an appropriate site.

In our example, **200 physical servers** will host **800 virtual servers**, meaning approximately 1,000 systems depend on the on-premises data center. The remaining 500 will run in the cloud. So location planning matters a great deal.

**Instructor:** Notice how we began with the simple phrase “build a server” and have already reached data-center location planning.

**Participant:** Yes, yes.

### 10. Public Data Centers and Colocation

**Instructor:** There are public or third-party data centers that host infrastructure for different companies. If you search for data centers in Noida, you may find service providers such as NTT, Sify, Nextra, CtrlS, and other operators. The instructor also mentions Yotta as an example.

Suppose we need to install 200 physical servers that will support 800 virtual machines. We could contract with a data-center operator and rent dedicated **racks**. They can give us rack space, power, connectivity, and physical installation services, depending on the agreement.

A rack is the physical cabinet where servers and related equipment are installed. We can arrange for our hardware to be placed in those racks. The operator might even perform installation work on our behalf as a paid service.

We do not necessarily have to build and own a complete data-center building just because we have won a project. System SLA could accept the IBM project and subcontract part of the facility or physical operations work to a specialist data-center provider. We would need to check the cost, services, performance, and responsibilities before signing the contract.

### 11. Evaluating a Third-Party Data Center

**Instructor:** Suppose we decide to use Nextra. We cannot simply give the provider our money and assume everything will be fine. We need to verify whether it can deliver the required facilities and support for our 200 servers.

What if 20 servers are down? What if 50 are down? What if all 200 stop working? The customer will still expect us to deliver the service. We therefore need to understand the provider's infrastructure and responsibilities.

During evaluation, authorized members of our team may visit the facility, inspect its environment, and confirm where the equipment would be installed. The contract must make clear what services the provider will deliver.

The final location also depends on the customer's geography. Our company could be based in Delhi, but IBM might require the infrastructure in **Los Angeles, California**, instead of Delhi or Noida. A company does not have to be physically located in the same country as every client site it supports.

**Instructor:** Is it possible to arrange such a project in Los Angeles?

### 12. A Participant's Real Remote Data Center Example

**Participant (Speaker 2):** Yes, it is possible. I have a rack at a location the transcript identifies as Ottawa. There are **16 physical servers** there, and around **48 virtual machines** run on them. My company has hired a local consultant.

If there is a hardware issue or a physical restart is needed, I contact the consultant. The consultant coordinates with the team at the facility. The consultant also performed an on-site check, documented the setup, identified our contact people, and submitted a report. We paid for that service.

**Instructor:** Correct. We could arrange similar services in Los Angeles. We can find data centers there, pay for the necessary space and services, and coordinate the work without having every member of our own company permanently on site.

### 13. What If the Data Center Must Be Built On the Client's Premises?

**Instructor:** Now suppose IBM wants its servers installed within its own on-premises facilities rather than in a public data center. Our approach will be different.

First, our HR team may need to hire local Wintel and data-center engineers in Los Angeles. System SLA might employ four, five, or six people for the initial project.

Why would we not hire just one person? Because a **24×7** operation cannot depend on one engineer. Even three people are not necessarily enough for three shifts once leave and other absences are considered. The instructor suggests having two team members available per shift, and discusses hiring roughly five or six engineers for the site as an initial example. The exact staffing level would depend on the actual coverage requirement.

One or two existing team members may travel from India to visit the site and work with the locally hired engineers. This is one reason people are sometimes asked to travel internationally for IT projects.

During the initial deployment, the visiting and local teams inspect the facility, carry out the setup, and confirm that the systems are operational.

### 14. Contract Hiring and Changing Staffing After Go-Live

**Instructor:** Sometimes we hire people in another country on a contract basis. The cost of employing engineers in different countries may vary considerably. I might pay an engineer in India around seven lakh rupees annually, whereas the equivalent project arrangement abroad might cost thirty or forty lakh rupees or more in my illustrative example.

Once the implementation is finished and the project is stable, we may reduce the number of contract staff if the operational requirements allow it. Instead of maintaining the full implementation team, perhaps two, three, or several engineers will handle ongoing support.

With a third-party data center, the provider may already offer all the required on-site assistance. In that arrangement, we might not need to hire our own local engineers at all. The important point is to understand precisely what the contract covers.

### 15. New Hardware, Vendor Support, and Server Replacement

**Instructor:** Assume the 200 physical servers are new systems purchased for this project. We have not picked up random old servers from a market and put them into an enterprise production environment.

When buying new server hardware, we normally also purchase a support agreement. In the instructor's example, that agreement lasts **five years**. If we need to continue using the equipment after that, we may be able to extend support for one or two more years.

Many organizations plan to replace physical servers after roughly five or six years. Some may keep them for seven years, and longer use can happen, though the instructor considers eight or nine years unusual for this scenario. One reason for delayed replacement may be that the client has not approved downtime to migrate applications and workloads.

When hardware is considered obsolete, the organization can retire or sell it and purchase newer equipment. This refresh cycle is part of managing a physical server estate.

**Instructor:** We have already spent a lot of time discussing these processes and we still have not installed the server operating system. That is intentional: server building involves infrastructure decisions long before OS installation.

**Participants:** Yes, sir.

### 16. Student Question: Can We Physically Enter a Public Data Center?

**Participant:** Sir, I have a question. Sorry, I have a sore throat. You mentioned that when a company owns servers installed inside a public data center, its own staff might not be allowed to enter. But sometimes a company representative can visit. I am confused about when access is permitted.

**Instructor:** Direct visits are usually restricted. I called this a *rare token* in the class. In other words, specific authorization and a valid reason may be required. The fact that our company owns the hardware does not mean any one of our employees can walk into the facility whenever they want.

Let us take a hypothetical example involving Anil, who works for System SLA. Imagine he has worked here for two or three years and has not received a salary increment for two years. He enters a data center to inspect our systems. Accidentally—or even intentionally—he disturbs a cable or switches off a device belonging to another company. I am not accusing Anil of anything; this is just a risk example.

Who would pay for the damage? Anil? System SLA? The data-center operator? These questions explain why physical access must be controlled.

**Participant:** Yes, I understand. It is a very big risk.

**Instructor:** Exactly. A similar risk can exist even in a company's own facility. Someone might be leaving the company and, on the last working day, switch off a network device. The point is not to assume that everyone will do this, but to understand the security risk and the need for supervision and access controls.

### 17. Student Question: How Do We Troubleshoot If We Cannot Enter?

**Participant:** That makes sense. But if our server goes down, its services stop, or some troubleshooting is needed, what do we do if we cannot enter the data center?

**Instructor:** The data-center provider has its own engineers and representatives on site. Those people give us technical assistance. They can show us the problem over a video call or a Microsoft Teams call. They can share their laptop screen, show the physical server, and give us access to its remote management interface, such as **iLO**, where available.

If iLO itself is not responding, the local engineer can help inspect the issue physically. You can still receive support remotely, even when you are not standing in front of the equipment.

I am not saying it is impossible for us to visit. With specific permission, System SLA staff can be authorized to enter. But a routine hardware fault does not automatically mean our own representative must enter the facility.

**Participant:** Okay, now it makes complete sense.

### 18. OEM Engineers, Supervised Repairs, and Access Logs

**Instructor:** Suppose a network card or cable fails on an HP or Dell server. We raise a support case with the manufacturer or vendor. An **OEM engineer** comes to the data center to work on the hardware.

A representative of the data-center provider accompanies the OEM engineer. That person observes the work and makes sure the engineer works on the correct server and follows the site rules. When the repair is complete, both people leave according to the facility's process.

The visit is also recorded in the data center's access logs. This accountability is another reason we purchase hardware support: the vendor and on-site provider can coordinate work under controlled conditions.

**Participant:** Thank you very much. This is very clear now.

**Instructor:** You're welcome.

### 19. Planning a Disaster Recovery Site

**Instructor:** Suppose the data center has now been implemented and we have decided that our primary location will be in Los Angeles. Sarfraz raised another important point earlier: we should also have a **disaster recovery (DR)** site.

Of course. With so many servers, some systems will be critical. We need to ask IBM where it wants the DR location. The customer may already have an answer, or our team may be expected to recommend an appropriate site.

As architects, we should be prepared to make recommendations rather than coming to the discussion without options. We could ask a data-center provider where its other facilities are located and which locations could support a DR arrangement.

### 20. RTO, RPO, and Disaster Recovery Drills

**Instructor:** When discussing a primary data center and disaster recovery, we need to think about **RTO** and **RPO**. We discussed these ideas in our cloud computing class too.

RTO and RPO help define what happens if the primary data center becomes unavailable, how quickly operations should be restored, and how much recent data the organization may have to recover or could lose. These are important considerations when choosing the DR design and location.

It is also not enough to build a DR site and assume it will work forever without checking it. Organizations run **DR drills**, meaning tests of the recovery arrangements. Depending on the organization, those tests may be monthly, quarterly, or every six months. The instructor describes a test in which the primary data-center service is deliberately made unavailable under controlled conditions to check whether recovery works.

**Participant:** That is a good thing.

**Instructor:** Yes. We cannot simply say, “We will find out when a real disaster happens.” A drill reveals which parts of the recovery environment are functioning and which parts are failing. The team then creates tickets for the problems identified and works to resolve them.

**Participant:** Right, very clear.

### 21. What We Have Not Yet Covered

**Instructor:** Notice how our discussion began with a server build and has grown into a complete data-center discussion. We have spent about half an hour on the environment, and we still have **not installed an OS**.

We have not properly discussed storage, networking, backup tools, or monitoring tools either. We are still focusing on the server side and the decisions that surround it.

**Instructor:** Anil, are you with us? Any doubts or questions?

**Participant:** Yes, sir. No questions.

**Instructor:** Sarfraz?

**Participant:** No, sir. Let us continue.

### 22. Transition to the Next Section: Implementing the Servers

**Instructor:** We have now discussed where the primary data center and DR site should be. For another version of the class example, suppose we put the primary data center in **Delhi** and the DR site in **Hyderabad**. This gives us a local scenario to work with.

Now it is time to consider the **implementation**. That is where our next discussion will begin.

---

**End of Part 3.** The following transcript section begins at **line 497**, where the instructor asks whether Windows Server must be installed individually on each of 200 machines and how that could be done within the project timeline.

> **Source fidelity note:** Quantities, site choices, staffing figures, support years, and recovery-drill examples here are examples from the instructor, not universal requirements. The source uses some imperfect terminology and transcription; this translation conveys the classroom discussion without presenting every remark as an independently verified technical rule.
