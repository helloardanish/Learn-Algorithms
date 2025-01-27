An **algorithm** in programming is a **step-by-step set of instructions** or rules designed to perform a specific task or solve a problem.


The term algorithm is used in computer science to describe a finite, deterministic, and effective problem-solving method suitable for implementation as a computer program.


If you want to find the largest number in a list, the algorithm in english language might look like this:

1. If list is empty, there is no result.
2. If list only contains 1 number it is the largest number.
3. If list contains more than 1 number
	1. Start with the first number as the largest.
	2. Compare it with the next number in the list.
	3. If the next number is larger, update the largest number.
	4. Repeat this process for all numbers in the list.
	5. At the end, the largest number will be the result.

Programming language:

```
	public static int largestNumber(int[] arr){
	    if(arr.length == 0){
	        return -1;
	    }
	    
	    if(arr.length == 1){
	        return arr[0];
	    }
	    
	    int largest = arr[0];
	    for(int i=1; i<arr.length; i++){
	        if(arr[i] > largest){
	            largest = arr[i];
	        }
	    }
	    return largest;
	    
	}
```


Euclid’s algorithm

English-language description:

**Compute the greatest common divisor of two nonnegative integers p and q as follows: If q is 0, the answer is p. If not, divide p by q and take the remainder r. The answer is the greatest common divisor of q and r.**


Java-language description:

```
	public static int gcd(int p, int q){
	    if(q==0) return p;
	    int r = p%q;
	    return gcd(q, r);
	}
```



When we use a computer to help us solve a problem, we typically are faced with a number of possible approaches. Like in the above examples we can start from last or from mid by going left and right


For small problems, it hardly matters which approach we use, as long as we have one that correctly solves the problem. 

For large-scale problems (or scenarios requiring the resolution of numerous smaller problems), we are soon compelled to develop approaches that optimize both time and space efficiency.

The Java libraries provide implementations for a wide range of essential algorithms.

Selecting the most suitable algorithm for a specific task can be a complex process, often requiring advanced mathematical analysis. The field of computer science dedicated to exploring these questions is known as algorithm analysis.

It is important to understand the resources an algorithm may consume before using it, which is why we aim to evaluate and predict the performance of our algorithms.


**Fundamentals**: Java programming model, data abstraction, basic data structures, abstract data types for collections, methods of analyzing algorithm performance

**Sorting**: insertion sort, selection sort, shellsort, quicksort, mergesort, and heapsort
we will also learn priority queues, selection, and merging.

**Searching**: binary search trees, balanced search trees, and hashing

**Graph**: depth-first search, breadth-first search, connectivity problems

Kruskal’s and Prim’s algorithms for finding minimum spanning tree and Dijkstra’s and the Bellman-Ford algorithms for solving shortest-paths problems


In this course, we will explore both complex and challenging algorithms, as well as those that are simple, elegant, and easy to understand.
