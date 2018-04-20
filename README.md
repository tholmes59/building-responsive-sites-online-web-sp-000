# Building Responsive Sites

## Objectives

* Gain a better understanding of why we build responsive websites
* Discuss existing solutions and techniques to responsive web design

## Why Build a Responsive Website?

On the modern web, we frequently access the same content on a variety of
platforms, and as front end developers, we want our web sites to look
good and function well regardless of whether a user is on their laptop, phone
or tablet. Each device will display our content differently due to their sizes
and proportions, causing text to shrink, or parts of the page to shift around,
leading to poor user experience if we're not careful.

This has been an issue for a few years, so a couple of different strategies have
been developed to address it.

## Server-Side Device Detection

It is possible for web servers to check the requesting device's headers info,
and send back files specific to the type of device. Going to
[twitter.com](twitter.com) on your phone will automatically redirect you to
[mobile.twitter.com](mobile.twitter.com) because their servers detected that a
phone was sending the request.

Unfortunately, while this is a common solution, it requires building _two_
separate websites. Every time you want to change something about the content
of your site, you have to do it twice, once for both the desktop and mobile
versions of your site.

## Responsive Layouts Using CSS

The other common solution to is to use Cascading Style Sheets.  Instead of a
server detecting the type of device, every user receives the same content,
and the provided CSS informs the user's browser on how to style the DOM. A well
designed, responsive website relies on a combination of CSS media queries,
layout properties like flexbox and grid, and HTML viewport settings.

## Desktop-Down Design

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
for tablet or mobile styling

## Mobile-Up Design

Going in the opposite direction is _Mobile-up_, an approach gaining popularity in
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

## Graceful Degradation

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

## Progressive Enhancement

Just as with mobile-up and desktop-down, progressive enhancement is
the same as graceful degradation, but in the opposite direction.  Progressive
enhancement means first designing your website to function at its most basic,
then upscaling the functionality if the user's browser can handle it.

## Can't We Just Make Users Update Their Browsers?

Yes, we can. Sometimes, you might have to. If, for instance, your website is an
HTML5 canvas game built with JavaScript, some users will not be able to play
your game without updating. Beyond that, it is often good practice to make sure
your site is accessible to the most visitors possible.

Luckily, the number of users still on out of date browsers is continuously
shrinking, and most modern browsers automatically update to the newest version.

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/building-responsive-sites' title='Building Responsive Sites'>Building Responsive Sites</a> on Learn.co and start learning to code for free.</p>
