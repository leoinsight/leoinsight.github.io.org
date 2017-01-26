## Skills

```
Programming Language — Java, Python

Web — HTML/5, CSS/3, JavaScript, JSON, REST, jQuery

Development Tools — Eclipse, Git, SVN

Framework — Spring, JPA, MyBatis
```

## JPA

### @OneToMany

Member to Phone

* Member (seq, name)
* Phone (seq, no, member_id)

```java
@Entity
public class Member {
	
	@Id
	@GeneratedValue(strategy=GenerationType.AUTO)
	private int seq;
	
	private String name;

	@OneToMany(fetch=FetchType.EAGER, cascade=CascadeType.ALL)
	@JoinColumn(name="member_id")
	private Collection<Phone> phones;

	public Member() {}
  (...)
}

@Entity
public class Phone {

	@Id
	@GeneratedValue(strategy=GenerationType.AUTO)
	private int seq;
	private String no;
	/*@Column(name="member_id")
	private int memberId;*/
	
	public Phone() {}
  (...)
}
```

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/leoinsight/leoinsight.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
