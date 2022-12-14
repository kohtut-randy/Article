# Function

Functions များသည် JavaScript ၏ အခြေခံကျသော အဆောက်အဦများထဲမှ တစ်ခုဖြစ်သည်။ JavaScript ရှိ လုပ်ဆောင်ချက်တစ်ခုသည် လုပ်ထုံးလုပ်နည်းတစ်ခုနှင့် ဆင်တူသည်—အလုပ်တစ်ခုကို လုပ်ဆောင်သည့် သို့မဟုတ် တန်ဖိုးတစ်ခုကို တွက်ချက်သည့် ဖော်ပြချက်အစုအဝေးတစ်ခုဖြစ်သော်လည်း လုပ်ဆောင်ချက်တစ်ခုအဖြစ် အရည်အချင်းပြည့်မီရန်အတွက်၊ ၎င်းသည် အချို့သော input ကိုယူကာ ထင်ရှားသောဆက်နွယ်မှုရှိသည့် output တစ်ခုကို ပြန်ပေးသင့်သည်။ input နှင့် output ကို။ လုပ်ဆောင်ချက်တစ်ခုကို အသုံးပြုရန်၊ ၎င်းကို သင်ခေါ်ဆိုလိုသည့် နယ်ပယ်အတွင်းရှိ တစ်နေရာရာကို သတ်မှတ်ရပါမည်။

Defining functions
Function declarations

လုပ်ဆောင်ချက်အမည်။
ကွင်းအတွင်းထည့်သွင်းပြီး ကော်မာများဖြင့် ပိုင်းခြားထားသော လုပ်ဆောင်ချက်အတွက် ကန့်သတ်ချက်များစာရင်း။
အကောက်ကောက်ကွင်းများအတွင်း ထည့်သွင်းထားသော လုပ်ဆောင်ချက်ကို သတ်မှတ်သည့် JavaScript ထုတ်ပြန်ချက်များ၊
{ /_ … _/ }။

```
function square(number){
    return number * number;
}
```

လုပ်ဆောင်ချက်စတုရန်းသည် နံပါတ်ဟုခေါ်သော ကန့်သတ်ချက်တစ်ခုယူသည်။ function တွင် function ၏ parameter (ဆိုလိုသည်မှာ နံပါတ်) ကို သူ့ဘာသာသူ မြှောက်ပေးသည့် parameter ကို ပြန်ပေးမည့် statement တစ်ခု ပါဝင်ပါသည်။ Statement return သည် function မှ ပြန်ပေးသော တန်ဖိုးကို သတ်မှတ်သည်။

```
    return number * number;
```

ပါရာမီတာများကို တန်ဖိုးအလိုက် လုပ်ဆောင်ချက်များသို့ ပေးပို့သည် — ထို့ကြောင့် လုပ်ဆောင်ချက်တစ်ခု၏ကိုယ်ထည်အတွင်းရှိ ကုဒ်သည် လုပ်ဆောင်ချက်သို့ ပေးပို့ထားသော ကန့်သတ်ဘောင်တစ်ခုသို့ လုံးဝအသစ်တန်ဖိုးတစ်ခုကို သတ်မှတ်ပါက၊ ပြောင်းလဲမှုသည် ကမ္ဘာလုံးဆိုင်ရာ သို့မဟုတ် ထိုလုပ်ဆောင်ချက်ဟုခေါ်သော ကုဒ်တွင် သက်ရောက်မှုမရှိပါ။

အရာဝတ္ထုတစ်ခုအား ကန့်သတ်ဘောင်တစ်ခုအဖြစ် သင်ဖြတ်သန်းသောအခါ၊ လုပ်ဆောင်ချက်သည် အရာဝတ္ထု၏ ဂုဏ်သတ္တိများကို ပြောင်းလဲပါက အောက်ပါဥပမာတွင် ပြထားသည့်အတိုင်း အပြောင်းအလဲကို လုပ်ဆောင်ချက်အပြင်ဘက်တွင် မြင်နိုင်သည်-

```
/* Declare the function 'myFunc' */
function myFunc(theObject) {
  theObject.brand = "Toyota";
}

/*
 * Declare variable 'mycar';
 * create and initialize a new Object;
 * assign reference to it to 'mycar'
 */
const mycar = {
  brand: "Honda",
  model: "Accord",
  year: 1998
};

/* Logs 'Honda' */
console.log(mycar.brand);

/* Pass object reference to the function */
myFunc(mycar);

/*
 * Logs 'Toyota' as the value of the 'brand' property
 * of the object, as changed to by the function.
 */
console.log(mycar.brand);

```

