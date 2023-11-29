# ✅ Frontend Mentor: Product Preview Card Component

Hello everybody! 😊

🚶‍♂️ I just completed the [Frontend Mentor's product preview card component challenge](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa)! These challenges are fantastic for enhancing your coding skills through hands-on experience with real-world projects.

## 🗿 Overview

### 📷 Screenshots

![Desktop version of the solution](./screenshots/desktop-mobile-view.png)

🏆 I am happy that I made a fully responsive design, even though it was a little tiring process, I think it turned out a nice design as a result, what do you think?

### 🔗 Links

- CodeSandbox URL: [https://553vgx.csb.app](https://553vgx.csb.app)
- Live Site URL: [https://yavuzkarakus.github.io/frontendMentorProductCard/](https://yavuzkarakus.github.io/frontendMentorProductCard/)

## 🚀 My process

### ⚡ Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Grid
- Mobile-friendly full responsive.

### 👾 What I learned

In this challenge, I learned the CSS grid structure and CSS flex structure by reinforcing it well. I tried to get a proper result by experimenting as much as possible. It was a good study for me to understand the media query structure better.

HTML Code Snippets:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link
      rel="icon"
      type="image/png"
      sizes="32x32"
      href="./images/favicon-32x32.png"
    />
    <title>Frontend Mentor | Product preview card component</title>
    <link rel="stylesheet" media="screen" href="/styles/main.css" />
  </head>
  <body>
    <div class="container">
      <section class="image">
        <img
          src="/images/image-product-desktop.jpg"
          alt="desktop-perfume-img"
        />
        <img
          id="mobile-img"
          src="/images/image-product-mobile.jpg"
          alt="mobile-perfume-img"
        />
      </section>

      <section class="component">
        <header>
          <h3>Perfume</h3>
        </header>
        <main>
          <h2>Gabrielle Essence Eau De Parfum</h2>
          <p>
            A floral, solar and voluptuous interpretation composed by Olivier
            Polge, Perfumer-Creator for the House of CHANEL.
          </p>
          <div class="price">
            <p>$149.99</p>
            <del>$169.99</del>
          </div>
        </main>
        <footer>
          <button type="button">
            <svg width="15" height="16" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M14.383 10.388a2.397 2.397 0 0 0-1.518-2.222l1.494-5.593a.8.8 0 0 0-.144-.695.8.8 0 0 0-.631-.28H2.637L2.373.591A.8.8 0 0 0 1.598 0H0v1.598h.983l1.982 7.4a.8.8 0 0 0 .799.59h8.222a.8.8 0 0 1 0 1.599H1.598a.8.8 0 1 0 0 1.598h.943a2.397 2.397 0 1 0 4.507 0h1.885a2.397 2.397 0 1 0 4.331-.376 2.397 2.397 0 0 0 1.12-2.021ZM11.26 7.99H4.395L3.068 3.196h9.477L11.26 7.991Zm-6.465 6.392a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Zm6.393 0a.8.8 0 1 1 0-1.598.8.8 0 0 1 0 1.598Z"
                fill="#FFF"
              />
            </svg>
            <span> Add to Cart </span>
          </button>
        </footer>
      </section>
    </div>
  </body>
</html>
```

CSS Code Snippets:

```css
@import url(/styles/variables.css);
@import url("https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,700&family=Montserrat:wght@500;700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-weight: normal;
  font-size: var(--theme-paragraph-size);
}

#mobile-img {
  display: none;
}

body {
  background-color: var(--theme-bg-color);
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  background-color: var(--theme-white-color);
  width: 37.5rem;
  border-radius: 0.8rem;
  display: grid;
  grid-template-columns: 1fr 1fr;
}

.container > .image > img:first-child {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-top-left-radius: 0.8rem;
  border-bottom-left-radius: 0.8rem;
}

.container > .component {
  width: 100%;
  height: 100%;
  object-fit: cover;
  padding: 2rem;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.component header > h3 {
  font-family: "Montserrat", sans-serif;
  text-transform: uppercase;
  color: var(--theme-text-color);
  letter-spacing: 0.4rem;
  font-weight: 400;
  font-size: 0.7rem;
}

.component main {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.component main > h2 {
  font-family: "Fraunces", serif;
  font-size: 2rem;
  line-height: 1;
  color: var(--theme-title-color);
}

.component main > p {
  color: var(--theme-text-color);
  font-family: "Montserrat", sans-serif;
  font-size: 0.9rem;
  font-weight: 400;
  line-height: 1.6;
}

.price {
  display: flex;
  align-items: center;
  gap: 1rem;
}

main .price > p {
  font-family: "Fraunces", serif;
  font-size: 2rem;
  color: var(--theme-button-color);
}

main .price > del {
  font-family: "Montserrat", sans-serif;
  color: var(--theme-text-color);
  font-weight: 400;
  font-size: 0.75rem;
}

footer button {
  width: 100%;
  height: 3rem;
  background-color: var(--theme-button-color);
  padding: 1rem;
  font-family: "Montserrat", sans-serif;
  color: var(--theme-white-color);
  border: none;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 0.8rem;
  border-radius: 0.5rem;
}

footer button:hover {
  background-color: var(--theme-hover-color);
  cursor: pointer;
}

footer button > svg {
  transform: scale(0.9);
}

footer button > span {
  font-size: 0.9rem;
  font-weight: 700;
}
@media screen and (max-width: 376px) {
  .image > img:first-child {
    display: none;
  }

  #mobile-img {
    display: inline;
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-top-right-radius: 0.8rem;
    border-top-left-radius: 0.8rem;
  }

  .container {
    display: flex;
    flex-direction: column;
    margin: auto 1rem;
  }

  .container > .component {
    padding: 1.5rem;
    gap: 1rem;
  }

  .component main {
    gap: 1.2rem;
  }

  .component header h3 {
    font-size: 0.85rem;
  }

  .component main h2 {
    font-size: 2.3rem;
  }

  .component main p:nth-child(2) {
    font-size: 1.04rem;
  }

  main .price {
    gap: 1.6rem;
  }

  main .price p {
    font-size: 2.4rem;
  }

  main .price del {
    font-size: 0.9rem;
  }

  footer button {
    padding: 1.75rem;
  }

  footer button span {
    font-size: 1rem;
  }
}
```

### 💪 Continued development

For front-end developers, the learning process never ends. For this reason, I want to improve myself as much as possible in HTML and CSS. Then I want to complete my development with JS and React.js, discover new CSS libraries and improve myself in every aspect of the field as much as possible.

## 🚩 Author

- Frontend Mentor - [@yavuzkarakus](https://www.frontendmentor.io/profile/yavuzkarakus)

## 📒 Notes

🚶‍♂️ I plan to continue these challenges as long as I can. If you are interested in these topics, don't forget to tune in and follow me.

⭐ If you liked this project and the challenge, please don't forget to star it.
