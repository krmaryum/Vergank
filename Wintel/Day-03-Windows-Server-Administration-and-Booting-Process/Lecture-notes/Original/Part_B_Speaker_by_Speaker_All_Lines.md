# Wintel Day 03 Part B — FULL ORIGINAL CLASSROOM TRANSCRIPT

**Original language preserved; not a translation. 319 lines.**

**[B:001]** Speaker 1: کیسے ہوتا ہے، کیا کیا پروسیس ہیں؟ یعنی کہ ابھی ہم نے just installation ہی کری ہے، but installation کے باوجود بھی کافی ساری queries ایسی generate ہو جاتی ہیں، جیسے سرور build کیسے ہوتا ہے، کیا کیا procedure ہوتا ہے، آپ کی کمپنی میں کیا کیا procedures use کر سکتے ہیں، یا سرور کا OS کون سا select کرنا چاہیے۔ آپ کسی کو کسی کا کوئی سرور آپ نے build کرنا ہے تو کیسے suggest کرتے ہو کہ کیا configuration کے ساتھ ہم نے سرور کو use کرنا ہے۔

**[B:002]** Speaker 1:  So same way، ابھی اگلا جو question ہے، that is، سرور build ہونے کے بعد جب آپ سرور کو power on کرتے ہیں تو سرور power on ہونے کے لیے کیا procedure چلتا ہے، یعنی کہ Windows server booting process۔ بڑا common سا question ہے، interview میں پوچھتے ہی پوچھتے ہیں، اور اگر especially اگر آپ سے نہیں پوچھا ہے تو it means آپ سے ان کی expectations ہیں کہ وہ might be کہ L2 اور L3 کے questions پوچھ رہے ہیں۔

**[B:003]** Speaker 1:  ویسے تو یہ question L1 کا ہے، لیکن اگر آپ L2 اور L3 کے answers زیادہ اچھے نہیں کر پا رہے، trust me، interviewer گھوم کر L1 کے basic fundamental questions پر آئے گا، اور یہ question پوچھے گا ہی پوچھے گا کہ اچھا ایک کام کرو یہ بتاؤ Windows کا booting process کیا ہوتا ہے، یہ میرے کو بتاؤ۔

**[B:004]** Speaker 1:  اب ہمیں لگتا ہے Windows booting کا مطلب جیسے ہی ہم نے power button press کر دیا CPU سے، یا سرور کے جو ہمارا rack سرور ہے وہاں سے ہم نے power button press کر دیا، اور اس کے بعد ہمیں ایک screen logo دکھتا ہے، logo blink ہوتا ہے، اور blink ہونے کے بعد وہاں لکھا ہوتا ہے "Please wait"، تھوڑی دیر بعد login screen آ جاتی ہے، password ڈالتے ہیں، login کر دیا۔ But interviewer وہ known technical answer نہیں سننا چاہتا۔

**[B:005]** Speaker 1:  تو because we are doing this Microsoft curriculum، officially ہم لوگوں کا یہ curriculum ہے جسے ہم MCSA بھی بولتے ہیں، Microsoft Certified System Administration۔ تو اب یہ training certification کرنے کے بعد ہمیں کیا benefit ہے، اور ہمیں کس طریقے سے answers کرنے ہیں، وہ ہم نے سیکھنا ہے، right۔

**[B:006]** Speaker 1:  So سب سے پہلی چیز، آپ کوئی بھی electronic gadget جب power on کرتے ہیں تو سب سے پہلی ایک چیز run ہوتی ہے، which is called POST۔ POST کا مطلب ہے Power On Self Test، یعنی کہ آپ نے جیسے ہی hardware کے اندر power supply on کری اور power switch کو press کیا، تو SMPS یعنی کہ جسے ہم کل PSU بول رہے تھے، اسے ہم desktop کے اندر، laptop کے اندر ہم SMPS بولتے ہیں، server کے اندر ہم اسے PSU بولتے ہیں، power supply unit۔

**[B:007]** Speaker 1:  تو power supply unit سے جیسے ہی supply ہوتی ہوئی motherboard پر جاتی ہے، تو motherboard decide کرتا ہے کہ کس equipment کو یا کس gadget کو کتنی voltage دینی ہے۔ CPU کو کتنی جائے گی، memory کو کتنی جائے گی، storage کو یعنی کہ hard disk کو کتنی power supply کی ضرورت ہے، اسی کے according وہ power supply بھیجتا ہے۔

**[B:008]** Speaker 1:  اور سبھی gadgets کے پاس جب power supply جاتی ہے، اور سبھی gadgets جب واپس response کرتے ہیں کہ ہاں we are fine، تو ہمارا اگلا process run ہوتا ہے۔ لیکن اس time پہ اگر کسی بھی gadget سے reply یا response نہیں آتا ہے، تو ایسے case میں ہمارے system کے اندر یا تو beeps کی آواز آنی start ہو جائے گی، same it could be happen on your desktop، laptop، server، کسی بھی case کے اندر، تو آپ کو beeps کی آواز آنی start ہو جائے گی۔

**[B:009]** Speaker 1:  Server کے case میں آپ کو additional ایک benefit مل جاتا ہے کہ front panel پہ LED blinks ہوتی ہیں، وہاں پر آپ دیکھ سکتے ہو کہ کس طریقے کی light blink ہو رہی ہے، اور اس کے basis پہ آپ جیسے اگر وہ HP کا server ہے تو HP کی side پہ جا کے دیکھ سکتے ہو کہ یہ light blink ہو رہی ہے تو کیا issues ہیں، اور Dell کا server ہے تو کیا issues ہیں۔ حالانکہ پہلے کی کچھ پرانی series میں میں اگر جاؤں تو وہاں پر

**[B:010]** Speaker 1:  ہمیں ایک system tray مل جاتی تھی، تو ہم جیسے ہی button press کرتے تھے، اس میں سے ایک tray چھوٹی سی باہر آ جاتی تھی، اور اس میں alarm ہمیں دکھ جاتے تھے کہ یہ memory کا ہے یا CPU کا ہے یا کسی اور چیز کا ہے۔ پہلی چیز۔ دوسرا، still ہم ابھی بھی identify نہیں کر پا رہے، ہمیں alarm تو دکھ رہا ہے، beep کی آواز بھی آ رہی ہے، but still we are not able to identify کہ کیا issue ہے۔

**[B:011]** Speaker 1:  تو ہمارے پاس دوسرا solution کیا ہے؟ دوسرا solution یہ ہے کہ کل ہم لوگوں نے ایک چیز سنی تھی یا پڑھی تھی، which is called Remote Management Port۔

**[B:012]** Speaker 1:  Remote Management Port الگ الگ ہوتے ہیں، ہر ایک company کے الگ الگ remote management port ہوتے ہیں۔ تو جیسے اگر آپ HP کا server use کر رہے ہیں، تو HP کے server کے اندر ہم اسے بولتے ہیں ILO۔

**[B:013]** Speaker 1:  اگر ہم Dell کا server use کر رہے ہیں، تو ہم اسے بولتے ہیں ID Rack۔ اگر ہم IBM کا server یا Cisco کا server use کر رہے ہیں یا Fujitsu کا server use کر رہے ہیں، تو وہاں آپ کو یہ ملے گا RMM کے نام سے۔

**[B:014]** Speaker 1:  تو ہر server میں یہ الگ الگ remote management ports ہوتے ہیں۔ تو دوسرا طریقہ یہ ہے کہ اگر آپ کا server response نہیں کر رہا ہے یا beeps کی issues آ رہے ہیں اور آپ identify نہیں کر پا رہے کہ یہ issues کس چیز کا ہے، تو آپ یہ remote management port کا access کر لو۔

**[B:015]** Speaker 1:  بھلے ہی آپ کا server کا hardware بھی کیوں نہ failure ہو گیا ہو، تو بھی آپ کا یہ remote management port کام کرے گا۔ اس server کو جب آپ access کرو گے with the help of remote management port، تو ایک console کھل جائے گی، اور اس console کے اندر آپ کو دکھ جائے گا کہ آپ کا کون سا device faulty ہے۔

**[B:016]** Speaker 1:  Whether motherboard ہے، CPU ہے، RAM ہے یا کچھ اور issues ہیں۔ اور اس کے basis پہ اس کا screenshot لے کے اگر آپ کے پاس tech support ہے، HP کے ساتھ یا Dell کے ساتھ، تو آپ ان کو email کر سکتے ہو یا case raise کر سکتے ہو۔

**[B:017]** Speaker 1:  تو ہمارے پاس اس کا license ہونا چاہیے۔ License مطلب physical server کا license۔

**[B:018]** Speaker 1:  اور یہ tech support کا license ہے۔ ایک license تو ہوتا ہے کہ ہم نے OS کے لیے purchase کیا۔

**[B:019]** Speaker 1:  That is a different thing۔ وہ OS کے لیے ہے۔

**[B:020]** Speaker 1:  ایک ہم جب server purchase کرتے ہیں تو ہمیں license ملتا ہے، اور اس پہ tech support ہم جب purchase کرتے ہیں تو license key ملتی ہے۔ And that license key یا authorization key is valid till جب تک ہم آپ اسے renew نہیں کرتے۔

**[B:021]** Speaker 1:  تو ایک سال کا، دو سال کا، پانچ سال کا ہوگا۔ نیا server purchase کرتے ہیں تو on an average five year ہوتا ہے۔

**[B:022]** Speaker 1:  اس کے بعد جب آپ اسے expand کرتے ہیں، one one year کے basis پہ آپ اسے expand کر سکتے ہیں، but زیادہ تر companies آپ سے جب renew کرواتی ہیں تو وہ دو سال کے لیے بولتی ہیں۔ وہ کہتی ہیں کہ سر ایک سال کا renew کر کے کیا کرو گے، اگلے سال پھر renew کرنا پڑے گا۔

**[B:023]** Speaker 1:  تو سات سال اس کا maximum time period ہے۔ اس server کو سات سال چلاؤ، اور اس کے بعد آپ اسے sale out کر دینا یا ویسے ہی تو industry سے نکل ہی جائے گا یہ۔

**[B:024]** Speaker 1:  تو ایسے case میں لوگوں کو لگتا ہے ہاں یار سات سال ہی چلانا ہے maximum، تو ہم کیا کرتے ہیں اس server کو use کر لیتے ہیں، دو سال کا اور license agreement لے لیتے ہیں۔ تو سات سال کے لیے ہمیں support مل جاتا ہے۔

**[B:025]** Speaker 1:  تو اس سات سال کے لیے آپ کو ایک طریقے سے اس کا ایک amount، certain amount company کو pay کرنا پڑتا ہے۔ Same اگر آپ موبائل فون کے اندر بھی آپ جب نیا موبائل فون لیتے ہیں تو insurance لیتے ہیں کہ اگر کسی بھی طریقے کا کچھ damage issue آتا ہے تو company will pay۔

**[B:026]** Speaker 1:  تو اب آپ سے HP وہ pay کر رہی ہے۔ تو آپ نے جب وہ pay کر دیا، کچھ بھی issue آئے گا تو آپ نے جیسے ہی case raise کیا، تو case raise ہونے کے بعد آپ کے پاس HP سے ایک انجینئر visit کرے گا آپ کے data center میں، وہ آ کے اس part کو replace کرے گا۔

**[B:027]** Speaker 1:  پہلے تو آ کے ensure کرتے ہیں کہ یہ چیزیں issues آ رہی ہیں یا نہیں، اور issues آ رہی ہیں تو immediately they can replace the hardware۔ اگر آپ نے immediately hardware mention کیا ہے کہ اس hardware کی وجہ سے issue آ رہا ہے، تو وہ hardware کا part آنے سے پہلے delivery کروا دیتے ہیں۔

**[B:028]** Speaker 1:  کہ جیسے motherboard خراب ہو گیا، جیسے ابھی میرے case میں اگر میں بات کروں last چیز data center پہ میں support کر رہا تھا، تو میرے پاس ایک server two thousand eighteen میں install ہوا تھا، مطلب rack میں لگا تھا، لیکن اس server کے اندر کوئی بھی single OS install نہیں ہوا تھا، آج تک وہ empty پڑا تھا، لیکن ابھی کچھ time پہلے، لگ بھگ چار مہینے پہلے کی بات ہے، وہ server میں نے power on کیا، first time یا کہہ لو کہ جب وہ server rack

**[B:029]** Speaker 1:  میں لگا ہوا ہے، اس time پہ power on ہوا ہوگا، لیکن ابھی تک وہ server power off ہی پڑا تھا۔ نیا ایک دم server، صاف ستھرا server، مطلب اسے دیکھ کے میرا as a being mentor یا trainer، میرا دیکھنے کے بعد من تھا کہ میں یار یہ server اگر بیچنے لگی کمپنی تو یہ server میں خرید لوں گا۔ اس طریقے کا صاف ستھرا server۔

**[B:030]** Speaker 1:  تو still اس میں OS بھی install نہیں کیا گیا۔ میں پہلی بار مطلب وہ connect ہونے کے بعد میں power on کر رہا ہوں گا۔

**[B:031]** Speaker 1:  تو میں نے جیسے ہی power on کیا، میرے کو وہ alarm ملا، تو alarm ملنے کے بعد مجھے issue پتہ لگا کہ یار motherboard faulty ہے۔ تو عام طور پہ جو اس کا پہلا alarm آ رہا تھا، وہ alarm آ رہا تھا، تو اس کی وجہ سے مجھے RAM faulty لگ رہی تھی۔

**[B:032]** Speaker 1:  تو میں نے ایک case raise کیا HP کے ساتھ، اور وہ case raise کیا تو HP کا vendor آیا، vendor آنے سے پہلے انہوں نے RAM کی ہمیں RAMs بھیج دی۔ اور اس server کے اندر لگ بھگ I think بارہ RAM install تھیں، تو بارہ RAMs ان لوگوں نے پہلے ہی بھیج دیں۔

**[B:033]** Speaker 1:  RAM آ گئی، RAM آنے کے بعد انجینئر visit ہوئی، اس نے جا کے RAM replace کر دی۔ RAM replace کرنے کے بعد دیکھا، نہیں نہیں still the issue is same، ابھی بھی issue آ رہا ہے۔

**[B:034]** Speaker 1:  تو RAM میں issue نہیں تھا، تو بعد میں پتہ لگا کہ وہ check out کیا، وہ chip level پہ اس نے جب cross check کیا تو motherboard میں issue نکلا۔ تو پھر انہوں نے وہ motherboard بھیجا نیا۔

**[B:035]** Speaker 1:  نیا motherboard آیا۔ So جو نیا motherboard آیا، اس کی costing ہی sixty thousand Rupees تھی اس server کے لیے۔

**[B:036]** Speaker 1:  تو ساٹھ ہزار روپے کا نیا motherboard آیا، RAM یہاں سے واپس چلی گئی، اور نیا motherboard آیا۔ So in a meanwhile time، کیونکہ وہ ابھی اگر میں بات کروں server کے اندر، وہ critical نہیں تھا، کوئی بھی OS deploy نہیں تھا۔

**[B:037]** Speaker 1:  Otherwise اگر OS وغیرہ deploy ہوتا اور میں اس کو P1 یا P2 ticket raise کرتا، case raise کرتا HP کے ساتھ، تو ایسے case میں ہو سکتا تھا کہ وہ same day ہی میرے پاس وہ نیا hardware بھیج دیتے۔ But کیونکہ میں نے اس پہ بولا ہوا تھا پوری condition کہ there is nothing، but we are planning to install اور upgrade something، تو ہمیں اس server کی requirement اور یہ server ابھی ہمارے پاس long time سے down پڑا تھا۔

**[B:038]** Speaker 1:  تو انہوں نے وہ دو دن بعد ایک نیا motherboard بھیجا، اور وہ same day انجینئر visit ہوئی، اس نے نیا motherboard replace کیا، RAM لگائی، دوبارہ وہ server چل گیا۔ But کہنے کا مطلب یہ ہے کہ جب ہم اس طریقے کی چیزیں لیتے ہیں تو tech support بھی لیتے ہیں۔

**[B:039]** Speaker 1:  کیونکہ اگر میں نے tech support نہیں لیا، اور یہ issue اگر آ جاتا تو جیسے ابھی میں نے بتایا کہ وہ جو motherboard کی cost تھی، وہ sixty two thousand Rupees، sixty two thousand four hundred something کچھ Rupees کا ایک amount تھا۔ تو ساٹھ ہزار روپے مجھے pay کرنے پڑتے۔

