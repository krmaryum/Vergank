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

<img src="../images/Servers explained_ print-files-downloads.png" width="400">


END OF PART 01
The remainder of the original transcript has not been translated in this file.
