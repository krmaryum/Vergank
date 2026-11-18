# Wintel Training Class — English Translation
## Part 2: Enterprise Roles, Server Builds, and the Company Scenario

**Source:** `wintel.txt`, approximately lines 132–253. This is a readable English translation, retaining the order, participants, examples, and technical terms. The original transcript contains recognition errors and incomplete spoken sentences; these have been lightly cleaned for readability. Speaker labels match the source, even where the transcription may have combined speakers.

### 1. Identity and Access Management: An Enterprise Example

**Speaker 1 (Instructor):** We have many kinds of services. For example, inside a company, we need identity and access management. I use that term because when we connect these concepts with cloud computing later, they will be easier to understand. We also need user management.

Let's imagine we're all administrators working in different teams in an organization. Nadeem handles storage, Khalid handles virtualization, and Sarfraz handles physical servers such as HP and Dell. Whenever we need to obtain a server, we contact Sarfraz. Anil is responsible for the operating systems, such as Windows Server and Linux.

Today, let's keep the discussion general so these concepts become clear. Think of me as the data center architect. I'll coordinate work among all of you. Nadeem will be on the storage team; Khalid will handle virtualization, whether Hyper-V or VMware; Sarfraz will handle physical servers; and Anil will handle server operating systems.

Imagine each of you is also an architect with a team beneath you—perhaps two, five, or fifteen people. As the project grows, the team may expand. As the work is completed, the team may become smaller.

### 2. Establishing a Fictional Company for the Labs

**Speaker 1:** Let's assume that we are setting up a company. I'll use my company as an example, and we will keep the same company and domain naming throughout the course so the labs form a consistent scenario.

Suppose I've established a startup called **System SLA Technologies Private Limited**. It is an IT company that provides technical support services. We are working on its website to make it look more professional. The business provides IT support.

Now the startup has hired administrators, and we need to implement a data center. I believe everyone knows what a data center is. Anil, have you ever visited one?

**Speaker 3 (Anil):** No, sir. I work completely remotely, but I know that a data center is where servers are located and applications are hosted.

**Speaker 1:** Okay. Sarfraz?

**Speaker 3 [as labeled in source]:** I manage my company's own data center myself.

**Speaker 1:** Perfect. I will share some clips and videos of data centers so that you gain a clearer understanding of what the infrastructure looks like. Some things become much easier to understand after you see them.

### 3. Why Seeing Physical Servers Matters

**Speaker 1:** I received Windows Server training in 2006, using Windows Server 2003. In this course, we will use both **Windows Server 2022 and Windows Server 2025** in a mixed environment. I'll explain later why we are choosing both versions.

During my original training, I learned what Active Directory, DNS, dial-up, VPN, IAS, FTP, and routers were. I also completed networking training, including CCNA. But I still didn't know what a real physical server looked like in a production environment.

I started attending interviews around 2007. After completing several months of Windows Server, Exchange Server, and networking training, I began looking for opportunities. For a long time, I had never handled a physical server. Around 2009, I first looked up images of physical servers on Google.

Even today, you may meet people who have worked in IT for 18, 24, or 25 years without ever seeing a physical server. It can happen because all their work is remote. That doesn't make their work invalid; they simply never had that opportunity.

At AS Network Zone, we have some physical servers, and you will have a chance to do labs on them. We will also study the knowledge required to work with this hardware.

A common interview question, both then and now, is: **“Have you ever configured or built a new server?”** Some experienced candidates can answer yes, but many people who work only with preconfigured remote servers cannot.

**Speaker 2:** Yes, this question comes up in interviews. You're right; I hear it in almost every interview.

**Speaker 1:** I don't know how much physical-server work Nadeem and Khalid have done. Working remotely is one thing. But imagine a brand-new physical server arrives in front of you. You need to build it and install Windows, Linux, ESXi, or whatever the requirement specifies. An interviewer might ask you to describe the entire server-build process.

### 4. Instructor's Career and Experience with Server Builds

