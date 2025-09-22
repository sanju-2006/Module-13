# Exp.No:35  
## TOWER OF HANOI

---

### AIM  
To write a Python program to implement **Tower of Hanoi** and display all the moves of the disks using a recursive function.  
Consider the names of the tower pegs as A, B, C. Get the number of disks value from the user.

---

### ALGORITHM  

1. **Start the program.**
2. **Input** the number of disks `n`.
3. **Print** the number of disks.
4. Define a **recursive function** `TowerOfHanoi(n, source, destination, auxiliary)`:
   - If `n == 1`:
     - Print: "Move disk from source to destination".
   - Else:
     - Call `TowerOfHanoi(n - 1, source, auxiliary, destination)`  
       → Move `n-1` disks from source to auxiliary using destination as helper.
     - Print: "Move disk from source to destination"  
       → Move the largest disk to the destination.
     - Call `TowerOfHanoi(n - 1, auxiliary, destination, source)`  
       → Move `n-1` disks from auxiliary to destination using source as helper.
5. Call `TowerOfHanoi(n, 'A', 'C', 'B')` to start the process.
6. **End the program.**

---

### PROGRAM  

```
def TowerOfHanoi(n , source, destination, auxiliary):
	
	if n>0:
	    TowerOfHanoi(n-1, source,auxiliary,destination)
	    print("Move disk from",source,"to",destination)
	    TowerOfHanoi(n-1,auxiliary,destination, source)

n=int(input())		
print("No. of disks =",n)

```

### OUTPUT

No. of disks = 2
Move disk from A to B
Move disk from A to C
Move disk from B to C

### RESULT


<img width="849" height="836" alt="image" src="https://github.com/user-attachments/assets/c171a573-8710-4765-911d-0755c4a46f4f" />

