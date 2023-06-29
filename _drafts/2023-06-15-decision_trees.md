• 

# Decision Tree Leaning 

- Start with all examples at the root node
- Calculate information gain for all possible features, and pick the one with the highest information gain
- Split dataset according to selected feature, and create left and right branches of the tree
- Keep repeating splitting process until stopping criteria is met:
    - When a node is 100% one class
    - When splitting a node will result in the tree exceeding a maximum depth
    - Information gain from additional splits is less than threshold. Recall:
        $$ 
        \textnormal{Information gain} = H(p_{1}^{\textnormal{root}}) - [H(p_{1}^{\textnormal{left}}) * w^{left} + H(p_{1}^{\textnormal{right}}) * w^{right}], \textnormal{where} 
        H_{p_1} = -p_{1}* \log_{2}(p_1) - (1 - p_{1})* \log_{2}(1 - p_1)
        $$
    - When number of examples in a node is below a threshold