Sample JBoss BPM Suite Project
==============================

A simple example of JBoss BPM Suite Project created using v6.1.0

This project is only consist of 1 human task (approval form) to approve the input form.
Following is the process diagram:

![image](https://cloud.githubusercontent.com/assets/3068071/8433529/a0d13d20-1f70-11e5-9e6f-a30a455dfb41.png)

Form when starting the process and approve task are shown below:

![image](https://cloud.githubusercontent.com/assets/3068071/8433673/733661e6-1f71-11e5-8c49-c003559e9311.png)

Please make sure this following repository is exist in your ~/.m2/setting.xml (Windows: C:\Users\username\.m2\setting.xml):

            ```
            <repositories>
                <repository>
                    <id>jboss-ga-repository</id>
                    <name>JBoss GA Tech Preview Maven Repository</name>
                    <url>http://maven.repository.redhat.com/techpreview/all</url>
                    <layout>default</layout>
                    <releases>
                        <enabled>true</enabled>
                        <updatePolicy>never</updatePolicy>
                    </releases>
                    <snapshots>
                        <enabled>false</enabled>
                        <updatePolicy>never</updatePolicy>
                    </snapshots>
                </repository>
            </repositories>
            <pluginRepositories>
                <pluginRepository>
                    <id>jboss-ga-plugin-repository</id>
                    <name>JBoss 6 Maven Plugin Repository</name>
                    <url>http://maven.repository.redhat.com/techpreview/all</url>
                    <layout>default</layout>
                    <releases>
                        <enabled>true</enabled>
                        <updatePolicy>never</updatePolicy>
                    </releases>
                    <snapshots>
                        <enabled>false</enabled>
                        <updatePolicy>never</updatePolicy>
                    </snapshots>
                </pluginRepository>
            </pluginRepositories>
          ```
To run the sample you need to:

1. Login to business-central using user that has `admin` role
2. Clone this project 
3. Add a user with a role `taskadmin` and `user` using following command:
   ```
   ./add-user.sh -a -g admintask,user -u ejlp12 -p Passw0rd!
   ```
4. Login to business-central using username: ejlp12
 
