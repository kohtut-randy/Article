# V8 (JavaScript engine)

V8 သည် Google Chrome နှင့် Chromium ဝဘ်ဘရောက်ဆာများအတွက် Chromium ပရောဂျက်မှ ဖန်တီးထားသော free and open-source JavaScript အင်ဂျင်တစ်ခုဖြစ်သည်။

V8 အင်ဂျင်၏ first versionကို Chrome ၏ first version နှင့် 2 Sept 2008 တချိန်တည်းတွင် ဖြန့်ချိခဲ့သည်။

Couchbase နှင့် Node.js တို့တွင်လည်း ၎င်းကို server site တွင် အသုံးပြုထားသည်။

### History

V8 assembler သည် Strongtalk assembler ကို အခြေခံထားသည်။ 7 ဒီဇင်ဘာ 2010 တွင် Crankshaft ဟု အမည်ပေးထားသည့် a new compiling infrastructure ကို အရှိန်မြှင့်တင်ကာ ထုတ်ဝေခဲ့သည်။

2015 ခုနှစ် Chrome ၏ version 4.1 တွင်၊ asm.js ကဲ့သို့သော အလုပ်များနှင့်အတူ ပိုမိုစွမ်းဆောင်ရည် မြှင့်တင်ပေးရန်အတွက် ပရောဂျက် TurboFan ကို ထည့်သွင်းခဲ့သည်။

2016 ခုနှစ်တွင်၊ TurboFan နှင့် Crankshaft တို့နှင့် နှိုင်းယှဉ်ကာ အသေးစားမှတ်ဉာဏ် Android ဖုန်းများတွင် memory အသုံးပြုမှုကို လျှော့ချရန် ဒီဇိုင်းရည်ရွယ်ချက်ဖြင့် Ignition စကားပြန်ကို V8 သို့ ပေါင်းထည့်ခဲ့သည်။

Ignition သည် register based machine တစ်ခုဖြစ်ပြီး HotSpot မှအသုံးပြုသော template interpreter သို့ အလားတူ (အတိအကျမဟုတ်သော်လည်း) ဒီဇိုင်းကို မျှဝေပါသည်။

2017 ခုနှစ်တွင် V8 သည် Ignition (စကားပြန်) နှင့် TurboFan (အကောင်းဆုံးစုစည်းမှု) တို့ပါ၀င်သည့်
a new compiler pipeline တစ်ခုကို တင်ပို့ခဲ့သည်။
V8 ဗားရှင်း 5.9 မှစတင်၍ Full-codegen (အစောပိုင်းအခြေခံစုစည်းမှု) နှင့် Crankshaft တို့ကို JavaScript လုပ်ဆောင်ချက်အတွက် V8 တွင် အသုံးမပြုတော့ဘဲ၊ ၎င်းတို့သည် JavaScript ဘာသာစကားအင်္ဂါရပ်အသစ်များနှင့် လိုအပ်သော အင်္ဂါရပ်များကို ပိုမိုကောင်းမွန်အောင်လုပ်ဆောင်နိုင်တော့မည်မဟုတ်ဟု အဖွဲ့မှယုံကြည်သောကြောင့်ဖြစ်သည်။

2021 ခုနှစ်တွင်၊ HotSpot အသုံးပြုသော ပရိုဖိုင်း C1 Compiler နှင့် တိုက်ရိုက်အပြိုင် V8 အတွင်းရှိ TurboFan compiler ကို ဖြည့်စွက်ပေးသည့် SparkPlug compiler ကို ထုတ်ဝေခြင်းဖြင့် အဆင့်တန်းစုစည်းမှုပိုက်လိုင်းအသစ်ကို မိတ်ဆက်ခဲ့သည်။

### Design

