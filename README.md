# Benchmark Kits
This benchmark kits is a test suite designed to provides representative performance measures across three common scenarios of [FATE 1.5.0 (LTS)](https://github.com/FederatedAI/FATE/).

[Read more and see the results of our tests on physical hardware](https://github.com/FederatedAI/FATE/tree/master/cluster-deploy). For descriptions of the test types that we run, see the 
[test requirements section](https://github.com/FederatedAI/FATE/tree/master/cluster-deploy).

The current LTS release of FATE is v1.5.0. All the releases are available [here](https://github.com/FederatedAI/FATE/releases). 


## Highlights
---
### Starndard Dataset

- 1 guest, 1 host

- [5k*200 dataset](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv)

### Large-scale Dataset

- 1 guest, 1 host

- 1m*2k dataset, sample with replacement from [LIBSVM epsilon](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/epsilon_normalized.bz2)

### Multi-host Training

- 1 guest, 30 hosts 

- [5k*200 dataset](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv), with each host 5k\*7(hetero) and each host 60*200(homo)



## Quick Start Guide
---
To get started reproducing all the tests you'll need to first deploy FATE 1.5.0  [here](https://github.com/FederatedAI/FATE/tree/master/cluster-deploy).

1. Clone repo.

        $ git clone git@github.com:FederatedAI/benchmark_kits.git

2. Change directories

        $ cd benchmark_kits/{one_of_the_three_test}/dsl

3. Submit test jobs by fateflow client.

        $ python ${your_install_path}/fate_flow/fate_flow_client.py -f submit_job -d ${dsl} -c ${config}

