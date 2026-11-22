# Wintel Training Class — English Translation

## Part 01: Introductions, Instructor Background, And Wintel Fundamentals

Note: This is an English rendering of the opening portion of the uploaded transcript. Speaker labels follow the source. Some spoken words were unclear in the source transcription; technical terminology is retained as spoken, without independently verifying technical claims.

Speaker 1: I would also like to ask one thing. Are we comfortable in Hindi or English, or should the class remain in a mixed-language format?
Speaker 2: Hindi. Hindi.
Speaker 1: Okay, Hindi. What about Anil? Anil, are you comfortable in Hindi?
Speaker 3: Yes, sir. I'm comfortable in Hindi.
Speaker 1: Okay. Whenever you face issues or challenges, you can ask me or stop me. If you're uncomfortable with something, please say so, and we'll adjust accordingly. Right?
Speaker 3: Yes, yes.

Speaker 1: Let's do one thing. First, we'll introduce ourselves today. After that, we'll discuss the course curriculum and then begin the topics. Right? Let's start with you, Anil ji.
Speaker 3: I'm sorry. Nadeem, you can go ahead.
Speaker 2: No, no. Please continue.
Speaker 1: No issues, Anil.
Speaker 3: Hi, everyone. My name is Anil Kumar. I've been working as a service desk analyst for the past four years. I want to enhance my skills and learn Windows Server. I watched a couple of Vargank sir's videos on YouTube, learned about this training, and joined. I'm excited to learn Windows Server and get hands-on experience.
Speaker 1: Okay, that's completely fine. So your main objective is to learn this curriculum in order to change jobs or perhaps get promoted within the same company, with responsibilities related to server technology. Right?
Speaker 3: Yes, sir.
Speaker 1: Thank you very much, Anil. Hello, Sarfraz sir. How are you?
Speaker 4: I'm good, sir. Thank you.
Speaker 1: I think we're connecting after a long time.
Speaker 4: Yes, after June 2024.
Speaker 1: Yes.
Speaker 4: It's good to learn with you again. We also studied VMware 7.
Speaker 1: Yes, I think it's been almost three years?
Speaker 4: Approximately.
Speaker 1: Yes.
Speaker 4: January 2024.
Speaker 1: Yes. I would also like to update Khalid. Khalid is learning through the same source. Sarfraz and I connected when I started freelancing with KR Network Cloud, and he attended my batch. He is also geographically close to you.
Speaker 1: Sarfraz, please briefly introduce yourself and explain why you want to take this course.
Speaker 4: Sir, as we discussed last time, I mainly want to polish my knowledge. As you know, I have over ten years of experience working as a VMware and storage administrator. Now I'm trying to change jobs and improve my knowledge again.
Speaker 1: Okay. Thank you, Sarfraz sir.
Speaker 4: Thank you, sir.
Speaker 1: Nadeem ji?
Speaker 2: Yes. I've been working here in Dallas, Texas, but I'm based in Houston, Texas. My career has included Bank of America and Arista, and now I'm working with PNC Bank in IT. My knowledge of Windows and cloud computing isn't very strong, so I want to upskill, learn new technologies, and advance my career.
Speaker 1: Okay, absolutely. Thank you, Nadeem ji. Hello, Khalid.
Speaker 2: I'm new to this field. I attended your VMware classes previously. When you started this course, I thought I should take this one as well.
Speaker 1: Okay. Thank you. I believe everyone can see my screen.
Speaker 2: Yes, it's clear.
Speaker 4: Yes, sir.

INSTRUCTOR INTRODUCTION

Speaker 1: Thank you. My name is Vargank Panchal. I have completed 18 years in the IT industry. I started my journey with Windows Server 2003. Windows Server 2025 is now available in the market, but the curriculum still has many challenges and ups and downs.

Whenever I face difficulties or gain experience—good or bad—I try to share that experience with my students. I've been a Microsoft Certified Trainer since 2013, and you can see the certificate behind me.

I previously worked as a data center architect and have had opportunities to work with many technologies. Most of my 18 years of experience has involved Windows Server. I started with Windows Server 2003, followed by 2008 and 2012. Windows Server 2016 had less market presence in my experience, while Windows Server 2019 and 2022 are still being used. Windows Server 2025 is also available, and we'll discuss why organizations may not yet be using it widely.

I also have experience in VMware, virtualization, and VMware Cloud Foundation. I have over 15 years of experience in virtualization. Organizations often expect Windows Server engineers to know multiple technologies, so I learned VMware, ESXi, vCenter Server, clusters, and data centers. I worked on deployment, configuration, and troubleshooting projects.

Currently, most of my work is with VMware and Windows Server. I have also worked in cloud computing for about nine years, especially Microsoft Azure. At HCL, I was involved in a project called Adoku, where we managed approximately 20,000 cloud servers and 15,000 servers in an on-premises data center.

That was valuable experience because we dealt with many daily challenges and tickets. I was a technical team lead managing Windows and VMware teams rather than personally carrying out every task.

