---
title: "پشتیبان‌گیری"
---

### مراحل پشتیبان‌گیری از مرزنشین

{{< callout type="info" >}}
پشتیبان‌گیری منظم از فایل‌های مرزنشین یک راه عالی برای جلوگیری از از دست دادن داده‌ها در صورت خرابی سیستم است.
{{< /callout >}}

1. به طور پیش‌فرض، تمام فایل‌های مهم مرزنشین در `/var/lib/marzneshin` (نسخه‌های Docker) ذخیره می‌شوند. کافی است کل
   دایرکتوری `/var/lib/marzneshin` را به یک مکان پشتیبان از انتخاب خود، مانند یک هارد دیسک خارجی یا فضای ذخیره‌سازی ابری
   کپی کنید.
2. همچنین، حتماً فایل env خود را که حاوی متغیرهای پیکربندی شما است، پشتیبان‌گیری کنید. اگر مرزنشین را با استفاده از اسکریپت نصب کرده‌اید (روش نصب توصیه‌شده)، env و سایر پیکربندی‌ها باید
   در دایرکتوری `/etc/opt/marzneshin/` باشند.

{{< callout type="error" >}}
اگر پشتیبان‌گیری منظم انجام ندهید، ممکن است داده‌های خود را از دست بدهید و نتوانید آنها را بازیابی کنید. پس حتماً پشتیبان‌های خود را به‌طور مکرر نگه دارید تا از داده‌های خود محافظت کنید.
{{< /callout >}}

### ساختار دایرکتوری پشتیبان

{{< filetree/container >}}
  {{< filetree/folder name="var" >}}
    {{< filetree/folder name="lib" >}}
      {{< filetree/folder name="marzneshin" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
  {{< filetree/folder name="etc" >}}
    {{< filetree/folder name="opt" >}}
      {{< filetree/folder name="marzneshin" >}}
        {{< filetree/file name="env" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

با دنبال کردن این مراحل، می‌توانید مطمئن باشید که یک نسخه پشتیبان از تمام فایل‌ها و داده‌های مرزنشین خود، همچنین متغیرهای پیکربندی و پیکربندی Xray خود دارید، در صورت نیاز به بازیابی آنها در آینده. به یاد داشته باشید که بکاپ های خود را به‌طور منظم به‌روزرسانی کنید تا همیشه به‌روز باشند.