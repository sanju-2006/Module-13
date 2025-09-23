# Exp.No:34  
## implement stack using List and its built-in methods

---

### AIM  
Debug a Python program to implement stack using List and its built-in methods (append() and pop() ) in Python.  Get five items from the user and save them in stack, then pop two items from stack and display the stack before and after popped

---

### ALGORITHM

1. **Start the program.**
2. Define a set of valid operators: `*, -, +, %, /, **`.
3. Initialize an empty stack.
4. Traverse the prefix expression from **right to left**:
   - If the character is a **digit**, convert it to an integer and push it onto the stack.
   - If the character is an **operator**, pop two elements from the stack.
     - Apply the operator on the two popped operands.
     - Push the result back onto the stack.
   - If an invalid character is encountered, raise an error.
5. After traversal, the stack should contain only **one element**.
6. Return the **single element** as the evaluation result.
7. **End the program.**

---

### PROGRAM

```
stack = []
for i in range(5):
    a=input()
    stack.append(a)

print('Stack before elements are popped')
print(stack)

for i in range(2):
    stack.pop()


print('\nStack after elements are popped:')
print(stack)

```


### OUTPUT

<img width="1119" height="524" alt="image" src="https://github.com/user-attachments/assets/16db5157-d1dc-440f-9d40-c138dc8f43a9" />

### RESULT

Python program to implement stack using List and its built-in methods (append() and pop() ) in Python.  Get five items from the user and save them in stack, then pop two items from stack and display the stack before and after popped is successfully verified