I've also worked with messaging technology, including Exchange Server and Office 365. If you're working with Windows Server and VMware, it's also useful to understand Office 365. Compared with a full cloud or Windows Server curriculum, Office 365 is a relatively small subject. In my view, two hours of daily study could let someone cover the curriculum in around three weeks.

For the past four years, I've also worked as a data center architect and on solution designs. Through freelancing and my company, System SLA Technologies Pvt. Ltd., I've implemented data center projects involving Ubuntu, Windows Server virtualization, OpenStack, and other platforms. We've implemented monitoring tools too, and we'll discuss why they are used.

The main point is that knowledge of only one technology may not provide the best opportunities in IT. Companies need people who understand server technologies, virtualization, cloud, messaging, and security. To progress to an architect-level role, you need knowledge of multiple technologies.

I provided basic O-level and A-level training from 2004 to 2007. I began my Windows Server journey around 2006, when I was still a beginner. At that time, newspaper advertisements frequently mentioned requirements for MCSE and CCNA professionals. That motivated me to enroll in server training.

Since then, I've worked in the industry and provided corporate training, often on weekends. My education includes a BCA from IGNOU and an MCA from PTU. However, much of the academic content—such as arrays, object-oriented programming concepts, and circuitry—doesn't arise directly in my routine infrastructure work.

If you need to contact me, you can use the contact details on the screen. Please ask if you have any questions.
Speaker 2: Wonderful.

ABOUT THE TRAINING ORGANIZATION

Speaker 1: AS Network Zone is a subsidiary of System SLA. System SLA is my primary company, while AS Network Zone provides training. We are present on LinkedIn, YouTube, Instagram, and Facebook. Vishal is our training coordinator. You can contact us through the shared email address or social-media handles. I'll share the links after class.

WHAT IS WINTEL?

Speaker 1: Before we start, I want to ask: Does anyone know what Wintel means? Why was it given that name? Even when I search Google, I've seen many Wintel job openings since 2007.
Speaker 2: I only know that it relates to Windows and Intel.
Speaker 1: Okay.
Speaker 2: I would say the same.
Speaker 2: Sir, I haven't studied it in detail. I only understand that the names of two technologies were combined, and it also involves hybrid infrastructure.
Speaker 1: Okay. Anil?
Speaker 3: The name comes from combining the Windows Server operating system with Intel x86-based hardware.
Speaker 1: Yes, you're all correct. Windows Server needs hardware to run. That hardware can be a laptop, desktop, or physical server. In most cases, companies install it on physical servers, although today we also run Windows Server using virtualization.

There are two major processor companies: AMD and Intel. When you hear about servers, you may think of brands such as HPE, Dell, Cisco, Fujitsu, IBM, or Lenovo. For laptops, we commonly say HP, but for enterprise servers we refer to HPE. Lenovo also manufactures servers, while ThinkPad refers to a laptop product line.

These server manufacturers source components and technologies from companies such as AMD and Intel and integrate them into complete systems. The resulting hardware allows us to install and operate server operating systems.

On the software side, Microsoft is a major provider. There are also open-source operating-system platforms and distributions, including Ubuntu, Fedora, CentOS, and Linux Mint, among others.

WHAT IS A SERVER?

Speaker 1: A server is a system that provides services. It isn't necessary to have dedicated server hardware or a server operating system to provide a service. Even your laptop or desktop can act as a server.

For example, suppose I work in a small cybercafé. I have one printer attached to my desktop and five other computers connected through the same network. I want all five computers to be able to print through that printer. My computer can work as a print server, allowing those other systems to access the shared printer.

Similarly, a computer can offer file-transfer services. Suppose I frequently need to install programs such as Google Chrome, Mozilla Firefox, Adobe Reader, WinRAR, or WinZip on multiple systems. Downloading them repeatedly wastes time and may not be possible when the internet is down.

Instead, I can download the installers once, store them on one computer, and configure that computer as an FTP server. Other devices on the network can connect to it using its IP address and retrieve the files.

FTP stands for File Transfer Protocol. When you download software from a website, the website is hosted on an internet-connected server. You can sometimes use commands such as ping or nslookup to discover the IP address associated with its hostname.

For example, the instructor ran a command and obtained the IP address 151.101.105.91. That address was associated with the website he was examining.

[Translator's note: In the live explanation, the instructor refers to ordinary website downloads as FTP and describes SFTP as an upload method. These are not equivalent distinctions: HTTPS can deliver downloads, and both FTP and SFTP can upload and download files. The explanation above preserves his example without repeating that technical misconception as a rule.]

Speaker 1: I hope that's becoming clear.
Speaker 2: Yes, sir. This is the first time I've understood the difference between FTP and SFTP.
Speaker 1: Okay. Anil?
Speaker 3: Yes, sir.

END OF PART 01
The remainder of the original transcript has not been translated in this file.


---

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


---

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
