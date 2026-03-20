# Node class
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

# Linked List class
class LinkedList:
    def __init__(self):
        self.head = None

    # Method to add element at the start
    def push_front(self, newElement):
        new_node = Node(newElement)   # Create new node
        new_node.next = self.head     # Point to current head
        self.head = new_node          # Make new node as head

    # Method to print the list
    def PrintList(self):
        temp = self.head
        if temp is None:
            print("The list is empty.")
            return
        
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")

# Main program
MyList = LinkedList()

# Adding elements at the start
MyList.push_front(10)
MyList.push_front(20)
MyList.push_front(30)
MyList.push_front(40)

# Printing the list
print("Linked List:")
MyList.PrintList()

