# Accessibility Quiz

This project is a practice quiz designed to test and improve your knowledge of HTML and CSS accessibility features. It includes a variety of questions and interactive elements to make learning both fun and effective.

## Key Features

- **Responsive Design**: The quiz is designed to be responsive and works well on different screen sizes.
- **Accessibility-Focused**: The HTML and CSS are structured to ensure an inclusive experience for all users.
- **Smooth Scrolling**: Smooth scrolling is enabled for users who have not indicated a preference for reduced motion.

## Tech Stack

- HTML
- CSS (with media queries for reduced motion preferences)

## Key Points for CSS Styling

1. **Reset Default Styles**: Every browser has its own default CSS styles, so it's important to remove them to ensure your styling works properly across all browsers. This can be done using a CSS reset or by setting padding, margin, and `box-sizing` to `border-box` for all elements.

   ```css
   * {
     padding: 0;
     margin: 0;
     box-sizing: border-box;
   }
   ```

2. **Smooth Scrolling**: Enable smooth scrolling for users who have not indicated a preference for reduced motion. This enhances the user experience by providing a smoother navigation experience.

   ```css
   @media (prefers-reduced-motion: no-preference) {
     * {
       scroll-behavior: smooth;
     }
   }
   ```

3. **Responsive Design**: Use relative units like `em`, `rem`, `vw`, and `vh` to ensure your layout is responsive. Functions like `max()` and `min()` are great for responsive design.

   ```css
   #logo {
     width: max(10rem, 18vw);
   }

   h1 {
     font-size: min(5vw, 1.2em);
   }
   ```

4. **Accessible Colors**: Ensure the color contrast between text and background is sufficient for readability. Tools like the [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) can help with this.

5. **Semantic HTML**: Use semantic HTML elements like `<header>`, `<nav>`, `<main>`, `<section>`, and `<footer>` to improve the accessibility and SEO of your page.

6. **Focus Styles**: Ensure that interactive elements like buttons and links have visible focus styles to aid keyboard navigation.

   ```css
   button:focus,
   a:focus {
     outline: 2px solid #f1be32; /* Adjust the color to match your design */
     outline-offset: 2px;
   }
   ```

7. **Screen Reader Text**: Include a `.sr-only` class for screen reader-only text, which is great for accessibility.

   ```css
   .sr-only {
     position: absolute;
     width: 1px;
     height: 1px;
     overflow: hidden;
     clip: rect(0, 0, 0, 0);
     clip-path: inset(50%);
     white-space: nowrap;
   }
   ```

## How to Use

1. Clone the repository.
2. Open [index.html](http://_vscodecontentref_/1) in your browser to view the quiz.
3. Fill out the form and answer the questions.
4. Submit the form to see your results.

## Contributing

Feel free to fork the repository and submit pull requests. Any feedback or suggestions are welcome!

## License

This project is licensed under the MIT License.