**[B:040]** Speaker 1:  جبکہ ساٹھ ہزار روپے میں نے اس data center کے لیے پورا pay نہیں کیا، for a one year۔ تو آپ خود سوچ سکتے ہو کہ وہ کتنا سستا پڑا ہوگا مجھے۔

**[B:041]** Speaker 1:  So that is a good thing۔ تو ایسے case میں POST ہمارے لیے بڑا important ہے۔

**[B:042]** Speaker 1:  تو جتنے بھی equipment ہیں، اگر وہ proper کام کر رہے ہیں تو response کریں گے، اور response نہیں کریں گے تو وہ beeps کے alarm دیں گے۔ اور beeps کے alarms کے basis پہ ہمیں identify کرنا پڑے گا یا remote management سے check کرنا پڑے گا کہ server میں کیا issues ہیں۔

**[B:043]** Speaker 1:  Clear ہے سر؟

**[B:044]** Speaker 1:  Clear، clear، clear۔ اب POST نے response دے دیا، یعنی کہ سارے equipments proper کام کر رہے ہیں۔

**[B:045]** Speaker 1:  تو system میں BIOS active ہوگا۔ آج کے time میں BIOS is no more، مطلب زیادہ BIOS نہیں ملتا ہے۔

**[B:046]** Speaker 1:  زیادہ تر case کے اندر آپ کو UEFI ملتا ہے۔ اب یہ BIOS اور UEFI کیا ہے؟

**[B:047]** Speaker 1:  یہاں پر اس چیز کو logic کو بھی سمجھ لیتے ہیں۔ آپ نے laptop اور desktop کے اندر بھی دیکھا ہوگا، یہ BIOS اور UEFI۔

**[B:048]** Speaker 1:  Any idea سر یہ کیا کرتا ہے، کیا کام کرتا ہے؟

**[B:049]** Speaker 1:  سر وہ signal بھیجتا ہے ہر hardware کو on and off کا کہ وہ آپ صحیح ہیں، وہ کہتے ہیں ہم صحیح ہیں۔ Basic input output system۔

**[B:050]** Speaker 1:  سر وہ تو POST میں check ہو گیا، اب BIOS میں کیوں check کرنا ہے؟ Input output system۔

**[B:051]** Speaker 1:  Basic input output system check کرنے کے لیے ہوتا ہے نا وہ۔ Okay، مطلب check as in کیسے check کرتا ہے؟

**[B:052]** Speaker 1:  BIOS میں جو program ہوتا ہے نا، جو operating system کو load کرتا ہے، وہ کام کر رہا ہے کہ نہیں کر رہا۔ Basic input output system check بولتے ہیں اسے شاید۔

**[B:053]** Speaker 1:  نہیں، full form آپ کی correct ہے۔ لیکن آگے کا جو answer ہے، that is not a correct answer۔

**[B:054]** Speaker 1:  تو وہ چیز ہم correct کرنا چاہ رہے ہیں۔ ٹھیک ہے؟

**[B:055]** Speaker 1:  میرا بھی صحیح نہیں ہے۔ نہیں سر۔

**[B:056]** Speaker 1:  وہ POST میں run ہو گیا۔ وہ POST میں check ہو گیا کہ ہمارے device۔

**[B:057]** Speaker 1:  ہاں، اس میں POST میں ہو گیا۔ جی جی، وہ POST میں ہو گیا۔

**[B:058]** Speaker 1:  POST میں ہو چکا۔ BIOS میں نہیں ہوتا۔

**[B:059]** Speaker 1:  BIOS میں نہیں ہوتا۔ Shut کرتا ہوں۔

**[B:060]** Speaker 1:  سرفراز جی سے expectation ہے میری۔ سر وہ ایک firmware ہوتا ہے نا، جو ایک chip میں stored ہوتا ہے، جو سب سے پہلا program ہوتا ہے، run ہوتا ہے جو۔

**[B:061]** Speaker 1:  وہ BIOS میں ہوتا ہے نا۔ میں نے تو یہی یاد ہے۔

**[B:062]** Speaker 1:  BIOS میں ہوتا ہے۔ یہ یہ definition ٹھیک ہے۔

**[B:063]** Speaker 1:  لیکن وہ کرتا کیا ہے، کیوں use کر رہے ہیں، وہ answer نہیں ملا ابھی۔ Operating system کو load کرنے کے لیے ہوتا ہے شاید۔

**[B:064]** Speaker 1:  Yes، اس کی help سے operating system بھی load ہوتا ہے۔ But کیسے ہوتا ہے؟

**[B:065]** Speaker 1:  سر RAM میں load کرے گا اور کہاں کس میں؟ نہیں یار، دیکھو interviewer تو پوچھ سکتا ہے نا۔

**[B:066]** Speaker 1:  Interviewer کچھ بھی پوچھ سکتا ہے۔ تو best suggestion کہ ہم جب training کر رہے ہیں تو training کے اندر یہ ساری چھوٹی چھوٹی جو basic چیزیں ہیں، ان پہ بہت اچھی چیزیں کر لیں۔

**[B:067]** Speaker 1:  آگے جب ہم چیزیں کر رہے ہوں گے تو کئی ساری چیزیں ایسی ہوں گی کہ شاید میں fast forward mode میں کرا رہا ہوں گا۔ میں بولوں گا اس کی ضرورت نہیں ہے، اس پہ interviewer زیادہ focus نہیں کرتا۔

**[B:068]** Speaker 1:  In in portions پہ زیادہ focus کرتا ہے، تو ہم ان پہ زیادہ focus کر لیں۔ تو اب یہ basic چیزیں ہیں۔

**[B:069]** Speaker 1:  تو یہاں پر تو وہ پکڑ کے مطلب یہ جو basic fundamental ہے، یہاں ہمیں پکڑ کے دھوتے ہی ہوتے ہیں۔ تو کوئی یہ بھی کہہ رہا ہے نا کہ میرے کو بیس سال کا، بائیس سال کا experience ہو گیا ہے۔

**[B:070]** Speaker 1:  تو ہو سکتا ہے اسے بھی پکڑ کے کچھ basic fundamental میں دھویا جائے۔ Even آئی got the two time opportunity کہ میں نے Microsoft میں interview دیا۔

**[B:071]** Speaker 1:  And ابھی last time میں نے چھ مہینے پہلے interview دیا تھا۔ So that was for the Pune location۔

**[B:072]** Speaker 1:  And میری expectation تھی کہ نوئیڈا دے دیں۔ اگر نوئیڈا وغیرہ میں دے دیا تو I will join۔

**[B:073]** Speaker 1:  تو سر دو گھنٹے interview چلا۔ And they ask about the TCP/IP only۔

**[B:074]** Speaker 1:  TCP/IP کیا ہوتا ہے؟ اس طریقے سے travel ہوتے ہیں۔

**[B:075]** Speaker 1:  Two hours only basic fundamental they have asked۔ They have not asked کہ Windows server کیا ہوتا ہے، role کیا ہوتا ہے، AD کیا ہوتی ہے، nothing they asked۔

**[B:076]** Speaker 1:  Basic fundamental۔ تو اتنا deep drive چلے گئے اور کئی بار تو مطلب جیسے ہوتا ہے نا کہ سر ہم اس طریقے سے من کرتا ہے پکڑ کے کھجالے کہ بھائی بچے کی جان کیوں لے رہا ہے، چھوڑ دے اب۔

**[B:077]** Speaker 1:  ہو گیا جتنا میں جانتا ہوں، میں بتا چکا ہوں۔ تو اس طریقے کی حالت ہو گئی تھی۔

**[B:078]** Speaker 1:  اور اس کے بعد خیر that was the مطلب might بھی ہو سکتا ہے کہ that was my good luck کہ اس کے بعد انہوں نے میرے کو offer کیا کہ we are giving you the Pune location۔ But Pune I don't want to change the really quote my locations۔

**[B:079]** Speaker 1:  So کیونکہ میری joint family ہے، میں یہاں پر رہتا ہوں family کے ساتھ، I am feeling happy۔ مجھے چھوٹا amount ملے گا، salary کم ملے گی، چل جائے گا۔

**[B:080]** Speaker 1:  لیکن family کے ساتھ تو that's why I decline کیونکہ میں نے انہیں suggest کیا تھا کہ میں نوئیڈا یا گڑگاؤں آؤں، I will join۔ But they suggest نہیں نہیں، ہم لوگوں کا actually ان کا data center وہاں پر لگ رہا تھا۔

**[B:081]** Speaker 1:  And وہ huge level پہ تھا۔ And of course کہ میں کسی کے reference کے basis پہ میں نے interview بھی دیا تھا۔

**[B:082]** Speaker 1:  تو officially portal پہ نوکری وکری پہ یا ادھر ادھر کہیں پہ وہ requirement نہیں تھی۔ تو میں نے جس بندے کا reference لگایا تھا، وہ بندہ بھی دو ہزار تیرہ سے ابھی تک Microsoft میں کام کر رہا ہے۔

**[B:083]** Speaker 1:  So اس بندے کے basis پہ میں نے بھی interview دیا تھا تو he was also expecting کہ یار ورگاں اور میرے کو اس نے بولا بھی کہ ورگاں بھائی آپ کچھ پڑھنا مت پڑھنا، fundamental پڑھ لینا اور کبھی دو ہزار تیرہ میں we was kind of colleagues، وہ بھی training میں تھے، میں بھی training میں تھا اور that would not be a good point، مطلب میں وہ بولنا تو صحیح نہیں ہوگا لیکن کئی ساری چیزوں میں topics میں یا Windows server پڑھاتے ہوئے میں ان کی help

**[B:084]** Speaker 1:  کرتا تھا کہ یار بھائی آپ کو نہیں پتا یار یہ ایسے ایسے ہوتا ہے تو پھر وہ سمجھتے تھے اچھا یہ تو وہ چیزیں ہیں but since مطلب میرے سے پہلے وہ لگ گئے تو زیادہ اچھی بات ہے خیر وہ زیادہ talented ہوئے but he suggested me کہ ورگاں بھائی آپ سے زیادہ یہ مت سوچنا کہ L3 یا SMEs کے لیے اگر آپ آ رہے ہو تو آپ سے زیادہ بڑی بڑی چیزیں پوچھیں گے، fundamental clear کر لینا تو اب میں fundamental Windows میں بیٹھا ہوں لے

**[B:085]** Speaker 1:  کے کہ بھئی file system میں پڑھ لوں گا کہ file system کیا ہوتا ہے، کس طریقے سے کام کرتا ہے، کیوں use کرتے ہیں file system and all وہ TCP/IP پہ بیٹھا ہے بندہ، میں کہہ رہا ہوں بھیا آگے چل کچھ اور پوچھ، OS میں جا، وہاں بات چیت کر، وہ بات چیت ہی نہیں کر رہا۔ So جب ہم بڑے level کا سوچ کر جاتے ہیں تو fundamental پوچھتے ہیں اور جب fundamental یعنی L1 level پر جاتے ہیں تو پھر ان کی queries وہ L3 والی

**[B:086]** Speaker 1:  یا SMEs والی ہوتی ہیں تو کچھ وہ چیزیں۔ بالکل ایسا ہی ہے، ایسا ہی ہے۔ تو یہ کیوں ہوتا ہے مجھے بھی نہیں پتا، HR کیوں پوچھتے ہیں یا interviewer technical persons کیوں پوچھتے ہیں، I don't have any idea but یہ پتہ ہے کہ اگر آپ L3 کے لیے جا رہے ہو اور L3 کے آپ questions کے دو چار questions کے answers نہیں کر رہے ہو تو interviewer واپس roll back کر کے اپنے آپ کو fundamental کے questions میں لاتا ہے اور وہ یہ questions پوچھتا ہی

**[B:087]** Speaker 1:  پوچھتا ہے۔ تو yes of course we was talking about the BIOS and basic اگر ہم بات کریں تو BIOS کی full form یہی ہوتی ہے basic input output system اور یہ بھی ایک طریقے کا operating system ہے، ابھی ہم بول بھی رہے ہیں basic input output system but اگر ہم دیکھیں تو last میں OS بھی لکھا ہے تو یہ OS بھی ہے، mini OS ہے ہمارے کمپیوٹر کا۔ اگر ہم کمپیوٹر میں کچھ بھی install نہیں کرتے، نیا laptop، desktop، server کچھ بھی چیز purchase کر کے لائیں،

**[B:088]** Speaker 1:  by default یہ آپ کو ملے گا ہی ملے گا۔ تو یہ کیا contain کر کے رکھتا ہے؟ First thing، it's holding your computer hardware configuration۔

**[B:089]** Speaker 1:  آپ نے جو بھی hardware کے اندر install کیا ہے، جتنی GB بھی memory ہے، CPU ہے، آپ نے date and time کیا set کیا ہوا ہے، آپ کے کمپیوٹر کا hard drive کتنے hard drives لگے ہوئے ہیں، first boot device کیا ہوگا، وہ ساری کی ساری information یہ hold کر کے رکھتا ہے۔ ٹھیک ہے؟

**[B:090]** Speaker 1:  تو یہ ایک basic output input system ہے، مطلب basic ایک operating system ہے جو ہمارے system کی ساری information hold کر کے رکھ رہا ہے۔ اب اس BIOS کے ساتھ ایک اور چیز ہے جو بڑی important ہے، جو اس booting process کے اندر نہیں لکھا۔

**[B:091]** Speaker 1:  That is CMOS۔ CMOS بھی ایک چیز ہوتی ہے، that is called CMOS cell۔

**[B:092]** Speaker 1:  اگر آپ لوگوں نے دیکھا ہوگا اور اگر ہم Google کریں تو ہمیں ایک چیز مل جائے گا اور I believe کہ ہم hundred one percent جیسے ہی میں وہ دکھاؤں گا، آپ سب ہی بولیں گے ہاں سر ہم نے دیکھا ہے۔ So اگر میں لکھتا ہوں۔

**[B:093]** Speaker 1:  میری گھڑی میں بھی ہے۔ ہاں۔

**[B:094]** Speaker 1:  Cell in PC یا server میں بھی اگر میں لکھوں گا تو آپ کو دیکھنے کو مل جائے گا۔ اور image پہ اگر ہم click کریں تو یہ کچھ ایسا سا۔

**[B:095]** Speaker 1:  تو یہ CMOS cell ہمارے system کے اندر لگا ہوا ہوتا ہے۔ Server میں بھی ہوتا ہے۔

**[B:096]** Speaker 1:  تو BIOS کے ساتھ یہ CMOS cell بھی کام کرتا ہے۔ یہ CMOS cell کیا کام کرتا ہے؟

**[B:097]** Speaker 1:  جب ہم کمپیوٹر کو power off کر دیتے ہیں، shut down کر دیتے ہیں، تو کمپیوٹر کا date and time update کرنے کے لیے یہ CMOS cell لگا ہے۔ اگر یہ CMOS cell discharge ہو جاتا ہے تو آپ کے کمپیوٹر کا date and time corrupt ہو جاتا ہے، back date میں چلا جاتا ہے، اور back date میں جانے کی وجہ سے کئی بار ایسا بھی ہو جاتا ہے کہ آپ کا system power on نہیں ہو پاتا۔

**[B:098]** Speaker 1:  یہ تک issues آ جاتے ہیں۔ اب آپ کو لگے گا کہ یار کیا issues آ گئے؟

**[B:099]** Speaker 1:  But issues is a CMOS cell۔ تو that could be also a reason کہ server آپ power on کر رہے ہیں، وہ power on ہی نہیں ہو رہا۔

**[B:100]** Speaker 1:  تو ایسے case میں CMOS کا alarm بھی دیکھ سکتے ہیں، ہمیں front panel پہ ہی server کے اندر دیکھنے کو نظر آ جاتا ہے، وہاں لکھا ہوتا ہے CMOS battery down۔ تو وہ بھی ہمیں پتہ لگ جاتا ہے۔

**[B:101]** Speaker 1:  لیکن laptop یا desktop کے اندر ایسا نہیں ہوتا کہ ہمیں CMOS battery کے بارے میں کچھ پتہ لگ جائے۔ تو ہم ideally یہ check list ہوتی ہے جب server کو install کرتے ہیں۔

**[B:102]** Speaker 1:  Install کا مطلب OS installation نہیں ہے۔ Install کا مطلب ہے rack میں جب ہم mount کرتے ہیں۔

**[B:103]** Speaker 1:  تو ہم note down کر لیتے ہیں، آج ہم نے اسے rack mount کیا ہے، اگلا اس کا maintenance ہمارا اتنے time period بعد ہوگا۔ تو وہ maintenance window جیسے ہی آئے گی، آپ اس time پہ وہ activity کرو گے ہی کرو گے۔

