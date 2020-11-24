---
layout: post
title: "Games as Benchmarks for Artificial Intelligence"

---

There is a lot to be learned from playing games, both for humans and artificially intelligent agents. Different games encapsulate different facets of the world we live in. Across different games there are differences in substrate (physical vs virtual), number of players (single- vs multi-player), time format (real-time vs turn-based), randomness (deterministic vs stochastic), and completeness of information (partially- vs fully-observable) which test our physical, cognitive, and social capabilities in a variety of complex environments. Therefore, it’s not surprising that games have been used as a benchmark of progress in artificial intelligence (AI) since the field’s inception.

Symbolic AI systems of the late 20th century proved sufficient to defeat world champions in games like Backgammon and Chess, and very recently, deep learning systems have been able to defeat world champions in games like Go (AlphaGo) [1] and Poker (Libratus) [2]. But despite these incredible accomplishments, agents like AlphaGo and Libratus are only intelligent in a very narrow sense of the word: their abilities do not generalize, and it would be difficult to argue that they truly understand what they are doing.

We have seen similar deficiencies even with newly developed deep transformer models which have enabled state-of-the-art results across natural language processing and computer vision. These transformer models perform impressively on many tasks, such as dialogue [3], object detection [4], code completion [5], and theorem proving [6]. However, because the models are not grounded in any formal semantic representation, they often generate nonsensical output [7], showing that there are likely limitations to the types of reasoning that will emerge, especially as we reach bottlenecks on quantity and types of training data.

A natural next step, therefore, is to augment models with some form of commonsense reasoning and knowledge. How exactly to do this is unclear, but there are many approaches that have shown promising results, including multimodal perception [8, 9], grounded language understanding [9, 10], automated knowledge base construction [11, 12], and interactive task learning [13]. Additionally, new technologies like graph convolutional networks [14, 15], knowledge graph embeddings [16], and cognitive architectures [17] have started to bridge this gap toward hybrid statistical-symbolic systems which seem to incorporate knowledge into their outputs. There is good reason to believe that this approach, combining the inductive strengths of statistical AI with the deductive strengths of symbolic AI, will yield better results in the long run than either approach alone [18].

Building off the idea that games are an effective means of testing AI systems, researchers have started to experiment with new forms of virtual environments.

For example, take the fairly new MineRL Competition [19]. The competition used completion of tasks in the open-world sandbox video game Minecraft as a benchmark for deep reinforcement learning agents. And while the challenge is a fantastic initiative, I believe it could and should be expanded greatly, for example by encouraging the use of domain knowledge rather than prohibiting it. Allowing systems to scrape the Internet for information and use it for reasoning more accurately reflects real world scenarios in which an agent might be trying to learn a new skill or accomplish some task. Additionally, given that the incorporation of domain knowledge will likely make the current ObtainDiamond task much easier, more difficult in-game tasks ought to be used as benchmarks. Conveniently, the game has 80 built-in goals that are designed to ease newer players into the game, several of which would serve perfectly as challenges. 

The use of text-based adventure games has also proved a promising means of testing AI systems. In 2018, Microsoft published TextWorld [20], an open-source library for text-based game generation, and in 2019, Urbanek et al. published LIGHT [21], a crowdsourced text adventure game designed for the study of grounded dialogue. These environments are typically modeled as partially observable Markov decision processes, and researchers design reinforcement learning agents to navigate them and accomplish goals. In [22], Ammanabrolu et al. introduce a knowledge graph-augmented deep Q-network and demonstrate its potential by applying it to TextWorld environments, and in [23], Ammanabrolu et al. extend LIGHT with a crowdsourced dataset of quests and show that a commonsense knowledge graph and commonsense reasoning-based language model pre-training are effective mechanisms for training an agent to act and converse in the LIGHT environment. Text-based environments are still a very new idea however, and there are many ways in which the exploration of them can be expanded, for example, by exploring multi-agent settings (drawing from [24] and [25]), environments more closely resembling the real world (like [26]), and agents that can operate in a variety of different environments without needing to be retrained. 

These works show that virtual environments are an effective means of testing various kinds of perception, inference and action, from commonsense physics to open-domain dialogue, and while these subproblems might be more tractable when studied in isolation, as long as the end goal is to integrate these abilities into a single system, the use of virtual environments as a testing mechanism is not going anywhere. I hope to spend my graduate studies researching these virtual environments and building autonomous agents that can operate in them and exhibit increasingly complex forms of intelligent behavior. 


### References

