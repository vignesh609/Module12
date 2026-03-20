# 🌀 Queue using Linked List - Insert, Display, and Delete

## 🎯 Aim

To write a Python program that:
- Inserts elements into a queue.
- Displays all inserted elements.
- Deletes the first element.
- Displays the updated queue after deletion.

---

## 🧠 Algorithm

1. **Create a Queue**:
   - Initialize an empty list named `queue`.

2. **Insert Elements**:
   - Use the `append()` method to insert elements `'a'`, `'b'`, and `'c'` into the queue.

3. **Display Initial Queue**:
   - Print the message `"Queue after elements are inserted:"` followed by the queue contents.

4. **Delete First Element**:
   - Use `pop(0)` to remove the first inserted element (FIFO - First In First Out).
   - Print the message `"Deleting the first element inserted:"` and the element removed.

5. **Display Updated Queue**:
   - Print the message `"Queue after the first element is deleted:"` followed by the updated queue contents.

---

## Program
~~~
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class Queue:
    def __init__(self):
        self.front = None
        self.rear = None
    def insert(self, data):
        new_node = Node(data)
        if self.rear is None:
            self.front = self.rear = new_node
        else:
            self.rear.next = new_node
            self.rear = new_node
        print(f"Inserted: {data}")
    def display(self):
        if self.front is None:
            print("Queue is empty.")
            return
        temp = self.front
        print("Queue elements:", end=" ")
        while temp:
            print(temp.data, end=" -> ")
            temp = temp.next
        print("None")
    def delete(self):
        if self.front is None:
            print("Queue is empty. Nothing to delete.")
            return
        deleted_data = self.front.data
        self.front = self.front.next
        if self.front is None:
            self.rear = None
        print(f"Deleted: {deleted_data}")
if __name__ == "__main__":
    q = Queue()
    q.insert(10)
    q.insert(20)
    q.insert(30)
    q.display()
    q.delete()
    q.display()
~~~

## Output
![Screenshot 2025-05-23 115256](https://github.com/user-attachments/assets/cee987cd-47c1-480c-8832-52ff75bc835c)

## Result
Thus the program has been executed successfully.
