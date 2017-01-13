# APUS

This project combines RDMA and Paxos. The raw evaluation results are available here:  
1. [performance on replicated programs](https://docs.google.com/spreadsheets/d/1MvrqbfpKeLdDNBBNahvRja3pGs5ilBgtL7p-QUyhYwk/edit#gid=0)  
2. [consensus latency breakdown](https://docs.google.com/spreadsheets/d/1MvrqbfpKeLdDNBBNahvRja3pGs5ilBgtL7p-QUyhYwk/edit#gid=976109886)  
3. [scalability comparison with DARE](https://docs.google.com/spreadsheets/d/1MvrqbfpKeLdDNBBNahvRja3pGs5ilBgtL7p-QUyhYwk/edit#gid=780560038).
  
OS: Ubuntu 14.04.02 64bit.
## How to run
### Install the dependencies for the program
Use $RDMA_ROOT/RDMA/mk to download and install the dependencies for the program.
### Install the applications
We have prepared all the Makefiles for you in each application's directory.
### Run the evaluation framework
For example, to run Redis hooked by APUS, just go to $RDMA_ROOT/eval and run `python eval.py -f redis-output.cfg`. After that, you can collect the results by `cd current`.
## APUS robustness on exceptional scenarios (leader and non-leader failures)
Evaluated with Redis (12 parallel clients). The ping latency between the client machine and the server machine is 0.082 ms.
![reconfiguration](https://github.com/icdcs17-p256/apus/blob/master/extra-figures/reconfiguration.png)
