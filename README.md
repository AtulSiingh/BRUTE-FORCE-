# BRUTE-FORCE-
to delete middle of linked list
/**
 * Definition for singly-linked list.
 * struct ListNode {
 *     int val;
 *     ListNode *next;
 *     ListNode() : val(0), next(nullptr) {}
 *     ListNode(int x) : val(x), next(nullptr) {}
 *     ListNode(int x, ListNode *next) : val(x), next(next) {}
 * };
 */
class Solution {
public:
    ListNode* deleteMiddle(ListNode* head) {
        if(head->next==NULL)
            return NULL;
        ListNode* temp=head;
        int count=0;
        while(temp!=NULL){
            count++;
            temp=temp->next;
            
        }
        count=(count/2)-1;
        temp=head;
        ListNode* temp2=temp->next;
        while(count--){
            temp=temp->next;
            temp2=temp2->next;
        }
        temp->next=temp2->next;
        return head;
    }
};
