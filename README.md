# SolidPrinciple
 ## 🧱 Single Responsibility Principle (SRP)

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
Note: Report class have  Business logic: GenerateReport(),Persistence logic: SaveToDataBase(),Communication logic: SendEmail()

Each of these responsibilities can change for different reasons:Business rules for report generation may change.
DB layer structure/schema or repository pattern might evolve.
Email formatting or SMTP configuration might need changes.

👉 One class, multiple reasons to change = SRP violation.
