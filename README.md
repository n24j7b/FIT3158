java cMonash University Faculty of Information Technology 2nd Semester 2024 
 
FIT3158 Business Decision Modelling 
 
Assignment 2: Linear Programming, Integer Linear Programming, Network Analysis, 
Transportation, Transshipment and Economic Order Quantity (EOQ) - using Microsoft Excel 
Solver 
 
This assignment is worth 24% of your final mark (subject to the hurdles described in the 
FIT3158 Unit Guide and links therein). Among other things (see below), note the need to hit 
the `Submit’ button (and the possible requirement of a video and/or an interview). 
 
Due Date: Monday 30th September 2024, 11:55 pm 
Method of submission: Your submission should consist of 2 files: 
1. A Microsoft Excel spreadsheet named as: 
FamilyName-StudentId-2ndSem2024FIT3158Asst2.xlsx 
2. A text-based .pdf file named as: FamilyName-StudentId-2ndSem2024FIT3158Asst2.pdf 
Both the files must be uploaded on the FIT3158 Moodle site by the due date and time. 
The text-based .pdf file will undergo a similarity check by Turnitin at the time you submit 
to Moodle. Please read submission instructions here and elsewhere carefully regarding 
the use of Moodle. 
 
Total available marks = 50 + 34 + 16 = 100 marks. 
 
Note 1: Please recall the Academic Integrity rules (and, as per Moodle week 0, you might 
also wish to confer with https://www.monash.edu/student-academic-success). This is an 
individual assignment. Recall various resources from FIT3158 Moodle week 0. 
In submitting this assignment, you acknowledge both that you are familiar with the relevant 
policies, rules and regulations regarding Academic Integrity (including, e.g., doing your own 
work, not sharing your work, not using ChatGPT in particular, not using generative AI at all) 
and also that you are familiar with the consequences of being deemed to be in contravention 
of these policies. 
 
Note 2: And a reminder not to post even part of a proposed partial solution to a forum or 
other public location. This includes when you are seeking clarification of a question. 
If you seek clarification on an Assignment question then – bearing in mind the above – word 
your question very carefully and see the `Welcome to FIT3158’ Ed Discussion forum post 
(bearing in mind instructions in week 1 Introductory Lecture). If you are seeking to 
understand a concept better, then (please see the Welcome post in Ed Discussion, and) try to 
word your question so that it is a long way removed from the Assignment (which, in turn, 
makes it easier to answer – and probably also able to be answered by more people). You are 
reminded that Monash University takes academic integrity very seriously. 
 
Note 3: As previously advised, it is your responsibility to be familiar with the special 
consideration policies and special consideration process – as well as academic integrity. 
Please see the relevant links within FIT3158 Moodle (week 0 and perhaps also elsewhere). 
Students should be familiar with the special consideration policies and the process for 
applying. 
  
 
Note 4: As a general rule, don’t just give a number or an answer like `Yes’ or `No’ without 
at least some clear and sufficient explanation - or, otherwise, you risk being awarded 0 
marks for the relevant exercise. Make it easy for the person/people marking your work to 
follow your reasoning. Your .pdf should typically cross-reference the corresponding 
answer in your spreadsheet. For each and every question, sub-question and exercise, 
provide a clearly labelled separate spreadsheet tab with clear content, accompanied with 
clearly cross-referenced clear .pdf explanation. Without clear cross-reference between .pdf 
and spreadsheet tab – and without a separate spreadsheet tab for each sub-question - 
there is the possibility that any such exercise will be awarded 0 marks. 
Your .pdf file should not be generated from LaTeX (and/or Overleaf), nor OpenOffice, nor 
LibreOffice. 
Note 4b (and this is part of Note 4) : Re-iterating a point above, for each and every question, 
sub-question and exercise, clearly explain your answer and clearly show any working. 
 
Note 5: As a general rule, if there is an elegant way of answering a question without 
unnecessarily re-running the Solver, try to do it that way. (Recall, e.g., sensitivity report and 
some notions from Week 3 and thereabouts.) More generally, more elegant solutions are 
preferable - and will at least sometimes be given more marks (possibly many more marks, 
and the inelegant way might possibly get very few marks). Among other things, if a problem 
is a linear programming (LP) problem, then it would be more elegant to solve it using the 
linear simplex model. In a similar vein, a linking constraint (where appropriate) will be far 
preferable to a seemingly equivalent use of the IF() function. 
 
