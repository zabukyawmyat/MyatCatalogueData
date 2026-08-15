# မြတ် Catalogue Data

ဒီ Public repository က **Customer App ရဲ့ Online Product / ဈေးနှုန်း / Stock / App update data** အတွက်ပဲ အသုံးပြုပါသည်။ App source code၊ signing key၊ password မထားပါနှင့်။

## Product အသစ်ထည့်ရန်

1. `product-images` folder ကိုဝင်ပါ။
2. **Add file > Upload files** နဲ့ Product ပုံတင်ပါ။ Filename ကို `MYAT-103.jpg` လိုထားတာအကောင်းဆုံးပါ။
3. Repo ရဲ့ **Actions** ကိုဝင်ပါ။
4. **Add New Catalogue Product** ကိုရွေးပြီး **Run workflow** နှိပ်ပါ။
5. Product Code / Name / Price / Category / Description စတာတွေ ဖြည့်ပါ။
6. `image_file` မှာ upload တင်ထားတဲ့ filename ကိုပဲ ထည့်ပါ — ဥပမာ `MYAT-103.jpg`။ URL ကူးစရာမလိုပါ။
7. Run ပြီး Customer App မှာ **Refresh** နှိပ်ပါ။ Product အသစ်ပေါ်လာပါမယ်။

Product အသစ် Code ကို `MYAT-103` ကနေစပြီး အစဉ်လိုက်သုံးပါ။

## Online-added Product ပြန်ပြင်ရန်

**Actions > Edit Added Catalogue Product** ကိုသုံးပါ။ `MYAT-103+` Product တွေရဲ့ Name / Price / Category / Sub-category / Description / Image / Stock / Featured ကို ပြင်နိုင်ပါတယ်။ မပြောင်းချင်တဲ့ field ကို blank/no_change ထားပါ။ Sub/Description ကို အလွတ်ပြန်လုပ်ချင်ရင် `__CLEAR__` သုံးပါ။

## Online-added Product ဖျက်ရန်

**Actions > Delete Added Catalogue Product** ကိုသုံးပါ။ Product Code ထည့်ပြီး confirm မှာ `DELETE` လို့အတိအကျရိုက်ပါ။ `delete_image=true` လုပ်ရင် `product-images` ထဲက အဲဒီ Product ပုံကိုပါ ဖျက်ပေးနိုင်ပါတယ်။

## Product ဈေး/Stock/Featured ပြောင်းရန်

**Actions > Update Catalogue Product** ကိုသုံးပါ။ Bundled `MYAT-001`–`MYAT-102` သာမက Online ထည့်ထားတဲ့ `MYAT-103+` Product တွေကိုပါ update လုပ်နိုင်ပါတယ်။ ဈေးမပြောင်းရင် blank၊ Stock/Featured မပြောင်းရင် `no_change` ထားပါ။

## Product အများကြီးကို တစ်ခါတည်းပြောင်းရန်

**Actions > Batch Update Catalogue Products** ကိုရွေးပြီး `updates` box ထဲမှာ Product တစ်ခုကို တစ်ကြောင်းစီ ရေးပါ။

Format:
`ProductCode,Price,Stock,Featured`

ဥပမာ:
```
MYAT-001,22000,in_stock,no_change
MYAT-002,6500,no_change,featured
MYAT-003,,out_of_stock,no_change
```

## Online ပြောင်းထားတဲ့ override အားလုံး Reset လုပ်ရန်

**Actions > Reset Online Catalogue Changes** ကိုရွေးပါ။ `confirm` မှာ `RESET` လို့ အတိအကျရိုက်ပြီး Run လုပ်ပါ။

## MediaFire APK အသစ်တင်ပြီး Update အသိပေးရန်

1. APK အသစ်ကို MediaFire မှာအရင်တင်ပါ။
2. **Actions > Update App Download Link** ကိုဝင်ပါ။
3. Version Code / Version Name / MediaFire URL ထည့်ပါ။
4. Run workflow လုပ်ပါ။

Version Code က အသုံးပြုသူ App ထက်မြင့်ပြီး MediaFire URL ရှိရင် App မှာ Version အသစ် Download banner ပေါ်ပါမယ်။

## Data files

- `manifest.json` — Online catalogue version/status
- `overrides.json` — Price/Stock/Featured overrides
- `additions.json` — APK ထုတ်ပြီးနောက် ထပ်ထည့်ထားသော Products
- `product-images/` — Online-added Product ပုံများ
- `app-release.json` — MediaFire App update metadata

## အရေးကြီး

- `MyatCatalogue` source repo ကို **Private** အတိုင်းထားပါ။
- ဒီ Public repo ထဲ Signing Key / `.jks` / Password / Secret Token မတင်ပါနှင့်။
- Product အသစ် Code ကို `MYAT-103` ကနေ စပြီး duplicate မဖြစ်အောင် အစဉ်လိုက်သုံးပါ။
