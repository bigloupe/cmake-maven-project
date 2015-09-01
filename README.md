# cmake-maven-project [![Build Status](https://travis-ci.org/ksclarke/cmake-maven-project.png?branch=master)](https://travis-ci.org/ksclarke/cmake-maven-project)

A git copy of the cmake-maven-project hosted in Git on [BitBucket](https://bitbucket.org/cowwoc/cmake-maven-project) 

The cmake-maven-project allows CMake projects to be compiled using Maven.

For more details, visit the project's [Google Code page](https://bitbucket.org/cowwoc/cmake-maven-project).

Support CMAKE version <b>3.2.2-b1</b>

Usage Maven :

```xml
<plugin>
				<groupId>com.googlecode.cmake-maven-project</groupId>
				<artifactId>cmake-maven-plugin</artifactId>
				<!-- Support new generator like Visual Studio 12 2013, Visual Studio 14 2015 -->
				<version>3.2.2-b1</version>
				<executions>
					<execution>
						<id>cmake-generate-launcher</id>
						<goals>
							<goal>generate</goal>
						</goals>
						<configuration>
							<sourcePath>${project.basedir}/launcher/${cmake.launcher}</sourcePath>
							<targetPath>${project.basedir}/launcher/${cmake.launcher}</targetPath>
							<generator>Visual Studio 12 2013</generator>
						</configuration>
					</execution>
					<execution>
						<id>cmake-compile</id>
						<goals>
							<goal>compile</goal>
						</goals>
						<configuration>
							<projectDirectory>${project.basedir}/launcher/${cmake.launcher}</projectDirectory>
						</configuration>
					</execution>
				</executions>
			</plugin>
'''
