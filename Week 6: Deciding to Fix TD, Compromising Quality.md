<img src="assets/2023.05.12%20-%2009_43_21%20-%20%20%5BGoogle%20Chrome-Course%20COMP4130%20-%20Managing%20Software%20Quality%20and%20Process%20-%20Sem%201%202023%5D%20-.jpg" alt="2023.05.12 - 09_43_21 -  [Google Chrome-Course COMP4130 - Managing Software Quality and Process - Sem 1 2023] -" style="zoom:20%;" />  







## Intuition (TD is a Economic Issue)

### TD is ultmately an economic issue

-   Ingeneral the key driver for makign deicison about a SE project is max value while min cost; Yuu are developing software to earn money. Verything involves SE development can be **addessed through money**: 

    -   The delveopers salary 
    -   The cost of delaying a releave 
    -   The earning of users paying for your software 
    -   Your earning if your sofwtare has adebrtisement 

    Therefore you must be able to calcualte the cost of doing whatever you need to do with TD items. 

    This inovlves computing or **estimating the cost** to carry and to eliminate the TD 

### Economic Concept: 

#### Current Principal 当前本金

-    If you take TD item from yoru registry you can estimate httotal effor invobes in eliminating the associated TD. The assocated debt is htat we hav ecalled the **current principal**, and it inclubdes the cost of changing the code and all accuring interestt. (that is undoing the modicitaitons and owrkaround that piled up on the non-quite-right code, deisgn, or production infrastrutre)
-   (In finance, the "current principal" refers to the outstanding balance of a loan or debt at a particular point in time. It represents the amount of money that still needs to be repaid to fully satisfy the debt obligation.)

#### Return on Investment (ROI) 回报比率

-   A simple return on investment (ROI) calculation for devt reduction comapres the benifinties of reducing the recurring interest, with the cost of paying the current principal and accuring interest (remadation cost)
    -   Current Principal 当前本金
    -   Accuring Interest 应计利息

#### Tipping Point  

-   you will need to know the cost of the technical debt you have in your system and understnad when you will reach the tipping point (AKA the point wher eyou will start to suffer from the technical debt)

-   <img src="assets/2023.05.12%20-%2009_55_58%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 09_55_58 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 







## High to Economically Highlight TD items 

### Overview 

Steps to highlight TD items: 

1.   Refine the TD descritpion, identify the **impacted and related artefacts** 

     (An exmaple of such artefacts are: documentation, code smells, refacroting cost, ...)

2.   Use the artefact to calculate the cost of remidation 

     (AKA: how difficult to fix the artefacts)

3.   Use the artefact to calculate the recurring interest 

     (AKA: how much will you, as a developer, suffere if you do not fix it as immediate)

### Step1: Refine TD description

##### PART-I

-   Ask you team:

    -   How much TD do we have ? 
    -   How much does it cost to fix ? 
    -   What are the impacts of not fixing ? 

    These questions about the futrue **do not consider only the code**, it also will need to consider: the Architecture, the Production Infrastructure. They assume that when the issue is fixed, all the associated task will be fixed. 

    AKA: **You cannot calcualte TD impact from a code-only approach**

-   Holistically automating the entire deicsion making and resource allocation process is not possible, and automated analysis cannot make these calcualte for your. You can identify issues nad make deisgn trade-off for fixing them, ut assessing issue as technical debt and managing them as such reques uilding an **end-to-end economic argument** 

    <img src="assets/2023.05.12%20-%2010_06_29%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_06_29 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 

##### PART-II

-   The goal is **not to trigger analysis paralysis** 分析瘫痪 (meaning that you stop developing to only perform analysis), but rather **to be aware of the added costs related to accruing interests** and to make the changes so that the system is production ready. 
-   You can use configuration management and version control system, remember the 3 different deployment envinornemnts (development, staging, production environment) to analaysis your code and refine you TD items, managing them throughout the software's life cycle 



### Setp2: Calculate remidation cost (fixing cost)

-   The cost of fixing the quality problem compairses the **current principal** 本金 and **accured interest** 利息. 

    The team adjust these cost by an uncertainty factor an the csot to test the fix. 

