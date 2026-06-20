# گزارش تغییرات | Changelog

<!-- LANG:FA -->
تمام تغییرات و بروزرسانی‌های پروژه نهان (Project Nahan) در این فایل مستند خواهند شد.
<!-- LANG:FA -->
<!-- LANG:EN -->
All notable changes to Project Nahan will be documented in this file.
<!-- LANG:EN -->

---

## [2.6.1] - ۱۴۰۵-۰۳-۳۰ (2026-06-20)

<!-- LANG:FA -->
### اضافه شده (Added)
- **نام‌گذاری آی‌پی‌های تمیز**: پشتیبانی از فرمت ip:name برای آی‌پی‌های تمیز (مثلاً 1.1.1.1:Cloudflare)
- **متغیر {IP_NAME}**: افزودن متغیر {IP_NAME} به قالب‌های نام کانفیگ برای استفاده از نام اختصاصی آی‌پی
- **جهت LTR برای ورودی آی‌پی‌ها**: تنظیم جهت ورودی آی‌پی‌هایتمیز به چپ به راست برای خوانایی بهتر

### رفع شده (Fixed)

### بهبود یافته (Improved)
- **متن راهنما**: بروزرسانی placeholder و توضیحات آی‌پی‌های تمیز برای مستندسازی فرمت ip:name
<!-- LANG:FA -->

<!-- LANG:EN -->
### Added
- **Named Clean IPs**: Support custom names for Clean IPs using the format `ip:name` (e.g. `1.1.1.1:Cloudflare`)
- **{IP_NAME} Config Placeholder**: Added `{IP_NAME}` placeholder for use in config name strategy templates
- **LTR Input for Clean IPs**: Set Clean IPs textarea direction to left-to-right for better readability

### Fixed

### Improved
- **Help Text**: Updated Clean IPs placeholder and description to document the `ip:name` format
<!-- LANG:EN -->

---

## [2.6.0] - ۱۴۰۵-۰۳-۳۰ (2026-06-20)

<!-- LANG:FA -->
### شکننده (BREAKING CHANGE)
- **تغییر SubscriptionURL**: تمامی SubscriptionURL ها تغییر یافته اند و باید سابسکریپشن جدید در اختیار کاربران خود قرار دهید.

### اضافه شده (Added)
- **افزوده شدن UUID به SubscriptionURL**: افزایش امنیت برای سابسکریپشن های پابلیک - جلوگیری از جعل سابسکریپشن
- **افزوده شدن Subscription Route به پنل**: این مقدار را در تنظیمات، ست کنید.

### رفع شده (Fixed)

### بهبود یافته (Improved)

<!-- LANG:FA -->

<!-- LANG:EN -->
## BREAKING CHANGE
- **SubscriptionURL Change**: All SubscriptionURLs have been changed and you must provide the new subscription to your users.

### Added
- **Added UUID to SubscriptionURL**: Improving subscription security, for public subscriptions. 
- **Added Subscription Route to Control Panel**: Set this value in settings.

### Fixed

### Improved

<!-- LANG:EN -->

---

## [2.5.7] - ۱۴۰۵-۰۳-۲۹ (2026-06-19)

<!-- LANG:FA -->
### اضافه شده (Added)
- **پشتیبان‌گیری هوشمند از مقادیر اختصاصی کاربر**: امکان تنظیم آی‌پی تمیز دلخواه، آی‌پی پروکسی دلخواه و نام کانفیگ دلخواه با قابلیت استخراج خودکار و ادغام هوشمند با مقادیر تنظیم شده جهانی در پنجره‌های ویرایش و افزودن کاربر.
- **نگاشت بلادرنگ پرچم‌ها با api.country.is**: یکپارچه‌سازی وب‌سرویس متن‌باز، رایگان و بدون تحریم api.country.is جهت استخراج پرچم دقیق کشورها برای آدرس‌های آی‌پی پروکسی و تمیز.

### رفع شده (Fixed)
- **حل ناسازگاری آدرس‌های پشت کلودفلر**: رفع خطای عدم لود کامل صفحات و فایل‌های ایستای وب‌سایت‌های پشت کلودفلر (بلاک شدن اتصال به دلیل پراکندگی سشن‌ها) بر روی کلاینت‌هایی با آی‌پی‌های پروکسی متعدد؛ حل شده به کمک مکانیزم هش یکنواخت کاربر (Consistent Per-User Session Hashing) و سوییچ خودکار (Failover) به پروکسی‌های کلاینت دیگر.
- **تفکیک صحیح آی‌پی‌های جهانی**: تصحیح فیلتر و عبارات منظم فرانت‌اند در مروگر جهت تفکیک دقیق لیست آی‌پی‌های لبه سراسری که با اینتر، ویرگول، نقطه ویرگول یا بک‌اسلش از هم جدا شده‌اند.
- **حل خطای فلگ سازگاری کلودفلر**: برطرف کردن خطای بروزرسانی و استقرار خودکار پنل کلودفلر با جایگزینی فلگ منسوخ‌شده `unsafe-eval` با فلگ پیشرفته `allow_eval_during_startup` جهت عدم بروز کرش در شروع به کار.

