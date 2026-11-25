FREE FIRE ESPORTS HUB — POWERED BY DARK XCOP
================================================

এই ZIP-এ আছে:
- index.html
- style.css
- app.js
- firebase-config.js
- firestore.rules
- assets/logo.png (আপনার দেওয়া লোগো)

গুরুত্বপূর্ণ:
এটি একটি প্রাথমিক কার্যকর ওয়েবসাইট starter build। Firebase সংযোগ ও নিরাপত্তা নিয়ম সেট না করা পর্যন্ত Login/Database ফিচার কাজ করবে না। Tournament publishing/admin moderation-এর জন্য পরের উন্নয়ন প্রয়োজন।

A) নতুন Firebase Project তৈরি
1. https://console.firebase.google.com খুলুন।
2. Add project চাপুন, নাম দিন Free Fire Esports Hub।
3. Project তৈরি হলে Web app (</>) যোগ করুন।
4. Firebase config কপি করুন।

B) Firebase config বসানো
1. firebase-config.js ফাইল খুলুন।
2. PASTE_YOUR_... লেখা placeholder-গুলো নিজের Firebase web config দিয়ে বদলান।
3. Save করুন।
কখনো Service Account JSON/private key এখানে দেবেন না।

C) Authentication চালু
1. Firebase Console > Authentication > Get started।
2. Sign-in method > Email/Password Enable করে Save করুন।
3. Authentication > Settings > Authorized domains-এ আপনার GitHub Pages domain যোগ করুন (যেমন username.github.io)।

D) Firestore চালু
1. Firebase Console > Firestore Database > Create database।
2. Database তৈরি করুন।
3. Rules tab খুলে firestore.rules ফাইলের সব লেখা paste করে Publish করুন।

E) GitHub Pages-এ প্রকাশ
1. ZIP extract করুন।
2. সব ফাইল ও assets folder একইভাবে GitHub repository-র root-এ upload করুন।
3. GitHub repository > Settings > Pages > Deploy from branch নির্বাচন করুন।
4. main branch এবং /(root) নির্বাচন করে Save করুন।
5. GitHub Pages URL খুলুন।

F) Admin account সম্পর্কে
- Public website থেকে নিজেকে admin করা যাবে না।
- প্রথমে নিজের account register করুন এবং email verify করুন।
- Firestore Console > users collection-এ আপনার UID document খুলে role field-কে "admin" করুন।
- Admin access শুধুমাত্র বিশ্বস্ত account-কে দিন।
- admin role বদলানোর পর logout/login করুন।

G) সীমাবদ্ধতা ও পরের কাজ
- Player/Team profile, directory search, recruitment request, basic chat, report/block এবং ranking starter functionality অন্তর্ভুক্ত।
- Profile edit prompt-based; পরে সুন্দর edit form করা যাবে।
- Verified badge শুধু admin কর্তৃক Firestore-এ verified=true করলে দেখাবে।
- Tournament এখন placeholder; admin tournament create/edit interface পরের ধাপে যোগ করতে হবে।
- Notification inbox UI ও unread counter পরের ধাপে যোগ করতে হবে।
- Block collection-এ block save হয়; feed থেকে blocked users সম্পূর্ণ filter করার উন্নয়ন পরের ধাপে দরকার।
- Real-time chat requires correct Firestore rules and two verified users.
- Firestore rules production launch-এর আগে security review ও testing করা উচিত।

Troubleshooting:
- Firebase config না বসালে Firebase error হবে।
- Browser-এ file:// দিয়ে index.html চালাবেন না; GitHub Pages বা local web server ব্যবহার করুন।
- Firebase Console-এ Authentication, Firestore এবং Authorized domains ঠিক আছে কি না দেখুন।
