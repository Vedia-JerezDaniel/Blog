# Public spending efficiency in the Regional Government of Madrid after Covid-19


## Daniel H. Vedia-Jerez


## Abstract

This document proposes an experiment of optimal public expenditure under the economic recession of the Covid-19. The empirical part is based on a linear optimization model. We review the public expenditure of the Regional Government of Madrid; we propose a possible ‘stimulus spending’ package to battle the economic recession after the Covid-19. The linear optimization formula is expressed as a revision of the public budget with sufficient statistics of the expenditure, on the other hand, we propose to strengthen: the budget on health, education, and social policies, and other expenditures efficiently to increase economic growth in the following years.


## 1. Reviewing the efficient stimulus

Empirical evidence suggests that policy simulations show that reducing allocations for secondary education and correspondingly increasing allocations of public education expenses for higher education, produce monotonically decreasing growth if an expansion of higher education does not foster technological progress. On the other hand, if higher education is well integrated with technological innovation, the former can become a powerful engine of inclusive growth. Moreover, Gonand et al. (2009) highlight that efficiency gains in education spending will have large effects on GDP in the long run. A 10% increase in educational output might raise GDP by an estimated 3-6% in the long run in most OECD countries. 


However, economic growth is not monotonically increasing with respect to expenditures on higher education when the latter is closely linked with technological innovation. Further, there are other important expenditures as health and economic promotion policies.


```See: Frédéric Gonand, Robert Price and Douglas Sutherland (2009), “Improving public spending efficiency in primary and secondary education”. OECD Journal: Economic Studies 2009(1):4-4.``` 

For economic policymakers, ‘it is important to know how far a given economic sector can be expected to increase its output by simply increasing its efficiency, without absorbing further resources’. The effectiveness of public expenditure is more difficult to assess than efficiency since the outcome is influenced by political choices. The distinction between output and outcome is often blurred and the outcome is used in a substitutable manner. For example, the outputs of an education system are often measured in terms of performance, while efficiency in transports, could be measure in speed travel and environment cost. The effectiveness shows the success of the resources used in achieving the objectives set.


This document chooses a narrower approach and considers the public spending allocated to the production of a given public service, like public spending on health, education, or infrastructure as a measure of input. Although policymakers are interested in the outcome, like increasing economic growth, it is only partly under their direct influence and not always achievable within one political cycle. Against the background of efficiency and effectiveness analyses, it is important to scrutinize both large spending items, like social protection, and small, but growth-enhancing ones. As regards the latter, even if the spending items account for a small share of total spending efficiently, they can have a major impact on the performance of an economy.


## 2.	Creating the optimized model


The goal of this document is to help policymakers to structure and increase the efficiency of financial resources while maintaining budget equilibrium in an increasingly indebted regional economy. We also developed a fuzzy method for applying the optimization model using different scenarios that were simulated using the budget of the previous economic recession (2013/2011) , and the budget from 2016, which reflects a higher increment in the budget and economic activity in general. 

```We consider the budgets of 2011 and 2013, because the fiscal adjustments started in 2010/2011, an officially the budget expenditure increases again in 2016, also we have to consider the data availability since there is no official data before 2011. Among the limitations, previous fiscal budgets are not in excel format so we cannot consider disaggregated chapters.```

### 2.1	The problem structures 


In its simplest form, the public financing plan allocation problem can be formulated as a linear program, that was structured using the 14 main general accounts of the Community of Madrid Financial Plan for 2019, which is the latest approved budget. But it was much practical to reduce the number of accounts to 8, we gather together the following accounts and separate the Health services in two: Health central services and the 11 mayor hospitals for the Covid–19: ```Hosp.U. La Paz/Carlos III, Hosp.U.12 De Octubre, Hosp.U. Ramón y Cajal, Hosp. Clínico, Hosp.U. La Princesa, Hosp.U. Pta. De Hierro, Hosp.U. Getafe, Hosp.U. Severo Ochoa, Hosp.U. Ppe. De Ast., Hosp.G.U.G. Marañón, Hosp.U. Inf.Leonor.```


