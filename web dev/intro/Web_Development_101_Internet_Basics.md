# Web Development 101: Internet and Web Basics

> **Web Wing — First Class**  
> **Audience:** Complete beginners  
> **Goal:** Understand what the web is and how websites work before writing code.

## Contents

1. [What Is the Internet?](#1-what-is-the-internet)
2. [What Is the Web?](#2-what-is-the-web)
3. [How Does a Website Work?](#3-how-does-a-website-work)
4. [Client and Server](#4-client-and-server)
5. [Frontend, Backend, and Database](#5-frontend-backend-and-database)
6. [HTTP and HTTPS](#6-http-and-https)
7. [Requests and Responses](#7-requests-and-responses)
8. [URLs, Routes, and Endpoints](#8-urls-routes-and-endpoints)
9. [What Is an API?](#9-what-is-an-api)
10. [Useful HTTP Methods and Status Codes](#10-useful-http-methods-and-status-codes)
11. [Web Development Technologies](#11-web-development-technologies)
12. [Browser Developer Tools](#12-browser-developer-tools)
13. [What Are Git and GitHub?](#13-what-are-git-and-github)
14. [A Beginner's Learning Path](#14-a-beginners-learning-path)

---

## 1. What Is the Internet?

The **Internet** is a worldwide network that connects computers, phones, servers, and other devices so they can communicate.

We use the internet to:

- Browse websites
- Send messages and emails
- Make video calls
- Play online games
- Share files
- Use online applications

Think of the internet as a huge network of roads. Information travels between connected devices using these networks.

### What is a protocol?

A **protocol** is a set of rules that devices follow to communicate. You do not need to learn all the technical details today. Just remember that devices need shared rules to exchange information correctly.

---

## 2. What Is the Web?

The **World Wide Web**, usually called **the web**, is a collection of websites and web pages that we access over the internet, usually through a browser.

Examples include Google, Wikipedia, GitHub, and your college website.

- **Web page:** One page, such as a college's Contact page.
- **Website:** A collection of related web pages.
- **Web application:** A website that lets you do things, such as send messages, edit documents, or manage tasks.
- **Browser:** An application such as Chrome, Safari, Firefox, or Edge that lets you access websites.

### Internet vs Web

The internet is the network; the web is one service that uses it. Email, online games, and other services also use the internet.

---

## 3. How Does a Website Work?

Imagine typing `https://example.com` into your browser and pressing Enter.

1. The browser reads the website address.
2. It connects to the computer or service hosting the website.
3. The browser sends a **request** asking for the page.
4. The server sends back a **response**.
5. The browser uses the returned files and data to display the page.

A website may load additional files, such as styles, images, and JavaScript, to make the page look and behave as intended.

```text
You enter a website address
           |
           v
      Web browser
           |
           | Request
           v
        Server
           |
           | Response
           v
      Web browser
           |
           v
    Website appears
```

This is the basic idea behind loading a website. Real websites may involve more steps, but you can learn those later.

---

## 4. Client and Server

### Client

A **client** is the app or device that requests something. When you open a website, your browser acts as the client.

### Server

A **server** is a computer or software that responds to requests and provides resources or services.

For example, when you open a college website:

- Your browser is the **client**.
- The computer or service providing the website is the **server**.
- The browser requests the page, and the server responds with the content.

```text
CLIENT                         SERVER
Browser  ---- Request ------>  Website service
Browser  <--- Response -----   Website service
```

These words describe roles in communication. You do not need to know how servers are physically set up yet.

---

## 5. Frontend, Backend, and Database

Many web applications have three main parts.

### Frontend

The **frontend** is the part of a website that users see and interact with.

Examples: headings, buttons, menus, forms, images, and page layout.

Main technologies:

- **HTML:** gives the page its structure.
- **CSS:** controls how the page looks.
- **JavaScript:** adds behaviour and interactivity.

### Backend

The **backend** works behind the scenes. It processes requests and applies the application's rules.

Examples: checking login details, processing an order, or deciding which information a user can access.

Backend technologies include Node.js, Java, Python, PHP, and others.

### Database

A **database** stores information that an application needs to keep, such as user profiles, products, posts, or student records.

Examples of database systems include PostgreSQL, MySQL, and MongoDB.

### How they work together

Imagine a student checking their results on a college portal:

1. The frontend displays the page.
2. The browser asks the backend for the student's results.
3. The backend retrieves the required information from the database.
4. The backend sends a response to the browser.
5. The frontend displays the results.

```text
User
  |
  v
Frontend (what the user sees)
  |
  v
Backend (processes the request)
  |
  v
Database (stores information)
```

**Remember:** Frontend is what users interact with; backend handles the behind-the-scenes logic; a database stores information.

---

## 6. HTTP and HTTPS

**HTTP** is a set of rules that browsers and web servers use to exchange requests and responses.

**HTTPS** is the secure version of HTTP. It helps protect information while it travels between the browser and the website.

You can often see the difference in a website address:

- `http://example.com`
- `https://example.com`

For now, remember: **HTTP is used for web communication, and HTTPS adds protection to that communication.**

---

## 7. Requests and Responses

A **request** is a message the browser sends to a server. A **response** is the message the server sends back.

For example, when you open a product page:

- The browser requests the page or product information.
- The server processes the request.
- The server responds with a page or data.
- The browser displays the result.

A response often includes a **status code**, which gives a quick indication of what happened.

You do not need to memorise the format of a full HTTP message for your first class. The important concept is:

**Client sends a request → server sends a response.**

---

## 8. URLs, Routes, and Endpoints

### URL

A **URL** is a web address. For example:

`https://www.example.com/products`

Here, `https` indicates the communication scheme, `www.example.com` is the host name, and `/products` is the path.

### Route

A **route** is a rule in a website or backend that determines what should happen when a particular path is requested.

### Endpoint

An **API endpoint** is an address and operation that a program can use to request data or perform an action.

Examples:

- `GET /api/products` — request a list of products.
- `GET /api/products/5` — request details for product 5.

You will see routes and endpoints more often when you start backend development. For now, think of a URL as an address and an endpoint as a way for software to access a particular service or piece of data.

---

## 9. What Is an API?

**API** stands for **Application Programming Interface**. It defines how one piece of software can communicate with another.

A web API often lets a frontend request information from a backend.

For example, a weather app may ask a weather service for the current temperature. The service sends back data, and the app displays it.

```text
Frontend / App  ---- asks for data ---->  API / Backend
Frontend / App  <--- sends back data ---  API / Backend
```

### What is JSON?

**JSON** is a common format for sending structured data between programs. It looks like this:

```json
{
  "name": "Aarav",
  "department": "CSE"
}
```

The application can read this data and display the student's name and department. You will learn more about JSON when you start working with APIs.

---

## 10. Useful HTTP Methods and Status Codes

You only need a few common examples to begin with.

### HTTP methods

| Method | Simple meaning | Example |
|---|---|---|
| `GET` | Get information | View a list of products |
| `POST` | Send information | Submit a form |
| `PUT` / `PATCH` | Update information | Edit a profile |
| `DELETE` | Delete information | Remove a saved item |

### Status codes

| Code | Meaning | Example |
|---|---|---|
| `200` | OK — request succeeded | Page or data loaded |
| `404` | Not Found | Page does not exist |
| `500` | Server Error | Something went wrong on the server |

These are just common examples. You can learn the other methods and codes when you need them.

---

## 11. Web Development Technologies

Web development involves different technologies that work together.

| Technology | What it is used for |
|---|---|
| HTML | Structure and content of a page |
| CSS | Styling and layout |
| JavaScript | Interactivity and behaviour |
| Node.js | Run JavaScript outside the browser, often for backend development |
| Express | A framework commonly used to build Node.js web servers and APIs |
| PostgreSQL / MySQL / MongoDB | Store and manage application data |
| Git | Track changes in code |
| GitHub | Host code and collaborate with others |

You do **not** need to learn all these tools at once. HTML, CSS, and JavaScript are a good starting point for building your first web pages.

### A simple view of the web development areas

```text
Web Development
├── Frontend
│   ├── HTML
│   ├── CSS
│   └── JavaScript
├── Backend
│   ├── Server-side code
│   └── APIs
├── Database
│   └── Stores application data
└── Tools
    ├── Git
    └── GitHub
```

Git and GitHub are useful across frontend and backend work; they are not part of the frontend/backend split itself.

---

## 12. Browser Developer Tools

Browsers have built-in tools called **Developer Tools** or **DevTools**. Developers use them to inspect and debug websites.

For a first look:

1. Open a website in Chrome.
2. Right-click the page and choose **Inspect**.
3. Find the **Elements** panel to look at the page's HTML and CSS.
4. Find the **Console** panel to view messages and errors.
5. Find the **Network** panel to see requests made while the page loads.

### Small activity

In the Console, type:

```javascript
console.log("Hello, Web Wing!");
```

Press Enter. The browser should display the message. This is a simple way to see that JavaScript can run in the browser.

You can experiment with DevTools, but changes made there are usually temporary and do not edit the original website's code.

---

## 13. What Are Git and GitHub?

**Git** is a tool that tracks changes to your code. It lets you review earlier versions and work safely as your project changes.

**GitHub** is an online platform where people can store Git repositories and collaborate on projects.

A simple way to remember the difference:

- **Git:** the version-control tool.
- **GitHub:** a platform for hosting and sharing Git projects.

You can learn Git while building your first small website.

---

## 14. A Beginner's Learning Path

A practical starting order is:

1. **HTML** — create the structure of a page.
2. **CSS** — make the page look good.
3. **JavaScript** — add interaction.
4. **Git and GitHub** — save versions of your work and share projects.
5. **HTTP and APIs** — understand how websites exchange data.
6. **Backend development** — build server-side logic and APIs.
7. **Databases** — store and retrieve information.
8. **Deployment** — put your website online.

Start small. Build a personal introduction page, then a portfolio, then a project that uses an API. You do not need to learn a framework such as React on day one.

---

## The Main Ideas to Remember

- The **internet** connects devices and networks around the world.
- The **web** is a service that lets us access websites through browsers.
- A **client** sends a request; a **server** sends a response.
- The **frontend** is the user-facing part of a website.
- The **backend** handles logic behind the scenes.
- A **database** stores information.
- **HTTP/HTTPS** are used for communication between browsers and web servers.
- An **API** lets software components communicate.
- **HTML, CSS, and JavaScript** are the main technologies to start learning for frontend development.
- **Git and GitHub** help you track and share your code.

**Suggested next step:** Build a tiny HTML page and open it in your browser. Once you can see your own page, learning the rest of web development will feel much more concrete.
