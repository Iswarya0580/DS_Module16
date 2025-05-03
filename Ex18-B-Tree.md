# Ex18 B-Tree
## DATE:
## AIM:
To write a C function to delete an element in a B Tree.
## Algorithm
```
1.Start and try deleting the item using delValFromNode.
2.If not found, print "Not present" and return.
3.If node's count is 0, set tmp = myNode and update myNode to its first linker child.
4.Free tmp and update the global root.
5.Return after deletion and end.
```
## Program:

### Program to write a C function to delete an element in a B Tree
### Developed by: ISWARYA P
### RegisterNumber:  212223230082

```
structBTreeNode{
int item[MAX+1], count;
structBTreeNode*linker[MAX +1];
};
structBTreeNode*root;*/
void delete(int item,structBTreeNode*myNode) {
structBTreeNode*tmp;
if(!delValFromNode(item,myNode)) {
printf("Not present\n");
return;
} else {
if(myNode->count ==0) {
tmp = myNode;
myNode=myNode->linker[0];
free(tmp);
}
}
root=myNode;
return;
}
```
## Output:

![image](https://github.com/user-attachments/assets/b4a578bb-a05c-4632-b2d5-0c9222cceaf3)


## Result:
Thus, the C function to delete an element in a B Tree is implemented successfully.