# Arrow Function Expression

An arrow function expression သည် သမားရိုးကျလုပ်ဆောင်မှုအသုံးအနှုန်းတစ်ခုအတွက် သေးငယ်သောအစားထိုးမှုတစ်ခုဖြစ်သော်လည်း အကန့်အသတ်ရှိပြီး အခြေအနေအားလုံးတွင် အသုံးမပြုနိုင်ပါ။

မြှားလုပ်ဆောင်ချက်များနှင့် ရိုးရာလုပ်ဆောင်ချက်များအကြား ခြားနားချက်များအပြင် ကန့်သတ်ချက်အချို့ရှိသည်။

Arrow လုပ်ဆောင်ချက်များသည် ဤအရာ၊ အကြောင်းပြချက်များ သို့မဟုတ် စူပါတို့နှင့် ဆက်စပ်မှု မရှိသည့်အပြင် နည်းလမ်းများအဖြစ် အသုံးမပြုသင့်ပါ။
Arrow လုပ်ဆောင်ချက်များသည် new.target သော့ချက်စာလုံးကို အသုံးပြုခွင့်မရှိပါ။
Arrow လုပ်ဆောင်ချက်များသည် ယေဘုယျအားဖြင့် နယ်ပယ်တစ်ခုကို ထူထောင်ခြင်းအပေါ် အားကိုးသည့် ခေါ်ဆိုမှု၊ အသုံးပြုမှုနှင့် စည်းသည့်နည်းလမ်းများအတွက် မသင့်လျော်ပါ။
Arrow function များကို constructors အဖြစ် အသုံးမပြုနိုင်ပါ။
Arrow လုပ်ဆောင်ချက်များသည် ၎င်း၏ကိုယ်တွင်းရှိ yield ကို အသုံးမပြုနိုင်ပါ။

```
const materials = [
  'Hydrogen',
  'Helium',
  'Lithium',
  'Beryllium'
];

console.log(materials.map(material => material.length));
// expected output: Array [8, 6, 7, 9]

```

### Comparing traditional functions to arrow functions

```
// Traditional Anonymous Function
(function (a) {
  return a + 100;
});

// Arrow Function Break Down

// 1. Remove the word "function" and place arrow between the argument and opening body bracket
(a) => {
  return a + 100;
};

// 2. Remove the body braces and word "return" — the return is implied.
(a) => a + 100;

// 3. Remove the argument parentheses
a => a + 100;

```

အချို့ကိစ္စများတွင် { braces } နှင့် (ကွင်းအတွင်း ) နှင့် "return" လိုအပ်ပါသည်။
ဥပမာအားဖြင့်၊ သင့်တွင် အကြောင်းပြချက်များစွာရှိသည် သို့မဟုတ် အကြောင်းပြချက်များမရှိပါက၊ အကြောင်းပြချက်များတစ်ဝိုက်တွင် ကွင်းစဥ်များကို ပြန်လည်မိတ်ဆက်ရန် လိုအပ်ပါမည်-

```
// Traditional Anonymous Function
(function (a, b) {
  return a + b + 100;
});

// Arrow Function
(a, b) => a + b + 100;

const a = 4;
const b = 2;

// Traditional Anonymous Function (no arguments)
(function() {
  return a + b + 100;
});

// Arrow Function (no arguments)
() => a + b + 100;

```

# JavaScript Anonymous Functions

An anonymous function သည် အမည်မဖော်သော လုပ်ဆောင်ချက်တစ်ခုဖြစ်သည်။ အမည်မသိလုပ်ဆောင်ချက်ကို အောက်တွင်ဖော်ပြထားသည် ။

```
    (function(){
        //.....
    });
```

() တွင် အမည်မသိလုပ်ဆောင်ချက်ကို မထည့်ပါက syntax error တစ်ခုရလိမ့်မည်ကို သတိပြုပါ။ () သည် အမည်မသိ လုပ်ဆောင်ချက်ကို လုပ်ဆောင်ချက် အရာဝတ္တုကို ပြန်ပေးသည့် စကားရပ်တစ်ခု ဖြစ်စေသည်။

