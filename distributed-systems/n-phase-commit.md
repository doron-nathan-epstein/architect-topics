# N Phase Commit

## Definition

At the heart of every distributed system is a consensus algorithm. Consensus is an act wherein a system of processes agree upon a value or decision. The processes propose values for others and then agrees upon a value if it’s confident that every other process also has agreed upon the same value. The consensus has three characteristics:

- Agreement — all nodes in N decide on the same value.
- Validity — The value that’s decided upon should have been proposed by some process.
- Termination — A decision should be reached.

## 2 Phase Commit (2PC)

![2PC](https://www.researchgate.net/profile/Neeraj-Suri/publication/267854236/figure/fig2/AS:647167379243026@1531308135514/The-2-phase-commit-protocol.png)

This protocol requires a coordinator. The client contacts the coordinator and proposes a value. The coordinator then tries to establish the consensus among a set of processes (a.k.a Participants) in two phases, hence the name.

1. In the first phase, coordinator contacts all the participants suggests value proposed by the client and solicit their response.
2. After receiving all the responses, the coordinator makes a decision to commit if all participants agreed upon the value or abort if someone disagrees.
3. In the second phase, coordinator contacts all participants again and communicates the commit or abort decision.


## 3 Phase Commit (3PC)

![3PC](https://www.researchgate.net/profile/Neeraj-Suri/publication/267854236/figure/fig3/AS:647167379267586@1531308135544/The-3-phase-commit-protocol.png)

This is an extension of two-phase commit wherein the commit phase is split into two phases as follows.

1. Prepare to commit, After unanimously receiving yes in the first phase of 2PC the coordinator asks all participants to prepare to commit. During this phase, all participants acquire locks etc, but they don’t actually commit.
2. If the coordinator receives yes from all participants during the prepare to commit phase then it asks all participants to commit.

## 2PC vs 3PC

| Area | 2 Phase Commit | 3 Phase Commit |
| ---- | -------------- | -------------- |
| Use Case | Used when the coordinator is reliable. | Used when the coordinator is unreliable. |
| Performance | Blocking in nature. | Non-blocking in nature. |
| Fault Tolerance | If the coordinator fails after receiving yes from all participants in the first phase, then the participants will never know if the transaction should be committed or aborted. | If the coordinator fails after receiving yes from all participants in the first phase, then the participants will know that the transaction should be committed. |

## Sources

- <https://medium.com/@balrajasubbiah/consensus-two-phase-and-three-phase-commits-4e35c1a435ac>