#题意
给出一个列表中的某个点，删除它的下一个节点

#分析
一开始没读懂题，读懂了就简单了，用下一个节点的值代替当前节点的值，然后当前节点指向下下个节点

#代码
```C++
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode(int x) : val(x), next(NULL) {}
 * };
 */
class Solution {
public:
    void deleteNode(ListNode* node) {
        node->val = node->next->val;
        ListNode* nn = node->next->next;
        node->next = nn;
    }
};
```
