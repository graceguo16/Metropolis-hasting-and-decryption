**Introduction**

The Metropolis-Hastings (M-H)algorithm,a Markov chain Monte Carlo(MCMC)method,is one of the most popular techniques used by statisticians today.It is primarily used as a way to simulate observations from unwieldy distributions(Hitchcock,2003).New samples are added to the sequence in two steps:first a new sample is proposed based on the previous sample,then the proposed sample is either added to the sequence or rejected depending on the value of the probability distribution at that point(Wikipedia,2005).

For this project,our group chose the emphasis of Coding and aims to improve the accuracy of decrypting a message based on the Metropolis-Hastings algorithm.In the original setup,the decrypted code defines a sample space of 56 characters,consisting of lowercase and uppercase English letters only,and iteratively proposes new permutations by swapping two characters at a time to explore better likelihoods of decoded outputs.

However,such limited permutations often fail to recover natural English phrases;for instance,a word like  “while”may be incorrectly decoded as “ahile.”To address this,we propose two modifications:(1)in every step,we switch 5 letters in the current permutation at a time instead of 2 letters,and(2)we introduce a  temperature parameter to alter the acceptance rate.The proposal function is modified to generate more diverse  permutations,potentially improving the search efficiency and output accuracy.

Preliminary testing suggests that the first modification did not improve the result of the decoding because the deciphered text was still distorted,and many common English patterns were lost;however,the second modification does help the algorithm capture common English character sequences,resulting in more readable decoded messages.

The project is organized as follows:

·Section 2 introduces the encryption method and provides examples of the permutation of the alphabet, explains the likelihood function,and describes how training is performed.

·Section 3 discusses the theory and implementation of the Metropolis-Hastings algorithm,including our proposed modification.

·Section 4 presents results comparing the performance of two modified algorithms to the standard version.

·The appendix contains all relevant code and data files.
