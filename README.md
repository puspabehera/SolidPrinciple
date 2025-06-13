# SolidPrinciple

## 🧱 Single Responsibility Principle (SRP)

---

### 🔹 Definition  
> **A class should have only one reason to change** — this means it should have only one responsibility.

---

### ❌ SRP Violation Example

```csharp
public class Report
{
    public void GenerateReport() { }
    public void SaveToDataBase() { }
    public void SendEmail() { }
}
```

> 📝 **Note:**  
> `Report` class has:  
> - 🧠 Business logic: `GenerateReport()`  
> - 💾 Persistence logic: `SaveToDataBase()`  
> - 📧 Communication logic: `SendEmail()`  

Each of these responsibilities can change for different reasons:

- Business rules for report generation may change  
- DB layer structure/schema or repository pattern might evolve  
- Email formatting or SMTP configuration might need changes  

👉 **One class, multiple reasons to change = SRP violation**

---

## 🏨 The Scenario: A Restaurant Analogy for SRP

Imagine a restaurant.

There are:

- 👨‍🍳 A Chef – whose only job is to **cook the food**  
- 🧑‍💼 A Waiter – whose only job is to **serve the food to the customer**

---

Now picture this:

> What if the chef is also responsible for cooking, serving, and cleaning the tables?

That chef will:

- 🍳➡️🏃 Burn the food while running to serve it  
- ❗ Forget the order sequence  
- 😵 Get stressed out  
- 🔄 Be hard to replace or train

---

### ❌ Code That Violates SRP (Analogy in Code)

```csharp
public class RestaurantStaff
{
    public void CookFood() { }
    public void ServeFood() { }
    public void CleanTable() { }
}
```

🔥 This `RestaurantStaff` class is like one person doing all jobs — **chef + waiter + cleaner**.

If cooking logic changes, or the cleaning process is updated, this single class must change.

📌 **Too many reasons to change = SRP violation**