Note 6: You should include a screenshot of the relevant spreadsheet tab in your .pdf file. 
Apart from this, all of your submitted work should be in machine readable form, and none of 
your submitted work should be hand-written. 
 
Note 7: If you wish for your work to be marked and not to accrue (possibly considerable) 
late penalties, then make sure to upload the correct files and (not to leave your files 
as Draft). You then need to determine whether you have all files uploaded and that you are 
ready to hit `Submit’. Once you hit `Submit’, you give consent for us to begin marking your 
work. If you hit `Submit’ without all files uploaded then you will probably be deemed not to 
have followed the instructions from the Notes above. If you leave your work as Draft and 
have not hit `Submit’ then we have not received it, and it can accrue late penalties once the 
deadline passes. In short, make sure to hit ‘Submit’ at the appropriate time to make sure that 
your work is submitted. Late penalties will be as per Monash University Faculty of IT and 
Monash University policies. Within the requirements of these policies just mentioned, late 
penalties will accrue (in line with policy) at a rate of at least 5% per calendar day – where 5% 
refers to a proportion of the total marks available. It is possible that any work submitted at 
least 10 calendar days after the deadline might be automatically given a mark of 0. 
 
Note 8: The notation 1E-12 corresponds to 1 x 10
-12
, or 0.000000000001. A similar comment 
applies to 1E-14. If you see a figure of approximately this magnitude or comparable 
magnitude, then consider whether or not it might be round-off error for something else. 
 Unless otherwise stated, numbers should be stated to at least 3 significant figures, and 
numbers less than 10 in magnitude should be stated to at least 3 decimal places. 
 Note 9: Save your file(s) regularly. Most of the time, we expect that the Solver will run 
quickly. But for problems with many variables and many constraints – especially involving 
integers – please be mindful that if you are not careful to do some of the things mentioned in 
class to help your program finish more quickly, then there is a risk that your program might 
possibly go through at least tens or hundreds of thousands of subproblems and become very 
slow (as you wait and wait and …). If you save your file before starting a run that could be 
long and slow, then you can safely stop the program – if it becomes very slow – with reduced 
risk of losing your edit changes. 
 
