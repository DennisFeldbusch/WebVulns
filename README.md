# Writeup of Web Vulns

## [XSS (Cross-Site-Scripting)](https://youtu.be/EoaDgUgS6QA)

Injecting Code into a Website.

[Cheat Sheet](https://portswigger.net/web-security/cross-site-scripting/cheat-sheet)

### reflected XSS

Reflected XSS occurs when user input is immediately returned by a web application in an error message, search result, or any other response that includes some or all of the input provided by the user as part of the request, without that data being made safe to render in the browser, and without permanently storing the user provided data.

```
<script>alert(1)</script>
```

### stored XSS

server-sided

The XSS is stored in a db or so. Everytime this data is called the code should be executed. 
### local XSS

As defined by Amit Klein, who published the first article about this issue [1], DOM Based XSS is a form of XSS where the entire tainted data flow from source to sink takes place in the browser, i.e., the source of the data is in the DOM, the sink is also in the DOM, and the data flow never leaves the browser. For example, the source (where malicious data is read) could be the URL of the page (e.g., document.location.href), or it could be an element of the HTML, and the sink is a sensitive method call that causes the execution of the malicious data (e.g., document.write).”

## IDOR (Insecure-Direct-Object-Reference)

[video](https://youtu.be/rloqMGcPMkI)

## CSRF (Cross-Site-Request-Forgery)

[video](https://youtu.be/eWEgUcHPle0)

## SQLi (SQL-Injection)

## XXE (XML-External-Entity)

Using XML Entities to inject malicious code.

Nice [video](https://youtu.be/gjm6VHZa_8s) by pwnfunction on that subject.