1.	Executive and Assembly + Justice
2.	Education first and second. level + Educ. Scholarships + University + R&D
3.	Employment policies + Social policies and Family
4.	Health and central services 
5.	11 mayor hospitals Covid–19
6.	Culture, Tourism, and Sports + Environment
7.	Economy, Finance + Transports and housing
8.	Debt


### 2.2	Linear optimization model

We performed an extensive validation across all the options that could be selected. The validation was an exhaustive but critical effort because the results of the optimization included all the variables, so we also decided to make different assumptions to strengthen our results. In that way, we constructed three different scenarios:


i)	_The first includes the current values of each account for 2019 as accorded to the Financial Plan._

ii)	_Second, we propose an alternative version, in case of an economic recession, to do this we revise the Financial Plans from 2011-2016, considering its history and evolution, we changed the values in the objective function and some of the restrictions._

iii)	_The last one is the fuzzy model, we took into account the additional resources from the Central Government. Specifically, 10,000€ M. will be used to cover health expenses, 1,000€ M. for social spending, and education that will be distributed according to population criteria. Finally, the 5,000€ M. destined to alleviate the reduction in their resources. Additionally, fiscal deficit (debt) could be increased by 0.2%, we assume Madrid will take around the 3,400€ M. of these additional resources._


Within the executive budget, we introduce the following basic constraints for the financial plan system:

C1)  Do not exceed the budget for ‘less important’ sectors (culture and environment);  

C2)  Do not exceed size expenditure for the General administration;

C3)  Do not increase public debt for two years, during the economic recession of 2008, debt increases from 1,067€ M. to 2,909€ M.;

C4)  Possibly to increase the Health assistance budget for Covid-19,  

C5)  This is also an opportunity to increase the Education + R&D budget;   

C6)  To battle against the economic downturn we need additional expenditure on employment formation and social protection.


We developed some ‘sensitivity’ matrices that reflect the change for the different categories across the four years considered, total expenditure, and its value over the total income of the regional government, the matrices can be routinely updated as economic conditions change. We developed two optimized models for the different types of expenditure categories, then we compared the first optimized scenario with a fuzzy optimized model.

Under the first two scenarios, we varied several key assumptions and combinations that corresponded to each economic situation. For the 1st model, we assume _(i) the values of the objective function corresponding to a scenario without a recession and no additional expenditure; for the 2nd model, (ii) the previous values were according to the previous economic recession, and we also changed the restrictions._ 

We introduce Equation 1 and its restrictions for the 1st model, later we will also include the equations for the fuzzy optimized model. 


Max: 2.7*E.A.Just + 16.15*A.Educ + 2.1*Soc.emp + 18.3*HCS + 17.2*HCov + 0.09*ECT + 1.5*EcoTr + 15.9*Debt

$s.a.$

$E.A.Just + A.Educ + Soc.Emp + HCS + HCov + ECT + EcoTr + Debt \leq 23873$

0.07*E.A.Just -0.93*A.Educ - 0.93*Soc.Emp - 0.93*HCS - 0.93*HCov - 0.93*ECT - 0.93*EcoTr - 0.93Debt $\leq$ 0

$E.A.Just \leq 6024$

$Soc.Emp \leq 2302$

$HCS + HCov \leq 8109$

-0.98*E.A.Just - 0.98*A.Educ - 0.98*Soc.Emp - 0.98*HCS - 0.98*HCov + 0.02*ECT - 0.98*EcoTr - 0.98*Debt $\leq$ 0

$EcoTr \leq 2280$

$Debt \leq 3626$

Where the abbreviations of the formula are the following:

Executive, Assembly and Justice (E.A.Just), Public Debt (Debt), Education, University + R&D and Education scholarships (A.Educ), Social and employment policies (Soc.emp), Health Central services (HCS), top 11 Hospitals for Covid-19 pandemic (HCov), Environment, Culture & Tourism (ECT), Economy and Transports (Eco&Tr). 

Due to the low weight of some expenditure chapters to the total, we gather together some of them, for example, _Executive and Assembly + Justice_, and we sum together all the education chapters: _Education, University + R&D, scholarships_.

