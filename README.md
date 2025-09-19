# Insights
## 🔎 Pooling Modes Comparison

| Mode                | Kaise kaam karta hai 🛠️ | Pros ✅ | Cons ❌ | Real Life Analogy ✈️ |
|---------------------|------------------------|--------|--------|----------------------|
| **Session Pooling** | Har user ko ek dedicated DB connection milta hai (pure session ke dauran wahi rehta hai). | - Prepared statements work<br>- Stable connection per user | - Bohot zyada DB connections lagte hain<br>- Scale karna mushkil | **Business class** → ek passenger = ek crew poore flight me |
| **Transaction Pooling** (Supabase default) | Har transaction ke liye naya connection assign hota hai (khatam hote hi dusre user ko mil jata hai). | - Efficient use of connections<br>- Good for serverless apps<br>- Scale friendly | - Prepared statements **nahi chalti**<br>- Thodi overhead re-planning ki | **Economy class** → crew change hota hai har service me |
| **Statement Pooling** | Har SQL query ke liye naya connection assign hota hai. | - Sabse kam connections chahiye<br>- Massive scale possible | - Prepared statements bilkul off<br>- Query planning baar-baar hoti hai → CPU load zyada | **Ultra budget airline / bus** → har chhoti cheez ke liye alag staff |
