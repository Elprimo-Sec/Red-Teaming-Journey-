 🛡️ Linux PrivEsc Quick Checks

 🆔 Identity & Context
- `whoami` (مين أنا؟)
- `id` (إيه صلاحياتي وجروباتي؟)
- `hostname` (اسم الجهاز)

## 💻 System Info
- `uname -a` (إصدار الكيرنل - ممكن يكون فيه exploit)
- `cat /etc/issue` (إصدار التوزيعة)

 🔑 Sudo Privileges
- `sudo -l` (أهم أمر: هل أقدر أنفذ أوامر كمدير؟)

 🔍 SUID Binaries
- `find / -perm -4000 2>/dev/null` (ملفات بتشتغل بصلاحية صاحبها - ثغرة محتملة)

 📂 Interesting Files & Paths
- `/etc/passwd` (قائمة المستخدمين)
- `/etc/crontab` (المهام المجدولة - ممكن نستغلها)
- `/home/` (ملفات المستخدمين التانيين)
- `/var/www/html/` (ملفات موقع الويب)

📝 Writable Files
- `find / -writable 2>/dev/null | head` (أدور على ملفات أقدر أعدل فيها)

 ⚙️ Processes & Network
- `ps aux` (العمليات اللي شغالة - دور على حاجة Root مشبوهة)
- `ss -tulpn` (البورتات المفتوحة داخلياً)
