# Fitting Poisson  distribution

# Aim : 

To fit poisson distribution for the arrival of objects per minute from the feeder

# Software required :  

Python and Visual component tool

# Theory:

The Poisson distribution is the discrete probability distribution of the number of events occurring in a given time period, given the average number of times the event occurs over that time period.

![image](https://user-images.githubusercontent.com/104613195/166248326-fd042076-8b0b-40c4-8b11-1d8e8fcb74db.png)

 Conditions for Poisson Distribution:

1. An event can occur any number of times during a time period.
2. Events occur independently. I
3. The rate of occurrence is constant.
4. The probability of an event occurring is proportional to the length of the time period. 
 
# Procedure :

![image](https://user-images.githubusercontent.com/104613195/166251988-d0c53205-6080-4f7b-ae4c-398178586637.png)

# Experiment :

![image](https://user-images.githubusercontent.com/103921593/230282876-f4a5afbf-cac1-4648-a1b0-c78840638a8e.png)

# Program :

 ```python
import math

# observed values
x = [0,1,2,3,4,5]

# observed frequency
f = [5,9,12,8,4,2]

# total observations
N = sum(f)

# calculate mean (lambda)
sum_xf = 0
for i in range(len(x)):
    sum_xf = sum_xf + x[i]*f[i]

lam = sum_xf / N

print("Mean (lambda) =", lam)

print("\nPoisson Probability and Expected Frequency\n")

for i in x:
    p = (math.exp(-lam) * lam**i) / math.factorial(i)
    expected = N * p
    print("x =", i, "  P(x) =", round(p,4), " Expected Frequency =", round(expected,2))
```

# Output : 
<img width="1686" height="901" alt="image" src="https://github.com/user-attachments/assets/7b014e1b-f474-4c08-b262-469bf061997f" />

GITHUB LINK:
https://github.com/Dinesh7311/Poisson_distribution/edit/main/README.md

# Results

The Poisson distribution is fitted for the objects arrived from feeder per minute and the data is tested using Chi-square test. 
 