Note 10: As a general rule for solving a problem using MicroSoft Excel Solver, please 
consider carefully whether the various solver (settings or) Options (which you might 
be able to access after clicking on `Options’, which might be on the right about twothirds
of the way down after you click on `Solver’) might affect the results provided 
by the solver. (As an example, if dealing with integers then give some thought to `Integer 
Optimality’.) Put another way, rather than just use the default settings, make sure to check 
the solver settings and be willing to appropriately modify them if and as required. 
 
The optimisations to follow throughout Assignment 2 (Questions 1, 2 and 3) could 
(variously) include such considerations as (including but not limited to) (e.g.) limiting 
pollution, saving time, reducing waste, making the most of limited resources, improving 
organ donor and recipient compatibility, etc. It could involve work with the United Nations 
(UN) and/or the International Space Station (ISS). Any transportation, transshipment and/or 
shortest path problems could possibly pertain to emergency vehicles (e.g., ambulance, fire, 
police) and to Search and Rescue (e.g., drones) – or simply cars and trucks. 
 
Question 1 (5 + 4 + 4 + 4 + 6 + 5 + 6 + 5 + 5 + 6 = 50 marks) 
 
Throughout Question 1 and the entire Assignment 2, follow the given notes (near the top – 
e.g., Note 4, Note 5, Note 6, etc.) and other instructions. 

 
Consider now Figure 1 immediately below but with the modifications stated just below it.  
We make some changes. First, the edge JI now has cost 20. We also add another node (or 
vertex), K. We also add three edges – namely, HK (cost 45), JK (cost 70) and IK (cost 45). 
This describes the network which we analyse at least for the start of Question 1. 
 
Before starting the exercises in Question 1, please remember that it is the modified version of 
Figure 1 (with modifications stated immediately above) that should be used at least to start 
the question. 
 
Unless stated otherwise, throughout Question 1 we use the modified version of Figure 1. 
 
Stated edge costs are the costs of moving one vehicle – e.g., moving 2 vehicles along an edge 
with stated cost 64 would cost 128. 

1a) We wish to move 70 vehicles from A to K. 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Also explain whether or not the problem is a linear programming (LP) problem or not - and 
why or why not. 
(If the problem can be presented as an LP problem then it should be done that way.) 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
1b) We wish to move 100 vehicles from B to I. 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
 1c) We wish to move 70 vehicles from A to I. 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Also explain whether or not the problem is a linear programming (LP) problem or not - and 
why or why not. 
(If the problem can be presented as an LP problem then it should be done that way.) 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
1d) We wish to move 100 vehicles from B to K. 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and sol代 写FIT3158、Java/c++
代做程序编程语言utions 
as instructed.  
 
1e) We re-visit the problem from 1d). However, we make some changes. 
The edges HK and IK (which had cost of 45 in parts 1a-1d) are now both modified as 
follows. For flow up to 75 (i.e., < 75), these edges still cost 45 per unit. But for flows above 
75, the excess flow costs 80 per unit. So, as an example, if HK has a flow of 90 then that 
costs 45 * 75 + 80 * (90 – 75) = 45 * 75 + 80 * 15 = 3375 + 1200 = 4575 for the flow on that 
edge. 
 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
1f) We re-visit the problem from 1d) and 1e). However, we make some changes. 
The edges HK and IK (which had cost of 45 in parts 1a-1d) are now both modified as 
follows. For flow up to 75 (i.e., < 75), these edges still cost 45 per unit. But for flows above 
75, the excess flow now costs 110 per unit. So, as an example, if HK has a flow of 90 then 
that costs 45 * 75 + 110 * (90 – 75) = 45 * 75 + 110 * 15 = 3375 + 1650 = 5025 for the flow 
on that edge. 
 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 1g) Following on from 1f, we include the additional constraint that at most 4 edges have 
positive non-zero flow. 
 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
1h) Combining 1a and 1b (in some sense), we now have 70 vehicles at A and 100 cars at B. 
We are required to supply 70 vehicles to K and 100 vehicles to I. 
 
What is the shortest total cost, and what is the flow along the individual edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
For the earlier parts of the question, we have assumed that there was just one type of vehicle. 
So, those (sub-)questions could be done whether everything was a car or everything was a 
truck. 
For the remainder of the question, we now assume that there is more than one type of vehicle 
(e.g., ambulance, fire truck, police car, other truck, other car). If someone has demand for an 
ambulance then they want an ambulance and they might have no need for a fire truck. 
 
For simplicity, we might just assume that there are just two different types of vehicle – car 
and truck. For the avoidance of doubt, we want the correct number of cars to go from 
source/supply to demand/destination/sink, and we also want the correct number of trucks to 
go from source to sink. Put in other words, if a demand node seeks 2 cars and 1 truck but 
instead gets 1 car and 2 trucks then that is not a correct answer. 
 
 
1i) Combining 1a, 1b, 1c and 1d (in some sense), we now have two types of vehicles (cars 
and trucks). The cars can be thought of as in 1h. More specifically, we have 70 cars at A and 
100 cars at B. We are required to supply 70 cars to K and 100 cars to I. However, we also 
have 70 trucks at A and 100 trucks at B. We are required to supply 100 trucks to K and 70 
trucks to I. 
 
What is the shortest total cost, and what is the flow (both cars and trucks) along the individual 
edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 1j) This is the same as 1i, but with the additional constraint that no edge can carry more than 
100 vehicles. So, whether it’s (e.g.) 100 cars or (e.g.) 100 trucks or (e.g.) 27 cars and 73 
trucks, etc., no edge can carry more than 100 vehicles. 
 
What is the shortest total cost, and what is the flow (both cars and trucks) along the individual 
edges? 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
Question 2 (6 + 6 + 6 + 6 + 6 + 4 = 34 marks) 
 
Throughout Question 2 and the entire Assignment 2, follow the given notes (near the top – 
e.g., Note 4, Note 5, Note 6, etc.) and other instructions. 
 
There are 8 (agents or) workers to be potentially assigned to 12 possible (tasks or) jobs. 
 
The workers put in their first 4 preferences (P1, P2, P3, P4). 
For each worker that gets their 1st preference, there is a score of 10. 
For each worker that gets their 2nd preference, there is a score of 6. 
For each worker that gets their 3rd preference, there is a score of 3. 
For each worker that gets their 4th preference, there is a score of 1. 
No additional scores are given when a worker gets their 5th, 6th, 7th, … and/or 12th preference. 
 
The preferences (P1, P2, P3, P4) for each person (a, b, c, d, e, f, g, h) are given below:  
 
2a) Each of the eight workers is to be assigned to at most 1 job each. 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 2b) We modify 2a so that each of the eight workers can be assigned to at most 4 jobs each. 
 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
2c) We modify 2b so that no more than 6 of the 8 workers can be used. 
 
As before, each of these six workers can be assigned to at most 4 jobs each. 
 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
2d) We modify 2a and 2b so that all 8 workers can be used but each of these eight workers 
can be assigned to at most 2 jobs each. 
 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
 2e) We now modify 2d so that at most one (but not both) of worker a and worker b can do a 
task. If either worker a does at least one task or worker b does at least one task, then the 
other of these two workers can not do any tasks. Put another way, if worker a does at least 
one task then worker b does no task, and if worker b does at least one task then worker a does 
no task. 
Apart from this, all 8 workers can be used but each of these eight workers can be assigned to 
at most 2 jobs each. 
 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
2f) We modify 2d so that at most 6 workers can be used, and each of these six workers can 
be assigned to at most 2 jobs each. 
 
No job can be done by more than one worker. 
What is the maximum score that can be obtained, and what is the assignment of workers to 
jobs? 
 
Express all variables, the objective function, all constraints, working and solution (values of 
decision variables, value of objective function). 
Further to Note 4 and Note 6, (here and elsewhere) please place your working and solutions 
as instructed. 
 
Question 3 (5 + 5 + 4 + 2 = 16 marks) 
 
This question concerns variants of the Economic Order Quantity (EOQ) model. 
 
Throughout Question 3 and the entire Assignment 2, follow the given notes (near the top – 
e.g., Note 4, Note 5, Note 6, etc.) and other instructions. 
 
Consider a monthly demand of 2000, a monthly holding cost of 0.02 = 2%, a cost per unit of 
100 Malaysian ringgits (MYR) and an ordering cost of 500 MYR. 
Assume no quantity discounts and no back-order penalty. 
 
 3a) Calculate the economic order quantity (EOQ) value, Q*. 
 
Show your calculations in your .pdf file. 
There might be more than one way to do it in your spreadsheet tab. 
Whatever you do, show working and solution values (any decision variable or decision 
variables, any optimised objective function). 
 
3b) We re-visit Qu 3a but with a back-order penalty of p = MYR 102.32 per annum. 
 
Calculate Q*, S* and the maximum amount by which we would be out of stock before 
replenishing with new stock. 
 
Also state the minimum cost. 
 
Show your calculations in your .pdf file. 
Also show your calculations in your spreadsheet tab. 
Show working and solution values (any decision variable or decision variables, any optimised 
objective function). 
 
3c) We re-visit Qu 3a with discount for bulk orders. 
For an order of 1200 or more, there is a bulk discount of 19.5%. 
 
Calculate the optimal Q* and the minimum cost. 
 
Show your calculations in your .pdf file. 
Also show your calculations in your spreadsheet tab. 
Show working and solution values (any decision variable or decision variables, any optimised 
objective function). 
 
3d) Which is cheaper – the value from Qu 3b or the value from Qu 3c? 
 
Adjust the back-order penalty p from Qu 3b until the answers to 3b and 3c agree. 
 
What is the new value of p? 
 
Did you have to increase or decrease p - and, if you had to change p, then by how much? 
 
Recall notes and other instructions at the start of the Assignment and throughout the 
Assignment – and in the Ed Discussion `Welcome to FIT3158’ post - and follow these. 
 
END OF FIT3158 ASSIGNMENT 2 (Monash University, 2nd semester 2024) 

         
加QQ：99515681  WX：codinghelp