### بهبود یافته (Improved)
- **پایداری فرم‌‌ها و اشتراک**: افزایش پایداری و اصلاح کنترل اعتبارهای سمت سرور و فرانت‌اند برای ارتقای امنیت و سرعت پنل نهان.
<!-- LANG:FA -->

<!-- LANG:EN -->
### Added
- **Smart User-Specific Backups**: Support entering custom clean IPs, proxy IPs, and custom config names for each subscriber in Add/Edit modals, with automatic extraction and seamless database merging.
- **Real-time Country Flagging via api.country.is**: Integrated free, open-source and keyless api.country.is service for mapping IP addresses to country flags.

### Fixed
- **Cloudflare Compatibility Flag Fix**: Resolved update and deployment error (`No such compatibility flag: unsafe-eval` & startup `Uncaught EvalError`) by updating the compatibility flag to the modern `allow_eval_during_startup`.
- **Cloudflare IP Splitting Fix**: Resolved session disruptions and partial page loads for sites behind Cloudflare by implementing Consistent Per-User Session Hashing and automated failover.
- **Browser-Side IP Parsing**: Fixed UI regular expressions to split global IP lists separated by commas, semicolons, tabs, or backslashes.

### Improved
- **Robustness & Validation**: Enhanced stability of user management modals and subscription validation logic inside the control panel.
<!-- LANG:EN -->

---

## [2.5.6.1] - ۱۴۰۵-۰۳-۲۸ (2026-06-18)

<!-- LANG:FA -->
### اضافه شده (Added)
- **تنظیمات اختصاصی کاربر جدید**: امکان تعیین نام کانفیگ دلخواه، آی‌پی پروکسی اختصاصی و آی‌پی تمیز (Clean IP) به صورت مجزا برای هر کاربر در پنجره افزودن کاربر (Add User Modal) فراهم شد.

### رفع شده (Fixed)
- **رفع خطای بحرانی جاوااسکریپت**: رفع خطای بروز داده شده هنگام ثبت کاربر جدید مربوط به عدم تعریف صحیح متغیر آی‌پی پروکسی (`ReferenceError: proxyIp is not defined`).

### بهبود یافته (Improved)
- **هماهنگ‌سازی مقادیر اختصاصی**: بهبود فرایند ساخت کانفیگ‌های اشتراک و همگام‌سازی بی‌نقص مقادیر کاربری با پیکربندی‌های خروجی.
<!-- LANG:FA -->

<!-- LANG:EN -->
### Added
- **User-Specific Dynamic Settings**: Added options to set custom proxy IP, custom clean IP, and config name per subscriber in the Add User modal.

### Fixed
- **JavaScript Critical Fix**: Fixed a critical client-side error (`ReferenceError: proxyIp is not defined`) occurring during new user registration.

### Improved
- **Sync Optimization**: Enhanced subscription generation and alignment of custom user values.
<!-- LANG:EN -->

---

## [2.5.6] - ۱۴۰۵-۰۳-۲۸ (2026-06-18)

<!-- LANG:FA -->
### اضافه شده (Added)
- **توزیع بار آی‌پی‌های پروکسی چندگانه**: پشتیبانی از لیست آی‌پی‌های پروکسی چندگانه (بخش‌بندی شده با کاما، نقطه ویرگول یا خط جدید) در تنظیمات پروفایل برای توزیع و چرخش خودکار بین کانفیگ‌ها به منظور عبور از محدودیت‌های کلودفلر.
- **تطبیق دقیق پرچم کشور**: پیاده‌سازی تشخیص خودکار و بلادرنگ پرچم کشور بر اساس آی‌پی پروکسی فعال استفاده‌شده در کانفیگ‌های خروجی.

### رفع شده (Fixed)
- **فرمت حمل‌ونقل وب‌ساکت**: تصحیح و حل ناسازگاری‌های مربوط به فرمت‌های خروجی وب‌ساکت در Vless و Trojan برای کلاینت‌های Clash و Sing-Box.
- **کش اطلاعات پیش‌فرض**: تصحیح خطاهای کش پرچم در بارگذاری اولیه اشتراک‌ها.
<!-- LANG:FA -->

<!-- LANG:EN -->
### Added
- **Load Balancing Over Multi-Proxy IPs**: Automated rotating and load balancing across multi-proxy lists to bypass Cloudflare request limits.
- **Dynamic Flag Resolution**: Automatic country flag matching based on the active proxy IP coordinates in generated nodes.

### Fixed
- **Transport Configurations**: Corrected formatting errors in outbound VLESS/Trojan WebSocket settings for Clash and Sing-Box.
- **Cache Invalidation**: Rectified early flag rendering cache errors during initial subscription feed load.
<!-- LANG:EN -->
