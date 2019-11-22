# mybatis-generator-config

快速生成 MyBatis 逆向工程，使用 MyBatis Generator。

## 使用方法

生成的文件一览：

```
src/main/java/cn/shadowcat/pojo/  # POJO
src/main/java/cn/shadowcat/mapper/  # Mapper
src/main/resources/mapper/  # Mapper XML
```

使用前建议删除目录中的所有文件以免产生冲突的问题，可以使用项目根目录下的脚本：

```
chmod +x ./clean.sh && ./clean.sh
```

首先，在 `generatorConfig.xml` 中配置 JDBC 连接信息。

然后，需要在 `generatorConfig.xml` 中定义需要生成逆向工程的数据表名称。