The objective function values are the percentage of chapter expenditures divided by the Gross Domestic Product (GDP) of Madrid for 2018 (1st model) and 2011 (2nd model), additionally, for Education, Health, Transports + housing, Culture, we take the mean of its share on GDP and its respective percentage expenditures on GDP. Regarding the Public Debt, we assume it with a negative sign on the objective function, with -0.12 for the 1st model, and -0.15 for the 2nd model, we assume a moderate increment of 2.5%, since Madrid is already indebted.

•	Eq. (1) introduces the scenario with a growth episode, and with the restrictions that allocations for Executive+Justice, Environment+Culture do not exceed 7% and 2% of the total budget respectively.

•	For the 2nd model, the restrictions are: Executive+Justice, Environment+Culture with a restriction that both don’t surpass the 8%, all education couldn’t pass the 23% of the total, health increases a 2.5%, and the expenditure on Economy and Transports is around the 10%. We assume that the total budget has an increase of 2.3%.


### 2.3	Optimized values for the fuzzy model

In this section we introduce the optimization for the fuzzy model, we modeled uncertainty by combining the optimization model of the previous system with a fuzzy model that optimizes parameters under softening some of the restrictions (this is associated with the concept of memberships function).

It is important to remember that we change 1st model restrictions, here we took into account the additional resources from the Central Government to lighten the budget stress against the pandemic. We will consider the 10,000€ M. that will be used to cover health expenses, 1,000€ M. for social spending, and education that will be distributed according to population criteria, other 5,000€ M. destined to alleviate the reduction in their resources. Additionally, fiscal deficit (Debt) could be increased by 0.2%, we assume Madrid will take around the 3,400€ M. of the total – almost 21.25%-.

With that information, we introduce a left trapezoidal fuzzy membership function only for those chapters that will receive the additional resources, that is Education, Health and, employment and social spending - plus a right trapezoidal membership only for Total Budget and Public Debt, see Equation (2).


$ Max: \alpha$

$s.a.$

0.05*E.A.Just + 0.18*A.Educ + 0.07*Soc.Emp + 0.1*HCS + 0.14*HCov + 0.04*ECT + 0.1*EcoTr - 0.12Debt $\leq$ 24936

$E.A.Just \leq 1089$

$A.Educ +213*\alpha \leq 6024$

$Soc.Emp \leq 2302$

$HCS + HCov \leq 8109$

$ECT \leq 2281$

$EcoTr \leq 2280$

$Debt \leq 3626$

### 3.	Results and main conclusions

This document chooses a narrmver approach considering the public spending allocated to a given public service. Our results show the following tentative conclusions.

Table 1 shows the results for each model, in the first column we can sec that in growth episodes (no Covid-19), the distribution of expenditure would almost the same as the Official Financial plan, however with more investment in Social policies and increasing debt payments (it make sense to reduce debt under economic growth episodes), and considerable reductions in transportation and education. On the other hand, considering the budget allocation under economic recession (2010-2011), almost all budget allocation receives less investment, except for Health, transportation, and environment.

```Health expenditure increases almost 2.3% during the recession, and the investment in environment plan in 2011 was of 602€ Mill. in 2019 it was of 216€ Mill. It makes sense that the 2nd model considers a higher allocation for Culture and Environment since the values for the 2nd model considered the Financial plans of 2011-2013.```

Considering the results for the fuzzy model taking the values of the 1st model plus the additional resources, we assume we got. the maximum of resources that policymakers could invest after Covid-19 considering a possible outbreak of the virus, it makes sense, increase Health and, Employment and Social policies for a most likely economic recession, and additionally, it is an opportunity for the first. time to invest. in Education and R&D.

Concluding, although the results arc tentative, it. also introduces good rules of budget management, that is, under growth episodes, you could increase public debt, and in recession, don't get overindebted, reviewing the Financial plans, Madrid never recovered its income budget, it just contracted debt . Also, it attracts my attention that the budget for a green policy is around 200€ Mill. for the next years, the third part of 2010.

After t his exercise for Public Budget, for the next future, it could be more interesting to take disaggregatcd information of each chapter to probably get a more precise idea of how we can increase public expenditure efficiency.


```python
from scipy.optimize import linprog
```

