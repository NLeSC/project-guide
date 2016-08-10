# Introduction
A web-application is a highly customizable, cross-platform way to create an application.
Depending on the project a web-application can be a good choice over a native application,
especially when data is stored on a remote server, or when computation is done at a remote site.  

A web-application consists of three cornerstone technologies:
  * [HTML (HyperText Markup Language)](web_development/html.md) - The markup language for creating web-pages.
  * [CSS (Cascading Style Sheets)](web_development/css.md) - The stylesheet language which describes the presentation of pages written in HTML.
  * [JavaScript](web_development/javascript.md) - JavaScript is the de-facto standard scripting language for the web and allows for manipulation of nearly anything in the web-page.

## Getting Started
Plain HTML, CSS and JavaScript will suffice for small web-applications.
However, when creating larger applications using frameworks and pre-processors can be very benificial.
Using pre-processers allows you to write simpler code that is easier to maintain.
Using frameworks gives you access to powerful tools, without having to re-invent the wheel.

Frameworks and pre-processors are discussed in the respective pages for HTML, CSS and JavaScript.

To write a web-application you need a browser, a text-editor and a server to serve the html pages.
### Browser
There are many browsers out there. Keep in mind that they do not all
always implement the standards exactly and quirks happen.
For development a browser that has a built-in debugger is recommended, all major browsers currently have one.

Major Browsers:
* [Firefox (Mozilla)](https://en.wikipedia.org/wiki/Firefox)
* [Chrome (Google)](https://en.wikipedia.org/wiki/Google_Chrome)
* [Edge (Microsoft)](https://en.wikipedia.org/wiki/Microsoft_Edge)
* [Safari (Apple)](https://en.wikipedia.org/wiki/Safari_(web_browser))
* [Opera](https://en.wikipedia.org/wiki/Opera_(web_browser))

### IDE
There are many choices for IDE here are some examples that are made for web-development:
* JetBeans [WebStorm](https://www.jetbrains.com/webstorm/)
* Github [Atom](http://atom.io)
* Microsoft [Visual Studio Code](https://code.visualstudio.com)
* Adobe [Brackets](http://brackets.io/?lang=en) 

### Server
There are several servers for html, with several choices both for development and deployment.

The following are the three major web servers for production environments:
* [Apache2](https://httpd.apache.org/) - The goal of this project is to provide a secure, efficient and extensible server that provides HTTP services in sync with the current HTTP standards.
* [Nginx](https://www.nginx.com/resources/wiki/) - NGINX is a free, open-source, high-performance HTTP server and reverse proxy.
* [IIS](http://www.iis.net/) - Internet Information Services (IIS) for Windows® Server is a flexible, secure and manageable Web server for hosting anything on the Web.

When developing a web application a smaller server is usually more convenient.
For instance the [http-server package](https://www.npmjs.com/package/http-server) from the npm repositories is a good start.

## Frameworks
At NLeSC building web applications is usually done using the [angular](https://angular.io/) framework.