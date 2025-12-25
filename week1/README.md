# README — Python Basics (Roman Hindi)

## Intro: Programming Language kya hoti hai?

Programming language woh zubaan hai jisme hum computer se baat karte hain. Jaise insaan ek dusre se instructions dene ke liye Urdu/Hindi bolta hai — waise hi computer ko instructions dene ke liye programming language use karte hain.

**Real-life example:** Agar aap ghar pe chai banati ho to aap step-by-step batati ho: paani garam karo → chai patti daalo → doodh daalo → channi se chaan lo. Yeh step-by-step instructions hi ek "program" hain. Programming language is instructions ko computer ke liye likhne ka tareeqa hai.

---

## Python kya hai?

Python ek high-level programming language hai jo seekhne mein aasan aur readable hoti hai. Isko 1991 mein banaya gaya tha. Python simple syntax (bilkul natural language jaise) use karta hai, isliye beginners ke liye best hai.

**Real-life example:** Python ko samjho jaise ek friendly teacher jo short aur seedhi baatein karta hai — isliye beginners comfortable feel karte hain.

---

# Topics

Is README mein hum niche topics cover karenge:

1. Variables — kya hain, kyun use karte hain, kaise define karte hain
2. Strings — kya hote hain
3. Data types — String, Int, Float, Boolean
4. Comparison operators
5. Logical operators
6. input() function — kya return karta hai aur type conversion
7. Chhote exercises

---

# 1) Variables (variable kya hota hai?)

**Definition:** Variable ek container (dabba) hota hai jisme hum data store karte hain. Variable ko ek naam dete hain taake program mein us value ko baar-baar use kar saken.

**Kyun use karte hain?**

* Reusability: ek value ko baar-baar likhne se behtar hai variable mein store kar lo.
* Readability: naam se pata chal jata hai data kis cheez ka hai (e.g. `age`, `name`).

**Kaise define karte hain (Python syntax):**

```python
name = "Ayesha"
age = 18
price = 199.50
is_student = True
```

Yahan `name`, `age`, `price`, `is_student` variables hain.

**Real-life example:** Socho tum ek notebook mein likhti ho: "Ayesha — age 18, city Karachi". Notebook mein likha hua har cheez ek variable jaisa hai.

---

# 2) Strings (String kya hota hai?)

**Definition:** String characters ka sequence hota hai — jaise text. Python mein strings single quotes `'...'` ya double quotes `"..."` se likhte hain.

**Examples:**

```python
s1 = "Hello"
s2 = 'Python'
```

**Common operations:**

* Concatenation (jodna): `"Hello" + " " + "Ayesha"` → `"Hello Ayesha"`
* Length: `len(s1)`
* Indexing: `s1[0]` → pehla character (Python 0-based indexing)

**Real-life example:** Mobile ke contacts mein naam ek string hota hai.

---

# 3) Data Types — String, Int, Float, Boolean

Python mein har value ka type hota hai. Yahan chaar basic data types:

### String (str)

* Text ko represent karta hai.
* Example: `"Ali"`, `'Hello'`
* `type("Ali")` → `<class 'str'>`

**Real-life:** Kisi ka naam ya message text.

### Integer (int)

* Whole numbers (no decimal).
* Example: `10`, `0`, `-5`
* `type(10)` → `<class 'int'>`

**Real-life:** Age, number of students in class.

### Float (float)

* Decimal numbers.
* Example: `3.14`, `199.99`
* `type(3.14)` → `<class 'float'>`

**Real-life:** Price, weight (kg), temperature with decimals.

### Boolean (bool)

* Sirf do values le sakta hai: `True` ya `False`.
* Use hota hai condition checks mein.
* `type(True)` → `<class 'bool'>`

**Real-life:** Kisi cheez ka jawab: "Kya homework complete hai?" → Yes (True) / No (False).

**Example code showing types:**

```python
name = "Sara"        # str
age = 20              # int
gpa = 3.7             # float
passed = True         # bool

print(type(name), type(age), type(gpa), type(passed))
```

---

# 4) Comparison Operators (mukabla karne wale operator)

Comparison operators do values ko compare karte hain aur result `True` ya `False` dete hain.

| Operator | Matlab            | Example         |
| -------- | ----------------- | --------------- |
| `==`     | barabar           | `5 == 5` → True |
| `!=`     | barabar nahi      | `5 != 3` → True |
| `>`      | bada hai          | `7 > 5` → True  |
| `<`      | chhota hai        | `2 < 3` → True  |
| `>=`     | bada ya barabar   | `5 >= 5` → True |
| `<=`     | chhota ya barabar | `4 <= 6` → True |

**Real-life example:** Agar tum kehogi "agar tumhari age 18 se zyada hai toh ticket full price" → yahan `age > 18` check ho raha hai.

**Python example:**

```python
age = 17
print(age >= 18)  # False
```

---

# 5) Logical Operators (AND, OR, NOT)

Logical operators conditions ko combine karte hain.

* `and`: dono conditions True honi chahiye.
* `or`: koi ek condition True ho to True.
* `not`: condition ka opposite (True->False, False->True).

**Truth table (short):**

* `True and True` → `True`
* `True and False` → `False`
* `True or False` → `True`
* `not True` → `False`

**Real-life example:**

* `and`: "Agar tum homework complete karo **AND** parents allow karte hain, toh tum party ja sakti ho."
* `or`: "Agar tum chai **OR** coffee chaho, main bana doongi." (agar dono me se koi bhi chalega)

**Python example:**

```python
age = 20
has_ticket = True
can_enter = (age >= 18) and has_ticket
print(can_enter)  # True

likes_tea = False
likes_coffee = True
print(likes_tea or likes_coffee)  # True
```

---

# 6) `input()` function — kya karta hai aur type conversion

**Kya karta hai?**

* `input()` user se keyboard se text (string) leta hai.
* Hamesha `input()` string return karta hai — chahe user koi number type kare.

**Syntax:**

```python
name = input("Enter your name: ")
```

Yeh user se text lega aur `name` variable mein store karega (type = `str`).

**Agar number chahiye to convert karo:**

* `int()` — integer mein convert karta hai
* `float()` — float mein convert karta hai
* `bool()` — string se bool conversion tricky hai (empty string -> False, non-empty -> True)

**Example:**

```python
age_str = input("Enter your age: ")   # user ne "18" type kiya (string)
age = int(age_str)                     # ab age int ho gaya
print(age + 2)

price_str = input("Enter price: ")
price = float(price_str)
print(price * 2)
```

**Note on errors:** Agar user koi non-numeric text `int()` ko de de to program error (ValueError) dega. Isliye real programs mein `try/except` use karte hain:

```python
try:
    age = int(input("Enter age: "))
except ValueError:
    print("Please enter a valid number")
```

**Real-life example:** Jab app kisi se form mein "age" maangti ho — browser hamesha text bhejta hai; server ko number chahiye to convert karna padta hai.

---

# 7) Quick exercises (Practice ke liye)

1. `input()` se apna naam lo aur `Hello, <name>!` print karo.
2. User se do numbers lo, unka sum print karo (type convert karna zaroori hai).
3. User se temperature (float) lo aur check karo agar temperature > 37.5 toh print karo "fever" warna "normal".
4. User se age lo aur check karo `>=18` ho to "adult" warna "minor".
5. Do strings lo aur unko jod ke ek sentence banao.

---