##### A) Growth episodes, no Covid-19


```python
obj = [-0.05,-0.18,-0.07,-0.10,-0.14,-0.04,-0.1,0.12]

lhs_ineq = [[1,1,1,1,1,1,1,1],
              [1,0,0,0,0,0,0,0],
              [-.25,.75,-.25,-.25,-.25,-.25,-.25,-.25],
              [-.11,-.11,.89,-.11,-.11,-.11,-.11,-.11],
              [ 0,0,0,1,1,0,0,0],
              [0,0,0,0,0,1,0,0],
              [-.14,-.14,-.14,-.14,-.14,-.14,.86,-.14],
              [0,0,0,0,0,0,0,1]]

rhs_ineq = [23873,1098,0,0,8109,432,0,3626]
```


```python
opt = linprog(c=obj, A_ub=lhs_ineq, b_ub=rhs_ineq,method="simplex")
opt
```



##### B) Economic recession model


```python
obj_1 = [-0.05,-0.13,-0.07,-0.12,-0.13,-0.038,-0.1,0.15]

lhs_ineq_1 = [[1,1,1,1,1,1,1,1],
              [1,0,0,0,0,0,0,0],
              [-.23,.77,-.23,-.23,-.23,-.23,-.23,-.23],
              [-.11,-.11,.89,-.11,-.11,-.11,-.11,-.11],
              [0,0,0,1,1,0,0,0],
              [0,0,0,0,0,1,0,0],
              [-.12,-.12,-.12,-.12,-.12,-.12,.88,-.12],
              [0,0,0,0,0,0,0,1]]

rhs_ineq_1 = [24422,1035,0,0,8316,610,0,3808]
```


```python
opt_1 = linprog(c=obj_1, A_ub=lhs_ineq_1, b_ub=rhs_ineq_1, method="simplex")
opt_1
```





```python
from pulp import LpMaximize, LpProblem, LpStatus, lpSum, LpVariable
```


```python
# Define the model
model = LpProblem(name="resource-allocation", sense=LpMaximize)

# Define the decision variables
x = {i: LpVariable(name=f"x{i}", lowBound=0) for i in range(1, 9)}

# Add constraints
model += (lpSum(x.values()) <= 23873, "total")
model += (1 * x[1] <= 1089, "Exec")
model += (-.25*x[1]+.75*x[2]+-.25*x[3]+-.25*x[4]+-.25*x[5]+-.25*x[6]+-.25*x[7]+-.25*x[8] <= 0, "Educ")
model += (-.11*x[1]+-.11*x[2]+.89*x[3]+-.11*x[4]+-.11*x[5]+-.11*x[6]+-.11*x[7]+-.11*x[8] <= 0, "Soc. Pol")
model += (x[4]+x[5] <= 8190, "Health")
model += (x[6] <= 432, "Culture")
model += (-.14*x[1]+-.14*x[2]+-.14*x[3]+-.14*x[4]+-.14*x[5]+-.14*x[6]+.86*x[7]+-.14*x[8] <= 0, "Econ")
model += (x[8] <= 3626, "Debt")

model += 0.05*x[1]+0.18*x[2]+0.07*x[3]+0.10*x[4]+0.14*x[5]+0.04*x[6]+0.1*x[7]-0.12*x[8] 

```


```python
# Solve the optimization problem
status = model.solve()

# Get the results
print(f"status: {model.status}, {LpStatus[model.status]}")
print(f"objective: {model.objective.value()}")

for var in x.values():
    print(f"{var.name}: {var.value()}")

for name, constraint in model.constraints.items():
    print(f"{name}: {constraint.value()}")
```

##### B) Economic recession model


