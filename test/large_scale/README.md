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

