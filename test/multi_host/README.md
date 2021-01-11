# Multi-host Federated

## Data Source
   * [epsilon_5k(Modified)](https://github.com/FederatedAI/FATE/blob/master/examples/data/epsilon_5k_hetero_guest.csv), with each host 5k\*7d(hetero) and 60*200d(homo)

## DSL&Conf
   * [HeteroLR](./dsl/hetero_logistic_regression/hetero_lr_multi_host_conf.json)

   * [HomoLR](./dsl/homo_logistic_regression/homo_lr_multi_host_conf.json)

   * [HeteroSBT](./dsl/hetero_secureboost/secureboost_train_multi_conf.json)

   * [HomoSBT](./dsl/homo_secureboost/secureboost_train_multi_conf.json)


## Deployment


| Role     | Amount | Operating System    | Host Configuration | Storage     | Deployment Module |
| -------- | ------ | ------------------- | ------------------ | ------- | -------- |
| Exchange | 1 | CentOS 7.2          | 4C8G              | 100G    | Exchange |
| Host | 30 | CentOS 7.2          | 16C32G              | 500G    | clustermanager, nodemanger, rollsite, fate_flow, fateboard, mysql |
| Guest | 1 | CentOS 7.2           | 16C32G              | 500G    | clustermanager, nodemanger, rollsite, fate_flow, fateboard, mysql |