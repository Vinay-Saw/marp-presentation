---
marp: true
theme: default
paginate: true
header: 'Data Science & DSA Documentation'
footer: '23f2005452@ds.study.iitm.ac.in'
---

<style>
section {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

h1 {
  color: #FFD700;
  text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
  border-bottom: 3px solid #FFD700;
  padding-bottom: 10px;
}

h2 {
  color: #FFA500;
  border-left: 5px solid #FFA500;
  padding-left: 15px;
}

code {
  background: rgba(255,255,255,0.1);
  padding: 2px 6px;
  border-radius: 4px;
  color: #FFE4B5;
}

pre {
  background: rgba(0,0,0,0.3);
  border-radius: 8px;
  padding: 15px;
  box-shadow: 0 4px 6px rgba(0,0,0,0.2);
}

ul, ol {
  line-height: 1.8;
}

strong {
  color: #FFD700;
}

section.title {
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

section.data-bg {
  background: url('./world_map.webp') no-repeat center;
  background-size: cover;
}

section.data-bg::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0,0,0,0.6);
  z-index: -1;
}

table {
  background: rgba(255,255,255,0.1);
  border-collapse: collapse;
  width: 100%;
}

th {
  background: rgba(255,215,0,0.3);
  color: #FFD700;
}

td, th {
  border: 1px solid rgba(255,255,255,0.2);
  padding: 10px;
}
</style>

<!-- _class: title -->

# 🎯 Data Science & DSA
## Complete Technical Documentation

**Prepared by:** Technical Writing Team
**Contact:** 23f2005452@ds.study.iitm.ac.in
**Date:** December 2025

---

## 📚 Table of Contents

1. Introduction to Data Structures
2. Algorithm Complexity Analysis
3. Common Data Structures in Data Science
4. Sorting Algorithms
5. Search Algorithms
6. Machine Learning Data Structures
7. Best Practices & Recommendations

---

## 🔷 Introduction to Data Structures

**Data structures** are specialized formats for organizing, processing, and storing data.

### Why DSA Matters in Data Science:
- **Efficiency**: Process large datasets faster
- **Scalability**: Handle growing data volumes
- **Optimization**: Reduce memory footprint
- **Performance**: Enable real-time analytics

> *"Bad programmers worry about the code. Good programmers worry about data structures and their relationships."* - Linus Torvalds

---

## 📊 Algorithm Complexity Analysis

### Time Complexity Notation

**Big O Notation** describes the upper bound of algorithm performance:

$$O(1) < O(\log n) < O(n) < O(n \log n) < O(n^2) < O(2^n) < O(n!)$$

### Space Complexity

Memory usage as a function of input size:

$$S(n) = O(f(n))$$

Where $f(n)$ represents auxiliary space needed

---

## ⚡ Common Complexity Classes

| Notation | Name | Example |
|----------|------|---------|
| $O(1)$ | Constant | Array access |
| $O(\log n)$ | Logarithmic | Binary search |
| $O(n)$ | Linear | Linear search |
| $O(n \log n)$ | Linearithmic | Merge sort |
| $O(n^2)$ | Quadratic | Bubble sort |
| $O(2^n)$ | Exponential | Recursive Fibonacci |

---

<!-- _class: data-bg -->

## 🗃️ Core Data Structures

### Arrays & Lists
- **Arrays**: Fixed-size, contiguous memory
  - Access: $O(1)$
  - Insert/Delete: $O(n)$

### Linked Lists
- **Singly Linked**: One-way traversal
- **Doubly Linked**: Bidirectional traversal
  - Access: $O(n)$
  - Insert/Delete: $O(1)$ at known position

---

<!-- _backgroundColor: "#2d3748" -->

## 🌳 Tree Structures

### Binary Search Tree (BST)

Properties:
- Left subtree < Node < Right subtree
- Average case: $O(\log n)$ operations
- Worst case (unbalanced): $O(n)$

### Balanced Trees
- **AVL Trees**: Height difference ≤ 1
- **Red-Black Trees**: Self-balancing with color properties
- **B-Trees**: Multi-way trees for databases

**Application**: Database indexing, file systems

---

<!-- _color: white -->

## 🔍 Hash Tables in Data Science

### Hash Function

$$h(k) = k \bmod m$$

Where:
- $k$ = key
- $m$ = table size (typically prime)

### Performance
- Average case: $O(1)$ insert/search/delete
- Worst case: $O(n)$ with collisions

**Use Cases**: 
- Dictionary implementations (pandas)
- Feature hashing in ML
- Cache mechanisms

---

## 📈 Sorting Algorithms

### Quick Sort
```python
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)
```

**Complexity**: 
- Average: $O(n \log n)$
- Worst: $O(n^2)$
- Space: $O(\log n)$

---

## 🔎 Binary Search Algorithm

### Prerequisites
- Data must be **sorted**

### Mathematical Formulation

At each step, search space is halved:

$$T(n) = T\left(\frac{n}{2}\right) + O(1)$$

Solution: $T(n) = O(\log n)$

---

<!-- _paginate: false -->

## Binary Search Implementation

```python
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = (left + right) // 2
        
        if arr[mid] == target:
            return mid
        elif arr[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    
    return -1
```

