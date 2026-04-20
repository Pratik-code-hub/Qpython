❓ 1. n % 2 == 0 kyu nahi use kiya?
Tum use kar sakte ho, par yaha n naam ka variable hai hi nahi.
Tumhara data tuple me hai:
t = (True, 33, 25, 22, 'hi', 66, 3, 80)
👉 Isme hum har element ko access kar rahe hain:
t[i] % 2 == 0
✔ Matlab:
“jo element hai (t[i]), wo even hai ya nahi”
________________________________________
🔴 Agar tum n % 2 == 0 likhoge:
To error aayega ❌
Kyuki n define hi nahi hai
________________________________________
❓ 2. result = [] kyu liya?
👉 Kyuki hume multiple values store karni hain (22, 66, 80)
List [] use karte hain:
•	Mutable hoti hai (change ho sakti hai) 
•	.append() use kar sakte hain 
result.append(t[i])
________________________________________
❓ 3. () (tuple) kyu nahi use kiya?
Tuple:
result = ()
❌ Problem:
•	Tuple immutable hoti hai 
•	.append() nahi hota 
👉 Isliye dynamically values add nahi kar sakte
________________________________________
❓ 4. '' (string) kyu nahi use kiya?
String:
result = ''
❌ Problem:
•	String me numbers store karoge to wo text ban jayega 
•	Append karna mushkil / galat format 
Example:
result += str(22)
👉 Output: '226680' (galat format)
________________________________________
🔑 Final Summary:
•	t[i] % 2 == 0 → kyuki element check kar rahe ho 
•	result = [] → kyuki multiple values store + append karna hai 
•	() ❌ → immutable 
•	'' ❌ → string, numbers ke liye sahi nahi
baat to ek hi he chhe i%2 !=0 lelo ya t[i]%2!=0 lelo agr alg he to example se samjhao
Nahi — baat ek nahi hai 🙂
i % 2 != 0 aur t[i] % 2 != 0 bilkul alag cheezein check karte hain
Chalo example se clear karte hain 👇
________________________________________
🧠 Difference samjho:
1️⃣ i % 2 != 0
👉 Index check karta hai (position)
2️⃣ t[i] % 2 != 0
👉 Value check karta hai (number even/odd hai ya nahi)
________________________________________
🔍 Example:
t = (10, 21, 30, 41)
i (index)	t[i] (value)	i%2!=0 (odd index?)	t[i]%2!=0 (odd value?)
0	10	❌	❌
1	21	✅	✅
2	30	❌	❌
3	41	✅	✅
________________________________________
⚠️ Ab difference dekho:
👉 Case 1: i % 2 != 0
for i in range(len(t)):
    if i % 2 != 0:
        print(t[i])
✔ Output:
21
41
👉 Odd index wale elements
________________________________________
👉 Case 2: t[i] % 2 != 0
for i in range(len(t)):
    if t[i] % 2 != 0:
        print(t[i])
✔ Output:
21
41
👉 Odd numbers (value ke basis pe)
________________________________________
🚨 Ab main difference wala example:
t = (2, 4, 6, 8)
i % 2 != 0:
✔ Output:
4, 8
👉 index 1,3
________________________________________
t[i] % 2 != 0:
✔ Output:
(nothing)
👉 kyuki sab even numbers hain
________________________________________
🔑 Final samajh:
•	i % 2 != 0 → position (index) dekh raha hai 
•	t[i] % 2 != 0 → value (number) dekh raha hai 
👉 Dono ka kaam completely different hai
________________________________________
✅ Tumhare question me:
even integers at odd index
Isliye dono lagenge:




🔍 Tumhara question:
Difference between:
for i in lst
vs
for i in range(len(lst))
________________________________________
🧠 1️⃣ for i in lst
👉 Yaha i = direct element (value) hota hai
Example:
lst = [2,45,2,4]

for i in lst:
    print(i)
✔ Output:
2
45
2
4
👉 Yaha i ki value:
2 → 45 → 2 → 4
________________________________________
🧠 2️⃣ for i in range(len(lst))
👉 Yaha i = index (position) hota hai
Example:
lst = [2,45,2,4]

for i in range(len(lst)):
    print(i)
✔ Output:
0
1
2
3
👉 Yaha i ki value:
0 → 1 → 2 → 3
________________________________________
🔁 Agar value chahiye:
for i in range(len(lst)):
    print(lst[i])
________________________________________
⚖️ Main Difference:
Loop type	i kya represent karta hai
for i in lst	value (element)
for i in range(len(lst))	index
________________________________________
🔥 Greatest number ke liye kya better hai?
👉 Best & simple:
lst = [2,45,2,2,4,5,676,6,33,22,9,488,90,24]

max_num = lst[0]

for i in lst:
    if i > max_num:
        max_num = i

print(max_num)
________________________________________
🔁 Same using index:
max_num = lst[0]

for i in range(len(lst)):
    if lst[i] > max_num:
        max_num = lst[i]

print(max_num)
________________________________________
🔑 Final samajh:
•	Direct value chahiye → for i in lst ✅ (easy) 
•	Index bhi chahiye → range(len(lst)) ✅
🔹 Uppercase vs Lowercase
Lowercase	ASCII	Uppercase	ASCII	Difference
a	97	A	65	-32
b	98	B	66	-32
c	99	C	67	-32
d	100	D	68	-32
👉 Rule:
chr(ord('a') - 32) = 'A'
chr(ord('A') + 32) = 'a'
________________________________________
🔹 Code Example (ord())
print(ord('a'))   # 97
print(ord('b'))   # 98
print(ord('A'))   # 65
________________________________________
🔹 Code Example (chr())
print(chr(97))   # 'a'
print(chr(65))   # 'A'
________________________________________
🔹 Even ASCII check
for ch in "abcdef":
    print(ch, ord(ch), "Even" if ord(ch) % 2 == 0 else "Odd")
👉 Output:
a 97 Odd
b 98 Even
c 99 Odd
d 100 Even
e 101 Odd
f 102 Even
________________________________________
🔥 Visual Pattern samajh lo
👉 Lowercase letters:
a b c d e f g h
97 98 99 100 101 102 103 104
 O  E  O   E   O   E   O   E
👉 Pattern:
•	Odd → a, c, e, g 
•	Even → b, d, f, h 
________________________________________
🚀 Final Samajh (Exam Trick)
•	ord(char) → number deta hai 
•	chr(number) → character deta hai 
•	±32 → case change 
•	%2 → even/odd check







