# mybatis-generator-config-imbytecat-old
使用 MyBatis-Generator 快速生成 MyBatis 逆向工程。
**[请查看最新代码：imByteCat/mybatis-generator-config-imbytecat](https://github.com/imByteCat/mybatis-generator-config-imbytecat)**

## 使用方法

使用前建议删除目录中的所有已生成的逆向工程文件以免产生冲突的问题，可以使用项目根目录下的脚本：

```shell
sh clean.sh
```

首先，在 `generatorConfig.xml` 中配置 JDBC 连接信息。

然后，需要在 `generatorConfig.xml` 中定义需要生成逆向工程的数据表名称。

运行如果不报错基本上就可以了，刷新一下目录就可以看到生成的文件。

生成的文件一览：

```
# POJO，例如放在你项目的 pojo/src/main/java/
src/main/java/cn/shadowcat/pojo/

# Mapper，例如放在你项目的 mapper/src/main/java/com/github/mapper
src/main/java/com/github/mapper/

# Mapper XML，例如放在你项目的 api/resources/mappers
src/main/resources/mapper/
```

完成之后会抛出找不到 `MyMapper` 的异常，把 `src/main/java/com/github/utils/MyMapper.java` 复制到你项目的 `common/src/main/java/com/github/utils/MyMapper.java` 就可以了。
