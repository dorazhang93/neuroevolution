# Neuroevolution
This field started with fixed-topology networks (optimize weights only), moved to complexifying networks (TWEANN), and then began to focus on indirectly encoded networks (NEAT, CPPN, HyperNEAT). One other recent influential idea in the field is novelty search. Quality diversity algorithms (the next step beyond novelty search) add the notion of fitness back in, but in a careful way so as not to undermine the delicate push for novelty. Much research over the years and continuing to this day has focused on how to evolve plastic ANNs, which means networks with connection weights that change over the lifetime of the network.
## Fixed-topology Networks (the evolution of connection weights)

<img width="490" alt="fixed-topology-binaryEncode" src="https://user-images.githubusercontent.com/92612359/140245215-645576b5-535b-4f3c-a2a6-64fa5d2efd1f.png">

## Topology and Weight Evolving Artificial Neural Networks (TWEANN)
### The direct encoding scheme
Binary encoding is notable for its simplicity, using a bit string represents the connection matrix of a network. However, there are several limitations as well. First, the size of the connectivity matrix is the square of the number of nodes. Thus, the representation blows up for a large num- ber of nodes. Second, because the size of the bit string must be the same for all organisms, the maximum number of nodes (and hence connections as well) must be chosen by a human running the system, and if the maximum is not sufficient, the experiment must be repeated. Third, using a linear string of bits to represent a graph structure makes it difficult to ensure that crossover will yield useful combinations.

<img width="844" alt="The direct encoding for NN" src="https://user-images.githubusercontent.com/92612359/140246485-ee5d687e-07c4-4bd2-a2b4-9c5dc8294d04.png">
<img width="843" alt="The direct encoding for RNN" src="https://user-images.githubusercontent.com/92612359/140246611-c3be9553-e7db-44a6-b3a0-8fbb0a8a9145.png">

Graph encoding is more explicit and allow different kinds of crossover. PDGP uses graph encoding so that subgraphs can be swapped in crossover. Subgraph swapping is representative of a pre- vailing philosophy in TWEANNs that subgraphs are functional units and therefore swapping them makes sense because it preserves the structure of functional components.As in sGA, PDGP has a finite limit on the number of nodes in the network. However, we cannot be sure whether the particular subgraphs being combined in PDGP are the right ones to create a functional offspring.

<img width="409" alt="graph encoding" src="https://user-images.githubusercontent.com/92612359/140252536-8948b486-b892-4db8-98c1-7fe1bf40accc.png">

NeuroEvolution of Augmenting Topologies (NEAT)
NeuroEvolution of Augmenting Topologies (NEAT) that outperforms the best fixed-topology method on a challenging benchmark reinforcement learning task. We claim that the increased efficiency is due to (1) employing a principled method of crossover of different topologies, (2) protecting structural innovation using speciation, and (3) incrementally growing from mini- mal structure.

<img width="813" alt="NEAT components" src="https://user-images.githubusercontent.com/92612359/140269975-e11e508b-c486-4edd-8d3e-6c1c73933146.png">
<img width="815" alt="NEAT crossover" src="https://user-images.githubusercontent.com/92612359/140269984-5b71f0d8-1ff7-4cd9-aafc-4070d9becd68.png">

### The indirect encoding scheme
<img width="469" alt="The development rules of indirect encoding for architecture" src="https://user-images.githubusercontent.com/92612359/140249051-8403a003-d0e8-4771-a8fa-1b65d56d6dd3.png">

HyperNEAT
<img width="711" alt="connective CPPN" src="https://user-images.githubusercontent.com/92612359/140631142-4a932c77-08e3-46be-9171-c63ff358bf86.png">
<img width="723" alt="HyperNEAT" src="https://user-images.githubusercontent.com/92612359/140631146-955c79ce-517d-43b7-aa4a-f38d5b697bc0.png">

## Novelty Search
## Plastic ANNs
