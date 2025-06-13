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
