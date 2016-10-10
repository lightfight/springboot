1,右键项目-->>run as -->>maven build -->> name 为 springboot,Goals 为spring-boot:run

2,出现异常：Failed to execute goal org.springframework.boot:spring-boot-maven-plugin:1.4.1.RELEASE:run (default-cli 修改pom.xml文件，增加配置：

```xml

 	<build>
		<plugins>
			<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
				<!-- http://www.cnblogs.com/duyiwuai/p/4792676.html -->
				<!-- http://docs.spring.io/autorepo/docs/spring-boot/1.2.4.RELEASE/maven-plugin/usage.html -->
				<configuration>
					<mainClass>com.lightfight.springboot.SampleController</mainClass>
				</configuration>
			</plugin>
		</plugins>
	</build>

```

3,再次执行1操作

4,访问http://127.0.0.1:8080/hello

