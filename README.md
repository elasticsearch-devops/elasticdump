# elasticdump

## install nodejs
```
第一步：
curl --silent --location https://rpm.nodesource.com/setup_10.x | sudo bash -

第二步：
sudo yum -y install nodejs

如果以上步骤不能安装 最新版 node，执行以下命令后再执行第二步：
sudo yum clean all

如果存在多个 nodesoucre，执行以下命令删除，然后重新执行第一第二步：
sudo rm -fv /etc/yum.repos.d/nodesource*
```

## download es data example
```
elasticdump \
  --input=http://zhenxin.fun:9200/logs-2020.11.24 \
  --output=hdfs:///data/logs-2020.11.24.json \
  --type=data
  --limit=10000
```

## download es mapping example
```
elasticdump \
  --input=http://zhenxin.fun:9200/logs-2020.11.24 \
  --output=hdfs:///mapping/mapping-2020.11.24.json \
  --type=mapping
  --limit=10000
```
