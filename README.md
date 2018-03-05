# docker-dev-env
Multimachine docker dev and test environment

# Initial setup

Clone the repo:
```bash
$ git clone https://github.com/qba73/docker-dev-env.git
$ cd docker-dev-env
```

Spin up the cluster:
```bash
$ vagrant up
```

SSH to each machine:
```bash
$ vagrant ssh master
$ vagrant ssh node1
$ vagrant ssh node2
```
