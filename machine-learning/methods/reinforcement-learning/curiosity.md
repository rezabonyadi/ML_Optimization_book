# Curiosity

In reinforcement learning, you have an agent that is exploring an environment to perform a task for which it receives an award if it does it right \(or partially right\). Now assume that the rewards are not that frequent \(e.g., consider fishing, you only receive the reward once you capture a fish, while many steps are needed to actually capture the fish\). In that case, the agent experiences difficulty to find even one simple way to receive a reward. As such, it will be difficult for the agent to learn the game effectively as it cannot extent its learning as there is no reward for most actions it take. Here comes curiosity. The idea is, the agent should avoid strategies it has tried before and lean towards strategies that have not been explored much. This provides an "intrinsic" reward for the agent which help to find new ways which, hopefully, would lead to more rewards.

![](../../../.gitbook/assets/thegamespeop.gif)

A good example of where curiosity can be helpful is in the game Montezuma's Revenge \(see Fig. \@ref\(fig:montezuma\)\). The agent is required to find the "key" in the middle-left of the screen. To do so, it requires to find the path indicated in the figure, which is a quite complicated path. At the beginning, the agent has no idea about this environment, hence, it needs to explore options rather randomly. If the agent falls down or hits the skeleton, it will die. The agent does not receive any reward for most of the steps in this game, until it actually captures the key. Finding that successful path until the agent receives a reward randomly is close to impossible. In that case, because most paths lead to death rather than a reward, the agent would think that it would be better not to move at all to reduce the possibility of loss rather than finding any rewards. An intrinsic reward, here curiosity, would still keep the agent motivated to explore.

### Implementation idea

Curiosity provides intrinsic motivation for the agent to explore alternative solutions which have been investigated less frequently. One frequently used implementation is based on the following assumption: If the agent can guess what is the consequence of its move at the current step then the agent has tried this path before, hence, intrinsic reward would be lower. Adding this intrinsic reward to the total reward, the agent would receive a reward for the movements that are “novel”, which encourages the agent to be “curious”. See [https://arxiv.org/pdf/1808.04355.pdf](https://arxiv.org/pdf/1808.04355.pdf) \([https://arxiv.org/pdf/1808.04355.pdf](https://arxiv.org/pdf/1808.04355.pdf)\).

#### What does it solve?



