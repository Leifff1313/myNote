# 資料結構
## Abstract data type 
(ADT)用來儲存一般資料型態的資料結構<br>
例如
Array, List, Stack, Queue(lienar ADT)<br>
## Tree
1. Hierarchical階層的 ADT
2. root：一種node沒有任何parent 
3. internal node:至少有一個child<br>
   external node:沒有任何children
4. depth深度:有幾個ancestors
5. height:任意node的最大深度
6. tree node有<br>
   1. 元素
   2. parent的node
   3. children的node
## Binary tree
1. 每個node只有兩個children(left or right)或是沒有child
2. Binary node有
   1. 元素
   2. parent node
   3.  left child node
   4.  right child node 
## Proper binary tree
1. 每個internal node都有兩個children
2. n:node總數<br>e:external node總數<br>i:internal node總數<br>h:高度<br>
e=i+1<br> n=2e-1<br>h<=i<br> h<=(n-1)/2<br> e<=2*h<br> h>=log2e<br> h>=log2(n+1)
## Traversal(尋訪)
1. preorder:比後代早被拜訪
2. postorder:後代被拜訪才輪到他
3. inorder:左邊的樹先拜訪完再去右邊
## Heap(堆積)
1. Maxheap:parent key大於等於key
2. Minheap:parent key小於等於key
3. 可能在插入新的key後會違反heaporder，所以有upheap, downheap出現
4. upheap:key比parent大<br>downheap:key比parent小
## Random Access Machine(RAM)
中央處理器(CPU)的一種，可儲存任意資料
## Algorithm(演算法)
給定input如何做出想要的output>>>演算法
### Pseudo code
Primitve operations
1. evaluating an expression
2. assigning a value to a varible
3. indexing into an array
4. calling a method
5. returning from a method
### Big oh
是用另一個函式來描述一個函式數量級的漸近上界。<br>
例如：O(n), O(log n), O(n^2)<br> 
取最高次方的數量級

~~~java
int a = 3;
~~~