**[B:104]** Speaker 1:  تو یعنی activity کا مطلب آپ اس server کو down کرو گے، اس server کو down کر کے اس کے firmware کو upgrade کرو گے، اس کے سارے device and drivers upgrade کرو گے، اس کا CMOS cell replace کرو گے، اور جب یہ ساری activities ہو جائیں گی، واپس لگا کر server کو power on کر دو گے۔ تو عام طور پہ یہ yearly ہم اس طریقے کے task perform کرتے ہیں servers کے اوپر۔

**[B:105]** Speaker 1:  Yearly ویسے تو دو دو تین تین سال تک یہ server میں cell easily کام کر جاتے ہیں، but yearly ہم زیادہ تر اس طریقے کے task perform کرتے ہیں۔ ٹھیک ہے؟

**[B:106]** Speaker 1:  یہ وہ perform کرتے ہیں جو core data center کے اندر بیٹھے کام کر رہے ہیں۔ ایسا نہیں کہ ہم لوگ کام کر رہے ہیں۔

**[B:107]** Speaker 1:  We are the Windows server administrator یا ہم window administrator ہیں۔ ہم guide کر سکتے ہیں data center والے بندے کو بول کے کہ بھئی یہ یہ issues آ رہے ہوں گے، بھائی ذرا check کر لو۔

**[B:108]** Speaker 1:  Right؟ So ہمارا جو remediation ہوگا وہ سارا OS level پہ ہے۔

**[B:109]** Speaker 1:  Wintel کے اندر زیادہ تر ہمارا جو curriculum اگر آپ find out کرو گے، وہ OS level پہ ہے۔ ہم hardware level پہ بہت rare کام کر رہے ہیں۔

**[B:110]** Speaker 1:  Hardware level پہ کب کام کریں گے؟ جب ہمارے سامنے server رکھا ہوگا۔

**[B:111]** Speaker 1:  اور ninety percent area کے اندر you will found کہ employees آپ کو یہ کہتے ہوئے ملیں گے کہ ہمارا data center ہمارے سامنے ہے ہی نہیں۔ جو بندہ یہ کہہ رہا ہے کہ میرے سامنے میرا data center ہے، those guys are lucky۔

**[B:112]** Speaker 1:  کیونکہ انہیں پتہ ہے کہ real server کیا ہے۔ Otherwise ninety percent لوگ ایسے ہوں گے جنہیں آج تک کبھی physical server دیکھا ہی نہیں۔

**[B:113]** Speaker 1:  کےवल گوگل وغل کی image کر کے یا یوٹیوب کی ویڈیوز سے ہی دیکھ لیا۔ لیکن real server جب سامنے آئے گا، نہیں پتہ لگے گا۔

**[B:114]** Speaker 1:  جیسے example کے طور پہ میں کل آپ لوگوں کو ایک section پڑھا رہا تھا، plate server کے بارے میں۔ تو there is blade server میں ہم لوگوں نے بات کری تھی کہ ہمارا blade server کچھ ایسا سا نظر آتا ہے۔

**[B:115]** Speaker 1:  تو blade server پہ جب آپ کام کر رہے ہو، let suppose آپ نے یہ blade server rack میں install کر دیا، power on کر دیا، server پہ display ہی نہیں آ رہا۔ تو کیسے display آئے گا؟

**[B:116]** Speaker 1:  یا آپ کو یہ تیسرے نمبر کے blade پہ آپ کو access لینا ہے، remote لینا ہے یا console دیکھنی ہے کہ کیا چل رہا ہے۔ Local cable لگا کے دیکھنی ہے monitor کی۔

**[B:117]** Speaker 1:  تو کیسے دیکھو گے؟ ابھی تو ہمارے پاس کوئی answer شاید نہ ہو۔

**[B:118]** Speaker 1:  Even جو experience person ہیں، جو یہ بول رہے ہیں نا، ہمیں بارہ بارہ، چودہ چودہ، پندرہ پندرہ، بیس بیس سال کا experience ہو گیا۔ اگر directly they don't have even work with the data center اور physically data center کے اندر کبھی visit نہیں کیا یا چیزیں نہیں کری۔

**[B:119]** Speaker 1:  So I am damn sure وہ بھی decline کر دیں گے کہ نہیں idea ہے۔ وہ بول دیں گے ویسے تو cable لگاؤ server کے پیچھے اور چل جائے گا۔

**[B:120]** Speaker 1:  لیکن اگر server کے back side کا آپ اس کا area دیکھو گے، آہ، blade server کا، تو آپ کو ایک ہی وی جی اے پورٹ ملتا ہے۔ ایسا نہیں ہے کہ سبھی server کے لیے الگ الگ وی جی اے پورٹ ملیں گے۔

**[B:121]** Speaker 1:  نہیں۔ ایک ہی single وی جی اے پورٹ ہوگا۔

**[B:122]** Speaker 1:  اس پہ آپ cable لگا دو گے۔ اور اس پہ cable جو لگانے کے بعد display آئے گا، وہ آپ کے blade server کا display نہیں آئے گا سر۔

**[B:123]** Speaker 1:  وہ آپ کے enclosure کا display آئے گا۔ مطلب پوری cabinet کی body کا display آتا ہے۔

**[B:124]** Speaker 1:  تو ہمیں کیسے display ملے گا؟ ایسے case میں وہی بندے بتا سکتے ہیں جو servers پہ exactly کام کر رہے ہیں۔

**[B:125]** Speaker 1:  تو ایسے case میں server کے end پہ نیچے bottom section میں اگر آپ دیکھو گے، ایک چھوٹی سی ایل ای ڈی سکرین لگی ہے۔ ایل سی ڈی، چھوٹی سی پینل ہے۔

**[B:126]** Speaker 1:  ایل ای ڈی ہے، ایل سی، ایل ای ڈی ہے، میرے کو اتنا زیادہ نہیں پتا۔ چھوٹی سی ایک پینل کنسول ہے۔

**[B:127]** Speaker 1:  مطلب سکرین ہے۔ تو might be وہ ایل سی ڈی تو نہیں ہوگی، ایل ای ڈی ہی ہوگی۔

**[B:128]** Speaker 1:  کیونکہ ایل سی ڈی تھوڑی الگ طریقے کی ہوتی ہے اور ایل ای ڈی آج کے ٹائم میں advance ٹیکنالوجی ہے۔ ایل سی ڈی پرانی ہوتی تھی۔

**[B:129]** Speaker 1:  تو ایل ای ڈی ہے۔ اور اچھی quality کی ایسا بھی نہیں ہے کہ ہلکا سا بھی آپ نے touch کیا یا ویسا کرایا تو خراب ہو جائے گی۔

**[B:130]** Speaker 1:  اگر آپ اس پہ اس طریقے سے knock بھی کرو گے تو ٹوٹے گا نہیں یا خراب نہیں ہوگا۔ تو اچھی fine quality کی ہے۔

**[B:131]** Speaker 1:  کیونکہ server ہے اور rough and tough use کرنا ہے تو ایسے case میں یہ بڑھیا quality کی ہے۔ اور اسی کے بغل میں آپ کو کچھ buttons دکھائی دیں گے۔

**[B:132]** Speaker 1:  تو ان buttons کی help سے آپ کو toggle کرنا ہوگا اور toggle کر کے وہاں پر آپ سے پوچھے گا کہ یہ blade active کر دے گا۔ جیسے ہی active اس blade نمبر three پہ جاؤ گے یا four پہ جاؤ گے، جو بھی آپ نے active کرنا ہے، enter کرو گے، اسی میں enter کا بٹن بھی یعنی بیچ کا circle ہے، اوکے کرو گے تو آپ کو display ملے گا آپ کو۔

**[B:133]** Speaker 1:  Otherwise وہ enclosure کا body کا سکرین دکھا رہا ہوگا آپ کو۔ وہ دکھائے گا ہی نہیں۔

**[B:134]** Speaker 1:  تو اس طریقے کی کافی ایسی ساری چیزیں ہیں جو server admin ہونے کے بعد، experience ہونے کے بعد بھی ہمیں نہیں پتا لگتا۔ یہ کب پتا لگتا ہے؟

**[B:135]** Speaker 1:  جب کمپنی کے اندر جاتے ہیں، real servers پہ کام کرتے ہیں اور تب دیکھنے کو چیزیں ملتی ہیں۔ Right؟

**[B:136]** Speaker 1:  جیسے میں ایک example کے طور پہ بات کروں، recently ایک case کے اندر ایسا ہوا کہ میرے پاس ایک batch میں لے رہا تھا، اس batch کے اندر، اس batch میں they was using in their company Microsoft Hyper-V۔ ان کے ہاں Hyper-V چل رہا تھا اور Hyper-V کے انہوں نے clusters بنائے ہوئے تھے۔

**[B:137]** Speaker 1:  تو جیسے یہ blade servers ہیں، ان کے یہاں پہ میرے خیال سے I think بارہ servers تھے، بارہ server کا انہوں نے Hyper-V کا ایک cluster بنایا تھا۔ We will discuss اور we will see کہ کس طریقے سے cluster بناتے ہیں اور کس طریقے سے Hyper-V وغیرہ roll deploy کرتے ہیں and all۔

**[B:138]** Speaker 1:  Each and everything we will see۔ ابھی میں یہ ساری چیزیں اس لیے بات کر رہا ہوں کہ in generally جب ہم بات کریں گے اور آگے کریں گے تو میں آپ کو جب بات کر رہا ہوں تو آپ کو ایک دم سے چیزیں clear ہو جائیں۔

**[B:139]** Speaker 1:  تو ان کی کمپنی میں data center down کرنا تھا due to some reason۔ مطلب کچھ specific part down کرنا تھا، پورا complete data center down نہیں ہو رہا تھا۔

**[B:140]** Speaker 1:  تو وہ server آیا اس rack کے اندر کہ بھئی اسے down کرنا ہے۔ تو کیونکہ وہ server آہ cluster کا part تھے۔

**[B:141]** Speaker 1:  So اسے آہ اس نے کیا کرایا؟ Cluster وغیرہ بند کر کرا کے somewhere cluster تو بند نہیں کیا، direct server بند کر دیے۔

**[B:142]** Speaker 1:  اب server بند کر دیے، اسے یہ بھی نہیں پتا تھا کہ یہ blade server complete down کیسے ہوتا ہے۔ He don't have any idea۔

**[B:143]** Speaker 1:  تو اس نے کیا کرایا؟ بس blade کو بند کیا، یعنی power off کرایا، shut down کر دیا۔

**[B:144]** Speaker 1:  لیکن data center میں جا کر دیکھا تو light blink ہو رہی تھی۔ تو what he did، اس نے کچھ نہیں کیا، as it is چھوڑ دیا۔

**[B:145]** Speaker 1:  اس کے بعد light واپس سے جب یو پی ایس آیا، مطلب connection آ گیا اور آپ کا server up ہونے لگے، تو اس نے کیا کرایا؟ ان servers پہ جا کر اس پہ بھی check کیا کہ کہیں سے کچھ ہو رہا ہے، نہیں ہو رہا، اور display display میں somehow جیسے تیسے کر کے اس نے blades کو check کیا، display آ گیا اور server میں OS بھی چل گیا۔

**[B:146]** Speaker 1:  لیکن وہ server actually proper power off نہیں ہوئے تھے۔ ان کے OS ہی power off ہوئے تھے۔

**[B:147]** Speaker 1:  پورا یہ enclosure کو بھی power off نہیں کیا تھا۔ تو enclosure کو power off بھی ہمیں یہی section سے کرنا پڑتا ہے۔

**[B:148]** Speaker 1:  تو ایسے case کے اندر جب اس کا cluster پورا proper power off نہیں ہوا تو وہ واپس initialize نہیں ہو پایا۔ تو اب اس بندے کے لیے تو یہ first time تھا۔

**[B:149]** Speaker 1:  حالانکہ that person also says کہ سر میرے کو تو آٹھ سال کا experience ہے لیکن میرے کو پہلی بار opportunity ملی اور مجھے یہ failure ہو گیا۔ تو کافی ساری چیزیں ایسی ہوتی ہیں جو ہم life میں پہلی بار دیکھتے ہیں آپ۔

**[B:150]** Speaker 1:  وہ تو planned activity میں تھا ہی نہیں کچھ۔ اور ایسے case کے اندر ایسا issue آ گیا۔

**[B:151]** Speaker 1:  جس کی وجہ سے پھر company کو support لینا پڑا اور support کا پیسہ pay کرنا پڑا۔ وہ OS level کا support تھا۔

**[B:152]** Speaker 1:  کیونکہ OS level پہ issues آ گئے تھے۔ Cluster کام نہیں کر رہا تھا۔

**[B:153]** Speaker 1:  Hardware پہ issue آتا تو شاید ایچ پی یا ڈیل کام کر رہا ہوتا۔ تو ہمیں ہر چیز کا support لے کر رکھنا پڑتا ہے۔

**[B:154]** Speaker 1:  تو یہ چیز دھیان رکھیے گا کبھی بھی جب کبھی آپ کمپنیز کے اندر کام کر رہے ہو یا آپ کو opportunity ملتی ہے اور یہ کہا جاتا ہے کہ server کو reboot کرنا ہے یا server کا downtime لینا ہے، downtime مطلب for a long time بند کر رہے ہو، long time مطلب آدھا گھنٹہ، ایک گھنٹہ، دو گھنٹہ، پانچ گھنٹہ بند کر رہے ہو، power off کر رہے ہو۔ تو that is a long time اور server reboot کر رہے ہو مطلب آپ بند نہیں کر رہے، بس اسے

**[B:155]** Speaker 1:  up کر رہے ہو، مطلب refresh کر رہے ہو یا OS کی requirement ہو تو restart کرو، nothing else۔ تو server تو چل ہی رہا ہے۔ تو different case ہو جاتا ہے۔

**[B:156]** Speaker 1:  تو آپ کے پاس اگر اس طریقے کی long time activity کے لیے اگر آپ server down کر رہے ہو تو آپ بھلے ہی کتنے زیادہ experienced ہوں، آپ کا پہلا concern management سے یہ ہونا چاہیے کہ سر are we having آہ support from the vendor، یعنی کہ یہ جو ایچ پی کا server ہے یا ڈیل کا support ہے، اس او ای ایم کے ساتھ یا vendor کے ساتھ ہمارے پاس اس کا support ہے یا نہیں۔ اگر support نہیں ہے، سر sorry، میں اس server کو reboot نہیں

**[B:157]** Speaker 1:  کروں گا۔ کیونکہ اس طریقے کے issues میں زیادہ تر case میں server پھٹتے ہی پھٹتے ہیں۔ یہ دھیان رکھیے گا۔

**[B:158]** Speaker 1:  دوسرا hardware کا support ہے۔ سر are we having the operating system tech support؟

**[B:159]** Speaker 1:  Operating system کا support نہیں، tech support چاہیے۔ Operating system کا support مطلب basic چیزیں، وہ آپ کو بتا دیں گے، guide کر دیں گے کہ آپ کا OS صحیح چل رہا ہے یا کچھ کچھ چیز۔

**[B:160]** Speaker 1:  Tech support چاہیے بھائی۔ کیا ہمارے پاس وہ tech support ہے؟

**[B:161]** Speaker 1:  اگر وہ tech support ہے، then we are okay اور we are good to reboot the server، we are going to plan this activity۔ اگر اس طریقے کی activity نہیں ہے، بالکل بھی plan مت کریں۔

**[B:162]** Speaker 1:  یہ personally recommendation۔ بھلے ہی آپ کتنے بڑے server کے اندر expertise ہیں یا کچھ بھی ہے۔

**[B:163]** Speaker 1:  کیونکہ اس طریقے کے cases آتے ہیں اور آپ کے server worst cases میں پھٹ جاتے ہیں۔ اور ایسے case میں سارا پھر بل آتا ہے آپ کے اوپر۔

**[B:164]** Speaker 1:  تو بہتر ہے اگر اس طریقے کی کبھی کوئی activity plan ہو رہی ہے تو آپ یہ ساری کی ساری چیزیں دیکھ لیں اور اس کے basis پہ ہی آپ یہ ساری چیزیں plan کریں۔ کیونکہ activity میں جب آپ server reboot کر رہے ہوتے ہیں یا power off کر رہے ہوتے ہیں تو company آپ سے roll back plan بھی مانگتی ہے۔