**Speaker 1:** I interviewed with HCL several times between 2007 and 2016. I was selected in 2016 but didn't join then; I joined IBM instead. Later, I interviewed at HCL again in 2019 and joined. I worked there until 2025, and afterward I was associated with the Times Group during 2025–2026. I left that role near the end of October and now work fully with System SLA.

System SLA is my private company, where I take on projects. I enjoy working directly on projects, and the company also earns more for me than my employment did. Teaching is my passion, so I continue providing training.

A major interview question remains: “How do you build a server?” When I was new, I thought building a server meant inserting a CD or DVD, installing Windows Server, and configuring the required server role. Laptops weren't so readily available around 2006–2007, so I thought primarily of a desktop computer and installation media.

Even today, some courses teach only operating-system installation and call it server training. However, **building a production server requires much more than installing the operating system.**

### 5. What a Complete Production Server Build Includes

**Speaker 1:** As a beginner, I assumed installing Windows Server would take around half an hour, and then the build would be finished. But when I started working in companies, I learned that a new server build might have an **eight-hour SLA** (Service Level Agreement).

Anil, have you built a new server, or even watched someone build one remotely?

**Speaker 3 (Anil):** No, sir. Everything is already configured. We simply log in and do our work. I haven't had an opportunity for hands-on server-build experience.

**Speaker 1:** That's a common problem. Interviews ask us many questions, but once we join a company, most infrastructure may already be configured. We don't always get the chance to learn how those systems were deployed.

A full server build can involve:

1. Configuring the physical server's remote-management interface, such as **iLO**.
2. Configuring **RAID** storage.
3. Updating server **firmware**.
4. Installing the required **operating system**.
5. Installing **monitoring agents**.
6. Installing **security patches** and operating-system updates.
7. Joining the server to the **domain** when required.
8. Configuring **roles, features, and permissions**.
9. Working with the **network team** to assign IP settings.
10. Working with the **security team** on antivirus and other controls.

Different teams may need to participate. That's one reason the agreed SLA includes several hours rather than only the time needed for the OS installation.

### 6. Why a Build SLA Includes Buffer Time

**Speaker 1:** Imagine the build is scheduled to start around 11:30 a.m. and must be delivered around 6:30 or 7 p.m. You might have other tasks, calls, meetings, breaks, or shift-handover responsibilities. If you cannot complete the task, you should hand it over to someone else instead of allowing the SLA to be breached.

If I worked continuously on one build, I might finish in four or five hours. But companies may allow up to eight hours so that there is a buffer.

Physical servers can also take longer to reboot than ordinary desktops or laptops. After installing patches, a restart could take ten, fifteen, or twenty minutes. During that time, someone might be pulled into another meeting or task. That is why we plan the work and include buffer time.

As the course continues, I will explain the systematic ways companies perform these activities.

Another interview question that confused me when I was new was, “Have you worked with tools?” At the time, I didn't know which tools they meant. Experience helps you become more thoughtful about questions and solutions. Rather than answering immediately, it is useful to understand a person's complete problem first and then decide how best to solve it.

### 7. Returning to the Company Scenario

**Speaker 1:** Now let's return to the startup and the different teams we've established.

Hello, Gautam. Sorry we didn't welcome you earlier; I think you joined a little late. We've just started discussing how companies work and how infrastructure is deployed.

**Speaker 2 (Gautam, as labeled in source):** Hello, sir. Yes, sir. Okay.

**Speaker 1:** The company is setting up a new business. Some infrastructure will be for the company's own employees.

For **identity and access management**, we will learn **Active Directory Domain Services (AD DS)**. We will also require **DNS** for domain-name resolution and **DHCP** for IP-address configuration.

If we publish a website or other applications, we will need web services. We won't want to run those public services over plain HTTP if secure HTTPS is required. We will need certificates, and we will study a **Certificate Authority (CA)** server and how certificates are issued.

These are examples of servers that System SLA Technologies might operate to support its own employees. Later, we will also discuss how the company earns revenue by providing technology services to customers.

---

**End of Part 2.** Continues with the discussion of selling IT services, resources, project management, IBM's hypothetical bank project, and data center planning.

**Editorial note:** This translation preserves the instructor's descriptions and scenarios. It is not a separate technical fact-check of all claims in the class.
