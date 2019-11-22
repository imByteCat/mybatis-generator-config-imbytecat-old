# mybatis-generator-config

快速生成 MyBatis 逆向工程，使用 MyBatis Generator。

## 使用方法

使用前建议删除目录中的所有文件以免产生冲突的问题，可以使用项目根目录下的脚本：

```
chmod +x ./clean.sh && ./clean.sh
```

首先，在 `generatorConfig.xml` 中配置 JDBC 连接信息。

然后，需要在 `generatorConfig.xml` 中定义需要生成逆向工程的数据表名称。

运行如果不报错基本上就可以了，刷新一下目录就可以看到生成的文件。

生成的文件一览：

```
# POJO，例如放在项目的 pojo/src/main/java/
src/main/java/cn/shadowcat/pojo/
# Mapper，例如放在项目的 mapper/src/main/java/cn/shadowcat/mapper
src/main/java/cn/shadowcat/mapper/
# Mapper XML，例如放在项目的 api/resources/mappers
src/main/resources/mapper/
```

放完之后会报一个找不到 `MyMapper` 的错，把 `src/main/java/cn/shadowcat/utils/MyMapper.java` 复制到你项目的 `common/src/main/java/cn/shadowcat/utils/MyMapper.java` 就可以了。
