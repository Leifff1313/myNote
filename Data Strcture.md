# Data Strcuture (資料結構)<br>Algorithm(演算法)
給定input如何做出想要的output>>>演算法
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
7. 如果用array表示tree的話，A[0]永遠是空的
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
5. 時間複雜度為O(log n)因為分支高度為log n
6. insert=O(log n)
7. heap的每種method幾乎都是O(log n)因為要看有沒有符合規則(upheap, downheap)所以每個都要比較
## Sort
1. Selection-sort 沒有排序好的queue，所以insert要花O(n)然後remove要花O(n^2) 
2. Insertion-sort 是排序好的queue，所以insert要花O(n^2)然後remove要花O(n)
3. Bubble-sort  交換排序法，是從第一筆資料開始，逐一比較相鄰兩筆資料，如果兩筆大小順序有誤則做交換，反之則不動，接者再進行下一筆資料比較，花O(n^2)
~~~javascript
let data = [8,6,1,10,5,3,9,2,7,4]

function BubbleSort(array){
  let len = array.length
  while (len > 1) {
    len--
    for (let i = 0; i < len; i++) {
      // 如果前面的元素比後面的元素要大，則交換元素位置
      if (array[i] > array[i + 1]) {
        [array[i], array[i + 1]] = [array[i + 1], array[i]];
      }
    }
  }
  return array
}
console.log(BubbleSort(data))//[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
~~~
4. Heap-sort 要排序n個要素的話要花O(n log n)
5. Merge-sort O(n log n)
## Random Access Machine(RAM)
中央處理器(CPU)的一種，可儲存任意資料
## Singly LinkedList
由node所組成，每個node都有element, link to the next node(point)<br>
在頭增加或移除node及尾巴新增node為O(1)<br>
但在尾巴移除node為O(n)
## Doubly LinkedList
與singly相比只多了link to previous node
## Stack
ADT的一種，採取最後進先出的概念(last in first out)
## Queue
也是ADT的一種，採取先進先出的概念(first in first out)
## Brute force
每個元素都會被目標從前到後拿來比對，只有找到跟沒找到兩種。
~~~ 
Input text T of n size
      pattern P of m size
Output starting index of T equal to P

for i=0 to n-m
    j=0
    while j<m ^ T[i+j]=P[j]
        j=j+1
    if j=m
        return i
    else
        break
~~~
## Backward 
從後面往前面看
~~~
i=m-1 j=m-1
repeat
    if T[i]=P[j]
        if j=0
            return i
        else
            i=i-1
            j=j-1
    else
        i=i+m-j
        j=m-1
    until i>n-1
~~~
## Boyer moore
從後面往前看，並跳到最遠的地方
~~~
L=lastOccurenceFunction(P,summation)
i=m-1 j=m-1
repeat
    if T[i]=P[j]
        if j=0
            return i
        else
            i=i-1
            j=j-1
    else
        l=L[T[i]]
        i=i+m-min(j,1+l)
        j=m-1
    until i>n-1
~~~


## Pseudo code
Primitve operations
1. evaluating an expression
2. assigning a value to a varible
3. indexing into an array
4. calling a method
5. returning from a method
6. 細節
   1. if...then...
   2. while...do...
   3. repeat...until...
   4. for...do...
   
## Big oh
是用另一個函式來描述一個函式數量級的漸近上界。<br>
例如：O(n), O(log n), O(n^2)<br> 
取最高次方的數量級
## Big omega
大O符號表示函數在增長到一定程度時總小於一個特定函數的常數倍，大Ω符號則表示總大於。為下界。
## Big theta
為大O及大omega的合體
## Divide and Conquer
演算法的一種型態，將input分成很多集合分別處理，最後再合併成output。

~~~java
int a = 3;
~~~