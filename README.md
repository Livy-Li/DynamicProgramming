# Inventory Optimaization with Dynamic Programming
Stochastic Inventory Management using the Markov Decision Process (MDP)

---
## Summary
Inventory optimization models can be divided into two categories: deterministic and stochastic. Variable states are uniquely determined by the parameters in deterministic model; while stochastic models takes demand and/or system parameter uncertainties into account. The goal of stochastic inventory management is to determine the optimal timing of making replenishment orders and the order quantities, while taking demand and/or system parameter uncertainties into account.

In this inventory management project, the goal is to optimize an inventory system by finding an optimal (s,S) policy. Under an (s,S) policy, the system will automatically send orders to supplier when the inventory level reaches or falls below the safety stock, s, and such order will fulfill the inventory back to level S. However, since there is a lead time between when the order is placed and when the shipment of inventory arrives, the question is not easily solved. Therefore, dynamic programming with Markov Decision Process (MDP) is employed.

The given inventory problem is formulated as an MDP and solved using two different methods: Policy Iteration Algorithm and Q-Learning Algorithm.

---
## Model Setup

|Cost|Value|
|----|----|
|Market Price|$10|
|Wholesale Price|$4|
|Unit holding cost per year|$2|
|Fixed setup cost|$100|
|Unit Stockout Penalty|$15|

- Inventory is controlled according to weekly review
- Weekly demand follows a discrete uniform distribution between 0 and 10
- The maximum capacity of storage is 500
- The lead time is fixed at 2 weeks
