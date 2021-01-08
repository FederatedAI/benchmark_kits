# benchmark_kits


## 1. Starndard Test

- 1 guest, 1 host

- [dsl](./standard/dsl)

- dataset [epsilon_5k](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv)

## 2. Large-scale Test

- 1 guest, 1 host

- sample with replacement, extend the original dataset [LIBSVM epsilon](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/epsilon_normalized.bz2) to 1m*2k(dimensions) 

- [dsl](./large_scale/dsl)

## 3. Multi-host Test

- 1 guest, 30 hosts 

- [dsl](./multi_host/dsl)

- dataset [epsilon_5k](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv)