V8 သည် ၎င်း၏ကိုယ်ပိုင် parser ဖြင့် abstract syntax tree ကို ဦးစွာထုတ်ပေးသည်။ ထို့နောက်၊ Ignition သည် အတွင်းပိုင်း V8 bytecode format ကို အသုံးပြု၍ ဤ syntax tree မှ bytecode ကိုထုတ်ပေးသည်။ TurboFan သည် ဤ bytecode ကို machine code အဖြစ် စုစည်းသည်။
တစ်နည်းဆိုရသော် V8 သည် ၎င်းကို မလုပ်ဆောင်မီ အချိန်နှင့်တပြေးညီ စုစည်းမှုကို အသုံးပြု၍ ECMAScript ကို မူရင်း machine code သို့ တိုက်ရိုက်စုစည်းသည်။

ကုဒ်၏လုပ်ဆောင်မှုပရိုဖိုင်၏ heuristics ကိုအခြေခံ၍ runtime တွင် စုစည်းထားသောကုဒ်ကို ထပ်လောင်းပိုကောင်းအောင်ပြုလုပ်သည် (နှင့် ပြန်လည်ကောင်းမွန်အောင်ပြုလုပ်သည်) ကို ကုဒ်၏လုပ်ဆောင်မှုပရိုဖိုင်၏ heuristics ပေါ်တွင်အခြေခံသည်။

### Usage

V8 သည် ၎င်းတို့၏ 32-bit နှင့် 64-bit editions တွင် x86၊ ARM သို့မဟုတ် MIPS ညွှန်ကြားချက်အစုံဗိသုကာများကို စုစည်းနိုင်သည်။ ဆာဗာများတွင် အသုံးပြုရန်အတွက် ၎င်းကို PowerPC[16] နှင့် IBM s390[17][18] တွင် ထပ်လောင်းပေးပို့ထားပါသည်။

V8 ကို ဘရောက်ဆာတွင် သုံးနိုင်သည် သို့မဟုတ် သီးခြားပရောဂျက်များတွင် ပေါင်းစည်းနိုင်သည်။ V8 ကို အောက်ပါဆော့ဖ်ဝဲလ်တွင် အသုံးပြုသည်-

- Chromium-based web browsers - Google Chrome, Brave, Opera and Microsoft Edge.
- Couchbase database server
- Deno runtime environment
- Electron desktop application framework, used by the Atom and Visual Studio Code text editors
- MarkLogic database server
- NativeScript mobile application framework
- Node.js runtime environment
- Qt Quick runtime environment

---

---

---

# SpiderMonkeyEngine

SpiderMonkey သည် Netscape Communications တွင် Brendan Eich မှရေးသားသော ပထမဆုံး JavaScript အင်ဂျင်ဖြစ်ပြီး နောက်ပိုင်းတွင် open source အဖြစ် Mozilla Foundation မှ ထိန်းသိမ်းထားပြီး လက်ရှိတွင် ထိန်းသိမ်းထားသည်။ ၎င်းကို Firefox ဝဘ်ဘရောက်ဆာတွင် အသုံးပြုသည်။

### History

Eich သည် 1995 ခုနှစ်တွင် "ဆယ်ရက်အတွင်း JavaScript ကိုရေးသားခဲ့သည်"၊ ("ဘာသာစကားကို JAVA လို ပုံသဏ္ဌာန်ရှိရမယ်လို့" engineering management [ဆုံးဖြတ်] တုန်းက Scheme ကိုသုံးဖို့ စိတ်ကူးကို စွန့်လွှတ်ခဲ့တယ်။)

1996 ခုနှစ်နှောင်းပိုင်းတွင် Eich သည် ပထမနှစ်မှကျန်ခဲ့သော " substantial technical debt" ကိုဆပ်ရန်လိုပြီး "SpiderMonkey" ဟုလူသိများသော codebase အဖြစ် Mocha ကိုပြန်လည်ရေးသားရန် အိမ်တွင်နှစ်ပတ်ကြာနေခဲ့သည်။

Mocha သည် ဘာသာစကားအတွက် မူရင်းအမည်ဖြစ်သည်။

2011 ခုနှစ်တွင် Eich သည် SpiderMonkey ကုဒ်စီမံခန့်ခွဲမှုကို Dave Mandelin သို့လွှဲပြောင်းပေးခဲ့သည်။

### Internals

SpiderMonkey ကို C/C++ ဖြင့်ရေးသားထားပြီး စကားပြန်တစ်ဦး၊ IonMonkey JIT compiler နှင့် a garbage collectorပါရှိသည်။