၎င်း၏ကနဦးဖန်တီးပြီးနောက် အမည်မသိလုပ်ဆောင်ချက်ကို အသုံးပြု၍မရပါ။ ထို့ကြောင့်၊ သင်သည် ၎င်းကို variable တစ်ခုသို့ မကြာခဏ သတ်မှတ်ရန် လိုအပ်သည်။

```
    let show =(function(){
        console.log('Anonymous Function')
    });

    show()
```

ဤဥပမာတွင်၊ အမည်မသိလုပ်ဆောင်ချက်သည် လုပ်ဆောင်ချက်သော့ချက်စကားလုံးနှင့် ကွင်းစဥ် () ကြားတွင် အမည်မရှိပါ။ ကျွန်ုပ်တို့သည် အမည်မသိလုပ်ဆောင်ချက်ကို နောက်ပိုင်းတွင်ခေါ်ဆိုရန် လိုအပ်သောကြောင့်၊ ကျွန်ုပ်တို့သည် အမည်မသိလုပ်ဆောင်ချက်ကို show variable သို့ သတ်မှတ်ပေးပါသည်။

### Using anonymous functions as arguments

လက်တွေ့တွင် သင်သည် အမည်မသိလုပ်ဆောင်ချက်များကို အခြားလုပ်ဆောင်ချက်များသို့ အငြင်းအခုံများအဖြစ် ပေးပို့လေ့ရှိသည်။ ဥပမာ:

```
setTimeout(function(){
    console.log("Excute later after 1s")
},1000);
```

ဤဥပမာတွင်၊ ကျွန်ုပ်တို့သည် အမည်မသိလုပ်ဆောင်ချက်တစ်ခုကို setTimeout() လုပ်ဆောင်ချက်သို့ ပေးပို့ပါသည်။ setTimeout() လုပ်ဆောင်ချက်သည် ဤအမည်မသိလုပ်ဆောင်ချက်ကို တစ်စက္ကန့်အကြာတွင် လုပ်ဆောင်သည်။

# Callback Function

Callback Function သည် အခြားကုဒ်အပိုင်းတစ်ခုသို့ ငြင်းခုံမှုတစ်ခုအဖြစ် ဖြတ်သွားသည့် executable code ကိုမဆို ရည်ညွှန်းသည်။ ထိုကုဒ်သည် ၎င်း၏အလုပ်၏တစ်စိတ်တစ်ပိုင်းအနေဖြင့် ပြန်ခေါ်ရန် (ပြန်ခေါ်ရန်) လုပ်ဆောင်မှုကို လုပ်ဆောင်ရန် မျှော်လင့်ပါသည်။ ဤလုပ်ဆောင်မှုသည် တစ်ပြိုင်တည်းခေါ်ဆိုမှုတွင်ကဲ့သို့ ချက်ချင်းဖြစ်နိုင်သည် သို့မဟုတ် တစ်ချိန်တည်းတွင် တစ်ချိန်တည်းတွင် တစ်ပြိုင်နက်ပြန်ခေါ်ခြင်းကဲ့သို့ ဖြစ်နိုင်ပါသည်။ ပရိုဂရမ်းမင်းဘာသာစကားများသည် မတူညီသောနည်းလမ်းများဖြင့် ပြန်ခေါ်ခြင်းကို ပံ့ပိုးပေးသည်၊ ၎င်းတို့ကို ပုံမှန်လုပ်ရိုးလုပ်စဉ်များ၊ lambda အသုံးအနှုန်းများ၊ ဘလောက်များ သို့မဟုတ် လုပ်ဆောင်ချက်ညွှန်ပြချက်များဖြင့် အကောင်အထည်ဖော်လေ့ရှိသည်။

Callback Functionဆိုသည်မှာ အခြားလုပ်ဆောင်ချက်တစ်ခုသို့ အငြင်းအခုံတစ်ခုအဖြစ် ပေးပို့သည့် လုပ်ဆောင်ချက်တစ်ခုဖြစ်သည်။

ဤနည်းပညာသည် လုပ်ဆောင်ချက်တစ်ခုအား အခြားလုပ်ဆောင်ချက်ကို ခေါ်ရန် ခွင့်ပြုသည်။

အခြားလုပ်ဆောင်ချက်တစ်ခုပြီးသည်နှင့် နောက်ပြန်ခေါ်သည့်လုပ်ဆောင်ချက်ကို လုပ်ဆောင်နိုင်သည်။

