# Wintel Day 02 — Part 05: Rack and Blade Hardware, Network Ports, and Power Trade-offs (Roman Urdu)

**Source alignment:** Original `Wintel-day-02.txt`, lines 281–354. **Note:** Yeh source-based classroom adaptation hai, line-by-line literal translation nahin. Original har line `Original_Source/` mein hai. Speech recognition ne kabhi speaker labels combine kiye hain.

## Classroom discussion

**Instructor:** Ab physical server ports aur components ko dhyan se dekhein. Operating system se pehle hardware ka role samajhna hai. Server mein normal network interfaces ke ilawa dedicated management port bhi ho sakta hai. Management network aur production traffic ko ek hi cheez na samjhein. Different NICs aur storage interfaces ki apni purpose hoti hai.

**Instructor:** Advanced servers mein additional disks, CPU sockets, RAM slots, redundant fans aur management options ho sakte hain. Is se performance aur availability improve ho sakti hai, lekin cost bhi barhti hai. Customer ki workload aur budget requirements samjhe baghair high-end model recommend nahi karna chahiye.

**Instructor:** Lecture mein rack aur blade-type systems ka bhi comparison hota hai. Blade environment mein ek shared chassis ke andar server modules lagte hain. Kuch components shared hote hain, is liye cabling aur infrastructure compact ho sakta hai; lekin chassis cost, power aur cooling ki planning important hoti hai. Shared component fail ho jaye to multiple blades affect ho sakti hain, is liye failure domains aur redundancy samajhna zaroori hai.

**Instructor:** Physical power failure ke baad system recovery ka bhi plan hona chahiye. Sirf strong server khareedna solution nahi; maintainability aur recovery architecture ka part hain.

**Classroom note:** Jo prices aur component examples teacher ne diye hain woh lecture ki illustrative estimates hain, aaj ki verified market quotations nahi.
