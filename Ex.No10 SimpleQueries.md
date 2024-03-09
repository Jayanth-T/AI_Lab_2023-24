# Ex.No: 10  Logic Programming –  Simple queries from facts and rules
### DATE:                                                                            
### REGISTER NUMBER : 
### AIM: 
To write a prolog program to find the answer of query. 
###  Algorithm:
 Step 1: Start the program <br> 
 Step 2: Convert the sentence into First order Logic  <br> 
 Step 3:  Convert the sentence into Horn clause form  <br> 
 Step 4: Add rules and predicates in a program   <br> 
 Step 5:  Pass the query to program. <br> 
 Step 6: Prolog interpreter shows the output and return answer. <br> 
 Step 8:  Stop the program.
### Program:
### Task 1:
Construct the FOL representation for the following sentences <br> 
1.	John likes all kinds of food.  <br> 
2.	Apples are food.  <br> 
3.	Chicken is a food.  <br> 
4.	Sue eats everything Bill eats. <br> 
5.	 Bill eats peanuts  <br> 
   Convert into clause form and Prove that John like Apple by using Prolog. <br> 
### Program:


### Output:

### Task 2:
Consider the following facts and represent them in predicate form: <br>              
1.	Steve likes easy courses. <br> 
2.	Science courses are hard. <br> 
3. All the courses in Have fun department are easy <br> 
4. BK301 is Have fun department course.<br> 
Convert the facts in predicate form to clauses and then prove by resolution: “Steve likes BK301 course”<br> 

### Program:
```
likes(steve, easy_courses).
likes(_, have_fun_courses).  % Everyone likes courses in Have fun department
hard(science_courses).
have_fun_course(bk301).
likes(steve, Course) :-
    have_fun_course(Course).
```

### Output:
![image](https://github.com/Jayanth-T/AI_Lab_2023-24/blob/main/Screenshot%202024-03-09%20161053.png)
### Task 3:
Consider the statement <br> 
“This is a crime for an American to sell weapons to hostile nations. The Nano , enemy of America has some missiles and its missiles were sold it by Colonal West who is an American” <br> 
Convert to Clause form and prove west is criminal by using Prolog.<br> 
### Program:
```
american(colonel_west).
hostile(nano).
has_missiles(nano).
sold_weapons(colonel_west, nano).
criminal(Person) :-
    american(Person),
    sold_weapons(Person, Country),
    hostile(Country).
```

### Output:
![image](https://github.com/Jayanth-T/AI_Lab_2023-24/blob/main/Screenshot%202024-03-09%20161417.png)
### Result:
Thus the prolog programs were executed successfully and the answer of query was found.