[1] Silver, David, et al. "Mastering the game of Go with deep neural networks and tree search." nature 529.7587 (2016): 484-489.

[2] Brown, Noam, Tuomas Sandholm, and Strategic Machine. "Libratus: The Superhuman AI for No-Limit Poker." IJCAI. 2017.

[3] Ham, Donghoon, et al. "End-to-End Neural Pipeline for Goal-Oriented Dialogue Systems using GPT-2." ACL, 2020.

[4] Carion, Nicolas, et al. "End-to-End Object Detection with Transformers." arXiv preprint arXiv:2005.12872 (2020).

[5] Kim, Seohyun, et al. "Code Prediction by Feeding Trees to Transformers." arXiv preprint arXiv:2003.13848 (2020).

[6] Polu, Stanislas, and Ilya Sutskever. "Generative language modeling for automated theorem proving." arXiv preprint arXiv:2009.03393 (2020).

[7] Marcus, Gary. “GPT-3, Bloviator: OpenAI's Language Generator Has No Idea What It's Talking About.” MIT Technology Review, MIT Technology Review, 9 Sept. 2020, www.technologyreview.com/2020/08/22/1007539/gpt3-openai-language-generator-artificial-intelligence-ai-opinion/.

[8] Liang, Junwei, et al. "Focal visual-text attention for memex question answering." IEEE transactions on pattern analysis and machine intelligence 41.8 (2019): 1893-1908.

[9] Paul, Rohan, et al. "Temporal grounding graphs for language understanding with accrued visual-linguistic context." arXiv preprint arXiv:1811.06966 (2018).

[10] Lindes, Peter, et al. "Grounding language for interactive task learning." Proceedings of the First Workshop on Language Grounding for Robotics. 2017.

[11] Bosselut, Antoine, et al. "COMET: Commonsense transformers for automatic knowledge graph construction." arXiv preprint arXiv:1906.05317 (2019).

[12] Adhikari, Ashutosh, et al. "Learning dynamic knowledge graphs to generalize on text-based games." arXiv preprint arXiv:2002.09127 (2020).

[13] Kirk, James R., and John E. Laird. "Learning Hierarchical Symbolic Representations to Support Interactive Task Learning and Knowledge Transfer." IJCAI. 2019.

[14] Kipf, Thomas N., and Max Welling. "Semi-supervised classification with graph convolutional networks." arXiv preprint arXiv:1609.02907 (2016).

[15] Wang, Xiaolong, Yufei Ye, and Abhinav Gupta. "Zero-shot recognition via semantic embeddings and knowledge graphs." Proceedings of the IEEE conference on computer vision and pattern recognition. 2018.

[16] Wang, Zhen, et al. "Knowledge graph embedding by translating on hyperplanes." Aaai. Vol. 14. No. 2014. 2014.

[17] Mao, Jiayuan, et al. "The neuro-symbolic concept learner: Interpreting scenes, words, and sentences from natural supervision." arXiv preprint arXiv:1904.12584 (2019).

[18] Maruyama, Yoshihiro. "The Conditions of Artificial General Intelligence: Logic, Autonomy, Resilience, Integrity, Morality, Emotion, Embodiment, and Embeddedness." International Conference on Artificial General Intelligence. Springer, Cham, 2020.

[19] Guss, William H., et al. "The minerl competition on sample efficient reinforcement learning using human priors." arXiv preprint arXiv:1904.10079 (2019).

[20] Côté, Marc-Alexandre, et al. "Textworld: A learning environment for text-based games." Workshop on Computer Games. Springer, Cham, 2018.

[21] Urbanek, Jack, et al. "Learning to speak and act in a fantasy text adventure game." arXiv preprint arXiv:1903.03094 (2019).

[22] Ammanabrolu, Prithviraj, and Mark O. Riedl. "Playing text-adventure games with graph-based deep reinforcement learning." arXiv preprint arXiv:1812.01628 (2018).

[23] Ammanabrolu, Prithviraj, et al. "How to Motivate Your Dragon: Teaching Goal-Driven Agents to Speak and Act in Fantasy Worlds." arXiv preprint arXiv:2010.00685 (2020).

[24] Bansal, Trapit, et al. "Emergent complexity via multi-agent competition." arXiv preprint arXiv:1710.03748 (2017).

[25] Suarez, Joseph, et al. "Neural MMO: A massively multiagent game environment for training and evaluating intelligent agents." arXiv preprint arXiv:1903.00784 (2019).

[26] Puig, Xavier, et al. "Virtualhome: Simulating household activities via programs." Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition. 2018.
