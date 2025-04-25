# cs382-lab-10-solved



**<span style='color:red'>TO GET THIS SOLUTION VISIT:</span>** https://www.ankitcodinghub.com/product/cs382-solved-3/

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;128063&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;4&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (4 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS382 Lab 10 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">
            
<div class="kksr-stars">
    
<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
    
<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">
            

<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>
                

<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (4 votes)    </div>
    </div>
&nbsp;

In CS-284 Data Structures you have learned a structure called linked list, and compared it with a traditional array. When iterating over either a linked list or an array, the time complexity for both is 𝒪(𝑛). This is true theoretically, but what about in reality?

In this lab, you will complete the following two tasks, while completing a lab report provided to you.

1 Task 1: Profiling a Linked List and an Array

To see if the performance of linked lists and arrays are really comparable, we provided you a starter code. Simply go to the starter code directory, and type make to compile the code. Then type the following:

What this program does is to create an array and a linked list, each of which consists of 10,000 random integer numbers. Then it will iterate over the array and the list, and time the execution, respectively.

Your task here is to change the size of the lists from 102, 103, 104, 105, to 106. Observe how the execution time of iterating the lists changes for both linked list and array. Record this experiment result, and present a graph or chart in your lab report.

Then explain: why does the two algorithms with both 𝒪(𝑛) complexity, have very different performance when 𝑛 increases? You need to explain in detail from the perspective of locality.

2 Task 2: Locality Improved Linked List

It’s a good idea to combine the advantages of both linked list and array, to improve the locality of their operations and thus the efficiency. This new structure is called Unrolled Linked List. Instead of storing just one data element in each node, unrolled linked list stores an array of elements in each node. When iterating over the list, in each node, we iterate over the array first, and then move on to the next node. For more information, see Wikipedia: https://www.wikiwand.com/en/Unrolled_linked_list.

We provide the starter code in both C and C++, and you are free to choose the one you’re most comfortable with. In the following we will use C version as an example.

In UnrolledLL.h , you will see the declarations of this new struct and functions:

uNode

u_int64_t

Struct is a node in a unrolled linked list. Each node has an array of size blksize (block size) that stores data.is an unsigned integer type of 64 bytes.

Your task is to compelete the code in UnrolledLL.c first, and profile the algorithm of iterating over the list:

This command will create a linked list of 10,000 nodes, an array of 10,000 random integers, and a unrolled linked list of = 100 nodes where each node contains 100 random integers. And then it will time the execution of iterating over lists for each of the structures.

Note: do not change any file provided to you other than UnrolledLL.c or UnrolledLL.cpp .

In your report, fix the block size 100, and change the size of the lists from 102, 103, 104, 105, to 106. Observe how the execution time of iterating the lists changes for all the structures. Record this experiment result, and present a graph or chart in your lab report.

Then explain: what is the time complexity of unrolled linked list? How does a unrolled linked list improve the efficiency of traversal in terms of locality?

3 Grading

The lab will be graded based on a total of 10 points, 3 for task 1 and 7 for task 2.

the report is handwritten; Task 1 (3 points):

• -2: the explanation is not from the perspective of locality; and/or does not consider how the two structures are stored in memory;

• -1: the graph in the report does not correctly show the experiment result, or is missing.

Task 2 (7 points):

• -7: the code does not compile, or executes with run-time error;

• -7: any file other than UnrolledLL.c or UnrolledLL.cpp is changed;

• -7: the presentation format of the result is one of the following: pie chart, bar chart, table;

• -2: the explanation is not from the perspective of locality; and/or does not consider how the structures are stored in memory;

• -2: the time complexity of unrolled linked list is wrong;

• -2: no pledge and/or name in the report (this counts for both tasks);

• -1: the graph in the report does not correctly show the experiment result, or is missing;

• -1: no pledge and/or name in the code.

Attendance: check off at the end of the lab to get attendance credit.
