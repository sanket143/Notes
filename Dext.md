# Dext: A new way to surf and serve websites

### **Abstract**

Dext lets the developer
package her website and upload it to **Dext Store** from
where it could be installed and could run on `Dexter` application.

The motto of this project is to provide seemless web experience.

### **Terminology**

_Dexter_: A desktop application where user can find applications and
install _Dext_ from the store.

_Dext_: A web application that will be served on _Dexter_

### **.dext**

Developer will package his/her webpage to `.dext`. Mostly it'll
contain the front-end of the website, which can make API calls to
the website server => fetch data and show it by mutating packaged
front-end.

### **Advantages**

- Reduces the amount of data that needs to be downloaded since
front-end of the application is already there.

It perfectly fit with in the analogy with Android application.
Dext is similar to an Android application but it runs in browser, and
serves application components served by _Dexter_.

Android application fetches data from the server and show it. Similarly
Dext will fetch data from the server and show it.

It is exactly like running your front-end on `localhost` which makes
api calls on a remote server and show you stuff.

Moreover, Dext have some advantages
- Let's the webpage store data in users computer.
- Gives a native experience by packaging like Electron.

### **Proposed tool and technologies**
**Servo:** Is a web driver sponsered by mozilla. It is still in beta
and need a lot of improvement. It is aiming for next generation
browser experience.

**Dexter:** Wrapper around the Servo, more like an API to make _Dext_s
possible to get out of the Sandbox of Servo and interact with local
files.

### **Why is it fascinating?**

- It is more of a backend and less of a designing.
- It appears to be something that doesn't exist.
- It is Light it could possibly be the biggest leap
in web performance. 
- Everyone wants to surf internet as fast as they can, _there is no fastest_.
