## Lecture 2: Adversarial Attacks

### Adversarial Examples:

**Adversarial examples are inputs to machine learning models that an attacker has intentionally designed to cause the model to make a mistake.**

Some known adversarial examples:

+ Some **noises** or some **changes to some specific pixel**:

![image-20210422161037018](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422161037018.png)

+ **Geometric transformation**:

  Attacker can do some simple Geometric transformation to fool network.

![image-20210422161206732](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422161206732.png)

+ Adversarial examples in **Reinforcement Learning**:

  Attacker can disturb the image to fool the network.

![image-20210422161652990](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422161652990.png)

+ Adversarial examples in **NLP**:

  Attacker can add some adversarial words to fool network.

![image-20210422161933079](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422161933079.png)

+ Adversarial Examples in **Audio Processing**:

![image-20210422162125435](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422162125435.png)

**In my opinion: these Adversarial Examples can fool the network just because the network have no such certification algorithm or some specific preset examples to check the small change within some acceptable range.**

### Robustness

##### Definition of Robustness:

**A network is robust if it returns correct output on all inputs.**

But it is not so impractical since **the input space is too large to be covered.**

So we come to **Local Robustness.**

##### Definition of Local Robustness (informal):

 A learning model is **locally-robust** if it returns the correct output on inputs **similar** to inputs in the training set.

This is performed by having high accuracy on test sets.

**BUT** high accuracy is not enough since: There are still many similar inputs that are **never tested** (and have low-probability for the given distribution)

### The Story of Clever Hans

This is a example the tells us that why our network or model can make mistake that is because sometimes we thought they have learned what we need them to learn but actually they learn some useless things but can give correct output in the train sets and test sets while in this way, if we add some noise or perturbations, the network will make mistakes.

### Why Do Adversarial Example Exists

**Neural Networks are too linear**, because linear functions are easy to optimize.

![image-20210422165443574](C:\Users\lenovo\AppData\Roaming\Typora\typora-user-images\image-20210422165443574.png)

So more non-linearity can allow us to get rid of some potential adversarial examples.