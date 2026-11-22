# Wintel Day 02 — Part 06: Home Lab Decisions and Choosing Windows Server Installation Media (Roman Urdu)

**Source alignment:** Original `Wintel-day-02.txt`, lines 355–429. **Note:** Yeh source-based classroom adaptation hai, line-by-line literal translation nahin. Original har line `Original_Source/` mein hai. Speech recognition ne kabhi speaker labels combine kiye hain.

## Classroom discussion

**Instructor:** Ab enterprise knowledge ko apne home lab se connect karte hain. Har student ke paas data center access nahi hota. Kuch overseas se practice kar rahe hain. Physical server mehnga, noisy aur maintain karna mushkil ho sakta hai. Bohat se Windows Server labs laptop ya desktop par virtualization ki madad se ho sakte hain, bas resources sufficient hon.

**Instructor:** Khalid apne home lab ki hardware configuration par discuss kar rahe hain. New vs refurbished machine, RAM, CPU, storage aur parallel VMs ki requirements dekhni hongi. Chhote labs kam memory mein chal sakte hain, lekin multiple concurrent virtual servers ke liye zyada resources chahiye.

**Instructor:** Windows Server ko directly laptop/desktop par install karne ke muqablay mein VMware Workstation ka faida yeh hai ke host OS ko replace nahi karna padta. Direct installation par device drivers aur compatibility ke issues aa sakte hain. Is liye training ke liye VM create karke ISO attach karna convenient hai.

**Instructor:** Training material ke shared folder mein operating-system ISO, VMware Workstation installer aur kuch doosray tools hain. Download karne ke baad installer ki authenticity, compatibility aur license verify karna achhi practice hai.

**Instructor:** Class mein system specifications aur Windows performance details bhi dikhayi gayin taake student ko pata ho kitni RAM, CPU aur storage available hai. Uske baad hi VM resources allocate karne chahiye.
