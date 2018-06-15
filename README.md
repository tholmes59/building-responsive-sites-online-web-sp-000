# Building Responsive Sites

## Problem Statement

On the modern web, we frequently access the same content on a variety of
devices. Each device will display content differently due to its size
and proportions. This can have unpredictable results: text might appear
too small, or parts of the page might shift around in an unusual way,
and can lead to poor user experience. As front-end developers, we want our 
web sites to look good and function well whether a user is on 
their laptop, phone or tablet.

In this lesson we will outline the high-level approaches for these concerns.
In subsequent lessons we will learn to code responsiveness into our sites.

## Objectives

1. Explain server-side detection for redirection
2. Explain creating responsive layouts with CSS
3. Explain desktop-down design
4. Explain mobile-up design
5. Explain graceful degradation
6. Explain progressive enhancement

## Using Server-Side Detection for Redirection

Every time your web browser opens a web page, it sends information to the server
called a "request". Part of that request includes a series of "headers". HTTP 
headers carry information about the client browser, the requested page, the server, 
and more. It is possible for web servers to check the requesting device's headers 
information, and send back files specific to the type of device. Going to
[twitter.com](twitter.com) on your phone will automatically redirect you to
[mobile.twitter.com](mobile.twitter.com) because their servers detected that a
phone was sending the request.

Unfortunately, while this is a common solution, it requires building _two_
separate websites. Every time you want to change something about the content
of your site, you have to do it twice, once for both the desktop and mobile
versions of your site. This is an expensive and error-prone solution.

## Creating Responsive Layouts with CSS

The other common solution to is to use Cascading Style Sheets.  Instead of a
server detecting the type of device, every user receives the same content,
and the provided CSS tells the user's browser how to style the rendered page. 
The ideal approach for a well designed, responsive website relies on a combination
of CSS media  queries, layout properties and HTML the viewport settings that 
scale the browser content. In subsequent materials we'll cover each of these
three techniques. Together they create "responsive layouts."

## What is Desktop-Down Design?

There are multiple approaches to responsive design.  One approach is
_Desktop-down_, where a site is first designed for desktop devices, then
modified layouts are developed for tablet and mobile devices. Since we're
_doing_ the work of designing a website on a desktop or laptop already, this
approach can feel the most natural.  Desktops and laptops offer more
capabilities with their more powerful hardware, and the larger screen size means
a larger space to work with, a larger canvas for us to paint on.

Desktop-down design often means that, by default, elements on the page are the
width and height they should be for a larger screen.  When a smaller screen size
is detected, the default styling will be overridden and replaced with the rules
for tablet or mobile styling.

## What is Mobile-Up Design

Going in the opposite direction is _mobile-up_ or _mobile-first_, an approach gaining popularity in
our modern, mobile world. The idea behind this approach is to design websites
for small screen sizes first. One benefit to this approach is that it ensures
users have a great experience on mobile, as there is no change it will end up
being a second thought during design.

Many, if not most, internet users now interact with the through their cell
phones more than their laptops, so it makes sense for businesses to cater to
these users first.  Chrome luckily provides a useful tool, the [device
toolbar](https://developers.google.com/web/tools/chrome-devtools/device-mode/emulate-mobile-viewports)
within the developer tools, that lets you mimic the proportions of popular
mobile devices.

Mobile-up design means that, by default, elements on the page are positioned are
positioned and sized for small screens, then overridden if a larger screen is
detected.

## Explain Graceful Degradation

The internet is used by a variety of users, all with different web browser
versions.  Although the [majority of
users](https://www.w3schools.com/browsers/default.asp) are now on modern web
browsers like Chrome, there are still some users that haven't updated since
[Internet Explorer
6](https://developer.microsoft.com/en-us/microsoft-edge/ie6countdown/#).
Graceful degradation is the practice of designing a web page for modern
browsers, but providing 'fall back' versions, alternative designs that have less
features, but still provide a good experience. Unless your website needs the
latest and coolest functionality, it is often a good idea to provide some
alternatives.  Fully embracing graceful degradation may mean designing your
website to work even without JavaScript or CSS, using the older, most compliant
HTML.

## Explain Progressive Enhancement

Just as with mobile-up and desktop-down, progressive enhancement is
the same as graceful degradation, but in the opposite direction.  Progressive
enhancement means first designing your website to function at its most basic,
then upscaling the functionality if the user's browser can handle it.


## Conclusion
There are a number of ways that front end developers can accommodate users
on different platforms. Which method or methods chosen can depend on the 
core functionality of the website. Understanding these various options will
help inform how your page is built for maximum accessibility--there is no 
single _right_ way!

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/building-responsive-sites' title='Building Responsive Sites'>Building Responsive Sites</a> on Learn.co and start learning to code for free.</p>