**[B:165]** Speaker 1:  اور roll back plan جیسے تیسے اگر آپ کے management نے دے بھی دیا، کل کو issue آیا تو آر سی آپ سے ہی مانگا جائے گا کہ بتاؤ کہ یہ server کیوں نہیں ہے پورا۔ سمجھ رہے ہو تو آپ پھنس جاؤ گے۔

**[B:166]** Speaker 1:  تو ایسے case میں اگر اس طریقے کی activity ہو رہی ہے، because it's a huge activity، لوگوں کی نوکری تک کھا جاتا ہے۔ تو it's a huge activity ایسے case کے اندر، I will suggest کہ آپ پہلے company سے بولو کہ بھئی ہم لوگوں کے پاس tech support ہے یا نہیں، hardware کا بھی اور Microsoft کا بھی، یا Linux چل رہا ہے تو Linux کا tech support ہے یا نہیں۔

**[B:167]** Speaker 1:  تو جو بھی OS چل رہا ہے، اس کا ہمارے پاس tech support ہے یا نہیں ہے۔ سمجھ رہے ہیں آپ؟

**[B:168]** Speaker 1:  چلیں سر آگے۔ Yes سر۔

**[B:169]** Speaker 1:  حالانکہ ابھی ہم booting process پہ بات کر رہے تھے لیکن دیکھو دوسری direction میں چلے گئے۔ آہ میاں آہ I would like to let you know کہ ابھی ہم لوگوں نے جو دو classes پہلے کی بھی کری ہیں وہ زیادہ تر ہماری classes کچھ اسی طریقے کے experience کو لے کر بات ہونی start ہو جاتی ہے اور جب ہم topic پہ کام کر رہے ہوتے ہیں تو کسی دوسری آہ direction میں بھی redirect ہو جاتی ہے۔

**[B:170]** Speaker 1:  But I believe کہ یہ چھوٹی چھوٹی چیزیں جو میں ابھی آپ لوگوں کو capture کرا رہا ہوں۔ So it is kind of experience جو میں نے face کیا یا میری ٹیم نے face کیا یا کسی نے بھی face کیا، میرے students نے، ٹیم کا مطلب it could be my students as well as۔

**[B:171]** Speaker 1:  تو till now I have given the trainings to many students، so if they are also facing the issues، they are also talking with me۔ یا مجھے کچھ issues آ جاتے ہیں تو میں اپنی ٹیم سے یا اپنے کچھ specific students سے پوچھ لیتا ہوں کہ بھئی یہ کیسے، کیا چیزیں کرنی ہیں یار یہ issue آ گیا یا آپ اس ٹیکنالوجی پہ کام کرتے ہو تو آپ میرے کو support کر دو۔

**[B:172]** Speaker 1:  Right؟ تو کچھ یہ چیزیں۔

**[B:173]** Speaker 1:  So جیسے صبح میں نے ہاں جی۔ Sorry، بس اپنے interview والے سوالات بھی share کر دیں۔

**[B:174]** Speaker 1:  سر وہ تو میں natural سی بات ہے، ابھی جیسے booting process کے بارے میں بات کر رہے ہیں تو ہم یہ چل رہے ہیں۔ تو جیسے جیسے natural سی چیزیں جو میں آپ کو topic پڑھاتا جا رہا ہوں، topic مطلب جو جو ہم table of content complete کرتے جا رہے ہیں، وہ وہ servers جیسے جیسے کراؤں گا تو وہ natural بات ہے، آپ دیکھنا بیچ بیچ میں میں خود بولتا چلا جاؤں گا کہ this is very important۔

**[B:175]** Speaker 1:  یہ interview میں پوچھتے ہیں۔ الگ سے شاید میں آپ کو check list نہ دے پاؤں کہ یہ یہ questions آپ رکھ لو۔

**[B:176]** Speaker 1:  نہیں سر۔ That thing I can't do۔

**[B:177]** Speaker 1:  But جب میں آپ کو topic training دے رہا ہوں، اس time پہ definitely I will let you know کہ بھئی یہ important ہے، یہ پوچھتے ہیں۔ یا اس طریقے کی چیزیں پوچھتے ہیں۔

**[B:178]** Speaker 1:  یا اس طریقے کا scenario پوچھتے ہیں۔ تو کچھ وہ چیزیں ہیں۔

**[B:179]** Speaker 1:  بہت بات ہے۔ ٹھیک ہے۔

**[B:180]** Speaker 1:  So ابھی ہم بات کر رہے تھے bios کی تو ہمارے system کے اندر basic input output system ایک چھوٹی سی chip ہی ہے۔ Yes۔

**[B:181]** Speaker 1:  It is also a chip as well as۔ لیکن یہ chip mini operating system ہے۔

**[B:182]** Speaker 1:  جو ہمارے complete hardware کی information کو store کر کے رکھتا ہے۔ Date and time کو update کر کے رکھتا ہے۔

**[B:183]** Speaker 1:  اگر CMOS down ہو جاتی ہے cell تو CMOS کے time کو بھی update کرنے کے لیے bios کو update کرنا پڑتا ہے۔ اور جب bios کو update کر کے restart کرتے ہو تو CMOS update ہوتا ہے۔

**[B:184]** Speaker 1:  Direct ہم CMOS کو update نہیں کر سکتے۔ تو firstly we will have to update to the bios، then CMOS will update۔

**[B:185]** Speaker 1:  تو جب deep drive میں گھستے ہیں، کئی بار hardware سے related interview میں questions پوچھے جاتے ہیں تو یہ بھی پوچھ لیتے ہیں کہ CMOS cell down ہو گیا، اب آپ نے CMOS change کر دیا۔ اب آپ کو کمپیوٹر کا date and time change کرنا ہے۔

**[B:186]** Speaker 1:  تو کیسے update ہوگا؟ آپ بولو گے سر bios میں جاؤ۔

**[B:187]** Speaker 1:  وہ کہے گا down تو آپ کا CMOS ہوا تھا، bios میں کیوں جا رہے ہو؟ CMOS کو ہی direct کیوں نہیں update کرتے؟

**[B:188]** Speaker 1:  So directly we don't have the authority کہ ہم CMOS کو update کر سکیں۔ Only آہ hard manufacturer جو ہیں وہ direct CMOS کو update کر سکتے ہیں۔

**[B:189]** Speaker 1:  چاہے وہ ایچ پی کا server ہے یا ڈیل کا server ہے۔ Only they can do۔

**[B:190]** Speaker 1:  But ہم لوگوں کے پاس authority نہیں ہوتی کہ ہم CMOS کو update کر سکیں۔ تو on behalf of CMOS ہم bios میں date and time ڈالتے ہیں اور جیسے ہی correct time ڈالتے ہیں اور reboot کرتے ہیں کیونکہ ہمیں restart بھی کرنا پڑے گا۔

**[B:191]** Speaker 1:  Restart کے مطلب یہ ہے کہ وہ system کے CMOS کو update کر رہا ہوتا ہے اپنے time کے ساتھ اس کو replicate کر رہا ہوتا ہے۔ تو کچھ وہ چیزیں ہیں۔

**[B:192]** Speaker 1:  تو کچھ یہ چیزیں ہیں۔ تو یہ ہمارا basic input output system ہمارے hardware کی information کو store کر کے رکھتا ہے۔

**[B:193]** Speaker 1:  اور ایک information جو سب سے میجر store کر کے رکھتا ہے کہ آپ کے کمپیوٹر کا first boot device کیا ہوگا؟ سیکنڈ boot device کیا ہوگا اور تھرڈ boot device کیا ہوگا؟

**[B:194]** Speaker 1:  یہ information بھی آپ یہاں پر دیتے ہیں۔ آپ لوگوں نے دیکھا ہوگا کئی بار جب ہم pen drive bootable بنا کر pen drive سے installation کرتے ہیں تو ہم first boot device pen drive select کرتے ہیں۔

**[B:195]** Speaker 1:  تو pen drive کہاں select کر رہے ہیں؟ وہ setting bios کے اندر ہی update ہو رہی ہے۔

**[B:196]** Speaker 1:  Bios کو ہی بتایا جا رہا ہے کہ بھیا اگلی بار جب آپ reboot ہوں گے۔ Reboot ہونے کا مطلب یہ نہیں ہے کہ آپ hard disk سے boot ہو جاؤ۔

**[B:197]** Speaker 1:  کیونکہ hard disk سے boot ہو گئے تو اس میں میرا یا تو OS نہیں ہے یا OS corrupt ہو گیا۔ تو اس لیے میں نے یہ pen drive لگائی ہے۔

**[B:198]** Speaker 1:  Pen drive سے boot ہونا ہے۔ Pen drive میں booting files پڑی ہیں۔

**[B:199]** Speaker 1:  تو pen drive کی configuration ہے۔ ہاں۔

**[B:200]** Speaker 1:  تو ہم جو یہ first boot device set کر رہے ہیں وہ بھی bios میں ہی store ہوتا ہے۔ Right؟

**[B:201]** Speaker 1:  تیسری میجر چیز جو bios میں update ہوتی ہے that is called virtualization ٹیکنالوجی۔ اگر آپ کمپیوٹر کے اندر VT enable کرنا چاہتے ہیں، virtualization کرنا چاہتے ہیں، آپ hyper V install کرنا چاہتے ہیں، آپ آہ VMware workstation install کرنا چاہتے ہیں، ESXi install کرنا چاہتے ہیں، firstly آپ کو bios سے جا کر VT کی functionalities کو enable کرنا پڑے گا۔

**[B:202]** Speaker 1:  ہر laptop، desktop یا servers کے اندر الگ الگ different different procedures ہوتے ہیں۔ So I will suggest اس case کے اندر آپ اپنے کمپیوٹر کے اندر چیک کریں کہ کیا procedure ہے۔

**[B:203]** Speaker 1:  تو آپ جو بھی ماڈل use کر رہے ہو laptop کا یا desktop کا وہ ماڈل ڈال کے اور اس میں گوگل پہ search کریں گے کہ اس میں مجھے VT enable کرنا ہے، کیسے enable ہوگا تو اس کے steps دے دے گا۔ اور جب VT enable ہو جاتا ہے، اگر میں آپ کو اپنے سسٹم پر دکھاؤں task manager، کل بھی شاید ہم بات کر رہے تھے یہ VT کو لے کر۔

**[B:204]** Speaker 1:  تو میرے سسٹم کے اندر performance tab میں میں جاؤں گا۔ CPU section پہ click کروں گا۔

**[B:205]** Speaker 1:  اور CPU پہ اگر یہاں دیکھیں گے virtualization ٹیکنالوجی enabled ہے۔ Enabled ہے۔

**[B:206]** Speaker 1:  اسی لیے میں VMware workstation پہ کام کر پا رہا ہوں۔ اسی لیے میں hyper V پہ کام کر پاؤں گا۔

**[B:207]** Speaker 1:  یا کسی دوسرے hypervisor پہ کام کر پاؤں گا۔ اگر یہ disable ہوتا تو مجھے پہلے bios سے جا کر enable کرنا پڑتا۔

**[B:208]** Speaker 1:  Right؟ So this information is also stored in your virtualization ٹیکنالوجی۔

**[B:209]** Speaker 1:  Sorry، in your bios، sorry۔ Right۔

**[B:210]** Speaker 1:  تو یہ information بھی store ہوتی ہے۔ اس کے علاوہ ایک اور چیز جو سب سے زیادہ common ہے security کے prosperous، that is secure boot۔

**[B:211]** Speaker 1:  تو ہمارے پاس secure boot کے اندر ایک option پہلا تو یہ آتا ہے کہ کیا آپ server کے اوپر کوئی password protect کرنا چاہتے ہیں کہ جیسے ہی کوئی power on کرے، power on ہوتی ہے، post on ہوگا، yes of course۔ لیکن bios بھی تب load ہو جب پہلے password ڈال دو آپ۔

**[B:212]** Speaker 1:  تو bios load ہوگا پھر یا bios load ہو جائے اس کے بعد وہ تبھی آگے boot ہو جب پہلے password ڈال دو۔ تو پہلے password ڈالنا پڑے گا۔

**[B:213]** Speaker 1:  تو secure رکھنا چاہتے ہو کیونکہ مان لو کل کو کوئی آپ کے data center میں unauthorized person آ گیا اور اس نے آپ کے سسٹم کو آپ کی absence میں on کر دیا تو ایسے case میں on کرنے کے time پہ وہ proper پورا on نہیں ہوگا۔ وہ بیچ میں ہی رکا ہوا ہے۔

**[B:214]** Speaker 1:  Post run ہو گیا، bios run ہو گیا۔ bios run ہونے کے بعد اب وہ پوچھ رہا ہے بھائی صاحب آپ کون ہو password بتاؤ۔

**[B:215]** Speaker 1:  password بتاؤ گے تبھی وہ آگے step پہ جائے گا۔ تب بتائے گا کہ first boot device کیا ہے ورنہ وہ بتائے ہی نہیں رہا۔

**[B:216]** Speaker 1:  اور جب بتائے گا نہیں تو سسٹم on نہیں ہوگا۔ تو ابھی وہ اسی stage پہ پڑا ہے۔

**[B:217]** Speaker 1:  تو آپ اپنے ایک server کے اندر یا laptop یا desktop کے اندر بھی functionality ہوتی ہے۔ آپ secure boot کو enable کر سکتے ہیں۔

**[B:218]** Speaker 1:  If you want۔ But data center already highly secure zone area کے اندر ہوتے ہیں۔

**[B:219]** Speaker 1:  تو servers کے اندر ہم یہ secure boot کو enable کرتے نہیں ہیں۔ یہ normal رہتا ہے۔

**[B:220]** Speaker 1:  Right؟ تو کچھ یہ چیزیں ہیں۔

**[B:221]** Speaker 1:  تو میجر ہے یہ bios کی basis پہ ہی ہم یہ identify کرتے ہیں کہ سسٹم کو کیسے boot ہونا ہے۔ Otherwise سسٹم سے bios ہٹا دیں۔

**[B:222]** Speaker 1:  اور bios کا ابھی ہمارے پاس ایک اور alternative آ گیا which is called UEFI۔ تو UEFI کے comparison bios اور UEFI میں comparison کریں تو bios کا advance version ہے UEFI۔

**[B:223]** Speaker 1:  جس کے اندر ہمیں یہ benefit ملتا ہے کہ سسٹم fast shut down ہو جاتا ہے، fast up ہو جاتا ہے۔ یہ سب سے بڑا میجر difference ہے۔

**[B:224]** Speaker 1:  Apart of that virtualization ٹیکنالوجی کو لے کر بھی کافی ساری اور features ہیں جن کو یہ higher configuration کے hardware کے ساتھ support کرتا ہے۔ bios پہ اگر آپ کام کر رہے ہیں تو وہ higher configuration کے servers کو support نہیں کر پائے گا۔

**[B:225]** Speaker 1:  تو یہ drawback ہے۔ اور آج کے time میں زیادہ تر ہمارے جو OS بھی آ رہے ہیں وہ بھی یہ کہتے ہیں کہ آپ کے جو سسٹم ہیں وہ UEFI based ہونے چاہیے۔

**[B:226]** Speaker 1:  Which is more good۔ تو اس case میں اچھی performance ملتی ہے۔

**[B:227]** Speaker 1:  Legacy پہ جاؤ گے یعنی کہ bios میں جاؤ گے۔ سرور آپ نے نیا خرید لیا۔

**[B:228]** Speaker 1:  آہ سرور مطلب hardware جو آپ کے پاس ہے ایچ پی کا یا ڈیل کا جو سرور ہے وہ آپ نے نیا خرید لیا لیکن legacy mode select کر دیا bios اور OS بھی latest ہے تو بھی آپ کو سرور کے اندر اچھی performance نہیں مل پائے گی تو ایسے case میں آج کے time میں اگر آپ کوئی نیا server build کر رہے ہیں you will have to select the UEFI اب یہ اس لیے بھی important ہے ٹھیک ہے تو fast boot کرانے کے لیے ہمیں یہ requirement

**[B:229]** Speaker 1:  ہے تو bios سے information collect ہو گئی کہ first boot device کیا ہوگا اب آپ کے سسٹم میں اگر مان لو دو hard drive لگی ہوئی ہیں یا تین hard drive لگائی ہے آپ نے کون سی hard drive bios میں select کرنی ہے اس کے basis پہ وہ اس کو select کر لیتا ہے جیسے ہی hard disk select ہوتی ہے ہمیشہ یہ دھیان رکھیے گا جس hard disk کے اندر آپ کا OS install ہے اس hard disk کے پہلے track پہ یا پہلے track and sector پہ

