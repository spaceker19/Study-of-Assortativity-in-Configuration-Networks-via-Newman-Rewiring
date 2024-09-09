# Study-of-Assortativity-in-Configuration-Networks-via-Newman-Rewiring
Here’s a well-structured GitHub README for your thesis:

---

# Assortativity in Networks: A Python Framework using NetworkX

This repository contains the Python framework developed as part of the thesis, *"Assortativity in Networks: A Study using Newman’s Rewiring Technique"*. The study explores assortativity in scale-free networks, leveraging the **NetworkX** library to manipulate assortative mixing using Newman’s rewiring technique.

## Thesis Summary

The primary focus of this thesis is to provide a systematic approach to control assortative mixing in networks. This is achieved by:

- Implementing **Newman’s rewiring technique** within the **configuration model**.
- Applying the **random hubs** method to generate degree sequences, minimizing fluctuations and enhancing structural stability.
- Developing a Python framework to experiment with various rewiring matrices and manage off-diagonal elements effectively.
  
Special emphasis is placed on **scale-free networks** and their structural characteristics, particularly through the lens of **Barabasi-Albert (BA) networks**. By leveraging these rewiring techniques, the study provides insights into the correlation structures of networks, offering a deeper theoretical and practical understanding of network assortativity.

## Key Features

1. **Newman’s Rewiring Technique**: Implemented within the configuration model to control assortative mixing.
2. **Random Hubs Method**: Generates degree sequences with minimal fluctuations, ensuring structural stability.
3. **Rewiring Matrices**: Exploration of sophisticated rewiring matrices, optimizing the handling of off-diagonal elements.
4. **Application to Barabasi-Albert (BA) Networks**: Comparison between preferential attachment networks and rewired configurations for scale-free distributions.
5. **Complete Network Connectivity**: Demonstrated in scale-free networks with a β parameter of 2 or greater.

## Installation

To run the code in this repository, you need to have Python 3 installed along with the following dependencies:

```bash
pip install networkx numpy matplotlib
```

## Usage

The framework provides a set of tools to experiment with assortativity and rewiring in networks. You can generate networks and control their assortativity by following these steps:

1. **Generate Scale-Free Networks**:
   ```python
   from networkx.generators.random_graphs import barabasi_albert_graph
   
   G = barabasi_albert_graph(n=1000, m=3)  # Example: BA network with 1000 nodes
   ```

2. **Rewire Network with Newman’s Technique**:
   ```python
   from rewiring_module import newman_rewiring
   
   rewired_graph = newman_rewiring(G, assortativity=0.5)  # Control assortativity
   ```

3. **Visualize the Network**:
   ```python
   import matplotlib.pyplot as plt
   import networkx as nx
   
   nx.draw(rewired_graph, node_size=20)
   plt.show()
   ```

4. **Analyze Assortativity**:
   ```python
   from networkx.algorithms.assortativity import degree_assortativity_coefficient
   
   coeff = degree_assortativity_coefficient(rewired_graph)
   print(f"Assortativity Coefficient: {coeff}")
   ```

## Applications

- **Scale-Free Network Analysis**: Modify and analyze networks with natural correlations, such as Barabasi-Albert (BA) networks.
- **Network Dynamics**: Understand and manipulate network dynamics by adjusting assortativity levels.
- **Network Robustness**: Demonstrate the role of rewiring techniques in achieving robust, connected networks.

## Results

The study shows that for scale-free distributions with a β parameter of 2 or greater, the networks achieved complete connectivity. This confirms the effectiveness of the configuration model and the rewiring techniques developed in producing robust network structures.

## Contributing

If you have any suggestions or improvements, feel free to open an issue or submit a pull request. Contributions are welcome!

## License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## References

- Newman, M. E. J. (2003). *Mixing patterns in networks*. Physical Review E, 67(2), 026126.
- Barabasi, A.-L., & Albert, R. (1999). *Emergence of Scaling in Random Networks*. Science, 286(5439), 509-512.

---

