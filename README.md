# TSP-Green-Logistics
👥 Group Members:  
Maisoon Mohammed Alabdullah  
Wajd Khalid Alkhaldi  
Jolie Jamal Salama  
Nabaa Nabeeh Alaswad  
Manar Saleh Alghamdi  
  
📌 Project Overview  
This project tackles the Traveling Salesperson Problem (TSP) within the framework of Green Logistics and Sustainable Supply Chain Management. The core challenge is to find the shortest possible route for a delivery vehicle that visits every customer location exactly once and returns to the starting depot — minimizing fuel consumption, operational costs, and carbon emissions.  
Two algorithmic approaches are implemented and compared:  
Nearest Neighbor  
Held-Karp  

📂 Repository Structure  
TSP-Green-Logistics-G1/  
│  
├── TSP_G1_Notebook.ipynb       # Main Jupyter Notebook (full implementation)  
│  
├── datasets/  
│   ├── tiny.csv                # 10 cities  
│   ├── small.csv               # 30 cities  
│   ├── medium.csv              # 100 cities  
│   └── large.csv               # 1,000 citie  
│  
└── README.md  
  
🗃️ Dataset  
Source: Kaggle — Traveling Salesman Problem (mexwell)  
Link: https://www.kaggle.com/datasets/mexwell/traveling-salesman-problem  
  
   
  
⚙️ Algorithms Implemented  
1. Nearest Neighbor (Greedy)  
  
Starts at a chosen depot city  
At every step, moves to the nearest unvisited city  
Repeats until all cities are visited, then returns to start  
Time Complexity: O(n²)  
Space Complexity: O(n)  
Cases defined by: Starting city choice  
  
2. Held-Karp (Dynamic Programming)  
  
Uses bitmask DP to evaluate all possible subsets of cities  
Builds optimal solutions from smaller subproblems upward  
Guarantees the mathematically shortest route  
Time Complexity: O(2ⁿ × n²)  
Space Complexity: O(2ⁿ × n)  
Cases defined by: Number of input cities  
  
🚀 How to Run  
Step 1 — Clone the Repository  
bashgit clone https://github.com/YourUsername/TSP-Green-Logistics-G1.git    
  
cd TSP-Green-Logistics-G1  
Step 2 — Install Required Libraries  
bashpip install numpy matplotlib pandas jupyter  
Step 3 — Launch Jupyter Notebook  
bashjupyter notebook  
Step 4 — Open and Run the Notebook  
  
Click on TSP_G1_Notebook.ipynb  
Click Kernel → Restart & Run All  
Wait for all cells to complete  
  
  
⚠️ Note: The Held-Karp worst case (20 cities) takes approximately 39 seconds to complete due to exponential complexity. This is expected — do not interrupt execution.  
  
Step 5 — View Outputs  
Once complete, the notebook will display:  
  
✅ Dataset loading summary  
✅ City map visualizations for all 4 datasets  
✅ 3 route visualizations per algorithm (Best, Average, Worst)  
✅ Full performance comparison table  
✅ Bar charts comparing execution time and distance  
  
  
🔑 Key Findings  
  
Nearest Neighbor is 925x faster than Held-Karp on comparable inputs
Held-Karp execution time multiplies by 32–70x with every 5 additional cities
Held-Karp always produces the mathematically optimal route
Nearest Neighbor routes are typically 10–25% longer than optimal
For real-world Green Logistics with hundreds of stops, Nearest Neighbor is the only practical choice
  
  
📝 Conclusion  
This project demonstrates the fundamental trade-off between algorithmic paradigms in the context of real-world logistics. The Nearest Neighbor algorithm is recommended as the primary routing strategy for large-scale sustainable supply chain operations, while Held-Karp serves as the gold standard for validating optimal solutions on small critical subproblems.  
  
📄 License  
This project was developed for academic purposes at Imam Abdulrahman Bin Faisal University.
CSC 301: Algorithm Analysis and Design — Academic Year 2025/2026.  
  