**[B:230]** Speaker 1:  آپ کے OS کی ساری information mention ہوتی ہے ساری information مطلب کیسے اس sector کو ہم بولتے ہیں volume boot sector ایم بی آر کو ابھی میں miss کر رہا ہوں skip کر رہا ہوں اس کے بارے میں بات کریں گے پہلے volume boot sector کو سمجھ لیں تو bios کے بعد ویسے تو ایم بی آر یا جی پی ٹی کچھ ایک چیز run ہوتی ہے اس پہ بات کریں گے لیکن ابھی میں volume boot sector پہ آ گیا پہلے تو volume boot sector کے اندر ایک

**[B:231]** Speaker 1:  طریقے کی information ہے کیا کہ آپ کے سسٹم کے اندر یہ جو hard disk ہے اس hard disk میں کتنے drives ہیں ایک ہی drive ہے سی drive یا سی drive ڈی drive ای drive ہے سی drive ہے تو سی drive کی booting files کس path پہ رکھی ہے اور index میں کہاں ہے index مطلب جیسے copy کے اندر یا book کے اندر آپ نے دیکھا ہوگا index ایک section ہوتا ہے index کہاں ہوتا ہے سب سے starting میں جہاں پر یہ mention ہے کہ chapter one

**[B:232]** Speaker 1:  page نمبر اتنے سے اتنے تک ہے chapter two اتنے page نمبر سے اتنے page نمبر تک ہے same way یہاں پر بھی آپ کے پاس ساری information store ہوتی ہے کہ hard disk کے اندر جو track and sector ہے تو کس track and sector میں کیا data رکھا ہے یہ information store ہوتی ہے تو volume boot sector سے وہ identify کرتا ہے کہ میرے سسٹم کی rest of the booting files کہاں پر ہے اس سبھی booting files کی information وہاں سے ہمیں مل جاتی ہے اور جب

**[B:233]** Speaker 1:  booting file کی information run ہو جاتی ہے مل جاتی ہے تو اس کے بعد جو track and sector کو read کرنے کے بعد run ہوتا ہے that is boot sector boot sector کہاں ہوتا ہے کل ہم لوگوں نے دیکھا تھا windows installation کے time پہ تین drives بنی تھیں ہماری ایک boot drive تھی ایک system drive تھی اور ایک سی drive تھی تو یہاں پر وہ anti boot sector کا مطلب یہ اس system drive کے پاس جا رہا ہے boot drive کے پاس جا رہا ہے جو

**[B:234]** Speaker 1:  hundred ایم بی کی تھی جس میں ساری سسٹم کی booting files ہیں تو وہاں سے وہ سسٹم کو initialize کر رہا ہوتا ہے اور جب وہ initialize کر رہا ہوتا ہے تو آپ کو front end پہ وہ logo blink ہوتا ہوا دکھ رہا ہوتا ہے مائیکروسافٹ کا that is the working of this anti boot sector booting files مل گئی اب باری آتی ہے ہمارے پاس boot ایم جی آر کی یہ آپ کے سسٹم کی health کو چیک کرتا ہے اس سسٹم کو direct run نہیں کر رہا

**[B:235]** Speaker 1:  وہ سسٹم کی health کو چیک کر رہا ہے اب ایسا ہو سکتا ہے یہ boot ایم جی آر الگ الگ cases پہ کام کرتا ہے تو یہ boot ایم جی آر کیا ہے boot ایم جی آر is windows server boot loader یہ بھی بڑا interview میں trending question ہے interview میں کئی بار booting process نہ پوچھ کے interviewer یہ پوچھ لیتا ہے کہ windows کا boot loader کیا ہے تو it's a boot ایم جی آر پہلے این ٹی ایل ڈی آر ہوتا تھا این ٹی ایل ڈی

**[B:236]** Speaker 1:  آر بہت corrupt ہو جاتا تھا لیکن boot ایم جی آر corrupt نہیں ہوتا ہے اور اگر corrupt ہو بھی جائے we can roll back اور we can restore it ابھی یہی بتائے گا دیکھو کیسے restore ہو جائے گا اگر اسے restore بھی کرنا ہے تو یا باقی کچھ اور files سب corrupt ہو جائیں تو وہ restore کی جا سکتی ہیں کیونکہ anti boot sector والی drive کے اندر جتنی بھی booting files ہیں وہ secure ہیں وہ crash نہیں ہوں گی یا corrupt نہیں ہوں گی سسٹم فائل

**[B:237]** Speaker 1:  corrupt ہو سکتی ہیں تو boot ایم جی آر کیا کرتا ہے وہ یہ چیک کرتا ہے کہیں ایسا تو نہیں ہے کہ سسٹم کو hybernate کر دیا ہے جیسے laptop کے case میں میرے پاس یہ میرا laptop ہے میں اس laptop پہ کام کر رہا ہوں اور میں نے اس laptop کو for a time being میں نے بند کر دیا ابھی یہ power on ہے میں نے اسے بند کر دیا اور power on سسٹم کو ہی میں گھر لے گیا لیکن اگر آپ دیکھو گے اس case

**[B:238]** Speaker 1:  میں گھر لے جانے کے time پہ جب میں اسے گھر سے نکالوں گا تو اس کے اندر بہت زیادہ heat ہو رہی ہوگی حالانکہ جب میں سسٹم کو کھولوں گا تو میرے پاس direct ایک دم سے login screen آ جائے گی تو وہ login screen کیوں آ رہی ہے آپ کا سسٹم ایک طریقے سے suspend ہو گیا تھا یا hybernate ہو گیا تھا laptop میں وہ hybernate کا option ہوتا ہے آ virtual machine کے اندر suspend ہوتا ہے physical سسٹم میں نہ hybernate ہوتا ہے نہ suspend

**[B:239]** Speaker 1:  ہوتا ہے وہ virtual machines میں ہی ہوتا ہے تو اگر آپ نے hybernate یا suspend کر دیا اپنی virtual machine کو یا server کو یا laptop کو تو جب واپس اسے power on کرتے ہو تو ایک دم سے win resume dot exe file load ہو جاتی ہے اور یہ win resume dot exe file آپ کو credentials پوچھتی ہے کہ آپ سسٹم پہ کون ہو authorize کرو اپنے آپ کو اگر آپ نے hybernate کیا ہے لیکن اگر آپ نے سسٹم پہلے power off کیا تھا power on کر

**[B:240]** Speaker 1:  رہے ہیں تو یہ boot ایم جی آر کیا کرتا ہے win load dot exe کو load کر دیتا ہے ٹھیک ہے تو یہ ہمارا win load dot exe ہماری ایک اور booting file ہے جو ہماری additional سسٹم کو boot load کرنے میں کام کر رہی ہے تیسرا ایسا ہو سکتا ہے کہ win load dot exe corrupt ہو جائے یا باقی سسٹم files نہ ملے crash ہو جائے یا کچھ اور issues آ جائیں تو ایسے case میں تیسرا طریقہ یہ ہے بی سی ڈی boot configuration data ویسے

**[B:241]** Speaker 1:  تو اسے ہم boot configuration wizard بھی بولتے ہیں تو اگر آپ کا OS corrupt ہو گیا crash ہو گیا تو آپ اسے repair بھی کر سکتے ہو تو کل ہم نے دیکھا تھا کہ installation کے time پہ میں نے ایک section پہ دکھایا تھا کہ installation کرنا ہے تو install اور repair کرنا ہے تو نیچے ایک section ایک چھوٹی line آ رہی تھی repair your system اس پہ click کرتے ہو تو بی سی ڈی کی console کھل جاتی ہے ابھی ہم نے repair نہیں کرا in future

**[B:242]** Speaker 1:  اگر کبھی opportunity ملی تو we will see but ہم بی سی ڈی دیکھ سکتے ہیں اور اس کے through اپنے سسٹم کو roll back کر سکتے ہیں restore کر سکتے ہیں اور restore کرنے کا سب سے اچھا طریقہ یہ ہے کہ جب آپ نے سسٹم ready کر دیا ہے تو آپ کو سسٹم کا restore point بھی بنا کر رکھنا پڑے گا اگر آپ نے restore point نہیں بنایا تو بڑی challenges آنے والے ہیں لیکن restore point بنا دیا تو well and good ہے تو کچھ وہ چیزیں

**[B:243]** Speaker 1:  ہیں win load dot exe کیا کام کرتی ہے win load dot exe anti OS kernel یعنی کہ windows کے kernel کو load کرتی ہے ابھی تک دیکھو kernel آیا ہی نہیں اور آپ کا وہ جو logo ہے مائیکروسافٹ کا وہ اس طریقے سے blink کر رہا ہے ابھی آپ یہ مان کے چلو back end پہ اتنے سارے process ہو گئے لیکن ابھی آپ کے پاس وہ logo اس طریقے سے blink کر رہا ہے so now anti OS kernel جب load ہوتا ہے تو سب سے پہلے یہ

**[B:244]** Speaker 1:  load کرتا ہے halt dot dll یا h a l double dll کو ہم جسے ہم بولتے ہیں halt dot dll file کیا کام کرتی ہے یہ جتنے بھی آپ کے سسٹم کے device and drivers ہیں ان کی index file ہے کہ آپ کے کمپیوٹر کا گرافک card کا driver کہاں ہے land card کا driver کہاں ہے یو ایس بی پورٹ کا driver کہاں ہے یا دوسری چیزوں کے drivers کہاں ہیں index file ہے اور اس کے اندر ساری information ہے کہ کس کی driver file کی آ

**[B:245]** Speaker 1:  location کہاں ہے اور وہ کہاں سے initialize ہو سکتی ہے تو halt dot dll کیا کرتا ہے آپ کے سارے کے سارے device and drivers کو load کرانے میں help کرتا ہے ساتھ ساتھ anti OS kernel اگلے stage پہ جا رہا ہوتا ہے یعنی اپنے آپ کو initialize کر رہا ہوتا ہے اپنی باقی services کو initialize کر رہا ہوتا ہے اس لیے اگر آپ دیکھو گے تو anti OS kernel پہ آنے کے بعد میں نے دو الگ سے اور face بنائے ہیں anti OS kernel کے اندر

**[B:246]** Speaker 1:  face zero and face one تو zero one کے zero کے اندر وہ driver کو چیک کر رہا ہوتا ہے ساتھ ساتھ کہ بھئی سارے device and drivers diagnosed ہو گئے یا نہیں کئی بار ایسا بھی ہو سکتا ہے کہ driver diagnosed نہ ہو اور driver diagnosed نہ ہونے کا کئی بار ایسا reason بھی ہو سکتا ہے آپ کا land card لگا تھا land card خراب ہو گیا اب land card خراب ہو گیا تو سسٹم میں alarm نہیں آئے گا سسٹم تو چل جائے گا لیکن آپ کو

**[B:247]** Speaker 1:  بعد میں پتہ لگے گا کہ سسٹم میں land card ہی نہیں کام کر رہا اور جب land card physically کام نہیں کر رہا تو وہ hardware نہیں کام کر رہا تو software کیسے کام کرے گا بھائی اگر میرا موبائل فون کا hardware کام نہیں کر رہا اور سسٹم میں موبائل فون power on ہی نہیں ہو رہا تو موبائل فون چلے گا کیسے مجھے display کیسے آئے گا same way یہاں پر بھی ہے تو سارے device and drivers کے ساتھ وہ diagnose کر رہا ہوتا ہے کہ وہ

**[B:248]** Speaker 1:  کام کر رہے ہیں یا نہیں کر رہے پھر وہ face one پہ آتا ہے اور face one کے اندر اپنی سبھی سسٹم files کو initialize کرتا ہے اب initialize ہونے کے بعد یہاں پر again اگلا ایک process آتا ہے which is called ایس ایم ڈبل ایس ڈاٹ ای ایکس سی اور اس کے آگے میں نے دو order لکھے ہیں ون تھرٹی ٹو کے ڈاٹ سس اور ون لوگن ڈاٹ ای ایکس تو سب سے پہلی چیز یہ ایس ایم ڈبل ایس ڈاٹ ای ایکس سی کیا کام کرتی

**[B:249]** Speaker 1:  ہے ویسے تو جتنی بھی چیزیں ابھی ہم نے بات کری ہیں کیا کام کرتی ہیں میں نے page نمبر one پہ mention کیا ہوا ہے ٹھیک ہے حالانکہ میں نے اسے اب آپ کو سارا کا سارا theoretical مطلب verbally بتایا ہے but اگر آپ theoretical دیکھنا چاہتے ہو تو یہاں سے بھی آپ دیکھ سکتے ہو تو ابھی ہم جیسے ہم بات کر رہے تھے ایس ایم ڈبل ایس ڈاٹ ای ایکس سی فائل کی تو اگر ہم اس کے بارے میں بات کریں گے تو یہ کیا کام

**[B:250]** Speaker 1:  کرتا ہے یہ load کرتا ہے ہمارے سسٹم کی رجسٹری کو اس کے علاوہ یہ environment بنا کر دیتا ابھی جب تک وہ cursor آپ کا یا logo blink ہو رہا تھا آپ کے سسٹم کے اندر آہ true کلرز نہیں آئے تھے windows کے windows کے true کلرز کیا ہوتے ہیں بتیس بٹ اس سے پہلے جو کلر ہوتے ہیں وہ سارے سولہ بٹ کے ہوتے ہیں تو سولہ بٹ کے اندر اگر آپ دیکھو گے آپ کے true کلرز نظر نہیں آئیں گے یعنی کہ اگر آہ rainbow دیکھیں

**[B:251]** Speaker 1:  ہم تو rainbow کے اندر پتہ نہیں کتنے کلرز ہوتے ہیں آئی think کتنے کلر ہوتے ہیں any idea سر basic کلر نہیں جاننے کے سات کلر آپ بولو کہ سات کلر ہوتے ہیں سات کلر نہیں ہوتے کروڑوں میں جا کے کچھ کلرز نکل کر آتے ہیں تو rainbow میں بھی اگر ہم count کریں کروڑوں میں کلرز ہیں تو اگر ہم سولہ بٹ پہ دیکھ رہے ہیں تو ہمیں وہ کروڑوں چھوڑو وہ سات کلر بڑی مشکل سے دکھ رہے ہوں گے لیکن وہ سات کلر مل کے آپ

**[B:252]** Speaker 1:  کے وہ کروڑوں کلرز نہیں بنا رہے ہوں گے تو سسٹم یہاں پر change ہو رہا ہوتا ہے اپنے graphics mode کو change کر رہا ہوتا ہے سولہ بٹ کی جگہ بتیس بٹ پہ that is اے true کلر بٹ تو وہاں پر آپ کی performance کے performance مطلب graphical representation اچھی ہو جاتی ہے تو کچھ یہ چیزیں ہیں اس کے علاوہ ایس ایم سیس کیا کرتا ہے آپ کی ون لون ون لوگن ڈاٹ ای ایکس سی فائل کو بھی load کرتا ہے اور یہ ون لوگن ڈاٹ ای

**[B:253]** Speaker 1:  ایکس سی کیا کام کرتی ہے login سکرین آپ کو دے دیتی ہے جہاں آپ اپنا user name password hit کرتے ہیں and جیسے ہی آپ اپنا user name password hit کرتے ہیں تو اگر آپ نے صحیح user name password hit کیا ہے تو authentication ہو جائے گا from سیم فائل آپ کے پاس ہر ایک سسٹم میں ابھی جیسے ہم نے یہ جو windows install کیا تھا اس windows کے اندر بھی ہمیں ایک فائل دیکھنے کو ملے گی سیم فائل اگر ہمیں نہیں پتا یہ سیم فائل کہاں

**[B:254]** Speaker 1:  ملے گی try کرتے ہیں ایک بار کہاں ملے گی ذرا گوگل پہ دیکھتے ہیں آ گوگل open کرتے ہیں اور اس میں لکھتے ہیں سیم ان ونڈوز path اور ذرا دیکھتے ہیں کیا path بتا رہا ہے تو یہ مجھے بتا رہا ہے ونڈوز میں یعنی کہ سی ڈرائیو ونڈوز سسٹم تھرٹی ٹو کنفیگ and then سیم ذرا چیک کرتے ہیں اس path پہ کوئی فائل ملتی ہے کہ سیم نام کی سی ڈرائیو میں جاتے ہیں آ یہ رہا ونڈوز سسٹم تھرٹی ٹو سسٹم تھرٹی ٹو کے اندر اس

