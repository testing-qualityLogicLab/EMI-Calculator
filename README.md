# 💰 EMI Calculator (Java)

This is a simple **console-based EMI (Equated Monthly Installment) Calculator** built using Java.
It takes the **loan amount**, **annual interest rate**, and **loan tenure in years** as inputs and calculates the **monthly EMI** using the standard EMI formula.

---

## 📌 Features

* Accepts:

  * Loan amount (Principal)
  * Annual interest rate (percentage)
  * Loan tenure (in years)

* Converts annual interest rate to **monthly interest rate**

* Converts loan tenure to **total months**

* Calculates EMI using the standard formula:

  ```
  EMI = [P * r * (1 + r)^n] / [(1 + r)^n – 1]
  ```

* Outputs the monthly EMI in a clear and readable format

---

## 🛠️ Technologies Used

* **Java**
* **Scanner** class for user input
* **Math.pow()** for exponential calculations

---

## 🚀 How to Run the Program

1. Ensure Java JDK 8+ is installed on your system.

2. Save the file as `EmiCalculator.java` inside the `day3` package folder.

3. Open a terminal and navigate to the project directory.

4. Compile the program:

   ```bash
   javac day3/EmiCalculator.java
   ```

5. Run the program:

   ```bash
   java day3.EmiCalculator
   ```

---

## 📂 Program Flow

1. User enters:

   * **Loan amount** in USD
   * **Annual interest rate** (in %)
   * **Loan tenure** (years)

2. Program computes:

   * Monthly interest rate

     ```
     r = annualInterestRate / (12 * 100)
     ```
   * Total number of monthly payments

     ```
     n = tenureYears * 12
     ```

3. EMI is calculated:

   ```
   EMI = P * r * (1 + r)^n / ((1 + r)^n − 1)
   ```

4. Displays the EMI result.

---

## 🧾 Example Output

```
Enter loan amount in USD
50000
Enter annual interest rate (in %)
7.5
Enter loan tenure in years
5
Your monthly EMI is: 1001.87
```

---

## 🔧 Code Snippet

```java
double monthlyInterestRate = annualInterestRate / (12 * 100);
int tenureMonths = tenureYears * 12;

double emi = (principal * monthlyInterestRate * Math.pow(1 + monthlyInterestRate, tenureMonths))
           / (Math.pow(1 + monthlyInterestRate, tenureMonths) - 1);

System.out.println("Your monthly EMI is: " + emi);
```

---

## 📘 Notes

* Interest rate must be provided as a percentage (e.g., **7.5**, not **0.075**).
* EMI value may include decimals; formatting can be added for cleaner output.
* You can extend the program by adding:

  * Total payable amount
  * Total interest amount
  * Amortization table
  * Input validation

---

## 📜 License

Free to use for learning, practice, and improvement.

---

Just let me know!

