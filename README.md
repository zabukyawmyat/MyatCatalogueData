# မြတ် Catalogue Data

ဒီ Public repository က **Customer App ရဲ့ Online Product / ဈေးနှုန်း / Stock / App update data** အတွက်ပဲ အသုံးပြုပါသည်။ App source code၊ signing key၊ password မထားပါနှင့်။

## ⭐ အဓိကသုံးရန် — Catalogue Product Manager

Product အသစ်ထည့်တာ၊ ရှိပြီးသား Product ပြင်တာ၊ ဈေး/Stock/Category/Description/Image ပြောင်းတာတွေကို **Actions > Catalogue Product Manager > Run workflow** တစ်ခုတည်းနဲ့လုပ်နိုင်ပါတယ်။

### Product Code
`M-001`, `MYAT-001`, `001` သုံးမျိုးလုံးရပါတယ်။ System က အလိုအလျောက် `MYAT-001` အဖြစ်သတ်မှတ်ပေးပါတယ်။

- `001`–`102` = APK ထဲရှိပြီးသား Product ကို Online override နဲ့ပြင်မယ်။
- `103+` = ရှိပြီးသားဆို Edit လုပ်မယ်၊ မရှိသေးရင် Product အသစ် Add လုပ်မယ်။
- Product အသစ် Code မသိရင် **product_id ကို blank ထားပါ**။ နောက်ဆုံး Code ရဲ့နောက်တစ်ခုကို အလိုအလျောက်ရွေးပေးမယ်။

### Product ပုံထည့်ရန်
1. `product-images` folder ကိုဝင်ပါ။
2. **Add file > Upload files** နဲ့ပုံတင်ပါ။
3. Filename ကို `M-103.jpg` သို့ `MYAT-103.jpg` လိုထားပါ။
4. Catalogue Product Manager ရဲ့ `image_file` မှာ `M-103` လို့ extension မပါဘဲရေးလည်းရပါတယ်။ `.jpg/.jpeg/.png/.webp` ကို system ကရှာပေးပါတယ်။

Product အသစ်ထည့်ရာမှာ Name + Price + Category + Image လိုပါတယ်။ Existing Product ကိုပြင်ရာမှာ မပြောင်းချင်တဲ့ field ကို blank/no_change ထားပါ။ Sub-category/Description ကိုရှင်းချင်ရင် `__CLEAR__` သုံးပါ။

Run ပြီး Customer App မှာ **Refresh** နှိပ်ရင် update ဝင်ပါမယ်။ APK အသစ်ပြန်ထုတ်စရာမလိုပါ။

## အခြား Actions

- **Update Catalogue Product** — ဈေး/Stock/Featured အမြန်ပြောင်းရန်
- **Batch Update Catalogue Products** — Product အများကြီးကို တစ်ခါတည်းပြောင်းရန်
- **Delete Added Catalogue Product** — Online ထည့်ထားသော Product ဖျက်ရန်
- **Reset Online Catalogue Changes** — Online overrides အားလုံး Reset
- **Update App Download Link** — MediaFire APK version/link update

အရင် `Add New Catalogue Product` / `Edit Added Catalogue Product` workflows တွေရှိနေသေးပေမယ့် ပုံမှန်အသုံးပြုမှုအတွက် **Catalogue Product Manager** ကိုပဲသုံးတာ အလွယ်ဆုံးပါ။

## Data files

- `manifest.json` — Online catalogue version/status
- `overrides.json` — APK bundled Products ပြင်ထားသော data
- `additions.json` — APK နောက်ပိုင်း ထပ်ထည့်ထားသော Products
- `product-images/` — Online Product ပုံများ
- `app-release.json` — MediaFire App update metadata

## အရေးကြီး

- `MyatCatalogue` source repo ကို **Private** အတိုင်းထားပါ။
- ဒီ Public repo ထဲ Signing Key / `.jks` / Password / Secret Token မတင်ပါနှင့်။
