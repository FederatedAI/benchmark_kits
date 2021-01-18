# Large-scle Dataset

## Data Source
   * [LIBSVM epsilon](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/epsilon_normalized.bz2), build by sampling with replacement from 

## DSL&Conf
   * [HeteroLR](./dsl/hetero_logistic_regression/hetero_lr_normal_dsl.json)

   * [HomoLR](./dsl/homo_logistic_regression/homo_lr_train_dsl.json)

   * [HeteroSBT](./dsl/hetero_secureboost/secureboost_train_dsl.json)
   
   * [HomoSBT](./dsl/homo_secureboost/secureboost_train_dsl.json)


## Deployment


| Role     | Amount | Operating System    | Host Configuration | Storage | Deployment Module |
| -------- | ------ | ------------------- | ------------------ | ------- | ----------------- |
| Exchange | 1 | CentOS 7.2          | 4C8G              | 100G    | Exchange |
| Host | 1 | CentOS 7.2          | 16C32G              | 500G    | clustermanager, rollsite, mysql |
| Host | 1 | CentOS 7.2          | 16C32G              | 500G    | fate_flow, fateboard |  
| Host | 18 | CentOS 7.2         | 16C32G              | 500G    | nodemanger |
| Guest | 1 | CentOS 7.2         | 16C32G              | 500G    | clustermanager, rollsite, mysql |
| Guest | 1 | CentOS 7.2         | 16C32G              | 500G    | fate_flow, fateboard |  
| Guest | 18 | CentOS 7.2        | 16C32G              | 500G    | nodemanger |






## Result


| Algorithm | Time     |  AUC   |  KS   | Precision  | recall |
| --------  | -------- | ----   | ----  | ------     | ------ |
| HeteroLR  | 13:36:28 |  0.769 | 0.381 | 0.788      |  0.789 |
| HomoLR    |  0:33:56 |  0.783 | 0.395 | 0.687      |  0.688 |
| HeteroSBT | 42:35:27 |  0.654 | 0.357 | 0.776      |  0.777 |
| HomoSBT   | 09:08:40 |  0.631 | 0.343 | 0.696      |  0.695 |