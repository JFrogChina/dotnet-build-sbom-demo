
1，Install the jfrog cli tool in a system with .Net environment

(1),Demo environment uses centos7 operating system, install .net 7.0SDK
···
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
sudo yum update
sudo yum install -y dotnet-sdk-7.0
···

(2),Install JFrog CLI
```
echo "\[jfrog-cli\]" > jfrog-cli.repo;
echo "name=jfrog-cli" >> jfrog-cli.repo;
echo "baseurl=https://releases.jfrog.io/artifactory/jfrog-rpms" >> jfrog-cli.repo;
echo "enabled=1" >> jfrog-cli.repo;
rpm --import https://releases.jfrog.io/artifactory/jfrog-gpg-public/jfrog\_public\_gpg.key
sudo mv jfrog-cli.repo /etc/yum.repos.d/;
yum install -y jfrog-cli-v2-jf;
```
To jump to the [JFrog CLI Installation Docs](#[JFrog CLI installation](https://docs.jfrog-applications.jfrog.io/jfrog-applications/jfrog-cli/install)).

2，Create nuget remote repo in JFrog environment


3，Set up JFrog CLI to connect to the JFrog 
```
jf c add
#Enter a unique server identifier:jfrogname
#JFrog Platform UR:https://jfrog.url.com
#Username and Password :
#Is the Artifactory reverse proxy configured to accept a client certificate? (y/n) [n]?n
```
To jump to the [JFrog CLI Setup Docs](#[JFrog CLI installation](https://docs.jfrog-applications.jfrog.io/jfrog-applications/jfrog-cli/cli-for-jfrog-artifactory/authentication).

4，Set up JFrog CLI .net global environment
```
jf c add
#Enter a unique server identifier:jfrogname
#JFrog Platform UR:https://jfrog.url.com
#Username and Password :
#Is the Artifactory reverse proxy configured to accept a client certificate? (y/n) [n]?n
```
To jump to the [JFrog CLI Nuget build Docs](#[JFrog CLI Nuget Env setup](https://docs.jfrog-applications.jfrog.io/jfrog-applications/jfrog-cli/cli-for-jfrog-artifactory/package-managers-integration#building-nuget-packages)).

5，Clone .net project source code

```
git clone https://github.com/JFrogChina/dotnet-build-sbom-demo.git
```

6，Build .net project with JFrog CLI

```
jf 
```

7，Upload build info to JFrog Server

8，setup JFrog Xray index
（1），Turn on Xray index for  build info 
（2），Run build again

9，Export SBOM report in JFrog Website

![Export SBOM Report](images/example.png)
