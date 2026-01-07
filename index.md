---
layout: default
---

## Hi, I’m Stephen Usselman

I’m a software developer with interests in data analysis, machine learning, and large-language models.

---

## Skills
- Languages: C++, Python, PHP, Java, JavaScript
- Machine Learning: Scikit-Learn, Pandas, Matplotlib
- Tools & Frameworks: Alpine.js, Tailwind.css, SQL, Git, Laravel, Gradle, Maven

---

## Projects

{% for project in site.projects %}
### {{ project.title }}
{{ project.excerpt }}

[View Project]({{ project.url }})

---
{% endfor %}

---

##  Resume

You can view or download my resume below.

[Download Resume (PDF)](/assets/resume/Stephen_Usselman_resume.pdf)  
[View Resume Page](/resume/)

## Contact
- GitHub: [Susse001](https://github.com/Susse001)
- Email: zusselman@gmail.com
