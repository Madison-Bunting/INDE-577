# Neural Networks

Neural networks are used in everything from image recognition to speech recognition to natural language. These are computational models inspired by the way biological neural networks in the human brain process information, composed of interconnected neurons that apply a function to inputs that computes outputs with associated weights (w) which designate a given input's relative importance to other inputs. 

![image](https://www.researchgate.net/profile/Zhenzhu-Meng/publication/339446790/figure/fig2/AS:862019817320450@1582532948784/A-biological-neuron-in-comparison-to-an-artificial-neural-network-a-human-neuron-b.png)

Parts of a neural network:

- Input Nodes (input layer): no computation is done in this layer; it just passes information to the next layer (often a hidden layer). A block of nodes is also called a **layer**.
- Hidden nodes (hidden layer): where intermediate processing/computation happens; after computing computations, these nodes pass along weights (which can be either signals or information) from the input layer to the following layer, which can be another hidden layer or the output layer. It is also possible to have a neural network without a hidden layer.
- Output nodes (output layer): uses an activation function to map information to the desired output format
- Connections and weights: a *network* consistes of connects that transfer the output from neuron i to neuron j, assigned weight W_ij
- Activation Function (aka transfer function): defines output of that node given a set of inputs. Its behavior is similar to the behavior of a single perceptron, but it is the ability to use nonlinear activation functions that allow networks to computer nontrivial problems with a small number of nodes
- Learning rule: algorithm which modifies the parameters of the neural network, in order for a given input to the network to produce a favored output. This *learning* process is often just modifying the weights and thresholds

There are several types of neural networks:
- **Feedforward neural network (artificial neural networks, ANN):** connections between units do **not** form a cycle or loop; the information only moves in one direction: forward, from input nodes through hidden nodes (if any) to output nodes
  - **[Single-layer perceptron](https://github.com/Madison-Bunting/INDE-577/tree/main/supervised%20learning/3%20-%20perceptron):** The simplest feedforward neural network and does not contain any hidden layers. It is called "single" because we do not include the input layer when counting layers due to the fact that the input layer is not used for computation; inputs are directly fed to outputs via a series of weights

![image](https://miro.medium.com/max/468/1*1WVSZV59q750l6ERCcRgCg.gif)

  - **Multi-layer perceptron (MLP):** multiple layers of computational units, usually interconnected in a feed-forward way. Each neuron in one layer has directed connections to the neurons of the subesquent layer. Many applications of these apply a sigmoid function as an activation. One particularly useful feature is MLP's ability to learn nonlinear representations because often data is not linearly separable.

![image](https://miro.medium.com/max/960/1*-NE4oK759a3uqKzI6McJwA.jpeg)

  - **Convolutional Neural Networks (CNN, ConvNet, shift variant, or space invariant):** variations of multi-layer perceptrons that ues minimal processing - the node connectivity pattern is specifically inspired by the organization of the visual cortex of the human brain: nodes respond to stimuli in a restricted region of space (receptive field). These fields partially overlap, over-covering the entire visual field. Thus, these networks require a significant amount of training data. Their response can be mathematically approximated using a convolution operations. CNNs have appliations in image and video recognition, recommender systems, and natural language processing.

![image](https://miro.medium.com/max/1050/1*N4h1SgwbWNmtrRhszM9EJg.png)

- **Recurrent Nerual Networks (RNN):** connections between units form a directed cycle (the propogate data forward, but they also send it backwards from later processing stages to earlier stages, which is called [back propogation](https://en.wikipedia.org/wiki/Backpropagation)), which allow them to exhibit dynamic temporal behavior. RNNs can use their internal memory to process arbitrary sequences of inputs, and they have applications in unsegmented, connected handwriting recognition, speech recognition, and other general sequence processors. 

![image](https://docs.paperspace.com/~/files/v0/b/gitbook-28427.appspot.com/o/assets%2F-LvBP1svpACTB1R1x_U4%2F-LwEQnQw8wHRB6_2zYtG%2F-LwEZT8zd07mLDuaQZwy%2Fimage.png?alt=media&token=93a3c3e2-e32b-4fec-baf5-5e6b092920c4)

**[Common Activation Functions](https://medium.com/@devalshah1619/activation-functions-in-neural-networks-58115cda9c96)**
A few of the most common functions and their uses are included in the chart below:

![image](https://www.simplilearn.com/ice9/free_resources_article_thumb/Perceptron/Perceptron_36.jpg)


The above information was largely based on [this article](https://towardsdatascience.com/a-gentle-introduction-to-neural-networks-series-part-1-2b90b87795bc), and [this article](https://cs231n.github.io/neural-networks-1/) contains more details for future research.