-   Accounting for uncertainty provides team members a mechnism to express their confidence in their ability to localize changes, to determine how much they need to account for unexpected ripple change 

    ​           (ripple change 涟漪效应,指的是一个小问题影响到其他的看似不相干的部分) 

    → remember the context always changes, regardless of what you do  

    ​           (需求永远是不断变更的, 你不管怎么做都改变不了这个事实)

-   Now you have to consider the trade-off between **a quick solution of patches**        (paying the recurringn interest)

    and **fixing the software properly**                                                                                       (paying off the principle)

    (But fixing the sofwtare properly may not be always possible ... as it usually requires a stall of development )

    ​	

### Step3: Calcualte recurring interest (not-fix cost)

-   The recurring intests reuqires you to **understnad the need of futrue changes,**  and estimating/guessing their cost related value impact. You will need to know the **conseqeunce** of **continuing carry the existing debt,** so you can weight them against conseqeunce of your strategy to remediate the debt.          (如果一直带着问题不修的结果是什么)

-   Steps

    -   To make a simple calculation of the benifit, consider the cost saved form no longer carrying the TD  ==根治==

        (this assumes that you have completely payes off the principle and eliminated TD, no recurring intests )

    -   You have been living with the TD so far, so you "know by experience" how will it cost                     ==小修小补==
    -   Use that "experience" to predict futrue cost on an extrapolation of                                                     ==预估代价==
        -   Past debt 
        -   Rework cost of anticipate changes 
        -   The gap to good engineering practices 
    -   Nuance: subtract recurring intest of your remediation strategy from cost of carrying debt  ==预估弥补方式差别==
        -   In the cast you are reducing but NOT eliminating the TD 
        -   This is the most common case. 



### Example: Phobe Case 

- Starting Point

     <img src="assets/2023.05.12%20-%2010_26_59%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_26_59 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 

- ↓ Step-1: Refinement of TD

     <img src="assets/2023.05.12%20-%2010_28_15%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_15 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" />  

- ↓ Step-2: Cost of fixing (remediation)

     <img src="assets/2023.05.12%20-%2010_28_22%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_22 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" />

- ↓ Step-3: Cost of not-fixing (recurring interest)

    <img src="assets/2023.05.12%20-%2010_28_49%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_49 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 









## Cost and Benifit 



### Weighting Cost and Benifit



#### What "Cost", What "Benifit" ?

In decising wtat to do, you will need to consider **the busness case** for the debts reducting, indcluding the cost and corresponding beninifts. 

-   Cost: 
    -   Current principal and accuring interests 
    -   Opporunity cost of delaying feature releases 
-   Beinift:
    -   Reduced recurring interests
    -   Reduced risk liability 

And here is an example of such cost and benifit case, 

(in timeline order )

1.   Evaluate the bennifts of reducing liability and recurring inetests 

2.   Estimate the **opportunity of delaying th delivery of new feature** 

     as you remediate the debt and the cost of paying the current principal and accuring interests 

3.   Consider the business case/scenario 

     when incurring or carrying depts swaps these facrots 

     (meaning TD has more beninits than developing more feature )

4.   In the case before ... the beninifts become the cost saving 

     of carrying the debt along with ealier feature delivery

5.   The cost becomes the recurring interests and increased liability



#### Utilizing the concept of Cost and Benifits 

With the answer to that question, you can examine the technical debt items youin your registry and determine:

-   Which TD you should **remediate**                  (fix:       benifit > cost) 
-   Which TD you **can continue to live with**    (not fix: benifit > cost)

Wighting cost and benifit of the TD items you have in yoru reister will also help you:

-   Discuss and prioritize action to take to decide how to remediate the debt





### Communicating Cost and Benift 

#### Intiuition 

-   **The question is: how do you communicate this?**
-   Saying "it makes the code easier to handle" can be understood by a fellow
    developer, but the people paying you (the stakeholders, the clients, etc)
    need the explanation translated into something they can understand.
-   That shared understanding is money and finances.

#### Building a business case: Risk of failture ==失败成本==

-   A reslistic business case for TD reductiojn is an important tool to put the ris and cost related to RD, on the radar of the business stakhodler who can do somehting baoutit. Risk and opportunity cost often have more impact than the recurring maintainacne and direct remediation cost (others like security risk are easily understood without eplaining it in money)

    <img src="assets/2023.05.12%20-%2010_53_30%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_53_30 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 

