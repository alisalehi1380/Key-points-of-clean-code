<div style="text-align: center;">
  <img src="https://github.com/alisalehi1380/Key-points-of-clean-code/assets/111766206/4185b039-6045-4133-9341-e80e18be074a" style="min-height: 600px;"/>
</div>

<div dir="rtl" style="margin-top: 20px;">
کدی تمیز است که به راحتی توسط همه ی اعضای تیم قابل درک باشد. کد تمیز میتواند توسط توسعه دهنده ای به غیر از نویسنده ی آن، خوانده و توسعه داده شود. خوانایی، قابلیت نگهداری، تغییر و توسعه پذیری کد، تنها زمانی امکان پذیر است که شما درک درستی از نحوه ی کار کد پیدا کنید.

_____________________________________

## قوانین عمومی

1. از **قوانین استاندارد** (مثل: نام گذاری کلاس ها و توابع، میزان فرورفتگی یا ایندنتیشن و ...) پیروی کنید. ([Standard Conventions][Standard Conventions])
2. تا حد امکان **پیچیدگی** را در کد **کاهش** دهید. همیشه سادگی بهتر است. (قانون [KISS][KISS])
3. سورس کد را **تمیز تر** از زمانی که تحویل می گیرید، تحویل دهید. (قانون [Boy Scout][Boy Scout])
4. همیشه به دنبال **یافتن مشکلات و ایرادات** در کد باشید. برای برطرف کردن آنها، **علل اصلی و ریشه ای** را شناسایی کنید. (قانون [RCA][RCA])

## قوانین طراحی

1. متغیر ها، ثابت ها و تمام داده های قابل تنظیم، باید در **بالا ترین سطح انتزاع** قرار داشته باشند. ([Configurable Data At High Levels][Configurable Data At High Levels])
2. به جای **نقض کردن** قانون [open-closed][open-closed]، از ویژگی [polymorphism][polymorphism] استفاده کنید. ([Replace Conditional With Polymorphism][Replace Conditional With Polymorphism])
3. م ([Separate multi-threading code][Separate multi-threading code])
4. از بیش از اندازه دادنِ **آزادی عمل** به توسعه دهنده های برنامه خود جلوگیری کنید. ([Prevent Over-Configurability][Prevent Over-Configurability])
5. به جای ساخت آبجکت (با استفاده از new)، از **تزریق وابستگی** استفاده کنید. ([Dependency Injection][Dependency Injection])
6. توابع و کلاس ها به جز کاری که انجام میدهند، نباید به جزئیات دیگری در کد **دسترسی** داشته باشند. (قانون [LoD][LoD])

## قوانین توابع

1. توابع شما باید **کوچک** باشند. ([Small][Small])
2. هر تابع باید فقط و فقط **یک کار** را انجام دهد. ([Do one thing][Do one thing])
3. نامی که برای هر تابع انتخاب میکنید باید به طور کامل، **کاری که انجام میدهد** را توصیف کند. ([Use descriptive names][Use descriptive names])
4. بهترین تابع، تابع نیلادیک ([Niladic][Niladic]) ست. تابع شما باید کمترین **آرگومان** را دریافت کند. ([Prefer fewer arguments][Prefer fewer arguments])
5. تابع شما نباید هیچ چیزی را که **خارج از اسکوپ** آن قرار دارد، تغییر دهد. ([Have no side effects][Have no side effects])

## قوانین کامنت‌ها

1. همیشه سعی کنید همه چیز را در کد توضیح دهید اگر امکان پذیر نبود، آنگاه روی نوشتن یک کامنت خوب وقت بگذارید.
2. از نوشتن کامنتی که هیچ توضیح بیشتری از کد نمیدهد (کامنت زائد) خودداری کنید. مثل: (`i++; // increment i`)
3. از نوشتن کامنتی برای توجه بیشتر، برای چیزی که کاملا واضح است، خودداری کنید. مثل: (`end of function // {`)
4. کامنت شما نیاز به **بسته بندی** ندارد! از `{ }`,`[ ]`,`( )` استفاده نکنید.
5. کد را به کامنت نکنید! فقط حذف ش کنید.
6. از کامنت به عنوان توضیح بیشتر در مورد **قصد و هدف** خود استفاده کنید.
7. از کامنت به عنوان **شفاف کننده** کد استفاده کنید.
8. به عنوان یک **هشدار**، در مورد عواقب تغییر استفاده کنید.

## تست‌ها

