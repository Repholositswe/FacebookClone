# Facebook Clone

This is a simple Facebook clone built using **HTML**, **CSS**, and **JavaScript**. It looks like Facebook, but it's just a website to show how posts, comments, and likes would work.

## Features

- **User Interface (UI) Mimic**: A responsive design that looks like Facebook with a home feed, profile page and a navigation bar.
- **Post Creation**: You can see posts with text and images.
- **Comment Section**: You can add comments to posts.
- **Responsive Design**: The website looks good on both big and small screens.
- **Dark Mode**: You can switch between light and dark mode.

## Dark Mode

The website includes a **Dark Mode** feature, allowing users to switch the theme from light to dark and vice versa with the click of a button.

- **Toggle Button**: A button is available to switch between **light mode** and **dark mode**. The button will toggle the theme on click.
- **Persistent Theme**: The selected theme (light or dark) is saved in the browser's local storage. This means that the theme choice persists even if the user refreshes the page or revisits the site at a later time.

### JavaScript Implementation

To make dark mode persistent, we used **JavaScript** and **localStorage**. When a user switches the theme, it updates the `localStorage` and the webpage theme is adjusted accordingly.

Here’s a small code snippet showing how the dark mode functionality is implemented:

```javascript
// Check for dark mode preference in localStorage

var darkBtn = document.getElementById("dark-btn");

function settingsMenuToggle() {
  settingsmenu.classList.toggle("settings-menu-height");
}

darkBtn.onclick = function () {
  darkBtn.classList.toggle("dark-btn-on");
  document.body.classList.toggle("dark-theme");

  // Store the theme preference in localStorage
  if (localStorage.getItem("theme") == "light") {
    localStorage.setItem("theme", "dark");
  } else {
    localStorage.setItem("theme", "light");
  }
};

// Check and apply saved theme preference when the page loads
if (localStorage.getItem("theme") == "light") {
  darkBtn.classList.remove("dark-btn-on");
  document.body.classList.remove("dark-theme");
} else if (localStorage.getItem("theme") == "dark") {
  darkBtn.classList.add("dark-btn-on");
  document.body.classList.add("dark-theme");
} else {
  localStorage.setItem("theme", "light"); // Default to light theme
}
```

## Acknowledgments

- Inspiration for the design came from Facebook.
- The dark mode was created with JavaScript and **localStorage** to save your theme choice.
- Thanks to **Meta AI** for generating the images used in this project.
