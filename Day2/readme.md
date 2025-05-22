# Why do we set requests and limits for CPU/memory in a production-grade product?
We set CPU and memory requests and limits to make sure each application gets the right amount of resources it needs to run properly. 
The request is the minimum it asks for and the limit is the maximum it can use. 
This helps prevent one app from using too much and affecting others. It keeps the system stable, especially when many apps run together.it is  like making sure everyone at a buffet gets a fair share of food.

# When would a product team apply node affinity in Kubernetes?
A product team uses node affinity when they want to run an app on certain types of machines inside the Kubernetes cluster.
For example, if an app needs a machine with a GPU or extra memory, they can tell Kubernetes to place it there. 
It is  like saying This app should only live in this kind of house.This helps with performance, special hardware needs, or organizing apps better. 
It gives more control over where apps run.

![image](https://github.com/user-attachments/assets/2016e935-d37f-4453-bd39-160cb1365ad8)


# About affinity rules applied
  affinity:
        nodeAffinity:
          requiredDuringSchedulingIgnoredDuringExecution:
            nodeSelectorTerms:
              - matchExpressions:
                  - key: disktype
                    operator: In
                    values:
                      - ssd



The rule is under requiredDuringSchedulingIgnoredDuringExecution, which means the rule must be followed during scheduling, but is ignored if the node’s label changes later. The pod will only run on nodes that have a label with the key disktype. It checks if the value of disktype is in the list of allowed values.
In this case, the allowed value is ssd. So, only nodes labeled like disktype=ssd will be selected.
If there are no such nodes, the pod won’t be scheduled at all.
This helps place pods on suitable hardware, like faster SSD storage.
It’s useful when the app needs specific node features for best performance.
