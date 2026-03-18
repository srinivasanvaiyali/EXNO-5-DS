# EXNO-5-DS-DATA VISUALIZATION USING MATPLOT LIBRARY

# Aim:
  To Perform Data Visualization using matplot python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
# Line Graph
```
import matplotlib.pyplot as plt
x= [0,1,2,3,4,5]
y=[0,1,4,9,16,25]
plt.plot(x,y)
plt.show()
```
<img width="836" height="582" alt="323063912-714c39f4-c504-451e-ba95-54704ab98ca1" src="https://github.com/user-attachments/assets/cdad03ba-8a2e-4cc0-a582-add9cad934ad" />
```
import matplotlib.pyplot as plt
x1 = [1,2,3]
y1 = [2,4,1]
plt.plot(x1, y1, label="line 1")

x2 = [1,2,3]
y2 = [4,1,3]
plt.plot(x2, y2, label="line 2")

plt.xlabel('x - axis')
plt.ylabel('y - axis')

plt.title('Two lines on same graph!')

plt.legend()
plt.show()
```
<img width="713" height="575" alt="560423380-bfb780f5-4399-4063-8bde-471f7a8b286e" src="https://github.com/user-attachments/assets/9c62195a-20b9-47a1-8fa6-510c91132d77" />
```
import matplotlib.pyplot as plt

x = [1,2,3,4,5,6]
y = [2,4,1,5,2,6]

plt.plot(x, y, color='red', linestyle='dashed', linewidth = 5, marker='o', markerfacecolor='blue', markersize=14)

plt.ylim(1,8)
plt.xlim(1,8)

plt.xlabel('x - axis')
plt.ylabel('y - axis')

plt.title('Line customization!')

plt.show()
```
<img width="695" height="566" alt="560424341-d8a861c8-8ed2-4046-a225-9f3c460143ec" src="https://github.com/user-attachments/assets/bb8584c2-5d43-4491-85d9-5e7dcca56d05" />
# Scatter Plot :
```
import numpy as np
x = np.arange(0,10)
y = np.arange(11,21)
x
y
```
<img width="372" height="51" alt="560425570-268e77b7-849c-47a4-b15d-9e07037f0a30" src="https://github.com/user-attachments/assets/9512aeb1-f485-4937-b75b-30189d1e56e5" />
<img width="479" height="56" alt="560425704-9d0e995a-996e-42e1-abdf-2e31ad0ebf8d" src="https://github.com/user-attachments/assets/c3a6dd78-5f5e-45b3-9085-04bda56acb69" />
```
y=x*x
y
```
<img width="473" height="44" alt="560425899-81a0566f-6927-4213-a765-f527e91181dc" src="https://github.com/user-attachments/assets/7f9d2908-91ba-4c65-bbcd-7ea89dec9057" />
```
plt.plot(x, y, 'g*', linestyle='dashed', linewidth = 2, markersize = 14)
plt.xlabel('x - axis')
plt.ylabel('y - axis')
plt.title('2d Diagram')
```
<img width="707" height="599" alt="560426057-7581d292-65b8-420b-82d5-825c22ff07dc" src="https://github.com/user-attachments/assets/73f8fd7c-8bc6-4bdd-b544-9de4bc4bfc29" />
```
np.pi
```
<img width="195" height="40" alt="560426430-77f8c7cd-c214-43c2-a044-77a3642bdbd4" src="https://github.com/user-attachments/assets/5cf57cba-a89e-4078-8e4e-aa4d6ab3919e" />
```
x = np.arange(0, 2*np.pi, 0.1)
y = np.sin(x)
plt.title("sine wave form")

plt.plot(x,y, 'go', markersize=8, color="pink")
plt.show()
```
<img width="725" height="596" alt="560426703-0e4ff3b8-c87f-4028-992f-27cf6b672e91" src="https://github.com/user-attachments/assets/4fba63dd-17e1-43d8-b8b0-4c8002d1b566" />
# Area Chart :
```
import matplotlib.pyplot as plt
import numpy as np
x = [1,2,3,4,5]
y1 = [10,12,14,16,18]
y2 = [5,7,9,11,13]
y3 = [2,4,6,8,10]
plt.fill_between(x, y1, color='blue')
plt.fill_between(x, y2, color='green')
plt.plot(x, y1, color='red')
plt.plot(x, y2, color='black')
plt.legend(['y1','y2'])
plt.show()
```
<img width="697" height="517" alt="560427130-441946d7-12a6-41bd-b5bb-75784a8f36aa" src="https://github.com/user-attachments/assets/ad7cac9c-c69e-4f53-a489-0dc35d384f4e" />
# Bar Chart :

import matplotlib.pyplot as plt
val=[5,6,3,7,2]
n=["A", "B", "C", "D", "E"]
plt.bar(n,val,color="green")
plt.show()

<img width="701" height="516" alt="324333423-c0033a63-164f-4cc4-996f-95201893ecd0" src="https://github.com/user-attachments/assets/f81e11bc-b915-4f9d-be5d-77da2480a872" />
```
import matplotlib.pyplot as plt 
val=[5,6,3,7,2] 
n=["A", "B", "C", "D", "E"] 
plt.barh(n,val,color="green")
plt.show()
```
<img width="674" height="519" alt="560428278-d4ef3611-c357-4b02-beef-0f98f2057d0a" src="https://github.com/user-attachments/assets/bbba98c5-45a1-4dcc-adcb-314ac277b951" />













# Result:
 Include your result here
