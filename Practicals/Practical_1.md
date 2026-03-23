# Practical 1 – Critical Analysis Report

## Design a URL Shortener System

### 1. Problem Statement Analysis

The document discusses the issue of designing a URL shortening service like TinyURL. A URL shortener changes long URLs into shorter, easier links. When users click the short URL, they are taken to the original long URL.

The main issue with URLs is that they are hard to share, remember, and manage. We need a system that can handle a number of URLs it has to be fast when redirecting and it must always be available and work well with a lot of users. The system also has to store a lot of URL mappings. It has to be good at handling people looking at the mappings and changing them.

The main challenges, with this problem are dealing with a lot of traffic, making a database that is scalable, coming up with URLs that are unique, avoiding problems when two URLs get the same short version and making sure the redirection happens fast by using something called caching with the URL mappings and the system.

### 2. Analysis of Author’s Solution

The author suggests a system plan that includes API points, database storage, caching, hashing and a special code conversion for making URLs.

The system has two main APIs:
1. POST API for creating a short URL
2. GET API for redirecting short URL to long URL

For URL shortening, the system makes a unique ID and changes it into a short string using a special code. This code uses numbers and letters and yhe URL remains short.

For redirecting to the URL the system first checks its quick memory. If it finds the information it takes the user right away. If not it gets the URL from its storage and then redirects user.

The author also discusses two hashing approaches:
* Hash + collision resolution
* Base 62 conversion

The author chooses Base 62 conversion because it avoids collision problems and is simpler to implement.

The solution also includes load balancers, database storage, caching, and distributed ID generation to support scalability and high availability.

### 3. My Understanding

From my understanding, the main goal of the system is to efficiently convert long URLs into short URLs and redirect users quickly when they use the short link. The system must handle very large data and traffic, so scalability and performance are very important.

I learned that system design involves multiple components such as APIs, databases, caching, hashing algorithms, load balancers, and distributed systems. I also understood the importance of using caching because read operations are much higher than write operations.

This topic is related to software engineering concepts such as system architecture, scalability, database design, distributed systems, REST APIs, and caching mechanisms.

### 4. Confusions

Some parts that were slightly confusing include the distributed unique ID generator and how it works in a distributed environment. I also want to understand more about bloom filters and how they help reduce database queries.

Another area that I would like to explore further is database sharding and replication, as these are important for scaling large systems.

### 5. Further Topics to Explore

After reading this document, I would like to explore the following topics:

* Distributed systems
* Load balancing
* Database sharding and replication
* Caching systems (Redis, Memcached)
* Bloom filters
* Rate limiting
* System scalability and performance optimization

### 6. Brief Summary of Critical Analysis

In conclusion, the document explains how to design a scalable URL shortening system that can handle a large number of requests and store billions of URL mappings. The author proposes a system using REST APIs, database storage, caching, load balancers, and Base 62 encoding for generating short URLs. The solution is scalable, efficient, and practical for real-world applications. This analysis helped me understand how large-scale systems are designed and the importance of scalability, caching, and distributed architecture in modern software systems.
