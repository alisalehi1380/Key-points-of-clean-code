<div dir="rtl">
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
3.
4. از **بیش از اندازه** دادنِ آزادی عمل به توسعه دهنده های برنامه خود جلوگیری کنید. ([Prevent Over-Configurability][Prevent Over-Configurability])
5. به جای ساخت آبجکت (با استفاده از new)، از **تزریق وابستگی** استفاده کنید. ([Dependency Injection][Dependency Injection])
6. توابع و کلاس ها به جز کاری که انجام میدهند، **نباید** به جزئیات دیگری در کد دسترسی داشته باشند. (قانون [LoD][LoD])

## تست ها

1. هر تست (بهتر است) **فقط یک** assertion داشته باشد. ([One Assertion Per Test][One Assertion Per Test])
2. از قوانین [F.I.R.S.T][F.I.R.S.T] پیروی کنید.

---

### مشارکت در پروژه

لطفا به ریپوی [Summery Of Clean Code][Summery Of Clean Code] مراجعه فرمایید.
</div>

[//]: # (قوانین عمومی)
[Standard Conventions]:https://www.google.com/search?q=standard+conventions+in+programming&client=firefox-b-d&sca_esv=600337699&bih=1247&biw=2560&hl=en&sxsrf=ACQVn09-2K8ClqJuqNYYCMM7cHuiX7oi7g%3A1705905381441&ei=5QyuZcjGGrmSkdUPkuOIqAc&ved=0ahUKEwiIzZ_isPCDAxU5SaQEHZIxAnUQ4dUDCBA&uact=5&oq=standard+conventions+in+programming&gs_lp=Egxnd3Mtd2l6LXNlcnAiI3N0YW5kYXJkIGNvbnZlbnRpb25zIGluIHByb2dyYW1taW5nMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSN0cUNobWNobcAJ4AZABAJgBAKABAKoBALgBA8gBAPgBAeIDBBgAIEGIBgGQBgk&sclient=gws-wiz-serp
[KISS]:https://www.google.com/search?client=firefox-b-d&sca_esv=600337699&sxsrf=ACQVn0-f1COpOvs7Bsqh0sedjHE1IlpiAg:1705904803111&q=KISS+principle+in+programming&spell=1&sa=X&ved=2ahUKEwi4mb3OrvCDAxV_SKQEHfoRBX0QirwEKAB6BAgOEAI&biw=2560&bih=1287&dpr=1.5
[Boy Scout]:https://www.google.com/search?client=firefox-b-d&q=Boy+scout+principle
[RCA]:https://www.google.com/search?q=RCA+principle+in+programming&source=lmns&bih=1287&biw=1110&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwi-iJi7sPCDAxX1caQEHQesCC4Q0pQJKAB6BAgBEAI

[//]: # (قوانین طراحی)
[Configurable Data At High Levels]:https://www.google.com/search?q=Keep+Configurable+Data+At+High+Levels&client=firefox-b-d&sca_esv=5c40852b81bce253&sxsrf=ACQVn080Vtmpoaci5xNevh2PdaAOilZKjA%3A1706983826718&ei=koG-Ze-9K7mpi-gP8vangAg&ved=0ahUKEwjvzoOl4o-EAxW51AIHHXL7CYAQ4dUDCBA&oq=Keep+Configurable+Data+At+High+Levels&gs_lp=Egxnd3Mtd2l6LXNlcnAiJUtlZXAgQ29uZmlndXJhYmxlIERhdGEgQXQgSGlnaCBMZXZlbHMyBBAjGCcyBBAjGCcyBBAjGCcyBRAAGIAEMgYQABgWGB4yCxAAGIAEGIoFGIYDMgsQABiABBiKBRiGA0itNlD_BViSCXACeAGQAQCYAa8DoAHcBaoBBTMtMS4xuAEMyAEA-AEBwgIKEAAYRxjWBBiwA-IDBBgAIEGIBgGQBgQ&sclient=gws-wiz-serp
[open-closed]:https://www.google.com/search?q=open-closed+principle&source=lmns&bih=1183&biw=1151&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwjoj8LT9Y-EAxUYTKQEHSZjA-kQ0pQJKAB6BAgBEAI
[polymorphism]:https://www.google.com/search?q=polymorphism+software+engineering&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn08cxYv5fgd7CjYxBMJJ8S2orIyZCQ%3A1706989062014&ei=Bpa-Ze8_0KaL6A-JuYWACQ&oq=polymorphism+s&gs_lp=Egxnd3Mtd2l6LXNlcnAiDnBvbHltb3JwaGlzbSBzKgIIADILEAAYgAQYigUYkQIyCxAAGIAEGIoFGJECMgsQABiABBiKBRiRAjILEAAYgAQYigUYkQIyBRAAGIAEMgUQABiABDIFEAAYgAQyBRAAGIAEMgUQABiABDIFEAAYgARI4EFQ1ilYnzNwAngBkAEAmAGDA6ABrwWqAQMzLTK4AQPIAQD4AQHCAgoQABhHGNYEGLADwgINEAAYgAQYigUYQxiwA8ICChAjGIAEGIoFGCfCAgQQIxgnwgIKEAAYgAQYigUYQ8ICCBAAGIAEGMsB4gMEGAAgQYgGAZAGCg&sclient=gws-wiz-serp
[Replace Conditional With Polymorphism]:https://www.google.com/search?client=firefox-b-d&q=Replace+Conditional+With+Polymorphism
[Prevent Over-Configurability]:https://www.google.com/search?q=prevent+over-configurability+in+software+development&client=firefox-b-d&sca_esv=600673538&hl=en&sxsrf=ACQVn0_HaGEsvW-AJSqm3jLZnxJfiDN5tQ%3A1705998019031&ei=w3avZeu0AeiJi-gPn-mS4AQ&oq=Prevent+over-configurability&gs_lp=Egxnd3Mtd2l6LXNlcnAiHFByZXZlbnQgb3Zlci1jb25maWd1cmFiaWxpdHkqAggAMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSPIWUABYAHABeAGQAQCYAQCgAQCqAQC4AQHIAQDiAwQYACBBiAYBkAYJ&sclient=gws-wiz-serp
[Dependency Injection]:https://www.google.com/search?client=firefox-b-d&q=devpendency+injection
[LoD]:https://www.google.com/search?q=law+of+demeter&client=firefox-b-d&sca_esv=602140452&sxsrf=ACQVn09ybUpL7K4NnL5KzYu0wb69Qfj7jQ%3A1706441247896&ei=Hzq2Zc6TNvaFxc8PktKlqA0&oq=principle+of+least+knowledge&gs_lp=Egxnd3Mtd2l6LXNlcnAiHHByaW5jaXBsZSBvZiBsZWFzdCBrbm93bGVkZ2VI0gNQAFgAcAB4AJABAJgBAKABAKoBALgBA8gBAOIDBBgAIEE&sclient=gws-wiz-serp&ved=0ahUKEwiOn6SD_f-DAxX2QvEDHRJpCdUQ4dUDCBA&uact=5

[//]: # (تست ها)
[One Assertion Per Test]:https://www.google.com/search?q=One+assert+per+test+principel&client=firefox-b-d&sca_esv=601759512&sxsrf=ACQVn0_pHHKj3NR9hJjKQTgAls9Ctm4OaA%3A1706288379195&ei=--SzZdO-C82Hxc8P8Kic-AQ&ved=0ahUKEwiTqOfFw_uDAxXNQ_EDHXAUB08Q4dUDCBA&uact=5&oq=One+assert+per+test+principel&gs_lp=Egxnd3Mtd2l6LXNlcnAiHU9uZSBhc3NlcnQgcGVyIHRlc3QgcHJpbmNpcGVsSMIyUABY3S1wAHgBkAEAmAEAoAEAqgEAuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp
[F.I.R.S.T]:https://www.google.com/search?q=F.I.R.S.T+principles+of+testing&client=firefox-b-d&sca_esv=602429663&sxsrf=ACQVn0_qC-m4AhcZzqiKkabWGtRZCwSaxw%3A1706557902727&ei=zgG4ZYyIK-CYi-gPs4eRyAI&ved=0ahUKEwiMp9HMr4OEAxVgzAIHHbNDBCkQ4dUDCBA&uact=5&oq=F.I.R.S.T+principles+of+testing&gs_lp=Egxnd3Mtd2l6LXNlcnAiH0YuSS5SLlMuVCBwcmluY2lwbGVzIG9mIHRlc3RpbmcyBRAAGIAEMgsQABiABBiKBRiGAzILEAAYgAQYigUYhgNI_ANQAFgAcAB4AZABAJgBnAKgAZwCqgEDMi0xuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp


[//]: # (مشارکت در پروژه)
[Summery Of Clean Code]:https://github.com/alisalehi1380/summary-of-clean-code