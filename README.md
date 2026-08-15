# မြတ် Catalogue Data

ဒီ Public repository က **Customer App ရဲ့ Online ဈေးနှုန်း / Stock / App update data** အတွက်ပဲ အသုံးပြုပါသည်။ App source code၊ signing key၊ password မထားပါနှင့်။

## 1. Product တစ်ခု ဈေး/Stock ပြောင်းရန်

1. GitHub repo ထဲက **Actions** ကိုဝင်ပါ။
2. **Update Catalogue Product** ကိုရွေးပါ။
3. **Run workflow** နှိပ်ပါ။
4. Product Code ထည့်ပါ — `MYAT-001` မှ `MYAT-102` အထိ။
5. ဈေးပြောင်းမယ်ဆို `price` ထည့်ပါ။ မပြောင်းရင် blank ထားပါ။
6. Stock ကို `in_stock` / `out_of_stock` / `no_change` ရွေးပါ။
7. Featured ပြောင်းလိုလျှင် `featured` / `normal` ရွေးနိုင်ပါသည်။
8. Run workflow လုပ်ပါ။ Customer App မှာ **Refresh** နှိပ်ရင် update ဝင်ပါမယ်။

Override တစ်ခုကိုဖျက်ပြီး APK ထဲက မူရင်းဈေး/Stock ပြန်သုံးချင်ရင် `remove_override` ကိုဖွင့်ပြီး Run လုပ်ပါ။

## 2. Product အများကြီးကို တစ်ခါတည်းပြောင်းရန်

**Actions > Batch Update Catalogue Products** ကိုရွေးပြီး `updates` box ထဲမှာ Product တစ်ခုကို တစ်ကြောင်းစီ ရေးပါ။

Format:
`ProductCode,Price,Stock,Featured`

ဥပမာ:
```
MYAT-001,22000,in_stock,no_change
MYAT-002,6500,no_change,featured
MYAT-003,,out_of_stock,no_change
```

- Price မပြောင်းရင် အလယ်နေရာကို blank ထားနိုင်ပါတယ်။
- Stock = `in_stock` / `out_of_stock` / `no_change`
- Featured = `featured` / `normal` / `no_change`
- တစ်ကြိမ်မှာ Product 102 ခုအထိ update လုပ်နိုင်ပါတယ်။
- Product Code မှားခြင်း၊ duplicate ဖြစ်ခြင်း၊ ဈေး format မှားခြင်းတွေကို workflow က စစ်ပြီးမှ commit လုပ်ပါတယ်။

## 3. Online ပြောင်းထားသမျှ အားလုံး Reset လုပ်ရန်

**Actions > Reset Online Catalogue Changes** ကိုရွေးပါ။ `confirm` မှာ `RESET` လို့ အတိအကျရိုက်ပြီး Run လုပ်ပါ။ `overrides.json` ကိုရှင်းပြီး Customer App က APK ထဲက မူရင်း catalogue ကိုပြန်သုံးပါမယ်။

## 4. MediaFire APK အသစ်တင်ပြီး Update အသိပေးရန်

1. APK အသစ်ကို MediaFire မှာအရင်တင်ပါ။
2. **Actions > Update App Download Link** ကိုဝင်ပါ။
3. Version Code / Version Name / MediaFire URL ထည့်ပါ။
4. Update message ထည့်နိုင်ပါသည်။
5. `required_update` ကို ပုံမှန်အားဖြင့် **false** ထားပါ။
6. Run workflow လုပ်ပါ။

Version Code က အသုံးပြုသူဖုန်းထဲက App ထက်မြင့်နေပြီး MediaFire URL ရှိရင် App မှာ **Version အသစ်ရရှိပြီ** Download banner ပေါ်ပါမယ်။

## Data files

- `manifest.json` — Online catalogue version/status
- `overrides.json` — ပြောင်းထားတဲ့ Product တွေရဲ့ ဈေး/Stock/Featured data ပဲ သိမ်းသည်
- `app-release.json` — MediaFire App update metadata

Product ပုံ၊ အမည်၊ အသေးစိတ် စတဲ့ base catalogue data က APK ထဲမှာရှိပြီးသားဖြစ်လို့ Public repo ကို ပေါ့ပါးစွာထားနိုင်ပါတယ်။

## အရေးကြီး

- `MyatCatalogue` source repo ကို **Private** အတိုင်းထားပါ။
- ဒီ Public repo ထဲ Signing Key / `.jks` / Password / Secret Token မတင်ပါနှင့်။
- Product Code ကို `MYAT-001` မှ `MYAT-102` အတွင်းပဲ အသုံးပြုပါ။
