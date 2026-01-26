---
layout: default
---

## Hi, I’m Stephen Usselman

I’m a developer interested in backend services, system design, and practical AI integrations.

---

## Skills
- Languages: C++, Python, PHP, Java, JavaScript
- Frameworks and Libraries: Spring Boot, Laravel, Alpine, Tailwind, pandas, scikit-learn, matplotlib
- Tools, Platforms, and APIs: AWS(Elastic Beanstalk, DynamoDB), OpenAI API, SQL, Git, Gradle, Jira, CI/CD

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
