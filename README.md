
1，Install the jfrog cli tool in a system with .Net environment
Demo environment uses centos7 operating system, install .net 7.0SDK
···
sudo rpm -Uvh https://packages.microsoft.com/config/centos/7/packages-microsoft-prod.rpm
sudo yum update
sudo yum install -y dotnet-sdk-7.0
···

Install JFrog CLI


To jump to the [Installation Docs](#[JFrog CLI installation](https://docs.jfrog-applications.jfrog.io/jfrog-applications/jfrog-cli/install)).

2，Set up JFrog CLI to connect to the JFrog 

3，Create nuget remote repo in JFrog environment

4，Set up JFrog CLI .net global environment

5，Clone .net project source code

```
git clone 
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
