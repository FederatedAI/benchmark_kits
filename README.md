# Benchmark Kits
This benchmark kits is a test suite designed to provides representative performance measures across three common scenarios of [FATE 1.5.0 (LTS)](https://github.com/FederatedAI/FATE/).

[Read more and see the results of our tests on physical hardware](./test). For descriptions of the test types that we run, see the 
[test requirements section](##Highlights).

The current LTS release of FATE is v1.5.0. All the releases are available [here](https://github.com/FederatedAI/FATE/releases). 


## Quick Start Guide
---
To get started perfroming all the tests you'll need to first deploy  [FATE 1.5.0 (LTS)](https://github.com/FederatedAI/FATE/tree/master/cluster-deploy).

1. Clone repo.

        $ git clone git@github.com:FederatedAI/benchmark_kits.git

2. Change directories

        $ cd benchmark_kits/{one_of_the_three_test}/dsl

3. Submit test jobs by fateflow client.

        $ python ${your_install_path}/fate_flow/fate_flow_client.py -f submit_job -d ${dsl} -c ${conf}

## Highlights
---
1) ### System Requirement

<center>

| Component   | Operating System    | Host Configuration | Storage | Networking
| ----------- | ------------------- | ------------------ | ------- | ---|
| Exchange    |CentOS 7.2           | 4C8G               | 100G    | 100M |
| Guest       |CentOS 7.2           | 16C32G             | 500G    | 100M |
| Host        |CentOS 7.2           | 16C32G             | 500G    | 100M |

</center>

2) ### Test Type

   1） Starndard-size Dataset

   * 1 guest, 1 host

   * [5k*200 dataset](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv)

   2） Large-scale Dataset

   * 1 guest, 1 host

   *  1m*2k dataset, build by sampling with replacement from [LIBSVM epsilon](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/epsilon_normalized.bz2)

   3）Multi-host Federated

   * 1 guest, 30 hosts 

   * [5k*200 dataset(modified)](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv)