```
function myFirst(){
    console.log("Hello")
}
function mySecond(){
    console.log("World")
}
myFirst()
mySecond()
```

တစ်ခါတစ်ရံတွင် သင်သည် လုပ်ဆောင်ချက်တစ်ခုကို လုပ်ဆောင်ရမည့်အချိန်ကို ပိုမိုကောင်းမွန်စွာ ထိန်းချုပ်လိုပါသည်။

# Higher-Order Functions

Javascript တွင်၊ strings များ သို့မဟုတ် arrays များလုပ်နိုင်သည့်ပုံစံအတိုင်း functions များကို variable များသို့သတ်မှတ်နိုင်သည်။ ၎င်းတို့ကို ကန့်သတ်ချက်များအဖြစ် အခြားလုပ်ဆောင်ချက်များသို့ ပေးပို့နိုင်သည် သို့မဟုတ် ၎င်းတို့ထံမှလည်း ပြန်လည်ပေးပို့နိုင်သည်။

“အဆင့်မြင့်သော လုပ်ဆောင်ချက်” သည် ဘောင်များအဖြစ် လုပ်ဆောင်ချက်များကို လက်ခံပြီး/သို့မဟုတ် လုပ်ဆောင်ချက်တစ်ခုကို ပြန်ပေးသည့် လုပ်ဆောင်ချက်တစ်ခုဖြစ်သည်။

Higher Orders Functions များသည် အခြားသော Function များတွင် လုပ်ဆောင်ချက်များကို လုပ်ဆောင်ပေးသည့် Function များဖြစ်သည်။ ဤအဓိပ္ပါယ်ဖွင့်ဆိုချက်တွင်၊ လုပ်ဆောင်ချက်များသည် တစ်ခု သို့မဟုတ် တစ်ခုထက်ပိုသော လုပ်ဆောင်ချက်များကို အငြင်းအခုံတစ်ခုအဖြစ် သို့မဟုတ် ရလဒ်အဖြစ် လုပ်ဆောင်ချက်တစ်ခုကို ပြန်ပေးသည်ဟု ဆိုလိုနိုင်သည်။ နှစ်ခုလုံးလုပ်စရာမလိုပါဘူး။ တစ်ခု သို့မဟုတ် အခြားတစ်ခုလုပ်ဆောင်ခြင်းသည် 
ပိုမိုမြင့်မားသောအစီအစဥ်လုပ်ဆောင်မှုအဖြစ် လုပ်ဆောင်ချက်တစ်ခုကို အရည်အချင်းပြည့်မီစေသည်။



JavaScript တွင်၊ လုပ်ဆောင်ချက်များသည် အကြောင်းပြချက်များအဖြစ် မူလအမျိုးအစားများ (နံပါတ်များ၊ စာကြောင်းများကဲ့သို့) အရာဝတ္ထုများ (အခင်းအကျင်းများ၊ ရိုးရိုးအရာဝတ္ထုများ၊ ပုံမှန်အသုံးအနှုန်းများစသည်ဖြင့်) ကို အသုံးပြုနိုင်ပြီး မူလအမျိုးအစား သို့မဟုတ် အရာဝတ္ထုကိုလည်း ပြန်ပေးနိုင်သည်။

ယခင်ဥပမာတွင်၊ တွက်ချက်ခြင်း([1၊ 2၊ 4]) သည် ကိန်းများကို အငြင်းအခုံတစ်ခုအဖြစ် လက်ခံပြီး နံပါတ် 7 — ပေါင်းလဒ်ကို ပြန်ပေးသည်။

သို့သော် လုပ်ဆောင်ချက်များကို တန်ဖိုးများအဖြစ် အသုံးပြုရန် ဖြစ်နိုင်ပါသလား။ လုပ်ဆောင်ချက်များကို ကိန်းရှင်များအဖြစ် သတ်မှတ်ပေးခြင်း၊ ၎င်းတို့ကို အငြင်းအခုံများအဖြစ် အသုံးပြုခြင်း သို့မဟုတ် ပြန်လာခြင်းပင်။ ဟုတ်တယ်၊ ဖြစ်နိုင်တယ်။

JavaScript ရှိ လုပ်ဆောင်ချက်များ အားလုံးသည် ပထမတန်းစား နိုင်ငံသားများ ဖြစ်သောကြောင့် ဖြစ်သည်။ ဆိုလိုသည်မှာ သင်လုပ်နိုင်သည်-


