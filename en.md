<div style="text-align: center;">
  <img src="https://github.com/alisalehi1380/Key-points-of-clean-code/assets/111766206/4185b039-6045-4133-9341-e80e18be074a" style="min-height: 600px;"/>
</div>

Clean code that is easily understood by all team members. Clean code can be read and developed by a developer other than its author. Code readability, maintainability, modifiability, and extensibility are only possible when you properly understand how the code works.
_____________________________________

## General rules

1. Follow **standard rules** such as naming classes and functions, the amount of indentation, etc. ([Standard Conventions][Standard Conventions])
2. **Reduce** the **complexity** in the code as much as possible. Simplicity is always better. (Law [KISS][KISS])
3. Deliver source code **cleaner** than when you receive it. (Law [Boy Scout][Boy Scout Law])
4. Always look for **finding problems and bugs** in the code. To fix them, identify **main and root causes**. (Act [RCA][RCA])

## Design rules

1. Variables, constants and all configurable data must be at the **highest level of abstraction**. ([Configurable Data At High Levels][Configurable Data At High Levels])
2. Instead of **breaking** the [open-closed][open-closed] rule, use the [polymorphism][polymorphism] property. ([Replace Conditional With Polymorphism][Replace Conditional With Polymorphism])
3. ([Separate multi-threading code][Separate multi-threading code])
4. Avoid giving your application developers too much freedom of action. ([Prevent Over-Configurability][Prevent Over-Configurability])
5. Instead of creating objects (using new), use **dependency injection**. ([Dependency Injection][Dependency Injection])
6. Functions and classes should not have **access** to other details in the code except what they do. (Law [LoD][LoD])

## Rules of functions

1. Your functions should be **small**. ([Small][Small])
2. Each function should do **one thing** only. ([Do one thing][Do one thing])
3. The name you choose for each function should fully describe **what it does**. ([Use descriptive names][Use descriptive names])
4. The best function is the Niladic function ([Niladic][Niladic]). Your function should take the fewest **arguments** possible. ([Prefer fewer arguments][Prefer fewer arguments])
5. Your function should not change anything that is **outside** its scope. ([Have no side effects][Have no side effects])

## Comments rules

1. Always try to **explain yourself in code**. If it's not possible, take your time to write a good comment.
2. Don't be redundant (e.g.: `i++; // increment i`).
3. Don't add obvious noise.
4. Don't use closing brace comments (e.g.: `} // end of function`).
5. **Don't comment out code**. Just remove.
6. Use as **explanation of intent**.
7. Use as **clarification of code**.
8. Use as **warning of consequences**.

## Tests

1. Each test (it is better) to have **just one** assertion. ([One Assertion Per Test][One Assertion Per Test])
2. Follow the [F.I.R.S.T][F.I.R.S.T] rules.
   1. Your tests must **run quickly**, even if there are 1000 of them. ([Fast][Fast])
   2. Your tests should be **isolated** and **independent** and nothing, including the operating system, environment variables, other programmer's codes, should interfere with their work. ([Isolated/Independent][Isolated/Independent])
   3. Your tests should be **conclusive** and **repeatable**, their variables should not change in different environments. ([Repeatable][Repeatable])
   4. ([Self-validating][Self-validating])
3. Your tests should be easy to **read** and **understand**. ([Readability][Readability])

## Error handling

1. **Don't mix** error handling and code.
2. Use **Exceptions** instead of returning error codes.
3. **Don't return null**, don't pass null either.
4. Throw exceptions **with context**.