**[B:255]** Speaker 1:  نے بولا تھا کنفیگ اور کنفیگ کے اندر بولا ہے سیم آ رہی ہے سر کوئی ایک فائل جی جی سیم آ رہی ہے بالکل تو ہمیں سیم فائل نظر آ رہی ہے یہ سیم فائل کیا کرتا ہے جتنے بھی آپ سسٹم کے اندر users بناتے ہو گروپ بناتے ہو وہ سارے یہاں store ہوتے ہیں اور ان کے جو password ہیں وہ password بھی یہاں store ہوتے ہیں تو جب آپ login سکرین پہ اپنے user name password add کر رہے ہو تو hit کر کے enter کرتے ہو

**[B:256]** Speaker 1:  تو ایک query جاتی ہے اور وہ اس فائل کے اندر جا کے cross check کرتی ہے کہ کیا آپ نے user name password صحیح دیا ہے یا غلط ہے اگر غلط دیا ہے تو message آ جائے گا sorry your user name password is mismatch retry یا try again تو آپ دوبارہ password ڈالتے ہو آپ کو یاد آ جاتا ہے ہاں یار شاید میں نے انڈیا at the rate one two three لکھنا تھا لیکن انڈیا کا آئی چھوٹا لکھ دیا غلط لکھ دیا تو یہ تو میری غلطی

**[B:257]** Speaker 1:  ہے تو دوبارہ try کر لیتا ہوں اور آپ دوبارہ try کرتے ہو صحیح password enter کرتے ہو اور login ہو جاتا ہے تو وہ یہاں سے verify کر رہا ہوتا ہے تو آپ نے غلط password enter کیا تھا تو وہ message آ گیا اور صحیح password ڈالا login ہو گیا authenticate ہو گیا authenticate کیسے ہوا یہاں پر ایک protocol کام کرتا ہے which is called این ٹی ایل ایم authentication protocol تو local سسٹمز میں وہ این ٹی ایل ایم authentication protocol کام کرتا ہے اور جیسے ہی

**[B:258]** Speaker 1:  آپ کا وہ protocol verify کر لیتا ہے کہ user name password صحیح ہے آپ کا سسٹم login ہو جاتا ہے ٹھیک ہے تو ابھی یہاں پر جیسے ہی win load لوگن ڈاٹ ای ایکس سی کے اوپر ہم آئے ہمارا user name password اس میں چیک ہوا تو ہمارے پاس next فائل load ہو جائے گی یہاں پر ایل سیس ڈاٹ ای ایکس سی یہ ایل سیس ڈاٹ ای ایکس سی کیا کام کرتی ہے آپ کی queries کو verify کرنے کے بعد desktop سکرین کو load کراتی ہے یعنی

**[B:259]** Speaker 1:  کہ جہاں آپ desktop دیکھتے ہیں یعنی کہ اگر میں بات کروں میرے سسٹم پہ یہ سکرین آ چلو بھائی سب minimize ہو جاؤ یہ desktop ہے تو یہ سکرین ہمارے پاس load ہوتی ہے تو this is اے complete booting process جہاں سے ہم اپنے سسٹم کو boot کر سکتے ہیں right تو یہ بہت important ہے اپنے آپ میں بہت زیادہ vast chapter ہے اگر آپ دیکھیں اور اس سے related میں نے کچھ information یہاں دی ہوئی ہے اور یہ information اگر میں بات کروں for client OS

**[B:260]** Speaker 1:  ونڈوز ویسٹا ونڈوز سیون ونڈوز ایٹ ونڈوز ٹین ونڈوز الیون سبھی میں same process ہے سرورز میں میں بات کرتا ہوں تو سرور دو ہزار بارہ سے لے کر دو ہزار پچیس تک same booting process ہے there is no changes تو interviewer اگر آپ سے کوئی پوچھتا ہے کہ booting process بتاؤ تو پہلے تو اسے ہمیں یہ نہیں confuse کرنا نہ نہ اس سے یہ پوچھنا ہے کہ بھئی کون سے OS میں پوچھ رہے ہو آپ آپ اسے یہی procedure بتاؤ ٹھیک ہے ہاں کیونکہ پرانے والے تو

**[B:261]** Speaker 1:  پوچھے گا نہیں ایچ پی تو پوچھے گا نہیں یا ونڈوز سرور دو ہزار تین تو پوچھے گا نہیں ٹھیک ہے یا دو ہزار آٹھ پوچھے گا نہیں کیونکہ آج کے ٹائم میں نہ تو چلتے ہیں نہ ان پہ support ہے تو support آپ کے پاس کس پہ ہے دو ہزار سولہ پہ یا انیس پہ یا بائیس پہ ہے تو ہم انہی کے بارے میں بات کریں گے تو this is the booting processor تو اس طریقے سے ہمیں ایک systematic طریقے سے اسے answer کرنا ہے آئی believe

**[B:262]** Speaker 1:  کہ کافی ساری چیزیں clear ہو گئی ہوں گی تو سر ہم بایوس پہ بھی نہیں جائیں گے یو ای ایف آئی پہ آ جائیں گے آج کے ٹائم میں yes یو ای ایف آئی پہ اگر آپ نے سسٹم رکھا ہے تو یو ای ایف آئی اگر آپ نے یو ای ایف آئی پہ سسٹم کو install کیا ہے اور کل کو اگر آپ نے اسے بایوس convert کر دیا تو آپ دیکھو گے آپ کا بایو ونڈوز load ہی نہیں ہو گا تو آپ نے OS کس پہ supportive

**[B:263]** Speaker 1:  آ بنایا ہے بایوس کے ساتھ یا یو ای ایف آئی کے ساتھ تو جو setting کے ساتھ آپ نے OS install کیا ہے even جب آج کے ٹائم میں pen drive بھی bootable بناتے ہو specially جو ہم کل last day میں دیکھ رہے تھے روفس ایک tool تھا یا آپ روفس is the bestest tool یونیور یو ایس بی یونیورسل انسٹالر کر کے بھی ایک tool آتا ہے that is also fine but وہ لینکس کے case میں بہت اچھا ہے لینکس اگر آپ کو bootable بنانا ہے تو

**[B:264]** Speaker 1:  it is fine but روفس اگر میں بات کروں ونڈوز non ونڈوز دونوں case میں بہت اچھا ہے کیونکہ اس میں آپ کو ایک additional functionality مل جاتی ہے آپ جب pen drive bootable بناتے ہو تو وہ پوچھتا ہے کہ بایوس bootable enable بنانی ہے یا یو ای ایف آئی enable bootable بنانی ہے تو اگر آپ کا hardware یو ای ایف آئی enable کو support کرتا ہے تو آپ یو ای ایف آئی option کو ہی select کریں گے جبکہ یو ایس بی installer جو ہے وہ یہ option

**[B:265]** Speaker 1:  نہیں پوچھتا تو اس لیے that's why روفس is اے good tool ٹھیک ہے تو اگر آپ نے سسٹم یو ای ایف آئی پہ رکھا ہے تو یو ای ایف آئی کو ہی سب select کرے گا یو ای ایف آئی کے ساتھ بایوس بھی ملتا ہے مطلب اگر ہم آج کے ٹائم میں بات کریں یو ای ایف آئی اگر install ہے تو بایوس بھی ہے اب نئے سرور خرید کے لے کر آئے ہو choice is yours کی بایوس پہ run کرنا ہے یا یو ای ایف آئی پہ

**[B:266]** Speaker 1:  آپ نے کہا مجھے یو ای ایف آئی پہ جانا ہے تو یو ای ایف آئی پہ آپ نے configurations کر دی ساری کی ساری اور OS install کر لیا لیکن کل کو trouble shooting ہونے لگی یا due to some reason آپ کا سرور down ہوا یا سیمو سیل down ہو گیا کئی بار ایسا بھی ہوتا ہے کہ سیمو crash ہو گیا خراب ہو گیا date and time تو اڑا ہی اڑا آپ نے date and time fix کر لیا کئی بار ایسا بھی ہوتا ہے کہ بایو جو

**[B:267]** Speaker 1:  first boot device ہے وہ اس پہ نہیں جاتا یو ای ایف آئی پہ نہیں جاتا وہ بایوس پہ چلا جاتا ہے legacy mode میں چلا جاتا ہے تو جس کی وجہ سے آپ کا OS تب بھی load نہیں ہوتا یہ بھی ایک problem ہو جاتی ہے سیمو سیل کے down ہونے سے تو آپ سسٹم کو یو ای ایف آئی کرنا پڑے گا of course نہیں تو سسٹم نہیں run ہو گا ٹھیک ہے جی so میں نے یہ already ہمارے ون ڈرائیو پہ share کر دیا ہے slide

**[B:268]** Speaker 1:  and ابھی آپ جب اسے access کریں گے تو آپ کو یہ slide مل جائے گی آپ اس کو refer کر سکتے ہیں right اس کے علاوہ additionally if you can search out anything in the booting process it is more good thing ہاں ایک چیز ہے جو ابھی ہم نے اس میں miss کری ہے یا میں نے اسے skip کیا ہے جان کے کیونکہ ہم اس کو ہم آگے discuss کرنے والے ہیں ایم بی آر which is ایم بی آر اور آج کے ٹائم میں ایم بی آر

**[B:269]** Speaker 1:  کے ساتھ ساتھ جی پی ٹی کو بھی use کرتے ہیں تو یہ ایم بی آر اور جی پی ٹی دونوں ہی آہ ڈسک انیشلائز کرنے کا ایک میتھڈ ہے تو ہم اس پہ کمنگ ویک کے اندر ڈسکشن کریں گے because ٹوڈے وی ڈونٹ ہیو دا سفیشنٹ ٹائم کہ ہم اس پہ زیادہ ٹائم لے کے بات چیت کر پائیں right تو دیز آر دا بیسک تھنگ ابھی میں زیادہ لیبز نہیں کر رہا ہوں آج بھی اگر دیکھو گے تو ہم نے لیب کے اندر آہ او ایس انسٹالیشن

**[B:270]** Speaker 1:  ہی کیا تھا یا وی ایم وے ٹول انسٹال کیا او ایس تو کل انسٹال کیا تھا تو آج ہم نے لیب کچھ بھی نہیں کری سارا کا سارا سینریو جو ہمارا تھیوریٹیکل چلتا رہا ہے تو بٹ یہ جو چیزیں ہیں چھوٹی چھوٹی چیزیں ہیں یہ بڑی امپورٹنٹ ہیں اینڈ آئی ویل سجیسٹ کی آپ ویک میں ٹائم ملاؤ کوئی ایک ایسا جس ٹائم پہ آپ اس ریکارڈنگ کو دوبارہ سے ریفر کرو بیفور یور ویک اینڈ یعنی کہ سیٹرڈے آنے سے پہلے آپ اس سیشن کو ایک بار دوبارہ

**[B:271]** Speaker 1:  ریفرنس لو دوبارہ سے سنو کیونکہ جب تک وہ ویک اینڈ آئے گا آئی ایم ڈیم شور اور سائنس بھی یہ کہتی ہے کہ آج جو چیز آپ نے پڑھی ہے اس کی آدھی سے زیادہ چیزیں آپ کل بھول چکے ہوں گے یعنی اتنی ڈیٹیلنگ میں بھول جاؤ گے جیسے اگر میں پوچھوں کہ لیٹ سپوز میں آہ کسی سے بھی لیٹ سپوز اگر میں آہ اگر کچھ اسپیشل ڈے نہیں ہے سو یو ویل ہیو ٹو گیو دا انسر آہ خالد جی آپ نے ویڈنس ڈے میں سر لنچ

**[B:272]** Speaker 1:  میں کیا کھانا کھایا تھا آپ نے میری گردن پکڑ لی ہے مجھے استاد اوہ سر وہ ملتا ہے آپ کا نبات تولہ ہی ملتا ہے شوگر کی وجہ سے میں بتا دوں گا کہ مجھے روٹی اور سالن ہی ملا تھا اچھا اوکے تو میں نے وہ کہا نا کہ اسپیشل کیس ہے تو ایک الگ چیز ہے تو آپ کا اسپیشل کیس ہو گیا ٹھیک ہے صرف سیم ڈے اگر میں سر مجھے صرف مجھے تو یاد نہیں ہے مجھے صرف رات کا یاد ہے اگلے دن بھی یاد

**[B:273]** Speaker 1:  نہیں اوکے تو اٹس اے جنرل تھنگ ابھی آپ نے لاسٹ ویک میں ہی تو کیا اور آپ کے ساتھ ہی ایونٹ ہوا ہے لیکن آپ بھول گئے کیوں بھول گئے کیونکہ دس از اے ٹیمپرری کیونکہ ہمارے پاس دو طریقے کی ہمارے دماغ میں بھی دو طریقے کی میموری ہے ایک پرماننٹ میموری ہے اور ایک ٹیمپرری میموری ہے جیسے سسٹم کے اندر ہوتی ہے تو پرماننٹ میموری مطلب ہارڈ ڈسک ہو گئی اور ٹیمپرری میموری مطلب ریم ہو گئی تو جو آپ کے مطلب کی چیز ہے جیسے اگر

**[B:274]** Speaker 1:  میں آپ سے پوچھوں کہ سر ایڈریس کیا ہے آپ نے بھلے ہی دس سال پہلے گھر خریدا ہو لیکن آج بھی اگر آپ کا ایڈریس وہی ہے آپ امیڈیٹلی بتا دو گے ورغاں میرے گھر کا ایڈریس یہ ہے لیکن اگر میں آپ سے پوچھ رہا ہوں ویڈنس ڈے میں کیا کھایا تھا آپ کو یاد نہیں ہے کیونکہ وہ ٹیمپرری میموری میں ڈیٹا اسٹور تھا کھایا پیا پیٹ میں چلا گیا دیٹس اٹ بات ختم تو سیم تھنگ سرور کے ساتھ بھی ہے تو سرور میں بھی جو ہم

**[B:275]** Speaker 1:  ٹیمپرری کام کر رہے ہیں جیسے آپ نے کوئی فائل کھولی اس میں کچھ کام کرنا چالو کیا تو جب تک کام کر رہے ہیں وہ سکرین پہ دکھ رہا ہے لیکن ان ایکسپیکٹڈ کمپیوٹر پاور آف ہو گیا تو وہ ریم میں ڈیٹا اسٹور تھا ریم سے وائپ آؤٹ ہو جائے گا جب ریبوٹ ہو جائے گا حالانکہ آج کے ٹائم میں کافی سارے ایپلیکیشنز اس طریقے کے بنائے جا رہے ہیں یا الریڈی بن چکے ہیں ایون آپ ورڈ کو بھی جب پاور آن کرو گے تو اس میں

**[B:276]** Speaker 1:  بھی ایک کیس ایسا آتا ہے لاسٹ نون گڈ کنفیگریشن ریکوری فائل آپ کلک کرتے ہو ان میں سے کسی ایک پہ پتہ لگا جو بند ہونے سے پہلے فائل تھی وہی کھل گئی ارے بچ گیا یار میں سیو نہیں کری تھی تو کئی بار ایسا ہو جاتا ہے کیوں وہ اس لیے ہو گیا کہ آپ کا سرور ریبوٹ ہوا تھا پاور آف نہیں ہوا تھا لانگ ٹائم کے لیے کیونکہ جب ہم سرور کو پاور آف بھی کرتے ہیں تو آن این ایوریج اس ہارڈ ویئر کے اندر

**[B:277]** Speaker 1:  ایک ٹیکنالوجی ہے کہ جو میموری کے اندر ڈیڑھ منٹ یعنی کہ اس کو اگر ہم سیکنڈز میں کچھ کاؤنٹ کریں تو لگ بھگ ڈیڑھ منٹ کا ٹائم نکلتا ہے ڈیڑھ منٹ تک آپ کی میموری میں ڈیٹا اسٹور رہتا ہے افٹر شٹنگ ڈاؤن یور کمپیوٹر آپ اگر دیکھو گے آپ نے پاور آف کیا یہاں لائٹ بند ہو گئی آپ اس کا بجلی میں سے تار نکال دو اور واپس لگا کر سرور کو آن کرو گے تو ڈیڑھ منٹ کے اندر اندر اگر آپ نے پہلے ہی سرور میں

**[B:278]** Speaker 1:  واپس بجلی کنکشن دے کے کنیکٹ کر لیا ہے تو یو کین ریسٹور یور ڈیٹا ٹو تو ریم میں جو ڈیٹا تھا وہ وائپ آؤٹ نہیں ہوا ڈیڑھ منٹ بعد ہوگا سو سیکیورٹی کے پروسپیریس بھی اگر ہم دیکھیں زیادہ تر آہ کچھ ایسے گیجٹس بھی آتے ہیں یو ویل ناٹ بیلیو اینڈ آئی اگین آئی ایم ناٹ آہ مطلب یہ تھریٹس نہیں ہیں کائنڈ آف سو کافی سارے ایسے ایکوپمنٹس آتے ہیں جب کبھی ہم ڈیٹا سینٹر لیول پر اٹیک کرتے ہیں اٹیک مطلب میں ڈیٹا سینٹر میں کسی میں

