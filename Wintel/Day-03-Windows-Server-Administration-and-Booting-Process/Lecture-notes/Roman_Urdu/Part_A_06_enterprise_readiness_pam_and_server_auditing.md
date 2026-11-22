# Day 03 Part A — Enterprise readiness, PAM and server auditing

**Original-source reference:** A:232–273.

**Instructor (A:232–241):** Main students se poochta hoon ke pace sahi hai ya topics bohat zyada lag rahe hain. Mera goal sirf installation ka button click karwana nahin; enterprise mein server build ka real environment samjhana hai. Aap jab company join karte hain to roles, permissions, auditing, monitoring aur approvals bhi important hote hain. Kai administrators ne server install karna seekha hota hai magar production procedure se waqif nahin hote.

**Instructor (A:242–253):** Ek common galti yeh hai ke administrator seedha high-privilege account se server login kar leta hai. Organizations privileged access ko control karne ke liye PAM tool use kar sakti hain. Password kisi notebook mein ya common static credential ke taur par rakhne ke bajaye, managed vault se temporary ya rotated password diya ja sakta hai.

**Student / Instructor (A:249–257):** Student ka sawal hai: 'Agar password khud set kar sakte hain to tool generate kyun kare?' Instructor jawab dete hain ke tool ka maksad sirf password banana nahin: authorized access, rotation, time-bound use aur activity accountability hai. Student pooch sakta hai ke AD account already available hai to PAM kyun? Instructor dikhate hain ke AD identity aur privileged session authorization alag controls ho sakte hain.

**Instructor (A:258–264):** PAM ke through session start ho to company kuch systems mein screen/session recording aur detailed audit log capture karti hai. Agar kisi ne reboot kiya aur baad mein mana kar diya, authorized audit trail incident review mein help karta hai. Yahan privacy, policy aur role-based controls ka khayal rakhna lazmi hai.

**Instructor (A:265–273):** Teaching ke dauran kabhi naya idea ya issue aaye to main note bana leta hoon. Classroom mein occasional troubleshooting aa jaye to use learning opportunity samjhein. Mere liye professional learning ka matlab questions se ghabrana nahin, balki systematic exploration karna hai.
