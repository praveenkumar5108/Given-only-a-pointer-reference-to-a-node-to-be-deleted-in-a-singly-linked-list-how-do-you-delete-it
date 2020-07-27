# Given-only-a-pointer-reference-to-a-node-to-be-deleted-in-a-singly-linked-list-how-do-you-delete-it

 solution is to copy the data from the next node to the node to be deleted and delete the next node. Something like following.

    // Find next node using next pointer
    struct Node *temp  = node_ptr->next;

    // Copy data of next node to this node
    node_ptr->data  = temp->data;

    // Unlink next node
    node_ptr->next  = temp->next;

    // Delete next node
    free(temp);
