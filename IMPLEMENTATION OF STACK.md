# Exp.No:31  
## evaluate the user given Prefix expression using stack

---

### AIM  
Write a Python program to evaluate the user given Prefix expression using stack. The infix expression must contain operators viz., Multiplication, Addition and Subtraction

[ Output format:

Prefix Expression : +23
Evaluation result : 5 ]

---

### ALGORITHM

1. **Start the program.**
2. **Define a class `st`** with the following methods:
   - `push(self, num)`: Adds the number `num` to the stack.
   - `pop(self)`: Removes and returns the top element from the stack.
3. **Create a stack object `s`** using the class `st`.
4. **Input the stack size**: Take an integer input `size` to define the size of the stack.
5. **Loop through numbers from 1 to size**: Add only the odd numbers to the stack using the `push()` method.
6. **Display the elements** in the stack after the loop completes.
7. **Call `pop()`** to remove the top element from the stack and display the popped element.
8. **Display the stack again** to show the remaining elements.
9. **End the program.**

---

### PROGRAM

```
OPERATORS=set(['*','-','+','%','/','**']) 

def evaluate(expression):
	
	stack = []
	for c in expression[::-1]:
	    if c not in OPERATORS:
	        stack.append(int(c))
	    else:
	        o1=stack.pop()
	        o2=stack.pop()
	        
	        if c == '+':
	            stack.append(o1+o2)
	        elif c=='-':
	            stack.append(o1-o2)
	        elif c=='*':
	            stack.append(o1*o2)
	return stack.pop()
test_expression=input()
print("Prefix Expression :",test_expression)
print("Evaluation result :",evaluate(test_expression))
```


### OUTPUT

Prefix Expression : +-927
Evaluation result : 14

### RESULT

<img width="782" height="236" alt="image" src="https://github.com/user-attachments/assets/97e409d7-bf87-4f6b-8e80-1c177921d71e" />
