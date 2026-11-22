# VMware November 21, 2026 — Part 06 — VM ko VDS se Connect Karna aur Practice

**Coverage:** Source lines 476–520 of 682.
**Format:** Detailed classroom-style reconstruction, following the lecture in sequence. Dialogue and illustrative examples are retained in the prose. Some automatic-transcription lines are repetitive or unclear; the authoritative unedited source is included in the bundle.

**Note:** This document is not a word-for-word sentence-by-sentence translation. See the source-aligned transcript companion for every utterance.

## 1. Move an existing VM to a distributed port group

**Instructor / classroom discussion:** Instructor Host 2 par ek VM select karte hain jo abhi host-local VM Network se connected hai. Woh Edit Settings mein ja kar available networks browse karte hain aur VMware Lab ya Cloud Lab jaisa distributed port group select karte hain. Confirm karne ke baad VM ka network attachment naye port group par aa jata hai.

## 2. Why consistent VDS backing helps migration

**Instructor / classroom discussion:** Instructor batate hain ke distributed port group sab participating hosts par available ho sakta hai. Is liye VM migrate ya restart hone par equivalent network par reh sakti hai—basharte physical uplinks, VLANs aur baqi connectivity theek configure ho. Woh isay inconsistent standard switches ke risk se compare karte hain.

## 3. Inspect rather than alter production environments

**Instructor / classroom discussion:** Students ko kaha jata hai ke apne available VMware environment mein Networking tab kholen, distributed switch ka icon identify karein aur configuration tabs/port groups dekhein. Instructor ka maqsad pehle deployed environment ko samajhna hai, production settings ko bina approval change karna nahi.

## 4. Hands-on priorities and exam emphasis

**Instructor / classroom discussion:** Instructor SAN storage aur VDS labs ko sabse important practice areas batate hain. Sirf doosre student ko lab karte dekhna kaafi nahi; har student ko khud step by step karna chahiye. Woh in topics ko interview aur exam ke liye bhi valuable samajhte hain, kyun ke physical aur virtual infrastructure ka connection samajhna parta hai.

## 5. Break, vCenter domain question and connection issues

**Instructor / classroom discussion:** Instructor VM chapter se pehle chhota break announce karte hain. Ek student vCenter ko AD domain ke saath join karne ke bare mein poochta hai. Instructor batate hain ke class ke end par karenge, kyun ke vCenter restart mein time lag sakta hai. Woh apne ISP aur public IP issue ka example bhi share karte hain jis se live services affect hui thin.
