

# Potential, On-Hold, and Self Admitted TD 

<img src="assets/2023.05.12%20-%2009_39_45%20-%20%20%5BGoogle%20Chrome-Course%20COMP4130%20-%20Managing%20Software%20Quality%20and%20Process%20-%20Sem%201%202023%5D%20-.jpg" alt="2023.05.12 - 09_39_45 -  [Google Chrome-Course COMP4130 - Managing Software Quality and Process - Sem 1 2023] -" style="zoom:20%;" /> 







## Potential Technical Debt (PTD)



### What is PTD ?

-   Not all technical items have the same immpact. Whether an issue is actual technical debt or not dependencies on what future evolution a develoment team wants to make to the software system. 

    >    Schimid descirbed as a **risk that can potentially become a problem** 

    PTD is quite **common on code reviews**, because it will evolve into TD if it has been introduced into software system without being resolved, otherwise it would not have any real imapct on the quality of the sofwtare. 



-   However PTD can be linked to any other practice 
    -   For example, deciding to divide a fix in multiple pull-request, has the potential to be TD because osmthing may happen and prevent devs from tacking what is left 
    -   If they ==complete== it, it ==nenver become TD==
    -   If they ==failed to complete it==, then that PTD transforms into ==actual TD==



-   Exmaple of PTD commented in code

    <img src="assets/2023.05.12%20-%2015_12_09%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_12_09 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 



### Types of PTD ? 

#### Design PTD 

<img src="assets/2023.05.12%20-%2015_15_45%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_15_45 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 

#### Defect PTD 

<img src="assets/2023.05.12%20-%2015_15_58%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_15_58 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 

#### Documentation PTD 

<img src="assets/2023.05.12%20-%2015_16_05%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_16_05 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 

#### Requirement PTD 

<img src="assets/2023.05.12%20-%2015_16_16%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_16_16 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 

#### Code PTD 

<img src="assets/2023.05.12%20-%2015_16_31%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_16_31 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 







## Self-Admitted Technical Debt (SATD)



### What is SATD? 

​	自我承认的技术债务 

-   Slef-admitted technical debt (SATD) consits of annotations, left by developers as in the source dode or elseware, as a reminder about pieces of software manifest techincal TD (i,e, not being done yet / not being ready yet)

    They are commonly found in **soruce code comments** 

    but hrey are also found in: commit messages, issue discussions, pull-requests / issue comments, gitter / Jira

-   An SATD comments in the source code is the result of decision taken by a developer whether to annotate the source code, and when doign so, that details to includes in the SATD annotation. 

    However, it does not mean that TD is nearby; the comment may be outdated (for instance an annotation in 1980 might be hard to understand for developer in 2022) 承认≠解决

    Finding SATD comments in the code may lead to devleopers deciding to "invest" time in repaying / fixing that debt ... or they may aso choose to simpley ifnore them 开发者如何面对SATD取决于个人

    

    >   SATD is important because awareness has been empirally shown to be very important factor when managing TD 
    >
    >   (Ernst et al. 2015)



### Examples of SATD ? 

-   <img src="assets/2023.05.12%20-%2015_28_14%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg" alt="2023.05.12 - 15_28_14 -  [Preview-11-Lecture-Week11.pdf] -" style="zoom:33%;" /> 





----

### SATD Freqeuncy & Usage 

(Zampetti's Paper (OSS stands for "Open Source Sofwtare")



#### Frequency and Reason behind Annotaiton 

![2023.05.12 - 15_29_56 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_29_56%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)![2023.05.12 - 15_30_56 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_30_56%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)



### Tracking Mechnism and Type of Annotation 

![2023.05.12 - 15_31_14 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_31_14%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)













## Pending 

-   [2023.05.12 - 15_32_08 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_32_08%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)

-   [2023.05.12 - 15_32_01 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_32_01%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)

-   [2023.05.12 - 15_31_51 -  [Preview-11-Lecture-Week11.pdf] -](assets/2023.05.12%20-%2015_31_51%20-%20%20%5BPreview-11-Lecture-Week11.pdf%5D%20-.jpg)