**Time Complexity**: $O(\log n)$
**Space Complexity**: $O(1)$

---

<!-- _paginate: true -->

## 🤖 ML-Specific Data Structures

### 1. K-D Trees (K-Dimensional)
- **Use**: Nearest neighbor search
- **Complexity**: $O(\log n)$ average search
- **Application**: KNN algorithm, spatial data

### 2. Priority Queue (Heap)
- **Use**: Dijkstra's, A* pathfinding
- **Complexity**: $O(\log n)$ insert/delete
- **Application**: Task scheduling, event simulation

### 3. Trie (Prefix Tree)
- **Use**: Autocomplete, spell checking
- **Complexity**: $O(m)$ where $m$ = word length
- **Application**: NLP, search engines

---

## 🎯 Graph Structures in Data Science

### Representations

**Adjacency Matrix**: $O(V^2)$ space
$$A[i][j] = \begin{cases} 
1 & \text{if edge exists} \\
0 & \text{otherwise}
\end{cases}$$

**Adjacency List**: $O(V + E)$ space

### Algorithms
- **BFS/DFS**: $O(V + E)$
- **Dijkstra**: $O((V + E) \log V)$ with priority queue
- **PageRank**: Iterative, used in recommendation systems

---

<!-- _header: "" -->

## 💾 Memory-Efficient Structures

### Bloom Filter
- **Probabilistic** data structure
- **Space**: Much smaller than hash table
- **Trade-off**: False positives possible, no false negatives

$$P_{false\_positive} \approx \left(1 - e^{-kn/m}\right)^k$$

Where:
- $k$ = number of hash functions
- $n$ = number of elements
- $m$ = bit array size

**Use Case**: Large-scale duplicate detection, cache filtering

---

<!-- _footer: "Contact: 23f2005452@ds.study.iitm.ac.in" -->

## 📊 Data Science Pipeline DSA

```
Data Ingestion → Preprocessing → Feature Engineering → Modeling → Deployment
     ↓              ↓                 ↓                  ↓           ↓
  Arrays        Hash Tables       Matrices           Trees       Graphs
  Queues         Heaps           DataFrames        Ensembles   Networks
```

### Key Structures by Phase:
1. **Ingestion**: Buffers, Queues
2. **Preprocessing**: Hash tables, Arrays
3. **Feature Eng**: Sparse matrices, Trees
4. **Modeling**: Tensors, Graphs
5. **Deployment**: Cache structures, Load balancers

---

## ⚖️ Time-Space Trade-offs

### Classic Examples

| Problem | Time Priority | Space Priority |
|---------|---------------|----------------|
| Sorting | Merge Sort $O(n \log n)$ | Heap Sort $O(1)$ aux |
| Search | Hash Table $O(1)$ | Binary Search $O(1)$ |
| Graph Traversal | BFS $O(V+E)$ | DFS $O(V)$ stack |

### The Principle
$$\text{Time} \times \text{Space} \geq \text{constant}$$

**Optimization Strategy**: Identify bottleneck (time vs space) in your application

---

## 🛠️ Best Practices

### 1. Choose the Right Structure
- **Access pattern**: Random access → Array
- **Insert/Delete heavy**: Linked list
- **Search intensive**: Hash table or BST

### 2. Consider Data Characteristics
- **Static data**: Arrays, sorted structures
- **Dynamic data**: Linked lists, balanced trees
- **Duplicate handling**: Sets, unique constraints

### 3. Profile Before Optimizing
```python
import timeit
# Measure actual performance
```

---

## 📚 Python Libraries & DSA

### NumPy
- Efficient **contiguous arrays**
- Vectorized operations: $O(n) \to O(1)$ effective

### Pandas
- **DataFrame**: Hash table + Array hybrid
- Index: Hash-based $O(1)$ lookups

### Scikit-learn
- **KDTree/BallTree**: Spatial indexing
- **Sparse matrices**: CSR/CSC formats

### NetworkX
- Graph algorithms implementation
- Multiple representations supported

---

## 🎓 Key Takeaways

1. **Understand Complexity**: Always analyze time/space trade-offs
2. **Match Structure to Problem**: No universal "best" structure
3. **Leverage Libraries**: Don't reinvent optimized structures
4. **Profile Performance**: Measure, don't guess
5. **Consider Scale**: Algorithm choice depends on data size

### Formula to Remember

$$\text{Performance} = f(\text{Algorithm}, \text{Data Structure}, \text{Data Size})$$

---

## 📞 Contact & Resources

**Technical Documentation Team**
📧 **Email**: 23f2005452@ds.study.iitm.ac.in

### Additional Resources
- **GitHub**: Company internal repositories
- **Confluence**: Detailed API documentation
- **Stack Overflow**: Community Q&A

### Version Control
- This presentation is maintained in Git
- Can be exported to: PDF, HTML, PPTX
- Automated CI/CD pipeline for updates

---

<!-- _class: title -->
<!-- _paginate: false -->

# Thank You! 🙏

## Questions?

**Stay Connected**
23f2005452@ds.study.iitm.ac.in

*"In data science, the right data structure is half the solution."*
