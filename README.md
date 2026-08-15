# မြတ် Catalogue Data

ဒီ Public repository က **Customer App ရဲ့ Online ဈေးနှုန်း / Stock update data** အတွက်ပဲ အသုံးပြုပါသည်။ App source code၊ signing key၊ password မထားပါနှင့်။

## Product တစ်ခု ဈေး/Stock ပြောင်းရန် အလွယ်ဆုံးနည်း

1. GitHub repo ထဲက **Actions** ကိုဝင်ပါ။
2. **Update Catalogue Product** ကိုရွေးပါ။
3. **Run workflow** နှိပ်ပါ။
4. Product Code ထည့်ပါ — ဥပမာ `MYAT-001`။
5. ဈေးပြောင်းမယ်ဆို `price` ထည့်ပါ။ မပြောင်းရင် blank ထားပါ။
6. Stock ကို `in_stock` / `out_of_stock` / `no_change` ရွေးပါ။
7. Run workflow လုပ်ပါ။
8. Customer App မှာ **Refresh** နှိပ်ရင် update ဝင်ပါမယ်။

`overrides.json` က ပြောင်းထားတဲ့ Product တွေကိုပဲ သိမ်းထားပါတယ်။ Product ပုံနဲ့ အမည်အစုံက APK ထဲမှာရှိပြီးသားဖြစ်လို့ ဒီ repo ကို ပေါ့ပါးအောင်ထားနိုင်ပါတယ်။

## App version အသစ် MediaFire မှာတင်တဲ့အခါ

`app-release.json` ထဲမှာ:
- `latestVersionCode`
- `latestVersionName`
- `apkUrl`
- `message`

တို့ကိုပြင်ပါ။ `apkUrl` ကို MediaFire download page/link ထည့်ပြီး versionCode က အသုံးပြုသူ App ထက်မြင့်သွားရင် App ထဲမှာ **Version အသစ်ရရှိပြီ** ဆိုတဲ့ Download banner ပေါ်လာပါမယ်။

## အရေးကြီး

- `MyatCatalogue` source repo ကို Private အတိုင်းထားပါ။
- ဒီ repo ထဲ Signing Key / JKS / Password / Secret Token မတင်ပါနှင့်။