1. هر تست (بهتر است) **فقط یک** assertion داشته باشد. ([One Assertion Per Test][One Assertion Per Test])
2. از قوانین [F.I.R.S.T][F.I.R.S.T] پیروی کنید.
    1. تست های شما باید **به سرعت اجرا** شوند، حتی اگر 1000 تا باشد. ([Fast][Fast])
    2. تست های شما باید **ایزوله** و **مستقل** باشند و هیچ چیزی اعم از سیستم عامل، متغیر های محیطی، کدهای برنامه نویس دیگر، نباید در نحوه ی کار آنها اختلال ایجاد کند. ([Isolated/Independent][Isolated/Independent])
    3. تست های شما باید **قطعی** و **تکرار پذیر** باشند، متغیر های آنها نباید در محیط های مختلف تغییر کند. ([Repeatable][Repeatable])
    4. ([Self-validating][Self-validating])
3. تست های شما باید به سادگی **خوانده** و **درک** شوند. ([Readability][Readability])

## هندل کردن اررورها

1. هیچگاه error handling را با کد logic ترکیب نکنید.
2. از Exception ها به جای بازگرداندن error code استفاده کنید.
3. هیچگاه null ریترن نکنید یا به تابعی به عنوان پارامتر، null ارسال نکنید.
4. همیشه Exception را با یک توضیح کامل از خطا ارائه کنید.

</div>

