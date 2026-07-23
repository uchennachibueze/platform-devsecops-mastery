## Linux
1. What is the difference between a process and a thread?
- Ans: The difference between a process and a thread is that, a process is one single unit of a task being executed by a CPU while a thread is a combination of multiple process being executed by a CPU in parallel.

2. What happens after you type a command into a Linux shell and press Enter?
- Ans: The shell interpretes, executes the command and possibly returns an output depending on what the commands asked the shell to do.

3. What is the difference between SIGTERM and SIGKILL?
- Ans: SIGTERM kills the process without force while SIGKILL kills the process forcefully.

4. What is a file descriptor?
- Ans: A file descriptor is an annotation used to describe a file

5. How would you investigate a Linux server with high CPU usage?
- Ans: I would use top command to see the processes or apps running on get details into the CPU consumption

## Networking
6. Explain what happens when you enter https://example.com into to browser.
- Ans: When I enter the url you provided, the webpage opened which shows the DNS was able to resolve and functional. I expected it would give a 400 or 500 error but it did not

7. What is the difference between DNS, TCP, TLS and HTTP?
- Ans: DNS which stand for Domain Name System is a system of catalogue that contains or stores domain names. A public DNS ensures that there are no domain name conflicts globally.
While a TCP which stands for Transfer Control Protocol is a protocol used in networking to communicate over the network when transferring data which could be text, files, database etc across the network. TLS which is Transport Layer Secured, is a networking layer in the networking OSI model which allows data to be transferred or transported securely across the network. Lastly, HTTP stands for hypertext transfer protocol is a networking protocol or technology that is used to transport or transfer data over the internet/web.

8. What causes a 502 Bad Gateway response?
- Ans: Different things could cause 502 response ranging from failing backend, gateway being unresponse or down or firewall rules blocking access from client to server. 

9. What is NAT?
- Ans: NAT which stands for Networking Address Translator is a technology used to translate and correctly map IP addresses to specific domain names. 

10. How would you investigate an application that works locally but cannot be reached from another server?
- Ans: I would start by looking at the networking configuration if the server where the application is running can be reached outside it by pinging the server. If I get a response, it means that the other server can reach the server where the application is running, then I would start looking at the firewall rules if there is a rule that blocks access on the port serving the application. If it is a firewall problem, I'll expose it to be reachable by the other server. Overall, I will look at how the application server has been configured and tackle it from the networking level as this is a network related problem. 

## Git
11. What is the difference between a branch, tag and commit?
- Ans: A branch is a folder in git while a tag is a label to identify different variants of a branch while a commit is a fingerprint used to identify changes that goes through git.

12. What is a detached HEAD?
- Ans: A detached HEAD is one that no longer has a parent commit

13. What does git fetch do that git pull does not?
- Ans: git fetch makes a remote branch locally available while git pull makes changes available remotely in a locally existing branch

14. What is a refspec?
- Ans: A refspec is a reference of a git commit hash

15. How would you recover a commit that appears to have been lost after a reset?
- Ans: I would run git log and do a git reset to that commit

## Python
16. What is the difference between a list, tuple, set and dictionary?
- Ans: A list is mutable, while a tuple is immutable, while a set I think is a list of tuples and a dictionary is list of lists

17. What is the difference between an exception and an error return value?
- Ans: An exception can be customized to provide detail into the error while a return value may not be detailed

18. What does a python virtual environment isolate?
- Ans: A python virtual environment isolates the installed packages from being globally present in the entire system to avoid conflicts with existing packages of different versions

19: Explain what this code does:
```
def filter_items(items, predicate):
    return [item for item in items if predicate(item)]
```
- Ans: A function called filter_items takes two parameters and return the item filtered from the items list if predicate contains item is true

20. What tests would you write for that function?
- Ans: I don't know

## Containers and Kubernetes
21. What makes a container different from a virtual machine?
- Ans: A container is portable and can run on any platform regardless the OS while a virtual machine would not be able to do that it, it is more OS specific

22. What are Linux namespaces and control groups?
- Ans: I don't know

23. What is the difference between a Kubernetes Pod, Deployments and Service?
- Ans: A pod is the smallest unit of kubernetes and it contains the container, while deployment is a collection of pods and service is collection of deployments

24. What happens internally after running:
```
kubectl apply -f deployment.yaml
```
- Ans: The existing deployment is forcefully overwritten by the new deployment and the pods are restarted forcefully

25. How would you investigate a Pod in CrashLoopBackOff?
- Ans: I would check that docker image exists. Mostly CrashLoopBackOff means that the docker image cannot be reached by the engine and often get stuck in a loop back

## Terraform, cloud and security
26. What is stored in Terraform state, and why must it be protected?
- Ans: Every metadata about the infrastructure is stored in the terraform state file and it must be protected because it represents the data about the infrastructure that has been provisioned. It is likened to a datastore about the infrastructure, if it is destroyed or corrupted, their is no way for the terraform engine to get the information about the infrastructure and what to do

27. What is the difference between authentication and authorization?
- Ans: Authentication is checking the identity of the user and granting them access while authorization is checking if the user has permission to access the resource they are requesting access to

28. What is least privilege?
- Ans: Least privilege is a term used to describe how much permission a user has in a system

29. What is an SBOM?
- Ans: I don't know. I have heard of that but haven't really used it but I think has something to do with bill of materials

30. Where should security controls exist in a software-delivery pipeline?
- Ans: It should exist in every stage of a software-delivery pipeline. From developement down to final stage