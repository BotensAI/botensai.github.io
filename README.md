# BOTENS Robotics website

Static website for BOTENS Robotics (Style 4, Dark Motion). No build step: open `index.html` in a browser, or serve the folder as-is (for example with GitHub Pages).

- `index.html`: all six pages (Home, About Us, Our Robots, Smart Delivery, AIoT Technology, Press), the contact form and one page per news article
- `styles.css`: layout and colours
- `script.js`: page switching, mobile menu, contact email draft, video controls, press year filter and animation
- `favicon.ico` and `assets/icon/`: browser tab and home-screen icons, made from the B in the logo
- `assets/`: logo, light logo for dark backgrounds, robot images, banner video and poster

Animation uses GSAP 3.13.0 (ScrollTrigger, SplitText) and Lenis 1.1.13 from public CDNs. Without them the site still shows all content, without motion.

The contact form opens an email draft to marketing@botens.onmicrosoft.com; it does not submit to a server. The EN / TH / 中文 language buttons are placeholders.

## Adding a news story

Each story is one `.article-page` block in `index.html` (see the comment above the existing one). Copy it and change the `id` (`page-<slug>`, opens at `#press/<slug>`), `data-image` (Home card photo), the type label, the `<time datetime>` (`YYYY-MM` or `YYYY-MM-DD`), the headline and the body. The Press list (all stories, newest first, with year tabs once there is more than one year) and the 3 newest cards on Home are built from these blocks automatically.
