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



### STEP2: Calculate remidation cost (fixing cost)

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



## Example: Phobe Case 

- Starting Point <img src="assets/2023.05.12%20-%2010_26_59%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_26_59 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 
- ↓ Step-1: Refinement of TD <img src="assets/2023.05.12%20-%2010_28_15%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_15 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" />  
- ↓ Step-2: Cost of fixing (remediation) <img src="assets/2023.05.12%20-%2010_28_22%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_22 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" />
- ↓ Step-3: Cost of not-fixing (recurring interest)<img src="assets/2023.05.12%20-%2010_28_49%20-%20%20%5BPreview-6-Lecture-Week6.pdf%5D%20-.jpg" alt="2023.05.12 - 10_28_49 -  [Preview-6-Lecture-Week6.pdf] -" style="zoom:33%;" /> 







