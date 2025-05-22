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
