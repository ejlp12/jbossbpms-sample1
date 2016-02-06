Sample JBoss BPM Suite Project
==============================

A simple example of JBoss BPM Suite Project created using v6.1.0 (Can be imported and run in 6.2)

This project is only consist of 1 human task (approval form) that can be viewed by user in group `taskadmin` to approve the input.

Following is the process diagram:

![image](https://cloud.githubusercontent.com/assets/3068071/8433529/a0d13d20-1f70-11e5-9e6f-a30a455dfb41.png)

![image](https://cloud.githubusercontent.com/assets/3068071/12863375/0f036d5c-cca7-11e5-824b-c670ffc41dd0.png)

Starting the process form and approve task form are shown below:

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

1. Login to business-central using a user that has `admin` role
2. Clone this project (Authoring > Administration > Repositories > Clone Repository)
3. Deploy the project
4. Add a user with a role `taskadmin` and `user` using following command in $JBOSS_BPMS_HOME/bin directory:

   ```
   ./add-user.sh -a -g taskadmin,user,manager -u ejlp12 -p Passw0rd!
   ```
5. Login to business-central using username: `ejlp12` and password `Passw0rd!`
6. Start the process definition `simple_proc`
 