```python
# Define the model
model_1 = LpProblem(name="resource-allocation", sense=LpMaximize)

# Define the decision variables
x = {i: LpVariable(name=f"x{i}", lowBound=0) for i in range(1, 9)}

# Add constraints
model_1 += (lpSum(x.values()) <= 24422, "total")
model_1 += (1 * x[1] <= 1035, "Exec")
model_1 += (-.23*x[1]+.77*x[2]+-.23*x[3]+-.23*x[4]+-.23*x[5]+-.23*x[6]+-.23*x[7]+-.23*x[8] <= 0, "Educ")
model_1 += (-.11*x[1]+-.11*x[2]+.89*x[3]+-.11*x[4]+-.11*x[5]+-.11*x[6]+-.11*x[7]+-.11*x[8] <= 0, "Soc. Pol")
model_1 += (x[4]+x[5] <= 8316, "Health")
model_1 += (x[6] <= 610, "Culture")
model_1 += (-.12*x[1]+-.12*x[2]+-.12*x[3]+-.12*x[4]+-.12*x[5]+-.12*x[6]+.88*x[7]+-.12*x[8] <= 0, "Econ")
model_1 += (x[8] <= 3808, "Debt")

model_1 += 0.05*x[1]+0.13*x[2]+0.07*x[3]+0.12*x[4]+0.13*x[5]+0.038*x[6]+0.1*x[7]-0.15*x[8]
```


```python
# Solve the optimization problem
status = model_1.solve()

# Get the results
print(f"status: {model_1.status}, {LpStatus[model_1.status]}")
print(f"objective: {model_1.objective.value()}")

for var in x.values():
    print(f"{var.name}: {var.value()}")

for name, constraint in model_1.constraints.items():
    print(f"{name}: {constraint.value()}")
```




##### FUZZY MODEL


```python
# Define the model
model_f = LpProblem(name="resource-allocation", sense=LpMaximize)

# Define the decision variables
x = {i: LpVariable(name=f"x{i}", lowBound=0) for i in range(1, 10)}

# Add constraints
model_f += (lpSum(x.values()) <= 24936, "total")
model_f += (x[1] <= 1089, "Exec")
model_f += (x[2]-213*x[9] >= 6024, "Educ")
model_f += (x[3]-213*x[9] >= 2302, "Soc. Pol")
model_f += (x[4]+x[5]-2125*x[9] >= 8190, "Health")
model_f += (x[6] <= 432, "Culture")
model_f += (x[7] <= 2281, "Econ")
model_f += (x[8]+73*x[9] <= 3699, "Debt")
model_f += (x[9] <= 1, "alpha")

model_f += 1*x[9]
```


```python
# Solve the optimization problem
status = model_f.solve()

# Get the results
print(f"status: {model_f.status}, {LpStatus[model_f.status]}")
print(f"objective: {model_f.objective.value()}")

for var in x.values():
    print(f"{var.name}: {var.value()}")

for name, constraint in model_f.constraints.items():
    print(f"{name}: {constraint.value()}")
```



|                                     | 1st Model                        |                                 | 2nd Model                            |                                   | Fuzzy Model<br />*Only for PULP         |
| ----------------------------------- | -------------------------------- | ------------------------------- | ------------------------------------ | --------------------------------- | --------------------------------------- |
| **Chapters**                        | **Growth   episode-no Covid-19** | **Current   budget allocation** | **Economic   recession-no Covid-19** | **Simulated   Budget allocation** | **Economic   Recession+     Covid-19*** |
| Executive and Assembly + Justice    | 1,098                            | 1,098                           | 1,035                                | 1,035                             | 0                                       |
| Education all levels + scholarships | 5,968                            | 6,023                           | 4,443                                | 5,617                             | 6,237                                   |
| Social policies + employment        | 2,626                            | 2,302                           | 2,029                                | 2,686                             | 2,515                                   |
| Health and central services         | 0                                | 4,184                           | 0                                    | 4,241                             | 16,183                                  |
| Top 11 Hospitals Covid - 19         | 8,109                            | 3,924                           | 8,316                                | 4,075                             | 0                                       |
| Culture and Environment             | 432                              | 432                             | 610                                  | 610                               | 0                                       |
| Economy and Transportation          | 3,342                            | 2,280                           | 2,213                                | 2,350                             | 0                                       |
| Debt                                | 2,298 <br />_2226_               | 3,626                           | 0                                    | 3,808                             | 0                                       |
| **Objective function (Maximum)**:   | 2,524<br />_2543_                | -                               | 2,070                                | -                                 | **Alpha** = 1                           |

