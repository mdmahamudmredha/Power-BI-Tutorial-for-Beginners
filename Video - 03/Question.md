## 📌 20টি Real Power Query ভিত্তিক প্রশ্ন

### নিচে আমি এমন **20টি Real-World প্রশ্ন** দিচ্ছি যেগুলোর সমাধান **শুধুমাত্র Power Query দিয়ে** করা যাবে।


### 1. **Year, Month, Day আলাদা করো OrderDate থেকে**

📌 Column: `OrderDate`
⚙️ Use: `Date → Year`, `Month`, `Day`
🎯 শেখাবে: Date breakdown / grouping এর জন্য কেন দরকার

---

### 2. **OrderDate থেকে মাসের নাম বের করো (January, February...)**

📌 Column: `OrderDate`
⚙️ Use: `Date → Month Name`
🎯 Use case: Human-friendly report label

---

### 3. **OrderDate থেকে সপ্তাহের দিন বের করো (Saturday, Sunday...)**

📌 Column: `OrderDate`
⚙️ Use: `Date → Day Name`
🎯 Use case: Weekday vs weekend analysis

---

### 4. **Start of Month বের করো OrderDate-এর**

📌 Column: `OrderDate`
⚙️ Use: `Date → Start of Month`
🎯 শেখাবে: Monthly grouping/report এর জন্য

---

### 5. **DeliveryDate - OrderDate = কতদিনে ডেলিভারি হয়েছে?**

📌 Columns: `OrderDate`, `DeliveryDate`
⚙️ Step: Add Column → `DeliveryDate - OrderDate`
🎯 Use case: Delivery performance check

---

### 6. **CustomerAge Column থেকে জোড় vs বিজোড় বের করো**

📌 Column: `CustomerAge`
⚙️ Use: `Number → IsEven`, `IsOdd`
🎯 শেখাবে: segmentation, pattern check

---

### 7. **Quantity Column কে Round করে দেখাও**

📌 Column: `Quantity`
⚙️ Use: `Number → Round`, `RoundDown`, `RoundUp`
🎯 Use case: Unit-level inventory handling

---

### 8. **SalesAmount নাম দিয়ে নতুন column বানাও → Quantity × UnitPrice**

📌 Columns: `Quantity`, `UnitPrice`
⚙️ Step: Add Column → Custom Column → `[Quantity] * [UnitPrice]`
🎯 শেখাবে: Transaction value তৈরির প্রক্রিয়া

---

### 9. **SalesAmount কে Round করে 2 decimal পর্যন্ত নিয়ে আসো**

📌 Column: New `SalesAmount`
⚙️ Step: `Number → Round (2)`
🎯 Use case: Money formatting

---

### 10. **Discount Column কে % Format-এ রূপান্তর করো (e.g. 0.1 → 10%)**

📌 Column: `Discount`
⚙️ Multiply by 100 → Format as Percentage
🎯 শেখাবে: কীভাবে numeric → readable % বানাই

---

### 11. **ReviewRating কে Capital round করে নতুন Column বানাও**

📌 Column: `ReviewRating`
⚙️ Round function → `Number.Round([ReviewRating], 0)`
🎯 Use case: Rating bucket বানানো

---

### 12. **Region Column থেকে শুধু Division বের করো (Text.Split → Last part)**

📌 Column: `Region` (e.g. Sylhet, Sylhet, Sylhet Division)
⚙️ Use: `Split by Delimiter (",") → Last Column`
🎯 শেখাবে: Address parsing logic

---

### 13. **Text Merge করে CustomerAge ও Region এক Column এ আনো**

📌 Columns: `CustomerAge`, `Region`
⚙️ Use: `Merge Columns → with "-" or ", "`
🎯 Use case: Labeling / ID generation

---

### 14. **UnitPrice থেকে শুধু টাকা অংশ বের করো (Before .)**

📌 Column: `UnitPrice`
⚙️ Use: `Extract → Text Before Delimiter "."`
🎯 Use: Round figure analysis

---

### 15. **Month Name থেকে শুধু 1st 3 letter বের করো (e.g. January → Jan)**

📌 Column: `MonthName`
⚙️ Use: `Text.Range([MonthName], 0, 3)`
🎯 শেখাবে: Label বানানো

---

### 16. **CustomerAge Column এ <30 হলে Youth, না হলে Adult লিখো**

📌 Column: `CustomerAge`
⚙️ Use: `Add Column → Conditional Column`
🎯 শেখাবে: Category segmentation

---

### 17. **Quantity = 1 হলে “Single Order” নয়তো “Bulk Order”**

📌 Column: `Quantity`
⚙️ Conditional Column → IF `=1` THEN Single ELSE Bulk
🎯 Use case: Order type detect

---

### 18. **OrderDate কে Text-এ রূপান্তর করো → “15 June 2024”**

📌 Column: `OrderDate`
⚙️ Use: `Transform → Data Type → Text` + Custom Format
🎯 Use: Export/readable format

---

### 19. **Top 5 Order by Quantity → Keep Only Top Rows (After Sort)**

📌 Column: `Quantity`
⚙️ Step: Sort Descending → Keep Top Rows → 5
🎯 Use case: Best order filtering

---

### 20. **SalesAmount-এর ওপর ভিত্তি করে Group করে Total বের করো Region অনুযায়ী**

📌 Column: `SalesAmount`, `Region`
⚙️ Use: Group By → `Region` → Sum of SalesAmount
🎯 শেখাবে: Aggregation logic