[//]: # (General rules)
[Standard Conventions]:https://www.google.com/search?q=standard+conventions+in+programming&client=firefox-b-d&sca_esv=600337699&bih=1247&biw=2560&hl=en&sxsrf=ACQVn09-2K8ClqJuqNYYCMM7cHuiX7oi7g%3A1705905381441&ei=5QyuZcjGGrmSkdUPkuOIqAc&ved=0ahUKEwiIzZ_isPCDAxU5SaQEHZIxAnUQ4dUDCBA&uact=5&oq=standard+conventions+in+programming&gs_lp=Egxnd3Mtd2l6LXNlcnAiI3N0YW5kYXJkIGNvbnZlbnRpb25zIGluIHByb2dyYW1taW5nMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSN0cUNobWNobcAJ4AZABAJgBAKABAKoBALgBA8gBAPgBAeIDBBgAIEGIBgGQBgk&sclient=gws-wiz-serp
[KISS]:https://www.google.com/search?client=firefox-b-d&sca_esv=600337699&sxsrf=ACQVn0-f1COpOvs7Bsqh0sedjHE1IlpiAg:1705904803111&q=KISS+principle+in+programming&spell=1&sa=X&ved=2ahUKEwi4mb3OrvCDAxV_SKQEHfoRBX0QirwEKAB6BAgOEAI&biw=2560&bih=1287&dpr=1.5
[Boy Scout Law]:https://www.google.com/search?client=firefox-b-d&q=Boy+scout+principle
[RCA]:https://www.google.com/search?q=RCA+principle+in+programming&source=lmns&bih=1287&biw=1110&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwi-iJi7sPCDAxX1caQEHQesCC4Q0pQJKAB6BAgBEAI

[//]: # (Structure rules)
[Configurable Data At High Levels]:https://www.google.com/search?q=Keep+Configurable+Data+At+High+Levels&client=firefox-b-d&sca_esv=5c40852b81bce253&sxsrf=ACQVn080Vtmpoaci5xNevh2PdaAOilZKjA%3A1706983826718&ei=koG-Ze-9K7mpi-gP8vangAg&ved=0ahUKEwjvzoOl4o-EAxW51AIHHXL7CYAQ4dUDCBA&oq=Keep+Configurable+Data+At+High+Levels&gs_lp=Egxnd3Mtd2l6LXNlcnAiJUtlZXAgQ29uZmlndXJhYmxlIERhdGEgQXQgSGlnaCBMZXZlbHMyBBAjGCcyBBAjGCcyBBAjGCcyBRAAGIAEMgYQABgWGB4yCxAAGIAEGIoFGIYDMgsQABiABBiKBRiGA0itNlD_BViSCXACeAGQAQCYAa8DoAHcBaoBBTMtMS4xuAEMyAEA-AEBwgIKEAAYRxjWBBiwA-IDBBgAIEGIBgGQBgQ&sclient=gws-wiz-serp
[Polymorphism]:https://www.google.com/search?q=polymorphism+futear+in+oop&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1183&biw=1151&hl=en&sxsrf=ACQVn0-uE1COXoqtBRAbQGOPfSHZNTWSFg%3A1708290022391&ei=5m_SZdeoF6Lpi-gP5JyB0AU&ved=0ahUKEwjXs9Sf5LWEAxWi9AIHHWROAFoQ4dUDCBA&uact=5&oq=polymorphism+futear+in+oop&gs_lp=Egxnd3Mtd2l6LXNlcnAiGnBvbHltb3JwaGlzbSBmdXRlYXIgaW4gb29wMgcQIRgKGKABMgcQIRgKGKABSMJRUJwBWKpPcAR4AZABAJgBtgOgAeEsqgEHMi03LjguMrgBA8gBAPgBAvgBAcICChAAGEcY1gQYsAPCAgoQIxiABBiKBRgnwgIEECMYJ8ICCxAAGIAEGIoFGJECwgIFEAAYgATCAgoQABiABBgUGIcCwgIGEAAYFhgewgILEAAYgAQYigUYhgPCAgUQIRigAcICBBAhGBXCAgUQIRifBYgGAZAGAg&sclient=gws-wiz-serp
[Replace Conditional With Polymorphism]:https://www.google.com/search?client=firefox-b-d&q=Replace+Conditional+With+Polymorphism
[Separate multi-threading code]:https://www.google.com/search?q=Separate+multi-threading+code&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn09X2CR4qE8xGzmdGuUp6tHq8mJMyg%3A1708072409625&ei=2R3PZe7kJbqLi-gP5Z2L4A0&ved=0ahUKEwiutefJua-EAxW6xQIHHeXOAtwQ4dUDCBA&uact=5&oq=Separate+multi-threading+code&gs_lp=Egxnd3Mtd2l6LXNlcnAiHVNlcGFyYXRlIG11bHRpLXRocmVhZGluZyBjb2RlMgoQIxiABBiKBRgnMgQQIxgnMgsQABiABBiKBRiGAzILEAAYgAQYigUYhgMyCxAAGIAEGIoFGIYDSLtiUO8FWN43cAF4AZABAJgBmAOgAeMKqgEHMi0xLjIuMbgBA8gBAPgBAcICChAAGEcY1gQYsAPCAggQABiABBiiBMICBRAhGKABwgIGEAAYFhgeiAYBkAYI&sclient=gws-wiz-serp
[open-closed]:https://www.google.com/search?q=open-closed+principle&source=lmns&bih=1183&biw=1151&client=firefox-b-d&hl=en&sa=X&ved=2ahUKEwjoj8LT9Y-EAxUYTKQEHSZjA-kQ0pQJKAB6BAgBEAI
[Prevent Over-Configurability]:https://www.google.com/search?q=prevent+over-configurability+in+software+development&client=firefox-b-d&sca_esv=600673538&hl=en&sxsrf=ACQVn0_HaGEsvW-AJSqm3jLZnxJfiDN5tQ%3A1705998019031&ei=w3avZeu0AeiJi-gPn-mS4AQ&oq=Prevent+over-configurability&gs_lp=Egxnd3Mtd2l6LXNlcnAiHFByZXZlbnQgb3Zlci1jb25maWd1cmFiaWxpdHkqAggAMgcQIxiwAxgnMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADMgoQABhHGNYEGLADSPIWUABYAHABeAGQAQCYAQCgAQCqAQC4AQHIAQDiAwQYACBBiAYBkAYJ&sclient=gws-wiz-serp
[Dependency Injection]:https://www.google.com/search?client=firefox-b-d&q=devpendency+injection
[LoD]:https://www.google.com/search?q=law+of+demeter&client=firefox-b-d&sca_esv=602140452&sxsrf=ACQVn09ybUpL7K4NnL5KzYu0wb69Qfj7jQ%3A1706441247896&ei=Hzq2Zc6TNvaFxc8PktKlqA0&oq=principle+of+least+knowledge&gs_lp=Egxnd3Mtd2l6LXNlcnAiHHByaW5jaXBsZSBvZiBsZWFzdCBrbm93bGVkZ2VI0gNQAFgAcAB4AJABAJgBAKABAKoBALgBA8gBAOIDBBgAIEE&sclient=gws-wiz-serp&ved=0ahUKEwiOn6SD_f-DAxX2QvEDHRJpCdUQ4dUDCBA&uact=5

[//]: # (Function rules)
[Small]:https://www.google.com/search?q=+small++rule+of+functions+&client=firefox-b-d&sca_esv=c24955e436027d1c&sxsrf=ACQVn08IXETC0FckjJDc1YsYF92aVKau5g%3A1708031089377&ei=cXzOZfDJFqLsi-gP_by0IA&ved=0ahUKEwiwxuPSn66EAxUi9gIHHX0eDQQQ4dUDCBA&uact=5&oq=+small++rule+of+functions+&gs_lp=Egxnd3Mtd2l6LXNlcnAiGiBzbWFsbCAgcnVsZSBvZiBmdW5jdGlvbnMgMgUQIRigATIFECEYoAEyBRAhGKABSIRaUOYFWPxUcAN4AZABAJgB9QKgAeMOqgEFMi0yLjS4AQPIAQD4AQH4AQLCAgoQABhHGNYEGLADwgIIECEYoAEYwwTCAggQABiABBiiBMICBRAhGJ8FiAYBkAYH&sclient=gws-wiz-serp
[Do one thing]:https://www.google.com/search?q=Do+one+thing+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0-V5wFF7rOe1Cu1OYL-mCbvCrGTZA%3A1708072429211&ei=7R3PZe7DDOiLi-gP2beN-As&ved=0ahUKEwiu7pLTua-EAxXoxQIHHdlbA78Q4dUDCBA&uact=5&oq=Do+one+thing+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiGERvIG9uZSB0aGluZyBpbiBmdW5jdGlvbjIGEAAYFhgeMggQABgWGB4YDzILEAAYgAQYigUYhgNIyD9Q8gdY6DtwAngBkAEAmAHiCqAB-TeqAQ0yLTIuMy4zLjIuMi4xuAEDyAEA-AEC-AEBwgIHECMYsAMYJ8ICChAAGEcY1gQYsAPCAgUQABiABMICBRAuGIAEwgIIEAAYFhgeGArCAgUQIRigAcICBxAhGAoYoAGIBgGQBgk&sclient=gws-wiz-serp
[Use descriptive names]:https://www.google.com/search?q=Use+descriptive+names+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0-iwuzevH6Ep8eTkIAUZu28-bA_og%3A1708072476918&ei=HB7PZf3RN4_0i-gPsqqKoAU&ved=0ahUKEwj9z_Lpua-EAxUP-gIHHTKVAlQQ4dUDCBA&uact=5&oq=Use+descriptive+names+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIVVzZSBkZXNjcmlwdGl2ZSBuYW1lcyBpbiBmdW5jdGlvbjIIECEYoAEYwwRI1gtQAFgAcAB4AZABAJgB0gKgAdICqgEDMy0xuAEDyAEA-AEC-AEB&sclient=gws-wiz-serp
[Prefer fewer arguments]:https://www.google.com/search?q=Prefer+fewer+arguments+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1184&biw=2304&hl=en&sxsrf=ACQVn0967KaRB29ve3UeOwfFxqD2wkR-iQ%3A1708072552083&ei=aB7PZaHjBMLsi-gP3pyaoA4&ved=0ahUKEwiht96Nuq-EAxVC9gIHHV6OBuQQ4dUDCBA&uact=5&oq=Prefer+fewer+arguments+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIlByZWZlciBmZXdlciBhcmd1bWVudHMgaW4gZnVuY3Rpb24yCBAhGKABGMMESIbeA1Ci2ANYotgDcAZ4AZABAJgBsAKgAbACqgEDMy0xuAEDyAEA-AEC-AEBwgIKEAAYRxjWBBiwA4gGAZAGCA&sclient=gws-wiz-serp
[Niladic]:https://www.google.com/search?q=niladic+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=1183&biw=1151&hl=en&sxsrf=ACQVn086g_f0nhc2nvxLG2z1wLQx_L2T_A%3A1708288578124&ei=QmrSZfKbB5uekdUP3aSwqAc&ved=0ahUKEwjyxP3u3rWEAxUbT6QEHV0SDHUQ4dUDCBA&uact=5&oq=niladic+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiEG5pbGFkaWMgZnVuY3Rpb24yBRAAGIAEMgQQABgeMgYQABgeGA9IwZ8DUP-XA1j_lwNwAngBkAEAmAH7AqAB-wKqAQMzLTG4AQPIAQD4AQL4AQHCAgoQABhHGNYEGLADiAYBkAYI&sclient=gws-wiz-serp
[Have no side effects]:https://www.google.com/search?q=Have+no+side+effects+in+function&client=firefox-b-d&sca_esv=c3f7936c6fd1a8dc&bih=699&biw=968&hl=en&sxsrf=ACQVn0-7OvVS0EKkEM0yIC3iVSCh5k7jPw%3A1708072615689&ei=px7PZeiaKcbmi-gP-LSCuAI&ved=0ahUKEwioioisuq-EAxVG8wIHHXiaACcQ4dUDCBA&uact=5&oq=Have+no+side+effects+in+function&gs_lp=Egxnd3Mtd2l6LXNlcnAiIEhhdmUgbm8gc2lkZSBlZmZlY3RzIGluIGZ1bmN0aW9uMggQIRigARjDBEi0mgZQspMGWKWYBnADeAGQAQCYAd4CoAHeAqoBAzMtMbgBA8gBAPgBAvgBAcICChAAGEcY1gQYsAOIBgGQBgg&sclient=gws-wiz-serp

[//]: # (Tests)
[One Assertion Per Test]:https://www.google.com/search?q=One+assert+per+test+principel&client=firefox-b-d&sca_esv=601759512&sxsrf=ACQVn0_pHHKj3NR9hJjKQTgAls9Ctm4OaA%3A1706288379195&ei=--SzZdO-C82Hxc8P8Kic-AQ&ved=0ahUKEwiTqOfFw_uDAxXNQ_EDHXAUB08Q4dUDCBA&uact=5&oq=One+assert+per+test+principel&gs_lp=Egxnd3Mtd2l6LXNlcnAiHU9uZSBhc3NlcnQgcGVyIHRlc3QgcHJpbmNpcGVsSMIyUABY3S1wAHgBkAEAmAEAoAEAqgEAuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp
[F.I.R.S.T]:https://www.google.com/search?q=F.I.R.S.T+principles+of+testing&client=firefox-b-d&sca_esv=602429663&sxsrf=ACQVn0_qC-m4AhcZzqiKkabWGtRZCwSaxw%3A1706557902727&ei=zgG4ZYyIK-CYi-gPs4eRyAI&ved=0ahUKEwiMp9HMr4OEAxVgzAIHHbNDBCkQ4dUDCBA&uact=5&oq=F.I.R.S.T+principles+of+testing&gs_lp=Egxnd3Mtd2l6LXNlcnAiH0YuSS5SLlMuVCBwcmluY2lwbGVzIG9mIHRlc3RpbmcyBRAAGIAEMgsQABiABBiKBRiGAzILEAAYgAQYigUYhgNI_ANQAFgAcAB4AZABAJgBnAKgAZwCqgEDMi0xuAEDyAEA-AEC-AEB4gMEGAAgQQ&sclient=gws-wiz-serp
[Fast]:https://www.google.com/search?client=firefox-b-d&q=Fast+principle+in+teting
[Isolated/Independent]:https://www.google.com/search?q=isolation+in+testing&client=firefox-b-d&sca_esv=5ee345275e04b3bb&sxsrf=ACQVn0-nhUyEHNmtORK6i2FCDChzXkt1BQ%3A1707244106997&ei=SnrCZeS2PMeqkdUPkPa2qAM&oq=isolation+in+testing&gs_lp=Egxnd3Mtd2l6LXNlcnAiFGlzb2xhdGlvbiBpbiB0ZXN0aW5nKgIIADIEEAAYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHjIGEAAYCBgeMgYQABgIGB4yBhAAGAgYHkjkPVCsDViAMXAPeACQAQGYAYYDoAGZCaoBBTItMy4xuAEByAEA-AEBwgIKEAAYRxjWBBiwA8ICCBAAGIAEGKIEwgIHEAAYgAQYDcICCBAhGKABGMMEwgIGEAAYBxgewgIIEAAYBxgeGA_CAggQABgFGAcYHsICCBAAGAgYBxgewgIJEAAYgAQYDRgK4gMEGAAgQYgGAZAGCA&sclient=gws-wiz-serp
[Readability]:https://www.google.com/search?q=Readability+in+tests&client=firefox-b-d&sca_esv=8cd01c0eb9e4bd98&sxsrf=ACQVn09VDxYVnWFCnly9aunTQaKwXZzw2g%3A1707077737717&ei=afC_ZYi0K7SLi-gPraeNkAk&ved=0ahUKEwjIjKSRwJKEAxW0xQIHHa1TA5IQ4dUDCBA&uact=5&oq=Readability+in+tests&gs_lp=Egxnd3Mtd2l6LXNlcnAiFFJlYWRhYmlsaXR5IGluIHRlc3RzMgQQIxgnMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeMgYQABgWGB4yBhAAGBYYHjIGEAAYFhgeSNwVUL0GWKUTcAN4AJABAZgBnAOgAbYMqgEHMi0yLjIuMbgBA8gBAPgBAcICChAAGEcY1gQYsAPiAwQYACBBiAYBkAYI&sclient=gws-wiz-serp
[Self-validating]:https://www.google.com/search?client=firefox-b-d&q=Self-validating+in+testing#ip=1
[Repeatable]:https://www.google.com/search?client=firefox-b-d&q=Repeatable+in+testing+
