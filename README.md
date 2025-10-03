# Experiment 18: Queue in C++
---

## Aim
---

To study and implement the **Queue data structure** in C++ by performing:
- Basic queue creation using arrays.
- Enqueue (insertion) operation.
- Dequeue (deletion) operation.
- Displaying elements of the queue.

---

## Objectives
---

- Understand the concept of linear data structures.
- Learn the principle of **FIFO (First In First Out)**.
- Study the basic operations: **Enqueue, Dequeue, Display**.
- Explore different types of queues (Simple, Circular, Priority, Deque).
- Compare queue with stacks, arrays, and linked lists.
- Identify real-life applications of queues in industry and operating systems.

---

## Tools Used
- **VS Code** (for coding and execution)  
- **C++ Compiler** (g++, clang++, MSVC)

---

## Theory

### Linear Data Structures
- Store elements sequentially in a single logical order.
- Traversal is linear (one element after the other).
- Examples: Arrays, Stacks, Queues, Linked Lists.
- Common operations: insertion, deletion, traversal.
- Applications: scheduling, buffering, compiler design, memory management.

---

### Queue
---

- A **queue** is a linear data structure based on the **FIFO principle**.  
- The element inserted first is removed first.  
- It has two ends:  
  - **Front** → for deletion (Dequeue).  
  - **Rear** → for insertion (Enqueue).  

---

### Types of Queues

#### 1. Simple Queue
- Linear structure with **insertion at rear** and **deletion at front**.
- Fixed size when implemented with arrays.
- Problems: *overflow* (full) and *underflow* (empty).

#### 2. Circular Queue
- Rear pointer wraps around to reuse freed space.
- Solves wastage in simple queues.
- Efficient for memory management.

#### 3. Priority Queue
- Every element has a **priority**.
- Higher priority elements are dequeued before lower ones.
- Implemented with **heaps, arrays, or linked lists**.

#### 4. Double-Ended Queue (Deque)
- Insertions and deletions allowed at both ends.
- Flexible structure for efficient task scheduling.
- Used in caching, sliding window problems.

---

### Difference Between Stack and Queue

| Feature            | Stack                          | Queue                         |
|--------------------|--------------------------------|-------------------------------|
| Principle          | LIFO (Last In First Out)       | FIFO (First In First Out)     |
| Insertion Point    | Top                            | Rear                          |
| Deletion Point     | Top                            | Front                         |
| Example            | Undo operations, recursion     | Scheduling, buffering         |
| Access             | One end                        | Two ends                      |

---

### Memory Storage
- **Array implementation**: stored in contiguous memory.  
- **Linked list implementation**: dynamic memory allocation with pointers.  
- For this experiment, **array-based implementation** is studied.

---

### Advantages of Queues
- Preserves order (FIFO).  
- Useful in real-world sequential processing (e.g., customer queues).  
- Efficient for scheduling and resource management.  
- Can be easily implemented with arrays or linked lists.  

---

### Disadvantages of Queues
- Fixed size in array-based queues → risk of overflow.  
- Underflow occurs if queue is empty and dequeue is called.  
- In simple array queues, freed spaces cannot be reused (solved by circular queue).  
- Searching is **O(n)**, unlike arrays with O(1) indexing.  

---

### Difference Between Array, Stack, Queue, and Linked List

| Aspect      | Array                          | Stack                           | Queue                           | Linked List                        |
|-------------|--------------------------------|---------------------------------|---------------------------------|------------------------------------|
| Structure   | Contiguous memory              | LIFO (Last In First Out)        | FIFO (First In First Out)       | Nodes connected via pointers       |
| Access      | O(1) by index                  | O(n) search                     | O(n) traversal                  | O(n) traversal                     |
| Insertion   | Costly (shifting needed)       | O(1) push/pop at top            | O(1) enqueue at rear            | O(1) with pointer update           |
| Deletion    | Costly (shifting needed)       | O(1) pop at top                 | O(1) dequeue at front           | O(1) with pointer update           |
| Size        | Fixed                          | Dynamic if LL-based             | Dynamic if LL-based             | Dynamic, flexible size             |
| Applications| Tables, matrices               | Undo stack, recursion           | Scheduling, buffering           | Dynamic memory management, graphs  |

---

## Algorithm
---

1. Start
2. Initialize Queue
   - Set front = -1 and rear = -1.
3. Enqueue Operation (Insert)
   - If rear == SIZE - 1, print "Queue Overflow" and stop.
   - If front == -1, set front = 0 (first element insertion).
   - Increment rear.
   - Insert element at arr[rear].
   - Print success message.
4. Dequeue Operation (Delete)
   - If front == -1 OR front > rear, print "Queue Underflow" and stop.
   - Print element at arr[front] as removed.
   - Increment front.
5. Display Operation
   - If front == -1 OR front > rear, print "Queue is empty".
   - Else, traverse array from front to rear and print elements.
6. Repeat Steps 3–5 as per user/program instructions.
7. Stop.

---

## Concepts Used
- **FIFO Principle** (First In First Out).
- **Array-based implementation** of queue.
- **Front and Rear Pointers** to manage insertion and deletion.
- **Static Memory Allocation** (array-based).
- **Queue Operations**: Enqueue, Dequeue, Display.
- **Overflow and Underflow handling**.

---

## Industrial Applications of Queues
- **CPU Scheduling** – Round-robin scheduling in operating systems.  
- **Disk Scheduling** – Managing disk I/O requests.  
- **Networking** – Packet buffering and load balancing in routers.  
- **Printers** – Print job scheduling.  
- **Call Centers** – Managing customer service queues.  
- **Simulation Systems** – Traffic flow, production lines.  
- **Messaging Systems** – Kafka, RabbitMQ, AWS SQS.  
- **OS Process Management** – Ready queue, wait queue.  

---

## Conclusion
- Queues are **essential linear data structures** for real-time processing.  
- They follow the **FIFO order**, ensuring fairness in handling tasks.  
- Efficient in **scheduling, buffering, and commu**

