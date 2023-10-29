# LRU_Cache
This LRU Cache implementation uses a combination of a HashMap and a Doubly Linked List.
The HashMap allows us to quickly retrieve and update nodes in the cache.
The Doubly Linked List is used to maintain the order of nodes in the cache, with the most recently accessed node at the head of the list, and the least recently accessed node at the tail of the list.
When we perform a 'get' operation, we check if the key exists in the HashMap. If it does, we remove the corresponding node from its current position in the list, update its value, and insert it back at the head of the list.
When we perform a 'put' operation, we check if the key exists in the HashMap. If it does, we remove the corresponding node from the list and update its value. If the key does not exist, we create a new node, add it to the HashMap, and insert it at the head of the list.
Before inserting a node at the head of the list, we check if the cache is full (i.e., the size of the HashMap equals the capacity of the cache). If it is, we remove the node at the tail of the list and its corresponding entry from the HashMap before inserting the new node.
This approach ensures that the least recently accessed nodes are always removed from the cache when it is full.
This LRU Cache implementation provides a time complexity of O(1) for both the 'get' and 'put' operations, assuming the hash functions of the HashMap and the Doubly Linked List can efficiently distribute the keys.
It also provides a space complexity of O(capacity), where 'capacity' is the maximum number of nodes that can be stored in the cache.
has context menu
Compose
