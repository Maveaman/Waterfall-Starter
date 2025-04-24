# Power BI Waterfall Chart – Native Visual, Minimal DAX

This project demonstrates how to create a **dynamic, scalable waterfall chart** in Power BI using only **native visuals** and **minimal DAX**, inspired by techniques shared by **Fomi Abdul Mutalib** (Power BI Park). The solution avoids custom visuals and SVG rendering, making it lightweight and easy to maintain.


##  Project Highlights

- ✅ **100% Native Visuals** – No custom visuals or external plugins
- ✅ **Minimal DAX Logic** – Clean and efficient use of `SWITCH(TRUE())`, variables, and calculated measures
- ✅ **Dynamic Scaling** – Adjusts automatically to dataset changes
- ✅ **Conditional Formatting** – Highlights positive/negative deltas clearly
- ✅ **Category Indexing** – Ensures correct ordering and totals
- ✅ **Optimized Labels & Layout** – Improves readability with no text wrapping and formatted headers


##  Why This Matters

Waterfall charts are critical in industries like:

- 📈 **Finance** – Variance analysis, budgeting, forecasting
- 🧾 **Operations** – Cost breakdowns, performance gaps
- 💼 **Business Reviews** – Profit/loss drivers, contribution analysis

This approach is ideal for building **clean, reliable reports** that are:

- Easier to update and scale
- Faster to load and render
- Better aligned with Power BI's performance best practices


## ⚙ Built With

- **Power BI Desktop**
- **DAX** for:
  - Conditional calculations
  - Label visibility
  - Delta classification
- **Native Power BI visuals** (Column Chart, Matrix, etc.)



## 🧪 Key Measures Used (DAX)

```DAX
Sales Category =
SWITCH(TRUE(),
    'Data'[Category] = "Increase", "Positive",
    'Data'[Category] = "Decrease", "Negative",
    "Total"
)
```

```DAX
Delta Measure =
VAR Current = SUM('Data'[Amount])
VAR Previous = [Some Previous Logic]
RETURN
    Current - Previous
```

> Full DAX logic is inside the `.pbix` file for detailed reference.



##  Credits

- Inspired by **Fomi Abdul Mutalib (Power BI Park)** for the clean native visual approach.  
- Developed and refined by **Aman Kumar Sharma** to enhance flexibility and real-world use.


## 🔗 Connect With Me

-  [LinkedIn](https://www.linkedin.com/in/amansharma270)
-  [GitHub](https://github.com/Maveaman)
- aamansharma027@gmail.com

