---
layout: default
---

## 👋 Hi, I’m Stephen Usselman

I’m a software developer with interests in data analysis, machine learning, and large-language models.

---

## 🧠 Skills
- Languages: C++, Python, PHP, Java, JavaScript
- Machine Learning: Scikit-Learn, Pandas, Matplotlib
- Tools & Frameworks: SQL (MySQL, SQLite), Git, Laravel, Gradle, Jira

---

## 📂 Projects

{% for project in site.projects %}
### {{ project.title }}
{{ project.excerpt }}

[View Project]({{ project.url }})

---
{% endfor %}

---

## 📫 Contact
- GitHub: [Susse001](https://github.com/Susse001)
- Email: zusselman@gmail.com
