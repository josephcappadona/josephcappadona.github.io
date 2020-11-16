---
layout: post
title: "Games as Benchmarks for Artificial Intelligence"

---


There is a lot to be learned from playing games, both for humans and artificially intelligent agents. Different games encapsulate different facets of the world we live in. Across different games there are differences in substrate (physical vs virtual), number of players (single- vs multi-player), time format (real-time vs turn-based), randomness (deterministic vs stochastic), and completeness of information (partially- vs fully-observable) which test our physical, cognitive, and social capabilities in a variety of complex environments. Therefore, it’s not surprising that games have been used as a benchmark of progress in artificial intelligence (AI) since the field’s inception. Symbolic AI systems of the late 20th century proved sufficient to defeat world champions in games like Backgammon and Chess, and very recently, deep learning systems have been able to defeat world champions in games like Go (AlphaGo) [1] and Poker (Libratus) [2]. But despite these incredible accomplishments, agents like AlphaGo and Libratus are only intelligent in a very narrow sense of the word: their abilities do not generalize, and it would be difficult to argue that they truly understand what they are doing. We have seen similar deficiencies with state-of-the-art language models like GPT-3, where despite its impressive language generation capabilities, the text it generates is not grounded in commonsense logic and fails when taken slightly out of distribution [3]. In general, it’s unclear whether approaches which rely only on deep learning will be sufficient in the long-run to achieve human-level artificial intelligence, and there is good reason to believe that combining the inductive strengths of statistical AI with the deductive strengths of symbolic AI will yield more powerful, general agents than either approach alone [4]. To account for the deficiencies of deep learning and current benchmarks which only test narrow forms of intelligence, new benchmarks and architectures are needed, and I believe that using virtual environments, especially games, that more closely mimic real-world environments as benchmarks is a promising direction toward this goal.

For example, take the fairly new MineRL Competition [5]. The competition used completion of tasks in the open-world sandbox video game Minecraft as a benchmark for deep reinforcement learning agents. However, while the challenge is a fantastic initiative, I believe it could and should be expanded greatly, for example by encouraging the use of domain knowledge rather than prohibiting it. Allowing systems to scrape the Internet for information and use it for reasoning more accurately reflects real world scenarios in which an agent might be trying to learn a new skill or accomplish some task. Additionally, given that the incorporation of domain knowledge will likely make the current ObtainDiamond task much easier, more difficult in-game tasks ought to be used as benchmarks. Conveniently, the game has 80 built-in goals that are designed to ease newer players into the game, several of which would serve perfectly as challenges.

Another fascinating initiative is the use of text-based adventure games to test AI systems. In 2018, Microsoft published TextWorld [6], an open-source library for text-based game generation, and in 2019, Urbanek et al. published LIGHT [7], a crowdsourced text adventure game designed for the study of grounded dialogue. These environments are typically modeled as partially observable Markov decision processes, and researchers design reinforcement learning agents to navigate them and accomplish goals. In [8], Ammanabrolu et al. introduce a knowledge graph deep Q-network and demonstrate its potential by applying it to TextWorld environments, and in [9], Ammanabrolu et al. extend LIGHT with a crowdsourced dataset of quests and show that a commonsense knowledge graph and commonsense reasoning-based language model pre-training are effective mechanisms for training an agent to act and converse in the LIGHT environment.

I am optimistic for what the future holds in this space. The evolution of the field of AI from simple neural networks that can only recognize digits to knowledge graph-augmented deep reinforcement learning agents capable of operating in open-world environments only took about a decade. I’m not foolish enough to propose what might be possible in another decade of work, but given the accelerating influx of researchers and investments into the field, I’m sure that we will continue to be amazed.


### References

[1] Silver, David, et al. "Mastering the game of Go with deep neural networks and tree search." nature 529.7587 (2016): 484-489.

[2] Brown, Noam, Tuomas Sandholm, and Strategic Machine. "Libratus: The Superhuman AI for No-Limit Poker." IJCAI. 2017.

[3] Marcus, Gary. “GPT-3, Bloviator: OpenAI's Language Generator Has No Idea What It's Talking About.” MIT Technology Review, MIT Technology Review, 9 Sept. 2020, www.technologyreview.com/2020/08/22/1007539/gpt3-openai-language-generator-artificial-intelligence-ai-opinion/.

[4] Maruyama, Yoshihiro. "The Conditions of Artificial General Intelligence: Logic, Autonomy, Resilience, Integrity, Morality, Emotion, Embodiment, and Embeddedness." International Conference on Artificial General Intelligence. Springer, Cham, 2020.

[5] Guss, William H., et al. "The minerl competition on sample efficient reinforcement learning using human priors." arXiv preprint arXiv:1904.10079 (2019).

[6] Côté, Marc-Alexandre, et al. "Textworld: A learning environment for text-based games." Workshop on Computer Games. Springer, Cham, 2018.

[7] Urbanek, Jack, et al. "Learning to speak and act in a fantasy text adventure game." arXiv preprint arXiv:1903.03094 (2019).

[8] Ammanabrolu, Prithviraj, and Mark O. Riedl. "Playing text-adventure games with graph-based deep reinforcement learning." arXiv preprint arXiv:1812.01628 (2018).

[9] Ammanabrolu, Prithviraj, et al. "How to Motivate Your Dragon: Teaching Goal-Driven Agents to Speak and Act in Fantasy Worlds." arXiv preprint arXiv:2010.00685 (2020).
