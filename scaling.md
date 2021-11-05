# Load Balancing

> The act of distributing network traffic across a set of servers is defined as load balancing, and a load balancer is a server that performs this action.

---

## Table of Contents

- [What is Load Balancing?](#what-is-load-balancing)
- [How Load Balancing works](#how-load-balancer-works)
- [Benefits of Load Balancing](#benefits-of-load-balancing)
- [Load Balancing Algorithm](#load-balancing-algorithm)
  - Round Robin
  - Least Connection
  - IP hashing
- [Scaling](#scaling)
  - Vertical Scaling
  - Horizontal Scaling
  - Difference b/w Vertical and Horizontal Scaling
- [References](#references)

---

### What is Load Balancing?

Present-day high-traffic websites and applications can get the concurrent request for content i.e. text, images, videos, or services by thousand or millions of users or clients. Single servers alone cannot handle these requests therefore, organizations spread their workload across multiple servers. Load balancing prevents server overworking that can cause the server to slow down, drop requests, and even crash.

---

### How Load Balancer Works

Load balancer act as an overseer sitting in front of our server and route client requests to all our servers that are capable of fulfilling those request. The load balancer also takes care of maximizing speed and capacity utilization and ensures that no server is overworked. </br>

There are two types of load balancer

1. Hardware Load Balancer</br>
   Hardwares load balancer are often referred as specialized routers or switches which are deployed in between the servers and the client. It can also be a dedicated system in between the the client and the server to balance the load.

2. Software Load Balancer</br>
   Software load balancers generally implements a combination of one or more scheduling algorithms.

![Load Balancer](https://www.nginx.com/wp-content/uploads/2014/07/what-is-load-balancing-diagram-NGINX-640x324.png)

The load balancer uses a predetermined pattern, known as a load balancing algorithm or method. Different algorithms manage the process using different techniques.

Basics of load balancer

1. A client, such as a browser or an application, receives a request and attempts to connect to a server.
2. A load balancer takes the request and sends it to one of the servers in a server group based on the algorithm's predetermined patterns.
3. The server gets the connection request and uses the load balancer to respond to the client.
4. When the load balancer receives the answer, it matches the client's IP to the IP of the chosen server. The packet with the response is then forwarded.

---

### Benefits of Load Balancing

- **Increase efficiency**: A network's efficiency is affected by overwork. We can redistribute the burden over numerous servers by implementing a load balancing system in our network.
- **Managing Traffic Flow**: Server's daily experiences a high volume of incoming and outgoing traffic. This traffic if not managed can overwork our system and reduce its speed and efficiency. Load Balancer manages traffic flow by spreading the workload over multiple servers.
- **Handling System Failure**: Load balancing provides built-in redundancy by dividing traffic among a set of servers.
  We can immediately divert the load to operating servers if a server fails, minimizing the impact on users.

---

### Load Balancing Algorithm

![Load Balancing Algorithms](https://cdn.hashnode.com/res/hashnode/image/upload/v1625327716741/mN2dgs1em.jpeg?auto=compress,format&format=webp)

1. Round Robin: Round robin load balancing is a simple way to distribute client requests across a group of servers. A client request is forwarded to each server in turn. The algorithm instructs the load balancer to go back to the top of the list and repeats again.

2. Least Connection: A new request is forwarded to the server that has the fewest active client connections.
   Each server's respective computational capacity is taken into account when evaluating which one has the fewest connections.

3. IP Hashing: The IP address of the client is used to determine which server receives the request.

---

### Scaling

> Scalability is the property of a system to handle a growing amount of work by adding resources to the system.

Scaling horizontally and vertically are identical in that they both involve increasing our infrastructure's system resources.
In terms of implementation and performance, there are significant differences between the two.

1. Vertical Scaling/ Scaling Up</br>
   ![Vertical Scaling](https://i.ibb.co/W5K7Wp1/vert.png)</br>
   Vertical scaling refers to scaling by adding more power (e.g. CPU, RAM) to an existing machine. Vertical scaling is easier because logic need no change. Instead, we are simply executing the same code on more powerful machines.

2. Horizontal Scaling/ Scaling Out</br>
   ![Horizontal Scaling](https://i.ibb.co/HG4hLmY/hori.png)</br>
   Horizontal scaling means scaling by adding more servers to your pool of servers. Breaking a piece of logic into smaller chunks so that it can be run in parallel across numerous machines is known as horizontal scaling.

---

### References

- Youtube
  - [Load Balancer by Gavrav Sen](https://www.youtube.com/watch?v=K0Ta65OqQkY)
  - [Load Balance by IBM Technology](https://www.youtube.com/watch?v=sCR3SAVdyCc)
  - [Scaling by Gavrav Sen](https://www.youtube.com/watch?v=xpDnVSmNFX0)
- Blogs
  - [IBM Blog on Load Balancing](https://www.ibm.com/cloud/learn/load-balancing)
  - [Nginx Blog on Load Balancing](https://www.nginx.com/resources/glossary/load-balancing/)
  - [Load Balancing in the Cloud by Derek DeJonghe](https://www.oreilly.com/library/view/load-balancing-in/9781492038009/ch01.html)
  - [Why is load balancing important](https://dealna.com/en/Article/Post/614/Why-is-Load-Balancing-Important)
  - [Load balancing (computing) wikipedia](<https://en.wikipedia.org/wiki/Load_balancing_(computing)>)
  - [Scaling Horizontally vs. Scaling Vertically](https://www.section.io/blog/scaling-horizontally-vs-vertically/)
  - [Scalability wiki](<https://en.wikipedia.org/wiki/Scalability#Horizontal_(scale_out)_and_vertical_scaling_(scale_up)>)

---
