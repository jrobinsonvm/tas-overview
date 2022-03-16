## Tanzu Application Service - 
### High Level Overview 

VMware Tanzu Application Service is an opinionated, application-aware platform that provides a rich set of developer tooling and a prepaved path to production to build and deploy software quickly and securely on any compliant public cloud or on-premises vCenter Data Center.


VMware Tanzu Application Service is a modern application platform for enterprises that want to continuously deliver and run microservices or traditional applications across clouds or on-premises.   
[Read more...](https://tanzu.vmware.com/application-service)

<br/>

# A modern runtime for microservices and traditional applications 
 ![image](https://user-images.githubusercontent.com/73367284/158693192-1b5d6762-f88f-4d8c-ab57-d399344c50f8.png)

<br/>

-----

## Day 1 - The Developer Experience 
<br/>

## cf push Automates Developer + Operator workflows 

### Automation, not Support Tickets 

![image](https://user-images.githubusercontent.com/73367284/158693716-e7fdd324-26da-4936-b027-ee2540e66c46.png)

<br/>

<br/>

<br/>

<br/>

<br/>



![image](https://user-images.githubusercontent.com/73367284/158695941-ee0c3804-313d-4dcd-b57e-a6eb64c047e0.png)



### So what happens after you execute the "cf push" cli command?: 
1. Uploads your code
2. Detects and installs required runtime and middleware (“Buildpacks”)
3. Sets up a route (or URL)
4. Creates a load balancing entry
5. Creates SSL termination
6. Creates health monitoring and logging subsystems
7. Starts your app in a healthy state, with the desired number of instances
8. Binds specified backing services

<br/>

<br/>

<br/>


## Let's Compare Deployment Tasks!
### Once code is complete and tested, what do you have to do to get to prod? 


![image](https://user-images.githubusercontent.com/73367284/158695526-b0db8e96-528f-4762-91d7-8e2599ba39e4.png)


<br/>

<br/>


## Dockerfiles:  Typically the most common way developers get started with containers.


###  1. It's a good starting point for most
###  2. Descriptive file specification (YAML)
###  3. It's pretty flexible

<br/>


```
FROM somewhere/ubuntu
MAINTAINER Anonymous Person <Anonymous.Person@email.com>

ENV USER root
ENV PASS aiPeekai0AeZ2meephoolais7doo1thu

RUN \
  apt-get update && \
  apt-get -y install \
          mysql-server-5.5 && \
  rm -rf /var/lib/apt/lists/*

COPY my.cnf /etc/mysql/my.cnf
COPY start.sh start.sh

VOLUME ["/var/lib/mysql"]

RUN rm /usr/sbin/policy-rc.d
CMD ["/start.sh"]

EXPOSE 3306

```

<br/>
<br/>
<br/>


### However containers built using dockerfile are hard to productionize and scale 

#### When dev teams build images differently, they introduce vulnerabilities and complexity


![image](https://user-images.githubusercontent.com/73367284/158699415-c539e7c3-3f09-4921-a8f7-691ff219fa6e.png)


### Image updates
1. Hard to debug, fix and maintain non-standard images across the fleet

### Security posture
2. Challenging to keep container images free of vulnerabilities

### Full stack container audits
3. Hard to uniformly track container dependencies

### IT governance
4. Hard to reinforce software compliance


<br/>

<br/>

### Containers done right with Tanzu

#### Tanzu can be an accelerator for enterprises on their app modernization journey


![image](https://user-images.githubusercontent.com/73367284/158700379-ac2341d1-e710-49ce-9966-db2b79b95747.png)


### Automated image updates
1. Automated container re-base on new code commits, dependency and OS updates

### Improved security posture
2. Easy to track and patch containers with latest CVEs

### Full stack container audits
3. Auditing is a breeze with bundled container metadata 

### Agile IT governance
4. Ability to verify policy enforcements reinforces software compliance


<br/>
<br/>
<br/>

## VMware Tanzu provides comprehensive support for containers 

![image](https://user-images.githubusercontent.com/73367284/158700970-c28cbc6e-27af-46b6-8845-a76d27d1380a.png)


<br/>
<br/>


## Extend Custom Apps with Popular Backing Services 
### Use the Open Service Broker API to manage the lifecycle of databases, caches, and more

![image](https://user-images.githubusercontent.com/73367284/158701336-15d40150-ce4f-432b-9036-f9ee9b069386.png)

<br/>

<br/>


## Tanzu Application Service Deployment Models 

![image](https://user-images.githubusercontent.com/73367284/158701908-daae94b4-69c0-40dc-98fc-41356cc300de.png)

<br/>

<br/>

## Observability within Tanzu Application Service

![image](https://user-images.githubusercontent.com/73367284/158702065-c94d26cf-4ba9-4eb8-82ad-01d2f733fab6.png)

<br/>

 -------
 
 
For more details see [Tanzu Application Service](https://tanzu.vmware.com/application-service)
