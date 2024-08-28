# Scrimba - Chrome extension leads tracker solution

This is a solution to the [Chrome extension leads tracker project on Scrimba](https://scrimba.com/learn/learnjavascript/). Scrimba helps you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
  - [How to install](#how-to-install)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- Save leads writing them into the input element
- Save the current Chrome tab in the list
- Maintain leads even after closing the browser
- Delete all leads by double clicking on the last button
- See hover states for interactive elements

### Screenshot

![screenshot](./screenshots/screenshot.png)

### Links

- Solution URL: [@GitHub](https://github.com/AnastasiiaHombalevska/chrome-extensions)
- Live Site URL: [@GitHub](https://silly-monstera-811fb6.netlify.app)

### How to install

- Clone Repo or Download Zip
- Visit chrome://extensions/ and turn on "Developer mode"
- Click "Load unpacked" button and navigate to the folder you downloaded
- That's it! 🎉

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- CSS Flexbox Layout
- Mobile-first workflow
- Google Chrome APIs

### What I learned

With this project I improved a lot my JS skills. The newest things I learnt are:

- How to get the active Chrome tab and store it into localStorage using JSON's methods

```js
tabBtn.addEventListener("click", function () {
  chrome.tabs.query({ active: true, currentWindow: true }, function (tabs) {
    myLeads.push(tabs[0].url);
    localStorage.setItem("myLeads", JSON.stringify(myLeads));
    render(myLeads);
  });
});
```

### Continued development

I'd like to:

- Give the ability to select which leads to remove from the list
- Improve UI

## Acknowledgments

A big thank you to [Per Harald Borgen](https://github.com/perborgen) who is a pleasure to listen to and to learn new things in a funny and interactive way 👏