### TraceMonkey

TraceMonkeyသည် JavaScript ဘာသာစကားအတွက် ပထမဆုံး JIT compiler ဖြစ်သည်။ beta ထွက်ရှိမှုတွင် ရွေးချယ်စရာတစ်ခုအဖြစ် စတင်မိတ်ဆက်ခဲ့ပြီး August 23, 2008 တွင် Brendan Eich ၏ဘလော့ဂ်တွင်မိတ်ဆက်ခဲ့သည်၊အဆိုပါ compiler သည် Firefox 3.5 ရှိ SpiderMonkey ၏တစ်စိတ်တစ်ပိုင်းဖြစ်လာပြီး "စွမ်းဆောင်ရည်တိုးတက်မှုများကို အကြိမ် 20 မှ 40 ကြားအထိပေးစွမ်းသည်။ Firefox 3 တွင် အခြေခံစကားပြန်ထက် ပိုမြန်သည်။

### JägerMonkey

Method JIT ဟု အမည်ပေးထားသည့် JägerMonkey သည် TraceMonkey တည်ငြိမ်သော မူရင်းကုဒ်ကို မထုတ်ပေးနိုင်သော ကိစ္စများတွင် စွမ်းဆောင်ရည်ကို မြှင့်တင်ရန် ဒီဇိုင်းထုတ်ထားသည့် JIT compiler တစ်ခုဖြစ်သည်။ Firefox 4 တွင် ပထမဆုံးထွက်ရှိခဲ့ပြီး နောက်ဆုံးတွင် TraceMonkey ကို လုံးဝအစားထိုးခဲ့သည်။ ၎င်းကို IonMonkey ဖြင့် အစားထိုးထားသည်။

JägerMonkey သည် ၎င်း၏အတန်းရှိ အခြားသော compilers များနှင့် အလွန်ကွာခြားစွာ လုပ်ဆောင်ခဲ့သည်
ပုံမှန် compilers များသည် function ကိုကိုယ်စားပြုသည့် control-flow graph ကိုတည်ဆောက်ကာ ပိုမိုကောင်းမွန်အောင်လုပ်ဆောင်နေသော်လည်း၊ JägerMonkey သည် SpiderMonkey bytecode မှတဆင့် linearly forward အတိုင်းပြန်ခြင်းပြုလုပ်ကာ internal function ကိုကိုယ်စားပြုပါသည်။ ညွှန်ကြားချက်ကို ပြန်လည်စီစစ်ရန် လိုအပ်သည့် အကောင်းဆုံးပြင်ဆင်မှုများကို တားမြစ်ထားသော်လည်း JägerMonkey compiling သည် အလွန်လျင်မြန်သောအားသာချက်ရှိပြီး၊ ၎င်းသည် ကွဲပြားသောအမျိုးအစားများပြောင်းလဲခြင်းကြောင့် ပြန်လည်ပေါင်းစည်းခြင်းသည် မကြာခဏဖြစ်သောကြောင့် JavaScript အတွက် အသုံးဝင်ပါသည်။

Mozilla သည် JägerMonkey တွင် အရေးအကြီးဆုံးမှာ polymorphic inline caches နှင့် type inferences တွင် အရေးပါဆုံးသော ပိုမိုကောင်းမွန်အောင် လုပ်ဆောင်မှုများစွာကို Mozilla မှ လုပ်ဆောင်ခဲ့သည်။

### IonMonkey

IonMonkey သည် ယခင် JägerMonkey architecture နှင့် မဖြစ်နိုင်သော အသစ်အဆန်းများစွာကို ပိုမိုကောင်းမွန်အောင်လုပ်ဆောင်နိုင်ရန် ရည်ရွယ်ထားသည့် Mozilla ၏ JavaScript JIT ရေးဖွဲ့သူဖြစ်သည်။

