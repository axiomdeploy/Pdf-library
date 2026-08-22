# 📚 PDF Library

আমার PDF সংগ্রহের ওয়েবসাইট। সবাই দেখতে পারবে, শুধু আমি edit করতে পারব।

## 🔗 Live Website
(https://axiomdeploy.github.io/Pdf-library/)

---

## ✏️ কিভাবে PDF যোগ / এডিট / ডিলিট করবে

GitHub এ যাও → `index.html` ফাইলে click করো → ডান পাশে pencil icon (✏️) → 
নিচের নির্দেশনা অনুযায়ী edit করো → নিচে "Commit changes" ক্লিক করো।

### ১. নতুন PDF যোগ করা

`index.html` এ `libraryData` খুঁজো (Ctrl+F চেপে)।
তারপর যেই Subject এর নিচে যোগ করতে চাও সেখানে গিয়ে:

```javascript
{
  title: "তোমার PDF এর নাম",
  tag: "Master Q Bank",           // যেকোনো tag লিখতে পারো
  tagColor: "cyan",               // cyan / purple / green / gold / pink
  desc: "ছোট বর্ণনা লিখো",
  links: [
    { label: "Drive Link", url: "https://drive.google.com/..." }
  ]
},
২টা link দিতে চাইলে:

links: [
  { label: "Drive Link", url: "https://drive.google.com/..." },
  { label: "Dropbox", url: "https://dropbox.com/..." }
],
Link না দিতে চাইলে:

links: [],
২. নতুন Subject যোগ করা (যেমন: "ICT")
যেই Section এর ভেতরে subjects array আছে সেখানে:

{
  name: "ICT",
  pdfs: [
    {
      title: "ICT Question Bank",
      tag: "Master Q Bank",
      tagColor: "cyan",
      desc: "সব chapter এর question",
      links: [
        { label: "Drive Link", url: "https://..." }
      ]
    }
  ]
},
৩. নতুন Section যোগ করা (যেমন: "Main Books")
libraryData array তে শেষ Section এর পরে comma দিয়ে:

{
  title: "Main Books",
  subjects: [
    {
      name: "Physics",
      pdfs: [
        {
          title: "Physics Main Book",
          tag: "Main Book",
          tagColor: "green",
          desc: "Main textbook",
          links: [
            { label: "Drive Link", url: "https://..." }
          ]
        }
      ]
    }
  ]
}
⚠️ শেষ Section এর পরে comma (,) দিতে ভুলো না!

৪. PDF এডিট করা
নাম বদলাতে: title: "নতুন নাম" লিখো
Description বদলাতে: desc: "নতুন description" লিখো
Link বদলাতে: url: "নতুর link" লিখো
Tag বদলাতে: tag: "নতুন tag" লিখো
৫. PDF ডিলিট করা
যেই { title: ..., links: ... } block টা মুছতে চাও, পুরো block টা (curly braces সহ) select করে delete করে দাও। শেষ block এর পরের comma ও মুছে দাও।

🎨 Tag Colors
Color	Code
নীল (Cyan)	"cyan"
বেগুনি	"purple"
সবুজ	"green"
হলুদ	"gold"
গোলাপি	"pink"
🔍 Search Features
উপরের ডান কোণে search icon এ click করো
বা keyboard এ / চাপো
ভুল বানানেও খুঁজে পাবে (fuzzy search)
Escape চাপলে search বন্ধ হবে
⚠️ Common Problems
সাইট আপডেট হচ্ছে না? → Browser এ Ctrl+Shift+R চাপো (hard refresh)

কিছু ভেঙে গেছে? → GitHub এ "History" তে গিয়ে previous version এ ফিরে যাও

JavaScript error আসছে? → Comma (,) check করো — শেষ item এর পরে extra comma আছে কিনা

📁 Files
├── index.html   → মূল ফাইল (এটাই এডিট করতে হবে)
└── README.md    → এই ফাইল (নির্দেশনা)
© 2026 PDF Library


---

## ✨ Final Features Summary:

| Feature | Status |
|---------|--------|
| ⬛ Pure black background | ✅ `#000000` |
| ⚡ Neon glow effects | ✅ Cyan/Purple/Green glow |
| �search Fixed corner search | ✅ Top-right, click to expand |
| �search Fuzzy search | ✅ ভুল বানানেও কাজ করে |
| ✍️ Handwritten font | ✅ Caveat (descriptions, buttons) |
| 🏷️ Monospace tags | ✅ Share Tech Mono |
| 📐 Futuristic section titles | ✅ Rajdhani uppercase |
| ➕ Easy new section | ✅ Comment এ instructions |
| 🔊 ৩ রকম sound | ✅ Click/Success/Error |
| 📱 Mobile optimized | ✅ No zoom, no gaps |
| 🎯 No emoji in UI | ✅ SVG icons |
| 📄 README included | ✅ সম্পূর্ণ বাংলা guide |