**[B:279]** Speaker 1:  گھس گیا انٹری کری میں نے توڑا فاڑی کری سرور نکال لیا اور نکال کے میں نے سب سے پہلا کام کیا اس کے جو کیبنٹ کا اوپر کا کور ہے وہ ہٹایا اس کی ریم کے اوپر میں ایک اسپرے آتا ہے وہ اسپرے میں اگر چھڑک دیتا ہوں تو دیٹ میموری ویل فریز اگر میں اس ریم کو نکال بھی لوں گا اور اس کے بعد جب تک دوسرے ڈیوائس میں لگا کر چلاؤں گا نہیں وہ وہیں پہ ہولٹ پڑی ہے پھر ڈیڑھ منٹ کا ٹائمر بھی کاؤنٹ

**[B:280]** Speaker 1:  نہیں کرتی اس طریقے کے گیجٹس بھی مارکیٹ میں اویلیبل ہیں سو جو اٹیکرز ہیں اٹیکرز مطلب جو چوری چکاری کا کام کرتے ہیں جو اس بڑے لیول پہ کام کرتے ہیں گینگ وینگ کام کرتے ہیں اس طریقے کی چیزیں بھی یوز کرتے ہیں اینڈ آل دا انفارمیشنز آر اویلیبل ان یور ڈارک ویب سائٹس اور ادر ویب سائٹس اگر آپ سیکیورٹی کے اندر اس طریقے کے آرٹیکلز کو پڑھتے ہو تو کافی ساری چیزیں آپ کو ایسے دیکھنے کو ملتی ہیں تو کبھی کبھی فری ٹائم کے اندر آئی

**[B:281]** Speaker 1:  ٹرائی ٹو ریڈ دا نیو تھنگز کی نئی چیزیں کیا ہو رہی ہیں تو نئی چیزیں جاننے میں میرے کو اور زیادہ مزہ آتا ہے جیسے وین آئی واز کڈ تو ہم لوگوں کا جو ایریا تھا یا ہم لوگ جس طریقے سے بات کرتے تھے دیٹ واز اے ڈفرنٹ تھنگ آج کے ٹائم میں اگر ہم دیکھیں نئے کسی بچے کو اگر آپ پکڑیں اسی ایج کا لائک میں بات کر رہا ہوں اگر میں بارہ تیرہ سال کا تھا آج کے ٹائم میں اگر بارہ تیرہ سال کے بچے

**[B:282]** Speaker 1:  سے بات کرو ہی ویل ٹاک ان اے ڈفرنٹ وے تو اس سے جب بات کرو گے وہ اپنے دوستوں سے الگ سلیگ لینگویج میں بات کر رہا ہے اس کے الگ کی ورڈز ہیں وہ الگ چیزوں پہ لے کے کام کر رہا ہے یا آپ کے ٹائم پہ ہو سکتا ہے کہ آپ کمپیوٹر کو پسند کرتے تھے آپ ٹی وی کو یا کیبل ٹی وی کو پسند کرتے تھے آج کے ٹائم پہ انٹرنیٹ اویلیبل ہے وہ بتا دے گا آؤٹ آف کنٹری کے اندر بھئی آئی لیو

**[B:283]** Speaker 1:  بی ٹی ایس وہ یہ بھی کہہ سکتا ہے ہمیں پتہ بھی نہیں تھا بی ٹی ایس کیا ہے کیونکہ وین آئی واز کڈ مجھے یاد ہے کہ میرے ٹائم پہ کامکس آتی تھی اینڈ آئی لو کہ وہ ناگ راج کی کامکس آ گئی یا چاچا چوہدری کی کامکس آ گئی یا کچھ اور کامکس آ گئی وہ دیٹ واز مائی ایرا بٹ ابھی والے ایرا کے اندر جائیں گے دے ڈونٹ لو دا کامکس دے لو آڈیو ریکارڈنگ آڈیوز اور ویڈیوز وہ وہاں سے دیکھیں گے سنیں گے اور

**[B:284]** Speaker 1:  اس کو مزہ آ رہا ہے اور وہ وہ چیزیں دیکھ رہے ہیں سو دے آر لیونگ ان دیر ڈفرنٹ لائف تو ہر ایرا کے اندر کچھ کچھ چیزیں چینج ہو جاتی ہیں تو سیکیورٹی کے پروسپیریس بھی وین آئی گیٹ دا فری ٹائم کبھی کبھی ایسا نہیں مطلب یہ فری فری کا مطلب یہ ہے کہ چھ مہینے میں یا سال بھر میں میرے کو ایک آدھی ٹریننگ کے پروسپیریس کچھ نئی چیز سیکھنی ہے جو میں ٹریننگ کے اندر بول سکوں تو میں کبھی کبھی دیکھ لیتا ہوں تو

**[B:285]** Speaker 1:  چھ مہینے میں سال بھر میں ایک دو بار میں اپنے آپ کو تھوڑا سا اپ گریڈ کر لیتا ہوں اس پروسپیریس کیونکہ سیکیورٹی کے اندر اپورچونیٹیز مجھے تھوڑی سی کم ملتی ہے چاہے وہ ٹریننگ ہو گئی یا ڈیٹا سینٹر کے اندر امپلیمنٹیشنز ہو گئے تو سیکیورٹی والا پارٹ شاید مجھے اس طریقے کی اپورچونیٹی نہیں ملتی زیادہ تر یا میں اپنے جو خود کے پرسنل پروجیکٹس بھی کرتا ہوں ان پروجیکٹس کے اندر بھی اس طریقے کی شاید میرے کو اپورچونیٹیز نہیں مل پاتی تو میں وہاں تھوڑا سا

**[B:286]** Speaker 1:  ایبسولیوٹ ہوں بٹ اسٹل تھوڑی بہت آئیڈیا ہے کہ کیا کیا چیزیں چلتی ہیں ٹھیک ہے خیال آ رہا ہے ہاں جی آہ جو آپ کے لیکچرز ہیں یا جیسے یہ ابھی آپ نے بایوس کا پڑھایا یا کوئی بھی ٹاپک ہو گیا کیا جی آپ آہ اس پہ کوئی ایکسرسائز کریٹ کر سکتے ہیں تاکہ ہو جائے چیٹ جی پی ٹی سے بولیں یا اس سے بولیں جیسا مناسب سمجھیں آپ کے پاس ٹائم آپ اے آئی اے آئی ٹول سے اگر آپ ہیلپ لو گے دیٹ وڈ بی گڈ

**[B:287]** Speaker 1:  کیونکہ اس کے لیے لیب وغیرہ یا کچھ ایسا پروسیجر تو ہے نہیں کہ ہم دیکھ سکیں یا کچھ کر سکیں سو اے آئی ٹول کین گائیڈ یو کہ کیا اس میں ہم اور چیزیں نکال کے دیکھ سکتے ہیں ادر وائز نتھنگ از دیر اینڈ آئی ویل سجیسٹ انٹرویو کی پروسپیریس یہ بوٹنگ پروسیس اتنا ہے آپ اسے اتنے ہی طریقے سے رکھیں زیادہ ڈیپ ڈرائیو بھی مت جائیں کیونکہ انٹرویوور اگر ہم ان جنرل لینگویج بات کریں سیلری وہ اتنی دے گا جو الریڈی پلان کر کے بیٹھا ہے

**[B:288]** Speaker 1:  وہ وہ نہیں دے گا جو آپ ڈیمانڈ کرو گے تو اس میں وہ بارگین کرے گا ہی کرے گا ٹھیک ہے تو دوسرے کو کےवल اتنی انفارمیشن دینی ہے جتنی وہ ہمیں پے کر رہا ہے اس سے زیادہ نہیں دینی ہے الویز کیپ دس تھنگ دوسرا انٹرویو کئی بار آپ کو ہائرنگ کرنے کے لیے نہیں لیا جاتا ہے کئی بار کیسز کے اندر یہ ہوتا ہے کہ کمپنی کے اندر کچھ ایشوز آ رہے ہیں اینڈ وہ ایشوز فکس کرنے کے لیے دے آر ناٹ ٹیکنگ ا ٹیکنیکل

**[B:289]** Speaker 1:  ہیلپ فرام دا کمپنیز یعنی کہ مائیکروسافٹ یا لینکس یا کسی اور سے ہیلپ نہیں لے رہے لیٹس سپوز یو آل گائز آر دا ڈفرنٹ ڈفرنٹ ٹیم پلیئرز تو کوئی ونڈوز کا ایکسپرٹیز ہے کوئی لینکس کا ہے کوئی ڈی بی کا ایکسپرٹ ہے کوئی سیکیورٹی کا ایکسپرٹ ہے کچھ کچھ ایشوز چل رہے ہیں کمپنیز میں میں نے ایک ہائرنگ نکال دی اور ہائرنگ کے اندر میں آپ سے پوچھ رہا ہوں اور ہائرنگ بھی میں نے اسی لیول کی دے دی کہ مجھے ایل تھری ریکوائرڈ ہے یا ایس

**[B:290]** Speaker 1:  ایم ایز ریکوائرڈ ہے تو وہی بندے آئیں گے ایل ون ایل ٹو تو آئیں گے نہیں تو اب جب آپ آؤ گے آپ پوچھو گے آپ اپنے بارے میں بتاؤ گے یا میں آپ سے پوچھوں گا ڈے ٹو ڈے ایکٹیویٹی کیا کرتے ہو اچھا مجھے پھر امیڈیٹلی میں آپ سے پوچھ لوں گا اچھا اس طریقے کا کچھ ایشو آیا کبھی آپ نے فیس کیا کیا سولیوشن نکالا تو اگر آپ نے وہ ایشو سالو کر دیا یا آپ نے وہ ایشو اس طریقے کا دیکھا ہوا ہے الریڈی

**[B:291]** Speaker 1:  سالو کر رکھا ہے تو اسے اس کا انسر مل گیا سو دے آر ناٹ ہائرنگ یو سم ٹائم اٹ ہیپن دے آر اسکنگ دا ٹیکنیکل تھنگز فرام یو ان کی ایکسپیکٹیشنز اتنی ہیں اور دوسرا سب سے بڑا گول کئی بار جو بڑی بگ کمپنیز ہیں ان کا گیم یہ ہوتا ہے کہ دے سیز کی آج لیٹس سپوز کوئی بھی ایک برانڈ آئی ایم ناٹ ٹیکنگ انڈیویجول کئی بار ایسا بھی ہوتا ہے کہ ان کا ٹارگٹ یہ ہوتا ہے سوشل میڈیا پلیٹ فارمز پہ یہ دکھانا کہ ہم

**[B:292]** Speaker 1:  نے لیٹس سپوز 120 لوگوں کی ہائرنگ تھی ہمارے پاس آج کیونکہ یہ واک ان انٹرویو تھا تو 120 کی جگہ ہمارے پاس آج ساڑھے تین ہزار پانچ ہزار آٹھ ہزار ایمپلائیز آئے ہیں اس رول کے لیے تو وہ ورلڈ پہ نمبر دکھانا چاہتے ہیں کہ دیکھو ہمارا برانڈ اتنا بڑا ہے اینڈ دیز گائز آر کمنگ دیٹس السو ریزن تو اس لیے کئی بار زیادہ ڈیپ ڈرائیو بھی نہیں جانا اور زیادہ چیزوں میں نہیں پڑنا اپنے آپ کو سیفر سائیڈ بھی رکھنا ہے اینڈ آگے میں آپ کو

**[B:293]** Speaker 1:  بتاؤں گا کہ انٹرویو کے اندر کئی بار کچھ چیزوں میں اگر ہم زیادہ اچھے نہیں ہیں تو کیسے اپنے آپ کو دوسرے سیکشن میں ری ڈائریکٹ کر سکتے ہیں ٹھیک ہے تو ہمارے جیسے جیسے سیشنز بڑھتے چلے جائیں گے سو ڈیفینیٹلی وی ویل ڈسکس دیٹ تھنگ ٹو کیونکہ ایسا نہیں ہے کہ میں آپ کو سرور کے اندر اتنی ساری چیزیں پڑھاؤں گا تو آپ ہر ایک ٹاپک کے اندر پرفیکٹ ہو جائیں دیٹ وڈ ناٹ بی پوسیبل شاید میں بھی ہر ایک کریکلم کے اندر اتنا زیادہ اچھا

**[B:294]** Speaker 1:  نہیں ہوں میرا وہ اچھا آپ لوگوں کو شاید اس لیے اچھا لگے گا کہ میں آپ کو کریکلم کرا رہا ہوں آپ کو لگے گا ہاں یہاں پر بھی نالج سیم ہے لیکن کافی ساری چیزیں تو ایسی ہوں گی نا مجھے پتہ ہے کہ میرے اینڈ پہ وہ کیا چیزیں ایسی کمیاں ہیں یا جہاں پر سب سے زیادہ پرابلمز ہیں تو ایسے کیس کے اندر مجھے پتہ ہے کہ انٹرویوور کو کس طریقے سے گائیڈ کرنا ہے یا کس طریقے سے اسے بتانا ہے کہ بھیا آپ نے

**[B:295]** Speaker 1:  یہ نہیں پوچھنا یہ پوچھو یہاں سے یہ یہ والا سیکشن پوچھنا ہے ان کے ساتھ ہمیں پلے کرنی ہے وہ چیز تو دیٹ تھنگ السو وی ویل ڈسکس ڈے ٹو ڈے جیسے ہم لوگوں کی اب کلاسز چلتی چلی جائیں گی تو وی ویل ڈسکس دیٹ تھنگ ٹو رائٹ کلیئر کلیئر آئی ہوپ کی میں نے زیادہ بور نہیں کیا ہوگا آج کے سیشن میں بالکل زبردست زبردست ٹھیک ہے سو آج پھر ہم اس میں اتنا ہی رکھیں گے لیکن کمنگ ویک کے اندر اف کورس کہ ہم لوگوں

**[B:296]** Speaker 1:  کی لیبز اسٹارٹ ہو رہی ہیں اینڈ ون مور سلائیڈ آئی ویل پٹنگ اوور ہیر ٹو سلائیڈز ناٹ ون سلائیڈ ون سلائیڈ الریڈی آئی ہیو پٹڈ اوور ہیر ان اور ون ڈرائیو جسٹ ا سیکنڈ اور سر نیکسٹ ویک والی بھی سلائیڈ دے دیں گے ہاں ہاں سر وہ الریڈی میں نے دے دیا ابھی ونڈوز بوٹ تو ہے ایک میں نے اور سلائیڈ رکھا ہے ابھی ونڈوز فائل سسٹم اس کو ہم پڑھنے والے ہیں دس از ا تھیوریٹیکل سیکشن حالانکہ لیب بھی ہے تو لیب میں بھی دیکھیں گے

**[B:297]** Speaker 1:  کہ کیسے اس کے ساتھ کام کرنا ہے اس کے ساتھ ساتھ ایک اور چیز ہے وچ از ورگروپ اور ڈومین وہ ابھی میرے پاس یہاں ہینڈ ہی نہیں ہے میرے لیپ ٹاپ میں ہے سو آئی ویل اوپن دیٹ لیپ ٹاپ اینڈ ویل پلیس اوور ہیر تو دیٹ از ورگروپ اور ڈومین کیا ہوتا ہے وہ ہم نے پڑھنا ہے ٹھیک ہے تو آئی ویل سجیسٹ آپ کے لیے تین چار کام ہو گئے ہیں ابھی کمنگ ویک اینڈ کے لیے سو سب سے پہلا کام ہاں جی آپ کی

**[B:298]** Speaker 1:  کوئی کوئری ہے تو پہلے آپ پوچھ لو پھر میں بتا دیتا ہوں کیا کیا ہمارے ٹاسک لسٹ تھوڑا سا روڈ میپ سمجھا دیں اگر آپ اگر آپ مناسب سمجھتے ہیں تو سر ابھی ابھی کمنگ ویک کا اور ٹائم دو میرے کو پھر میں اپنے آپ ہی آپ کو پہلے ہی بتا دوں گا کہ ہم کمنگ ویک میں یہ ٹاپک کرنے والے ہیں اچھا ٹھیک ٹھیک ٹھیک ہے ابھی انیشلی آئی ایم ٹرائینگ کہ میں کچھ بیسک سے ایڈوانس کی طرف جاؤں گا تو بیسک فنڈامینٹلز لے کے آپ