IonMonkey သည် ပို၍ သမားရိုးကျ ရေးဖွဲ့သူဖြစ်သည် ၎င်းသည် အလယ်အလတ်ကိုယ်စားပြုမှုအတွက် static single assignment form (SSA) ကို အသုံးပြု၍ SpiderMonkey bytecode ကို control-flow ဂရပ်အဖြစ် ဘာသာပြန်ဆိုပါသည်။ ဤ architecture သည် type specialization, function inlining,linear-scan register allocation, dead code eliminationနှင့် loop-invariant code motion.အပါအဝင် အခြားသော ပရိုဂရမ်ဘာသာစကားများမှ လူသိများသော ပိုမိုကောင်းမွန်အောင်လုပ်ဆောင်မှုများကို ဖွင့်ပေးခဲ့သည်။

compiler သည် ARM၊ x86 နှင့် x86-64 ပလပ်ဖောင်းများတွင် JavaScript လုပ်ဆောင်ချက်များကို လျင်မြန်သော မူရင်းကုဒ်ဘာသာပြန်ဆိုချက်များကို ထုတ်လွှတ်နိုင်သည်။ ၎င်းသည် Firefox 18 ကတည်းက မူရင်းအင်ဂျင်ဖြစ်သည်။

### OdinMonkey

OdinMonkey သည် asm.js အတွက် လွယ်ကူစွာ စုစည်းနိုင်သော JavaScript ၏ အခွဲခွဲတစ်ခုဖြစ်သည့် Mozilla ၏ new optimization module အမည်ဖြစ်သည်။ OdinMonkey ကိုယ်တိုင်က JIT compiler မဟုတ်ဘဲ လက်ရှိ JIT compiler ကို အသုံးပြုပါတယ်။ ၎င်းသည် Firefox 22 တွင်ပါ ၀င်သည်။

### WarpMonkey

Warp Monkey JIT သည် ယခင် IonMonkey အင်ဂျင်ကို ဗားရှင်း 83 မှ အစားထိုးသည်။ ၎င်းသည် လုပ်ဆောင်နေသည့် အချက်အလက်နှင့် အကြောင်းပြချက်များအပေါ် အခြေခံ၍ အခြား script များကို လိုင်းထည့်သွင်းနိုင်ပြီး ကုဒ်များကို အထူးပြုနိုင်သည်။ ၎င်းသည် bytecode နှင့် Inline Cache ဒေတာအား A Mid-level Intermediate Representation (Ion MIR) ကိုယ်စားပြုမှုအဖြစ် ဘာသာပြန်ပေးသည်။ ဤဂရပ်ကို Lower to a Low-level Intermediate Representation (Ion LIR) အဖြစ်သို့ နှိမ့်ချခြင်းမပြုမီ ဤဂရပ်ကို အသွင်ပြောင်းပြီး အကောင်းဆုံးဖြစ်အောင် ပြုလုပ်ထားသည်။ ဤ LIR သည် register allocationကို လုပ်ဆောင်ပြီး Code Generation ဟုခေါ်သော လုပ်ငန်းစဉ်တွင် မူရင်း machine codeကိုထုတ်ပေးသည်။

### Use

SpiderMonkey သည် JavaScript အတွက် လက်ခံဆောင်ရွက်ပေးသည့် ပတ်ဝန်းကျင်များကို ပံ့ပိုးပေးသည့် အခြားသော အပလီကေးရှင်းများတွင် ထည့်သွင်းရန် ရည်ရွယ်ပါသည်။

- Mozilla Firefox, Thunderbird, SeaMonkey, and other applications that use the Mozilla application framework
  - Forks of Firefox including the Pale Moon and Waterfox web browsers.

* Data storage applications:

  - MongoDB moved from V8 to SpiderMonkey in version 3.2
  - Riak uses SpiderMonkey as the runtime for JavaScript MapReduce operations
  - CouchDB database system (written in Erlang). JavaScript is used for defining maps, filters, reduce functions and viewing data, for example in HTML format.

* Adobe Acrobat and Adobe Reader, Adobe Flash Professional, and Adobe Dreamweaver. Adobe Acrobat DC uses Spidermonkey 24.2 with ECMA-357 .

* GNOME desktop environment, version 3 and later….

* Yahoo! Widgets, formerly named Konfabulator.
