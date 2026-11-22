# Wintel Day 02 — Part 11: Create a VMware Workstation Virtual Machine for Windows Server (Roman Urdu)

**Source alignment:** Original `Wintel-day-02.txt`, lines 741–810. **Note:** Yeh source-based classroom adaptation hai, line-by-line literal translation nahin. Original har line `Original_Source/` mein hai. Speech recognition ne kabhi speaker labels combine kiye hain.

## Classroom discussion

**Instructor:** Ab VMware Workstation mein new virtual machine banate hain. VM ek aisa computer hai jiska CPU, RAM, disk aur network adapter virtual hardware ki form mein host machine par chalta hai. Sab se pehle New VM wizard open karein aur installation media choose karein.

**Instructor:** Wizard mein CD/DVD device ya ISO select karne ka option ho sakta hai. Hamari lab mein ISO use ho rahi hai. Phir guest operating system family aur version choose karein. Yeh selection VMware ko suitable defaults aur virtual hardware settings set karne mein madad deti hai.

**Instructor:** Ab resources allocate karein: vCPU, RAM aur virtual disk. Windows Server ke liye OS disk banayi ja rahi hai. Data ke liye aage chal kar alag virtual disk bhi add kar sakte hain. OS aur data ko logically separate karna backup aur troubleshooting scenarios ke liye useful ho sakta hai.

**Instructor:** Guest ko diye hue resources host ki real capacity se aate hain. VM unlimited RAM create nahi karti. Bohat zyada allocation host aur guest dono ko slow kar sakta hai. Virtual network mode ka bhi connectivity par asar hota hai.

**Instructor:** Finish karne se pehle configuration review karein. Interview mein samjha sakna chahiye ke ISO, vCPU, memory, virtual disk aur vNIC ka kya role hai.