**[B:299]** Speaker 1:  کے سرورز کو کچھ رولز ایسے ہیں جو بیسک بیسک میں میں کور اپ کر لوں تو ابھی ہمارا جو کمنگ ویک بھی آئے گا دیٹ وڈ بی ان بیسک اینڈ آئی ویل سجیسٹ کہ مطلب اگر ایسا نہیں ہے کہ اٹس ا آئی سیڈ کہ اٹس ا ایٹ ویک کلاس تو مطلب دو مہینے کا ہمارا ٹائم ڈیوریشن ہے تو اٹ وڈ ناٹ ریمین فکس ہم اگر ریکوائرمنٹ پڑی تو ہم ایک ہفتہ یا دو ہفتہ ایکسٹینڈ کر سکتے ہیں یا پہلے ہو گیا میں نے فٹافٹ سے جلدی کرا

**[B:300]** Speaker 1:  دیا یو ریکوائرڈ دا پریکٹس یا یو ہیو دا سم کوئریز سو ہم وہ کوئریز بھی کر لیں بٹ اٹ از ناٹ وی آر ناٹ سٹنگ ان فاسٹ ٹیک کورس کریکلم کہ ہم نے فٹافٹ سے کمپلیٹ کرنا ہے اور بائے بائے ڈیٹا کر دینا ہے نو سو وی آر سٹنگ ٹو لرن سمتھنگ رائٹ سو اگر ہمیں ریکوائرڈ ہوئی تو ہم کورس کو ایکسٹینڈ بھی کر سکیں گے رائٹ بہت بہت شکریہ رائٹ سو ابھی انیشلی ابھی اس ویک کے اندر آپ لوگوں کا جو سب سے پہلا ٹارگٹ ہے

**[B:301]** Speaker 1:  وہ ٹارگٹ یہ ہے کہ آپ کو اپنے لیپ ٹاپ ڈیسک ٹاپ پہ وی ٹی کی سروس کو یعنی کہ ورچولائزیشن ٹیکنالوجی کو انیبل کرنا ہے وی ایم ویئر ورک اسٹیشن کو انسٹال کرنا ہے وی ایم ویئر ورک اسٹیشن میں آپ لوگوں کو دے چکا ہوں اور آپ لوگوں کو بتا چکا ہوں کہ اسے کیسے ڈیپلائے کرنا ہے نہیں پتا اگین آئی تھنک میں شاید کل مس کر گیا میں اپنے وہ پلے لسٹ کو شیئر نہیں کر پایا اوور دا واٹس ایپ میں آج ابھی وشال کو بول

**[B:302]** Speaker 1:  دوں گا ہی ویل شیئر ال دا کمپلیٹ تھنگز تو وہ آپ کو پلے لسٹ سیکشن میں شیئر کرے گا کہ کس طریقے سے وی ایم ویئر ورک اسٹیشن کے ساتھ کام کرتے ہیں اور وی ایم ویئر ورک اسٹیشن آپ اپنے نیٹ ورک میں یا اپنے ڈیسک ٹاپ پہ انسٹال کر سکتے ہیں تو یوٹیوب پہ الریڈی وہ پلیسڈ ہے وہاں سے آپ سیکشن کو گو تھرو کر سکتے ہیں اینڈ وہاں پر میں ون تھنگ کہوں گا کہ اگر آپ کو وہ سیکشن اچھا لگتا ہے تو آپ اسے

**[B:303]** Speaker 1:  لائک کر کے کمنٹ ضرور کر دیجئے گا اٹ وڈ بی گڈ تھنگ حالانکہ کافی سارے کیسز کے اندر میں خالد جی کے کمنٹس دیکھتا ہوں وہاں بھی کافی سارے کمنٹس آ رہے ہیں ایون پوسٹ پہ بھی کمنٹس آتے ہیں سو مائٹ بھی ہو سکتا ہے کہ وہ پوسٹ واقعی میں انہیں پسند آتی ہے یا مائٹ بھی کہ وہ ورگانگ کو لائک کرتے ہیں تو شاید ورگانگ کے ایفرٹس کو وہ وہاں پہ دونوں باتیں ہیں سر دونوں باتیں ہیں ٹھیک ہے تو کچھ وہ چیزیں ہیں بٹ سیم

**[B:304]** Speaker 1:  تھنگ آئی ویل ٹرائی ٹو ٹیک ا ہیلپ فرام یور سائیڈ کہ اگر آپ کو ویڈیو سیشنز واقعی میں اچھے لگ رہے ہیں یو کین پٹ ا کمنٹ اور اگر سیشن میں لگتا ہے کہ کچھ اور چیزیں مسنگ ہیں نوٹ ڈاؤن کر لو آپ وہ سیشن سر وہ میرے کو بتاؤ میں اس پہ دوبارہ ری سیشن کریٹ کروں گا رائٹ رائٹ رائٹ سو وہ میرے لیے بھی ہیلپ نہیں نہیں بہت بڑی بات ہے آپ آپ جس طرح چل رہے ہیں چلتے رہیے اپنے آپ کو اتنا ٹینشن میں

**[B:305]** Speaker 1:  مت لیجئے بس جس طرح آپ پڑھا رہے ہیں پڑھائیے جو آپ کے اندر فلو ہے ہم اس سے فائدہ اٹھائیں اٹھائیں گے پورا آپ استاد ہیں آپ چلتے رہیے جس طرح چلنا ہے ہم لوگ ہاتھ دھوئیں کھانا کھاتے ہیں سو میں واپس ایک بار ٹاسک کی ٹو ڈو لسٹ بنا لیتا ہوں تو ٹاسک کی ٹو ڈو لسٹ میں ہمیں سب سے پہلے وی ایم ویئر ورک اسٹیشن انسٹال کرنا ہے الریڈی میں آپ لوگوں کو شیئر کر چکا ہوں اسے ڈیپلائے کرنا ہے اگر آپ نے لیپ ٹاپ

**[B:306]** Speaker 1:  میں انسٹال نہیں کیا ہے تو دوسرا کام ونڈوز او ایس انسٹال کرنا ہے آپ کو یہ ونڈوز سرور 2000 میں نے آپ کو 19 بھی دیا ہے اینڈ 22 بھی دیا ہے آئی ویل سجیسٹ کہ دونوں ہی ڈیپلائے کرو اور کل آج تو نہیں میں کمٹمنٹ کر رہا کل آپ کو لینز سے پہلے پہلے 2025 کی آئی ایس او امیج بھی مل جائے گی آپ وہ بھی یوز کر سکتے ہیں بٹ 25 پہ تھوڑا سا ہم لیب کم کریں گے ریزن بینگ مائٹ بھی ہو سکتا ہے

**[B:307]** Speaker 1:  کہ میرے سسٹم پہ وہ ایشوز کرتا ہو میرے سسٹم پہ مطلب جب وی ایم ویئر ورک اسٹیشن کے اندر ہم لیب کرتے ہیں تو کبھی کبھی وہ لیک کر جاتا ہے کبھی کبھی وہ ہنگ اسٹیٹ میں آ جاتا ہے فزیکلی اگر آپ اسے یوز کرتے ہو اٹ از پرفیکٹلی فائن تو وی ایم ویئر ورک اسٹیشن میں میرے سسٹم پہ ایشوز کرتا ہے آپ ایک بار ٹرائی کر کے دیکھ لو اگر آپ کے سسٹم پہ وہ ایشو نہیں کرتا ہے ہنگ نہیں اس سٹیٹ میں ہوتا ہے جیسے

**[B:308]** Speaker 1:  آپ نے کام کر رہے ہو تھوڑی دیر کے لیے سسٹم کو وی ایم ویئر ورک اسٹیشن کو منیمائز کیا واپس ان کر کے جب دیکھ رہے ہو وہ اگر ہنگ اسٹیٹ میں نہیں آ رہا پرفارمنس اوکے کر رہا ہے تو آپ اس پہ کام کر سکتے ہو میرے سسٹم پہ اس طریقے کا ایشو آتا ہے آئی ہیو ابزروڈ دس اس لیے 2025 کو میں تھوڑا کم لیتا ہوں اور اگر لیتا ہوں تو میں ابھی انسٹالیشن کر کے رکھوں گا اور انسٹالیشن کے بعد مطلب جیسے آپ کو

**[B:309]** Speaker 1:  آج پڑھانا ہے تو میں انسٹالیشن کر کے رکھوں گا اس پہ لیب کرا دوں گا آپ کو لیب کرا کے پاور آف کر دوں گا میں پھر زیادہ پنگے نہیں کرتا اس کے ساتھ کہ وہ ہنگ اسٹیٹ پہ آئے ٹھیک ہے تو کچھ وہ چیزیں بھی ہیں بٹ 2025 بھی آئی ویل ٹرائی میں آپ کو کل لنچ سے پہلے پہلے دے دوں گا تو آپ کا ورک ہوگا کہ آپ نے 2019 2022 اینڈ 2025 دو یہ تینوں او ایس آپ نے اپنے وی ایم ویئر ورک اسٹیشن

**[B:310]** Speaker 1:  میں انسٹال کر کے رکھنے ہیں صحیح ہے سر میں میں آپ کو دو دن کے اندر یہ ہوم ورک کر کے دکھا دوں گا انشاءاللہ ٹھیک ہے کمپلیٹ سو اگلی چیز ونڈوز 11 کی بھی میں نے آپ کو ایک امیج دی ہے آئی ویل سجیسٹ کہ ونڈوز 11 بھی انسٹال کر کے رکھیں ایک ورچول مشین کم سے کم میں یہ نہیں کہہ رہا کہ دو بناؤ ایک کم سے کم بنا کر رکھ لیجئے گا بیکاز آنے والی کمنگ کلاس کے اندر ہمیں ونڈوز 11 کی بھی ضرورت

**[B:311]** Speaker 1:  پڑے گی حالانکہ وہ سارا کام ہم سرور پہ بھی کر سکتے ہیں بٹ آئی ویل سجیسٹ کہ کلائنٹ پہ اگر دکھاؤں گا تو اٹ وڈ بی مور گریس فل کیونکہ وہ کلائنٹ کے لیے بھی چیزیں بنی ہیں تو ہمیں وہ چیزیں پتہ لگ پائے سرور کے لیے تو ہمیں سارے فیچرز ملے ہی ہیں سرور میں تو سارے وہ فیچر جو کلائنٹ او ایس میں آ رہے ہیں وہ سرور میں ہیں ہی وہ ہو سکتا ہے منیمم اس سے زیادہ ہی فیچرز ہمارے پاس لوڈڈ ہیں تو اس

**[B:312]** Speaker 1:  لیے سرور کی چیزیں سرور میں کریں گے ایک دو چھوٹی چیزیں ہیں جو کلائنٹ کی ہیں وہ کلائنٹ میں کریں گے رائٹ تو کلائنٹ او ایس بھی آپ ڈیپلائے کر کے رکھیں تو یہ چار مشینز آپ اپنے لیپ ٹاپ یا ڈیسک ٹاپ پہ انسٹال کر کے رکھ لیجئے گا نیکسٹ ٹاسک آپ کا کیا ہے آپ کو نیکسٹ ٹاسک یہ کرنا ہے کہ جو میں نے آج آپ کو ایک تو ابھی بوٹنگ پروسیس کرایا ہے اس بوٹنگ پروسیس کو کرنے کے لیے مطلب آپ کو یہ سمجھنے کے

**[B:313]** Speaker 1:  لیے یہ جو آج کا سیشن ہے اسے آپ واپس ایک بار ریفرل ضرور کر لیجئے گا اور اسے ریفرنس کو لے کر آپ کو جو جو چیزیں سمجھ میں آ رہی ہیں وہ کہیں نوٹ ڈاؤن ضرور کر لینا کچھ سٹیپس نوٹ ڈاؤن کر لینا یہ یہ والے سٹیپس مت نوٹ ڈاؤن کرنا سر یہ جو میں نے بنایا ہے یہ نہیں کچھ بیسک جو آپ کے دماغ میں کی ورڈز یا سمری جو نکل کر آ رہی ہے کہ سر بوٹنگ پروسیس میں میجرلی یہ کام ہوتے ہیں تو

**[B:314]** Speaker 1:  وہ سمری آپ رکھ لیجئے گا کیونکہ میں رینڈملی مائٹ بی کہ کسی سے بھی پوچھ سکتا ہوں کہ یہ کیا ہوتا ہے یا کیا سمجھ میں آیا تھا آپ کو ٹھیک ہے تو پلیز ڈونٹ سے کہ سر پورا ویک اینڈ میرا بہت زیادہ بزی نکل گیا آئی نو کہ آپ کے ویک اینڈز یا ورک ڈیز بھی بزی جا سکتے ہیں اف کورس بٹ پلیز کوشش کیجئے گا کہ پورے ویک میں تھوڑا سا ٹائم نکال لو آپ ٹھیک ہے یہ 15 سے 20 منٹ لے گا آپ کا

**[B:315]** Speaker 1:  ٹوٹل تو ریکارڈنگ شاید زیادہ بڑی ہو سکتی ہے لیکن سمری بنانے کے لیے 15 سے 20 منٹ لے گا جس میں آپ سمری بنا لیں تو ونڈوز بوٹنگ پروسیس بہت زیادہ امپورٹنٹ ہے اور سمری بنوانے کا ایک ریزن یہ ہے کہ آپ نے اگر ایک بار سمری بنا لی تو آئی ایم ڈیم شور کہ آپ انٹرویوور کو انسر کر سکتے ہیں اور یہ ایک اکیلا ایک ایسا کوئسچن ہے اگر میں کہوں کہ 100 نمبر کا ایگزام ہے تو 25 نمبر کا اکیلا یہ کوئسچن ہے آپ یہ

**[B:316]** Speaker 1:  سمجھ لو رائٹ تو یہ اس طریقے کا کوئسچن ہے یہ 25 نمبرز کا کوئسچن ہے تو یہ اگر ہمیں آ گیا اچھے سے تو ہم آگے کے انسرز ایزیلی کر لیں گے آگے کے ہو سکتا ہے پتہ ہے لگا میں آپ کو زیادہ تر کہہ دوں کہ یہ سارے ایک ایک نمبر کے ہیں یہی اکیلا 25 نمبر کا تھا تو ایسا بھی ہو سکتا ہے بٹ ٹرولی یہ سب سے مہنگا کوئسچن ہے آپ کا رائٹ بوٹنگ پروسیس کے بعد میں نے دو سلائیڈز دی ہیں آپ کو

**[B:317]** Speaker 1:  ایک فائل سسٹم ٹھیک ہے ونڈوز کا فائل سسٹمز کیا کیا ہے اس کی ایک سلائیڈ دی ہے اور ایک انوائرمنٹ یعنی کہ ہمارا ورک گروپ اینڈ ڈومین کیا ہوتا ہے اس کے بارے میں ہم بات کریں گے اور پھر ہم اپنی کلاس کو کریں گے ٹھیک ہے تو یہ آپ کی ٹو ڈو لسٹ ہے یہ ٹو ڈو لسٹ میں ابھی ہمارے ون ڈرائیو میں پیسٹ بھی کر دوں گا ٹھیک ہے تو دیٹس ا تھنگ اب کسی کا کوئی کوئری ہے تو آپ پوچھ سکتے ہیں سر کوئی

**[B:318]** Speaker 1:  ہے سر کسی کی کوئری نہیں سر بالکل کوئی کوئری نہیں ہے بہت بڑھیا اوکے تھینک یو ویری مچ ٹھیک ہے پھر آج کا سیشن سر ہم اتنا ہی رکھنے والے ہیں کمنگ ویک میں ہم چیزیں سٹارٹ کریں گے اپنی اور لیب زیادہ ہوگی اگلے ویک کے اندر ہماری اف کورس کیونکہ ابھی جو ہم تھیوریٹیکل سیکشنز دیکھتے جا رہے ہیں وہ تھیوری ہماری الموسٹ دھیرے دھیرے کمپلیٹ ہوتی جا رہی ہے بٹ آگے ہمارے مکس اپ سے سیشنز چلیں گے تھوڑی تھیوری تھوڑی لیبز اس طریقے سے ٹھیک ہے

**[B:319]** Speaker 1:  تو کچھ ہی چیزیں ہیں تو آج اتنا ہی رکھتے ہیں تھینک یو سو مچ سر فار یور ٹائم دھنیوا دھنیوا تھینک یو یور ڈے ٹیک کیئر یو ٹو سر تھینک یو گڈ نائٹ گڈ نائٹ تھینک یو ویری مچ تھینک یو