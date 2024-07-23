### RL for Image Classification - Actor-Critic

### Problem Definition

The objective is to implement a reinforcement learning (RL) approach for image classification using the MNIST and CIFAR10 datasets. The agent is trained to classify images by interacting with a custom environment and receiving rewards based on its actions.

### Algorithm

The project uses the Actor-Critic method, combining value-based and policy-based RL techniques. Neural networks (`MNISTNet` and `CIFAR10Net`) serve as the function approximators for both the actor and the critic.

### Libraries and Environment

- `gym`: For creating custom RL environments.
- `torch`: For building and training neural networks.
- `keras`: For loading the MNIST and CIFAR10 datasets.

### RL Mapping

1. **States**: Observations from the environment (images with masked regions).
2. **Actions**: Movements within the image and classification predictions.
3. **Goal**: Correctly classify the image, maximizing total reward.
4. **Rewards**: 
   - -0.1 for misclassifications.
   - Positive rewards for correct classifications and exploration.

### Actor-Critic Method

The actor predicts action distributions, while the critic estimates the value function. Both networks are updated based on received rewards, improving policy and value estimations.

### Training and Evaluation

- **Training**: Involves multiple iterations and episodes, with rewards guiding the learning process.
- **Evaluation**: Tests the trained agent on a set of images to measure accuracy and performance.

### Conclusion

The project successfully demonstrates an Actor-Critic RL approach for image classification on the MNIST and CIFAR10 datasets, showcasing the agent's ability to learn and classify images effectively.
