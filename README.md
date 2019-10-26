# segTree
General purpose segment tree library.

1. include SegmentTree.h
2. to construct a segment tree you need to specify the following:<br>
   a. The datatype of array for which the tree is being constructed.<br>
   b. an array or vector for which the tree is to be constructed.<br>
   c. a value that can be used to fill the extra nodes of the tree.<br>
   d. a function combine that specifies how the result of left and right child of a node<br> 
        should be used to generate the value of current node.
3. Example usage:      
   int small(int x,int y){return min(x,y);}<br>
   SegmentTree < int > rangeMinQueries(dataVector,INT_MAX,small);<br>
   
   int sum(int x,int y){return x+y;}<br>
   SegmentTree < int > rangeSumQueries(dataVector,0,sum);<br>
   
   long long product(long long x,long long y){return x*y;}<br>
   SegmentTree < long long > rangeProductQueries(dataVector,1,product);<br>
   
solution to SPOJ GSS1 using segTree library : https://ideone.com/EFxf6O<br>
solution to SPOJ KGSS using segTree library : https://ideone.com/fUK5Jz<br>

