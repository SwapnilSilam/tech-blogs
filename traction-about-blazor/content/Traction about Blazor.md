# **Traction about Blazor**

csharp, Blazor, webdev, netcore

Nowadays "Blazor" word is getting more traction and attraction by programmers’ community. Let's understand what Blazor is and why everyone is talking about it? 

*If I say that .NET running in the browser with no plugins, no add-ons. Just .NET running in the browser.*

Yes, you heard and read correctly!! .Net running in the browser. 
A question would come how is it even possible? But yes, this is possible using WebAssembly.

## WebAssembly <a name="WebAssembly"></a>

Before we start with Blazor, let’s understand what is WebAssembly or wasm.

>*WebAssembly (abbreviated Wasm) is a binary instruction format for a stack-based virtual machine. Wasm is designed as a portable target for compilation of high-level languages like C/C++/Rust, enabling deployment on the web for client and server applications.*

This is an official definition on official site [WebAssembly](https://webassembly.org/)

**That looks more complex to understand right? Let me make it simple**

By WebAssembly you can run high-level languages in a browser by using its core speed. <br> WebAssembly is a milestone achievement in the tech world, using this we can run server-side development languages in the browser. <br>
WebAssembly runs in the same security sandbox-like Angular, React and other JavaScript code runs. <br>
Based on open web standards, WebAssembly is part of all modern web browsers, including mobile browsers. <br> With WebAssembly, not just C# but we can run all server-side programming languages. <br><br>

***Here, you might think, it's a Microsoft selling Silverlight in a new package?*** <br><br>
The answer is **BIG NO!!**, because as *Silverlight* you need to install a separate plug-in and run time as part of running the program in the browser.
WebAssembly is part of all Modern browsers and there is no need to install external plug-ins to install.

## Why to learn and what are the benefits of "Blazor"? 

Why do we need to learn Blazor?  Well, You got the answer off in the section of [WebAssembly](#WebAssembly). 
### Let’s see some more details. 
* Write C# instead of JavaScript
* .Net developers can directly be onboarded to project without having any formal training on other technologies.
* Leverage existing capabilities of C# and .net shared libraries
* Blazor is component-based i.e. you can share the same logic at server and client-side. 
* It can be coded with Visual Studio which works across different platforms like Windows, Linux, and Mac. 
* Build on a common set of languages, frameworks, and tools that are stable, feature-rich, and easy to use.


### **Let understand Blazor** 

While learning new techs, always strikes questions, can't we learn server-side languages and use the same technology for a client as well? Until Blazor, the answer was Big No! But it's possible with Blazor. <br><br>
>**Till now you have read the word **Blazor** more than 10 times and you might be thinking that why Blazor is called as Blazor?** <br><br>
*Blazor word formed by two words **"Browser" + "Razor" = "Blazor"**.* <br> Blazor uses more Razor, it’s a markup syntax for HTML and C#. <br><br>

## ***Welcome to Blazor!*** 
**Blazor has two types of Hosting Models**
1.	Blazor Web Assembly
2.	Blazor Server 

Let see one by one with its advantages and disadvantages. 

## **Blazor WebAssembly**

It’s also called as **Client-side Hosting** Models.
Blazor WebAssembly implements a Single-Page application framework for creating responsive and interactive web applications. As mentioned earlier, WebAssembly is based on Open Web Standards i.e. neither you need to install any plug-ins nor is any Code Transpiration needed for it. WebAssembly supports all modern browsers that including mobiles also. 

Running .Net inside a browser is only possible via WebAssembly (You will get more information in the section of [WebAssembly](#WebAssembly)). It is a compact bytecode and optimized format for download and run on maximum native speed.

Wasm code can access the full features of the browser via JavaScript Interporablilty or JavaScript Interop. We know that WebAssembly runs in a secure sandbox browser that protects from any malicious codes and actions being performed on the client-side.

 ![Blazor_WebAssembly](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Blazor WebAssembly")

### **Let's understand the underlying working of it.**

When we compile C# files and Razor files they get converted into .NET assemblies and those assemblies and .NET runtime are downloaded in the browser. Now Blazor WebAssembly kicks the .NET runtime and starts configuring the runtime to load all assemblies to run an app. 

**Advantages:**  
* Blazor WebAssembly runs entirely on client-side 
* No active connection to the server is required
* Client resources and capabilities are used.
* Fully hosted server is not required 
* We can host our application on own server, Azure or CDN 
 
**Disadvantages:**

* Very first request take longer to serve because it needs to download the compiled application and its dependencies
* Performance of an application is completely dependent on clients’ browser
* Browser should support WebAssembly

>Note: Still this in preview state and if you want still try your hands with it. Install Blazor WebAssembly template from the Nuget server and after installation is complete, restart Visual Studio 2019.


## **Blazor Server** 

It is also is known as Server hosting model. Blazor server model decouples the UI rendering logic and logic on how to apply those. 
Blazor application needs to be hosted as an Asp.Net Core app on a Server. Blazor server establishes a SignalR connection between client and server. 

![Blazor_Server](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Blazor Server")

SignalR used for updating UI, for example, any event happens at client-side like any button click; click event is sent to server and server handles the event and sends back the HTML response with operational diff which means server calculate the HTML difference and sends only those differences to the client and upon receiving a response, UI gets updated by Renderer. 

Blazor though embraces the Single Page Architecture, it does not refresh the entire page and update only some part of HTML. Using SignalR, the application becomes more very responsive, fast.

>Blazor server template is publically available and it's officially part of Visual Studio 2019.

**Advantages:** 

* App loads much faster and downloads size is significantly smaller 
* App can take advantages of server capabilities by using asp .net core compatible APIs
* App needs only browser no need for WebAssembly support
* This hosting model is more secure because application code is not sent to the client
 
**Disadvantages:**

* Fully managed ASP .net core server is required
* Active Signal R connection is required between Server and Client 
* High latency due to more round trips to the server
* Scalability can be challenging because the server needs to maintain multiple users and its multiple client states 

>Note: Scalability issues can overcome using the Azure Single R server.

## **Blazor is Component-based, what does it mean?** 

Blazor applications are component-based. A component in Blazor is UI elements such as Page, Dialog Box or user forms. Components are compiled .NET assemblies.

A component class is a Razor page with extension .razor. Blazor components are referred to as Razor Components and this is a combination of HTML and C# code. Blazor Razor pages are the same as MVC Razor pages, but the only significant difference it that Blazor pages are built for client-side UI logic and its compositions.

Components are represented into in-memory as the browser's DOM, so which is used to update UI elements very efficient way. The in-memory representation of components are called as **Render tree.**

**Benefits:**

* Share components across the project. 
* Components also distributed as Razor class libraries or Nuget Packages
* Also handles user events. 
* These can be nested and reusable.

## **Next big question can I use JavaScript while working with Blazor?** 
#### Absolutely Yes!!! 

JavaScript Interop, using this you can call JavaScript code by C# and C# code can be called by JavaScript. 

## **Pre-requisites for Blazor**
* Visual Studio 2019 
* .net core 3.0 and above
* Knowledge about HTML, CSS, and C# 

## **Browser Support chart**

| Sr. No             | Chrome | Mozilla Firefox | Safari | Microsoft Edge | Microsoft Internet Explorer |
|--------------------|--------|-----------------|--------|----------------|-----------------------------|
| Blazor WebAssembly | Yes    | Yes             | Yes    | Yes            | No                          |
| Blazor Server      | Yes    | Yes             | Yes    | Yes            | Yes                         |

> Note: Microsoft Internet Explorer does not support WebAssembly. 

<br>

### **Do you think  Blazor will be a Game changer in Web Application Development ?** 

Please share your thoughts and valuable feedback!

Happy Coding and stay connected!