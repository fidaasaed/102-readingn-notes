THE PAST, PRESENT & FUTURE OF LOCAL STORAGE FOR WEB APPLICATIONS

 **Cookies were invented early in the web’s history, and indeed they can be used for persistent local storage of small amounts of data.
 But they have three potentially dealbreaking downsides:**

* Cookies are included with every HTTP request, thereby slowing down your web application by needlessly transmitting the same data over and over
* Cookies are included with every HTTP request, thereby sending data unencrypted over the internet (unless your entire web application is served over SSL)
* Cookies are limited to about 4 KB of data — enough to slow down your application (see above), but not enough to be terribly useful


**What we really want is**

* a lot of storage space
* on the client
* that persists beyond a page refresh
* and isn’t transmitted to the server

USING HTML5 STORAGE
**HTML5 Storage is based on named key/value pairs. You store data based on a named key, then you can retrieve that data with the same key. The named key is a string. The data can be any type supported by JavaScript,
including strings, Booleans, integers, or floats.**

interface Storage {
  getter any getItem(in DOMString key);
  setter creator void setItem(in DOMString key, in any data);
};
Calling setItem() with a named key that already exists will silently overwrite the previous value. Calling getItem() with a non-existent key will return null rather than throw an exception.

Like other JavaScript objects, you can treat the localStorage object as an associative array. Instead of using the getItem() and setItem() methods, you can simply use square brackets. For example, this snippet of code:

var foo = localStorage.getItem("bar");
// ...
localStorage.setItem("bar", foo);
…could be rewritten to use square bracket syntax instead:

var foo = localStorage["bar"];
// ...
localStorage["bar"] = foo;


TRACKING CHANGES TO THE HTML5 STORAGE AREA
*If you want to keep track programmatically of when the storage area changes, you can trap the storage event. The storage event 
is fired on the window object whenever setItem(), removeItem(), or clear() is called and actually changes something. For example,
if you set an item to its existing value or call clear() when there are no named keys,*

if (window.addEventListener) {
  window.addEventListener("storage", handle_storage, false);
} else {
  window.attachEvent("onstorage", handle_storage);
};

BEYOND NAMED KEY-VALUE PAIRS: COMPETING VISIONS
*While the past is littered with hacks and workarounds, the present condition of HTML5 Storage is surprisingly rosy. A new API has been standardized and
implemented across all major browsers, platforms, and devices. As a web developer, that’s just not something you see every day, is it? But there is more
to life than “5 megabytes of named key/value pairs,” *
and the future of persistent local storage is… how shall I put it… well, there are competing visions.
the storage event will not fire, because nothing actually changed in the storage area.