#### Building a business case: Opportunity cost ==机会成本==

-   When the development team spends resource and time on reducing TD (upgrading, refacroting, repairing)

    the team will **procuce fewer end-user sorties** (implmenting less feature) during that time 

    Opportunity cost represent the business value that those end-user stories would have yielded, 

    as a way of accounting for the scarcity of the team's resource. 

    <img src="assets/2023.05.12%20-%2010_55_59%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_55_59 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 











## Pathway to Service TD 

### Servicing Existing Dept

-   When deciding what to do in the upcoming iterations, you will need to **consider all the items on your backlog**  yet to do and their dependencies, including the TD items;  If you want a system to **evolve in a certain direciotn**, for instance, by adding new feature, you will need to analuze which part of the system will be affectd by this evlution 

    

    **Steps to service the TD** 

    1.   Identify the path that will be affected by change 明确影响程度==
    2.   Determine whether TD items are associated with these part of the tstsem 明确依赖关系==
    3.   Identify the conseuqence of TD on this and possible other hcnages 预期不修补的后果==
    4.   Estimate the cost of TD repayment and ad it to the cost of the changes 预期修补需要的成本==
    5.   Estimate the beniit of TD relayment in enableing the devleopment of this and possibley other chagnes 预期未来回报==

### Servicing Potential Debt

-   You might have a **potential for TD**, but it will only be actual TD only if you have to evolve your system. You might also decide to walk away from your TD by running away from the old system (通过从头开始避免TD)
-   If you take a TD incurring deicsion, it may **only actualy become TD the moment at the moment your system has to evolve** ... meaning that: until the moment it will not negatively affect the quality of yoru system.



### What do you fix, then ?

-   You may have identified TD itmes, nut you camnot assocaite to them in any meaningful metric of cost **until you look into the furtue** and condier dependencies, among TD items and dependencies of **future** feature on them 

    All paths are influenced by the **cost-benifit trade-off** of servicing the debt.

-   Paths 

    -   **A prospective evluation 前瞻性评估**

        -   The system may have some potential debt, but because it is affected by a prospective evluation, it now has actual debt. 

        -   (如果业务要增长,那么有些潜在的债务就会被坐实)

            >   The cost to fix includes the cost of relaying the technical debt and the opportunity cost of delaying ghe feature

    -   Mitigating Risk 减轻风险

        -   Business decisions will always affect **what is done on** and about the sofwtare. If your system is already deployed, you may have defects to fix urgently These are negative because it decrease syste,'s usavility, and may make the customor unhappy. 

        -   (对生产进行例行更新, 可能会使得系统下线)

        -   Overtime risk liability may be the most important factor in the case for debt reduction 

            >    The total cost incldues the cost of backlogging item, the cost of repaying the technical debt, and the opportunity cost of delauing feature. 

    -   Discard TD 规避债务

        -   In amnesty, you write off the accured Td and do not have to relay it. (放弃不需要的部分)
            -   Example: throw-away prototype, delete a feature that is no longer needed
        -   Bankrupcy: (从零开始)
            -   The part of the sofatre system that has TD items is no longer viable to support future development, and a complete rewrite is needed. 



### Supplementary (release path)

#### A release pipeline with TD 

-   The differnt path to servicing technical debt can be used individually and in combination to sort out and prioritize the product backlog nad assign the backlog element of iteration or releaseses 

    <img src="assets/2023.05.12%20-%2011_18_42%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 11_18_42 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 

    -   When you ahve the mechnism in place ot service the technical debt, you can run some **what-if scenarios** to adjust the technical debt remediation timeline 
    -   While running what-if analysis on scenarios and comparing their implications will give you more information to make choices, you might still have the resouces to select only a few of the debt repayment refacrotings 

#### "Investing" on Technical Debt 

-   The NPV (net present value) is the hypothetical avlue (estimated today) of a investment made today comapred to its future returns, that is, it is possible value in the future. 

    <img src="assets/2023.05.12%20-%2011_21_15%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 11_21_15 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 

