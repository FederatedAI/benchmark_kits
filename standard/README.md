# benchmark_kits


## Dataset
[LIBSVM epsilon](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary/epsilon_normalized.bz2)

## DSL&Conf
[HeteroLR](./dsl/hetero_logistic_regression/hetero_lr_normal_dsl.json)

[HomoLR](./dsl/homo_logistic_regression/homo_lr_train_dsl.json)

[HeteroSBT](./dsl/hetero_secureboost/secureboost_train_dsl.json)

[HomoSBT](./dsl/homo_secureboost/secureboost_train_dsl.json)


## Deployment

- ### exchange
| Ip Address                    | Operating System    | Host Configuration | Storage | Deployment Module                                            |
| ----------------------------- | ------------------- | ------------------ | ------- | ------------------------------------------------------------ |
| 192.168.1.1 | CentOS 7.2          | 4C8G              | 100G    | rollsite


- ### host

| Ip Address                    | Operating System    | Host Configuration | Storage | Deployment Module                                            |
| ----------------------------- | ------------------- | ------------------ | ------- | ------------------------------------------------------------ |
| 192.168.0.1 | CentOS 7.2          | 16C32G              | 500G    | clustermanager，rollsite，mysql |
| 192.168.0.2 | CentOS 7.2          | 16C32G              | 500G    | fate_flow，fateboard |
| 192.168.0.3 - 192.168.0.20 | CentOS 7.2          | 16C32G              | 500G    | nodemanger |


- ### guest

| Ip Address                    | Operating System    | Host Configuration | Storage | Deployment Module                                            |
| ----------------------------- | ------------------- | ------------------ | ------- | ------------------------------------------------------------ |
| 192.168.0.21 | CentOS 7.2          | 16C32G              | 500G    | clustermanager，rollsite，mysql |
| 192.168.0.22 | CentOS 7.2          | 16C32G              | 500G    | fate_flow，fateboard |
| 192.168.0.23 -192.168.0.40 | CentOS 7.2          | 16C32G              | 500G    | nodemanger |

