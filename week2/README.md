# Python Programming – If / Elif / Else (Detailed with Real Life Examples)

## 📌 Introduction (Bilkul Simple Language Mein)

Python mein **if, elif (else if), aur else** ka matlab hota hai **decision lena**.
Jaisay hum real life mein soch kar faisla kartay hain, waisay hi program bhi sochta hai.

### Real Life Soch:

* Agar **mobile battery low ho** → charge lagao
* Agar **internet slow ho** → WiFi change karo
* Warna → kaam continue rakho

Programming mein yehi kaam **if / elif / else** karta hai.

---

## 🧠 If – Elif – Else Kaam Kaisay Karta Hai (Flow Samjho)

1. Program pehle **if** check karta hai
2. Agar if **true** ho → code run
3. Agar false → **elif** check hota hai
4. Agar sab false → **else** run hota hai

⚠️ Python sirf **pehli true condition** ka code run karta hai.

---

## ✅ Basic Syntax (Yaad Karnay Wala Rule)

```python
if condition:
    statement
elif condition:
    statement
else:
    statement
```

Indentation (space) bohot zaroori hoti hai.

---

## 🌱 Example 1: Simple If Else (Daily Life)

```python
weather = "rain"

if weather == "rain":
    print("Umbrella le lo")
else:
    print("Normal bahar jao")
```

📝 Samjho:

* Agar weather rain ho → umbrella
* Warna normal

---

## 🌿 Example 2: If – Elif – Else (Student Life)

```python
marks = 55

if marks >= 80:
    print("Excellent")
elif marks >= 60:
    print("Good")
else:
    print("Need Improvement")
```

📝 Step by Step:

* Pehla if check hua → false
* Elif check hua → false
* Else run hua

---

## 🔢 Comparison Operators (Asaan Samajh)

Comparison operators do cheezon ko compare kartay hain.

| Operator | Matlab           | Example |
| -------- | ---------------- | ------- |
| ==       | barabar          | x == 5  |
| !=       | barabar nahi     | x != 5  |
| >        | bara             | x > 5   |
| <        | chota            | x < 5   |
| >=       | bara ya barabar  | x >= 5  |
| <=       | chota ya barabar | x <= 5  |

---

## 🔹 Example: Comparison Operator (Real Life)

```python
age = 17

if age >= 18:
    print("CNIC ban sakta hai")
else:
    print("CNIC nahi ban sakta")
```

---

## 🔗 Logical Operators (Sirf AND & OR)

Logical operators multiple conditions ko **join** kartay hain.

| Operator | Matlab                    |
| -------- | ------------------------- |
| and      | dono condition true hon   |
| or       | koi aik condition true ho |

---

## 🔸 AND Operator – Detail Example 1

```python
age = 20
cnic = True

if age >= 18 and cnic == True:
    print("Bank account open ho sakta hai")
else:
    print("Bank account open nahi ho sakta")
```

📝 Samjho:

* Age bhi sahi
* CNIC bhi hai
* Dono true → result true

---

## 🔸 AND Operator – Detail Example 2 (Student)

```python
attendance = 80
assignment = True

if attendance >= 75 and assignment == True:
    print("Exam allow hai")
else:
    print("Exam allow nahi hai")
```

---

## 🔸 OR Operator – Detail Example 1

```python
email = False
phone = True

if email == True or phone == True:
    print("Login successful")
else:
    print("Login failed")
```

📝 Samjho:

* Email nahi hai
* Phone hai
* Aik bhi true → login

---

## 🔸 OR Operator – Detail Example 2 (Real Life)

```python
cash = False
card = True

if cash == True or card == True:
    print("Shopping possible")
else:
    print("Shopping not possible")
```

---

## 🎯 Final Combined Example (If + Elif + AND)

```python
gender = "female"
age = 19
marks = 65

if gender == "female" and age >= 18:
    print("Eligible for admission")
elif marks >= 60:
    print("Waiting list")
else:
    print("Not eligible")
```

---

## 📝 Assignments (Practice Questions)

### Q1:

User ki age lo, agar age 18 ya zyada ho to "Adult" warna "Minor" print karo.

### Q2:

Marks input lo aur grade print karo:

* 80+ → A
* 60+ → B
* warna → Fail

### Q3:

Check karo user ke paas **CNIC aur age >= 18** dono hon, to "Account Open" warna "Not Allowed".

### Q4:

Check karo payment ke liye **cash ya card** available ho.

### Q5:

Attendance aur assignment dono true hon to "Exam Allowed" print karo.

---

## ✅ Final Summary

* if → pehli condition
* elif → alternate condition
* else → last option
* Comparison → compare karna
* Logical (and / or) → multiple conditions

💡 Practice jitni zyada, concept utna strong 💪

📘 Happy Python Learning 🚀