[//]: # (قوانین عمومی)
[Standard Conventions]:https://www.google.com/search?q=standard+conventions+in+programming&client=firefox-b-d&sca_esv=600337699&bih=1247&biw=2560&hl=en&sxsrf=ACQVn09-2K8ClqJuqNYYCMM7cHuiX7oi7g%3A1705905381441&ei=5QyuZcjGGrmSkdUPkuOIqAc&ved=0ahUKEwiIzZ_isPCDAxU5SaQEHZIxAnUQ4dUDCBA&uact=5&oq=standard+conventions+in+programming&gs_lp=Egxnd3Mtd2l6LXNlcnAiI3N0YW5kYXJkIGNvbnZlbnRpb25zIGluIHByb2dyYW1taW5nMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSN0cUNobWNobcAJ4AZABAJgBAKABAKoBALgBA8gBAPgBAeIDBBgAIEGIBgGQBgk&sclient=gws-wiz-serp
[KISS]:https://www.google.com/search?client=firefox-b-d&sca_esv=600337699&sxsrf=ACQVn0-f1COpOvs7Bsqh0sedjHE1IlpiAg:1705904803111&q=KISS+principle+in+programming&spell=1&sa=X&ved=2ahUKEwi4mb3OrvCDAxV_SKQEHfoRBX0QirwEKAB6BAgOEAI&biw=2560&bih=1287&dpr=1.5
[Boy Scout]:https://www.google.com/search?client=firefox-b-d&q=Boy+scout+principle
[RCA]:https://www.google.com/search?q=RCA+principle+in+programming&source=lmns&bih=1287&biw=1110&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwi-iJi7sPCDAxX1caQEHQesCC4Q0pQJKAB6BAgBEAI

[//]: # (قوانین طراحی)
[Configurable Data At High Levels]:https://www.google.com/search?q=Keep+Configurable+Data+At+High+Levels&client=firefox-b-d&sca_esv=5c40852b81bce253&sxsrf=ACQVn080Vtmpoaci5xNevh2PdaAOilZKjA%3A1706983826718&ei=koG-Ze-9K7mpi-gP8vangAg&ved=0ahUKEwjvzoOl4o-EAxW51AIHHXL7CYAQ4dUDCBA&oq=Keep+Configurable+Data+At+High+Levels&gs_lp=Egxnd3Mtd2l6LXNlcnAiJUtlZXAgQ29uZmlndXJhYmxlIERhdGEgQXQgSGlnaCBMZXZlbHMyBBAjGCcyBBAjGCcyBBAjGCcyBRAAGIAEMgYQABgWGB4yCxAAGIAEGIoFGIYDMgsQABiABBiKBRiGA0itNlD_BViSCXACeAGQAQCYAa8DoAHcBaoBBTMtMS4xuAEMyAEA-AEBwgIKEAAYRxjWBBiwA-IDBBgAIEGIBgGQBgQ&sclient=gws-wiz-serp
[Polymorphism]:https://www.google.com/search?q=polymorphism+futear+in+oop&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1183&biw=1151&hl=en&sxsrf=ACQVn0-uE1COXoqtBRAbQGOPfSHZNTWSFg%3A1708290022391&ei=5m_SZdeoF6Lpi-gP5JyB0AU&ved=0ahUKEwjXs9Sf5LWEAxWi9AIHHWROAFoQ4dUDCBA&uact=5&oq=polymorphism+futear+in+oop&gs_lp=Egxnd3Mtd2l6LXNlcnAiGnBvbHltb3JwaGlzbSBmdXRlYXIgaW4gb29wMgcQIRgKGKABMgcQIRgKGKABSMJRUJwBWKpPcAR4AZABAJgBtgOgAeEsqgEHMi03LjguMrgBA8gBAPgBAvgBAcICChAAGEcY1gQYsAPCAgoQIxiABBiKBRgnwgIEECMYJ8ICCxAAGIAEGIoFGJECwgIFEAAYgATCAgoQABiABBgUGIcCwgIGEAAYFhgewgILEAAYgAQYigUYhgPCAgUQIRigAcICBBAhGBXCAgUQIRifBYgGAZAGAg&sclient=gws-wiz-serp
[Replace Conditional With Polymorphism]:https://www.google.com/search?client=firefox-b-d&q=Replace+Conditional+With+Polymorphism
[Separate multi-threading code]:https://www.google.com/search?q=Separate+multi-threading+code&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn09X2CR4qE8xGzmdGuUp6tHq8mJMyg%3A1708072409625&ei=2R3PZe7kJbqLi-gP5Z2L4A0&ved=0ahUKEwiutefJua-EAxW6xQIHHeXOAtwQ4dUDCBA&uact=5&oq=Separate+multi-threading+code&gs_lp=Egxnd3Mtd2l6LXNlcnAiHVNlcGFyYXRlIG11bHRpLXRocmVhZGluZyBjb2RlMgoQIxiABBiKBRgnMgQQIxgnMgsQABiABBiKBRiGAzILEAAYgAQYigUYhgMyCxAAGIAEGIoFGIYDSLtiUO8FWN43cAF4AZABAJgBmAOgAeMKqgEHMi0xLjIuMbgBA8gBAPgBAcICChAAGEcY1gQYsAPCAggQABiABBiiBMICBRAhGKABwgIGEAAYFhgeiAYBkAYI&sclient=gws-wiz-serp
[open-closed]:https://www.google.com/search?q=open-closed+principle&source=lmns&bih=1183&biw=1151&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwjoj8LT9Y-EAxUYTKQEHSZjA-kQ0pQJKAB6BAgBEAI
[Prevent Over-Configurability]:https://www.google.com/search?q=prevent+over-configurability+in+software+development&client=firefox-b-d&sca_esv=600673538&hl=en&sxsrf=ACQVn0_HaGEsvW-AJSqm3jLZnxJfiDN5tQ%3A1705998019031&ei=w3avZeu0AeiJi-gPn-mS4AQ&oq=Prevent+over-configurability&gs_lp=Egxnd3Mtd2l6LXNlcnAiHFByZXZlbnQgb3Zlci1jb25maWd1cmFiaWxpdHkqAggAMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSPIWUABYAHABeAGQAQCYAQCgAQCqAQC4AQHIAQDiAwQYACBBiAYBkAYJ&sclient=gws-wiz-serp
[Dependency Injection]:https://www.google.com/search?client=firefox-b-d&q=devpendency+injection
[LoD]:https://www.google.com/search?q=law+of+demeter&client=firefox-b-d&sca_esv=602140452&sxsrf=ACQVn09ybUpL7K4NnL5KzYu0wb69Qfj7jQ%3A1706441247896&ei=Hzq2Zc6TNvaFxc8PktKlqA0&oq=principle+of+least+knowledge&gs_lp=Egxnd3Mtd2l6LXNlcnAiHHByaW5jaXBsZSBvZiBsZWFzdCBrbm93bGVkZ2VI0gNQAFgAcAB4AJABAJgBAKABAKoBALgBA8gBAOIDBBgAIEE&sclient=gws-wiz-serp&ved=0ahUKEwiOn6SD_f-DAxX2QvEDHRJpCdUQ4dUDCBA&uact=5

[//]: # (قوانین توابع)
[Small]:https://www.google.com/search?q=+small++rule+of+functions+&client=firefox-b-d&sca_esv=c24955e436027d1c&sxsrf=ACQVn08IXETC0FckjJDc1YsYF92aVKau5g%3A1708031089377&ei=cXzOZfDJFqLsi-gP_by0IA&ved=0ahUKEwiwxuPSn66EAxUi9gIHHX0eDQQQ4dUDCBA&uact=5&oq=+small++rule+of+functions+&gs_lp=Egxnd3Mtd2l6LXNlcnAiGiBzbWFsbCAgcnVsZSBvZiBmdW5jdGlvbnMgMgUQIRigATIFECEYoAEyBRAhGKABSIRaUOYFWPxUcAN4AZABAJgB9QKgAeMOqgEFMi0yLjS4AQPIAQD4AQH4AQLCAgoQABhHGNYEGLADwgIIECEYoAEYwwTCAggQABiABBiiBMICBRAhGJ8FiAYBkAYH&sclient=gws-wiz-serp
[Do one thing]:https://www.google.com/search?q=Do+one+thing+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0-V5wFF7rOe1Cu1OYL-mCbvCrGTZA%3A1708072429211&ei=7R3PZe7DDOiLi-gP2beN-As&ved=0ahUKEwiu7pLTua-EAxXoxQIHHdlbA78Q4dUDCBA&uact=5&oq=Do+one+thing+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiGERvIG9uZSB0aGluZyBpbiBmdW5jdGlvbjIGEAAYFhgeMggQABgWGB4YDzILEAAYgAQYigUYhgNIyD9Q8gdY6DtwAngBkAEAmAHiCqAB-TeqAQ0yLTIuMy4zLjIuMi4xuAEDyAEA-AEC-AEBwgIHECMYsAMYJ8ICChAAGEcY1gQYsAPCAgUQABiABMICBRAuGIAEwgIIEAAYFhgeGArCAgUQIRigAcICBxAhGAoYoAGIBgGQBgk&sclient=gws-wiz-serp
[Use descriptive names]:https://www.google.com/search?q=Use+descriptive+names+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0-iwuzevH6Ep8eTkIAUZu28-bA_og%3A1708072476918&ei=HB7PZf3RN4_0i-gPsqqKoAU&ved=0ahUKEwj9z_Lpua-EAxUP-gIHHTKVAlQQ4dUDCBA&uact=5&oq=Use+descriptive+names+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIVVzZSBkZXNjcmlwdGl2ZSBuYW1lcyBpbiBmdW5jdGlvbjIIECEYoAEYwwRI1gtQAFgAcAB4AZABAJgB0gKgAdICqgEDMy0xuAEDyAEA-AEC-AEB&sclient=gws-wiz-serp
[Prefer fewer arguments]:https://www.google.com/search?q=Prefer+fewer+arguments+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0967KaRB29ve3UeOwfFxqD2wkR-iQ%3A1708072552083&ei=aB7PZaHjBMLsi-gP3pyaoA4&ved=0ahUKEwiht96Nuq-EAxVC9gIHHV6OBuQQ4dUDCBA&uact=5&oq=Prefer+fewer+arguments+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIlByZWZlciBmZXdlciBhcmd1bWVudHMgaW4gZnVuY3Rpb24yCBAhGKABGMMESIbeA1Ci2ANYotgDcAZ4AZABAJgBsAKgAbACqgEDMy0xuAEDyAEA-AEC-AEBwgIKEAAYRxjWBBiwA4gGAZAGCA&sclient=gws-wiz-serp
[Niladic]:https://www.google.com/search?q=niladic+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1183&biw=1151&hl=en&sxsrf=ACQVn086g_f0nhc2nvxLG2z1wLQx_L2T_A%3A1708288578124&ei=QmrSZfKbB5uekdUP3aSwqAc&ved=0ahUKEwjyxP3u3rWEAxUbT6QEHV0SDHUQ4dUDCBA&uact=5&oq=niladic+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiEG5pbGFkaWMgZnVuY3Rpb24yBRAAGIAEMgQQABgeMgYQABgeGA9IwZ8DUP-XA1j_lwNwAngBkAEAmAH7AqAB-wKqAQMzLTG4AQPIAQD4AQL4AQHCAgoQABhHGNYEGLADiAYBkAYI&sclient=gws-wiz-serp
[Have no side effects]:https://www.google.com/search?q=Have+no+side+effects+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=699&biw=968&hl=en&sxsrf=ACQVn0-7OvVS0EKkEM0yIC3iVSCh5k7jPw%3A1708072615689&ei=px7PZeiaKcbmi-gP-LSCuAI&ved=0ahUKEwioioisuq-EAxVG8wIHHXiaACcQ4dUDCBA&uact=5&oq=Have+no+side+effects+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIEhhdmUgbm8gc2lkZSBlZmZlY3RzIGluIGZ1bmN0aW9uMggQIRigARjDBEi0mgZQspMGWKWYBnADeAGQAQCYAd4CoAHeAqoBAzMtMbgBA8gBAPgBAvgBAcICChAAGEcY1gQYsAOIBgGQBgg&sclient=gws-wiz-serp

[//]: # (قوانین کامنت‌ها)


[//]: # (تست ها)
[One Assertion Per Test]:https://www.google.com/search?q=One+assert+per+test+principel&client=firefox-b-d&sca_esv=601759512&sxsrf=ACQVn0_pHHKj3NR9hJjKQTgAls9Ctm4OaA%3A1706288379195&ei=--SzZdO-C82Hxc8P8Kic-AQ&ved=0ahUKEwiTqOfFw_uDAxXNQ_EDHXAUB08Q4dUDCBA&uact=5&oq=One+assert+per+test+principel&gs_lp=Egxnd3Mtd2l6LXNlcnAiHU9uZSBhc3NlcnQgcGVyIHRlc3QgcHJpbmNpcGVsSMIyUABY3S1wAHgBkAEAmAEAoAEAqgEAuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp
[F.I.R.S.T]:https://www.google.com/search?q=F.I.R.S.T+principles+of+testing&client=firefox-b-d&sca_esv=602429663&sxsrf=ACQVn0_qC-m4AhcZzqiKkabWGtRZCwSaxw%3A1706557902727&ei=zgG4ZYyIK-CYi-gPs4eRyAI&ved=0ahUKEwiMp9HMr4OEAxVgzAIHHbNDBCkQ4dUDCBA&uact=5&oq=F.I.R.S.T+principles+of+testing&gs_lp=Egxnd3Mtd2l6LXNlcnAiH0YuSS5SLlMuVCBwcmluY2lwbGVzIG9mIHRlc3RpbmcyBRAAGIAEMgsQABiABBiKBRiGAzILEAAYgAQYigUYhgNI_ANQAFgAcAB4AZABAJgBnAKgAZwCqgEDMi0xuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp
[Fast]:https://www.google.com/search?client=firefox-b-d&q=Fast+principle+in+teting
[Isolated/Independent]:https://www.google.com/search?q=isolation+in+testing&client=firefox-b-d&sca_esv=5ee345275e04b3bb&sxsrf=ACQVn0-nhUyEHNmtORK6i2FCDChzXkt1BQ%3A1707244106997&ei=SnrCZeS2PMeqkdUPkPa2qAM&oq=isolation+in+testing&gs_lp=Egxnd3Mtd2l6LXNlcnAiFGlzb2xhdGlvbiBpbiB0ZXN0aW5nKgIIADIEEAAYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHkjkPVCsDViAMXAPeACQAQGYAYYDoAGZCaoBBTItMy4xuAEByAEA-AEBwgIKEAAYRxjWBBiwA8ICCBAAGIAEGKIEwgIHEAAYgAQYDcICCBAhGKABGMMEwgIGEAAYBxgewgIIEAAYBxgeGA_CAggQABgFGAcYHsICCBAAGAgYBxgewgIJEAAYgAQYDRgK4gMEGAAgQYgGAZAGCA&sclient=gws-wiz-serp
[Readability]:https://www.google.com/search?q=Readability+in+tests&client=firefox-b-d&sca_esv=8cd01c0eb9e4bd98&sxsrf=ACQVn09VDxYVnWFCnly9aunTQaKwXZzw2g%3A1707077737717&ei=afC_ZYi0K7SLi-gPraeNkAk&ved=0ahUKEwjIjKSRwJKEAxW0xQIHHa1TA5IQ4dUDCBA&uact=5&oq=Readability+in+tests&gs_lp=Egxnd3Mtd2l6LXNlcnAiFFJlYWRhYmlsaXR5IGluIHRlc3RzMgQQIxgnMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeSNwVUL0GWKUTcAN4AJABAZgBnAOgAbYMqgEHMi0yLjIuMbgBA8gBAPgBAcICChAAGEcY1gQYsAPiAwQYACBBiAYBkAYI&sclient=gws-wiz-serp
[Self-validating]:https://www.google.com/search?client=firefox-b-d&q=Self-validating+in+testing#ip=1
[Repeatable]:https://www.google.com/search?client=firefox-b-d&q=Repeatable+in+testing+