---
title: ideating/documentation
layout: post
description: ideas for everyhting sprint 1 related
permalink: /spt1
author: Jade
showReadingTime: true
---



By the end of this assignment, you will:

 - Master POJO Design — Understand how Plain Old Java Objects form the foundation of both the AP CSA exam and modern frameworks like Spring
 - Implement Data Persistence — Use JPA and SQLite to reliably store and retrieve your data object
 - Build a REST API — Create Spring Boot endpoints that expose your data with proper HTTP methods (GET, POST, PUT, DELETE)
 - Design Full-Stack Architecture — Connect a backend API to a frontend (GitHub Pages OR Thymeleaf admin page)
 - Portfolio & Exam Preparation — Document your work in a blog that demonstrates OOP mastery and prepares you for AP CSA exam

# DATA OBJECT DOMAIN MODEL
what is my team per se
my team is like
backend
we have admin panel
what coudl be useful?

i find things useful

i find that simple infographics and ui screen useful

i make

# a dedicated chart with graphics of different users, their schools, their github and student ids, as well as name and join date. this chart will differentiate between students as well as guest accounts added through the mentors

therefore i choose option b

Design your POJO based on your data object

    Identify all required fields (e.g., id, name, description, createdAt, updatedBy)
    Choose appropriate data types (primitives, Strings, LocalDateTime, etc.)
    Consider relationships (e.g., a Project belongs to a Team)


required fields:
id
name
createdAt
email

data types:
localdatetime
strings

relationships:
my project should tie into the admin panel and be a useful tool for administrators when dealing with account problems/reset passwords and similar.

Lombok Annotations:

https://dev.to/gianfcop98/10-lombok-annotations-every-java-developer-should-know-pcd

review review review

https://medium.com/javarevisited/all-the-16-lombok-annotations-explained-in-a-4-minute-article-926f71934ec6


this is my pojo
```java
import jakarta.persistence.*
import lombok.*

@Entity
@Data
@NoArgsConstructor
@AllArgsConstructor

public class POJO {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String name;
    private String email;
    private String school;
    private String studentID;
    private String githubUsername;
    private LocalDateTime createdAt;
    private String accountType;

}
```



