# Python

## Exercises

### 1. Print Hello, world
<details>
<summary>Solution</summary>
<p>

```python
print("Hello, world")
```

</p>
</details> 

### 2. Print user input
<details>
<summary>Solution</summary>
<p>

```python
i = input("input string: ")
print(i)
```

</p>
</details> 

### 3. Accept two numbers from the user and calculate multiplication
<details>
<summary>Solution</summary>
<p>

```python
num1 = int(input("Enter first number "))
num2 = int(input("Enter second number "))

res = num1 + num2
print("Sum is", res)
```

</p>
</details> 

### 4. Display float number with 2 decimal places

Display ```12.3456``` as ```12.34```

<details>
<summary>Solution</summary>
<p>

```python
print('%.2f' % 12.3456)
```

</p>
</details> 

### 5. Accept a list of 5 float numbers as an input from the user

Expected Output: ```[78.6, 78.6, 85.3, 1.2, 3.5]```

<details>
<summary>Solution</summary>
<p>

```python
floatNumbers = []
  
for i in range(0, 5):
    item = float(input("Enter float number:"))
    floatNumbers.append(item)
    
print("Float list: ", floatNumbers)
```

</p>
</details> 


### 6. Format the following data using a string.format() method

Input:
```
totalMoney = 1000
quantity = 3
price = 450
```

Output:
```
I have 1000 dollars so I can buy 3 apples for 450.00 dollars.
```

<details>
<summary>Solution</summary>
<p>

```python
quantity = 3
totalMoney = 1000
price = 450
statement1 = "I have {1} dollars so I can buy {0} apples for {2:.2f} dollars."
print(statement1.format(quantity, totalMoney, price))
```

</p>
</details>
