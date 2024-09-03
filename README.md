# best-practices

DevOps最佳实践记录

## Golang

> Go(程序间的协同工作,要什么功能就加上什么)

### goweb

> model: gorm
> config: vipper
> router: gin
> cmd: spf13/cobra
> ...



- 目录

```bash
.
|-- cmd
|   |-- generate
|       |-- generate.go	# Gen生成代码的配置,包含main函数，执行其即可完成gen生成代码步骤
|-- config
|   |-- config.go # 存储相关的数据库DSN (或者使用viper包管理配置文件,读取 `config.yaml`,在config.yaml配置文件中，一般来说，建议使用小写字母。使用小写字母可以增加配置文件的一致性和可读性，并且有助于避免因为大小写不一致而导致的错误。)
|-- dal # 数据访问层（Data Access Layer）
|   |-- db.go # 实现具体的数据库连接等操作
|   |-- model # 描述与数据库表对应的结构体
|   |   |-- dynamic.go # 自定义动态SQL查询接口,在generate.go中通过ApplyInterface添加为指定表添加自定义方法,Gen将对其进行解析，并为应用的结构生成查询API
|   |   |-- model.go # 自定义结构体
|   |   |-- tablename.gen.go # Gen生成的单个表的结构体
|   |-- query # 查询方法
|       |-- gen.go # Gen生成的通用查询代码
|       |-- tablename.gen.go # Gen生成的单个表字段和相关的查询代码
|-- go.mod
|-- go.sum
|-- handler # 业务逻辑,处理器
|   |-- handler.go 
|-- main.go # 程序入口
|-- route # 路由
    |-- route.go
```



## ES/TS

### react

```yaml
主题配色: 主白辅蓝,参照 google analytics
```



## Python

