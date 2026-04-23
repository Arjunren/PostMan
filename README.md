# PostMan
A lightweight, single-file API client with a built-in testing engine, environment variables, and instant code generation. No install required.

# 🚀 Mini Postman — PRO Edition

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.0+-38B2AC?logo=tailwind-css)
![Vanilla JS](https://img.shields.io/badge/JavaScript-ES6+-F7DF1E?logo=javascript)

**Mini Postman PRO** is a high-performance, single-file API testing client designed for developers who need a lightweight yet powerful alternative to bulky desktop applications. Built with a focus on speed, it offers a professional-grade suite of features including automated testing, environment management, and multi-language code generation.



---

## ✨ Key Features

### 🛠 Dynamic Request Builder
* **Multi-Method Support:** Effortlessly execute `GET`, `POST`, `PUT`, `PATCH`, and `DELETE` requests.
* **Smart Auth:** Native support for **Bearer Tokens** and **Basic Auth**.
* **Flexible Body:** Toggle between `JSON` and `Form-Data` (including file uploads).

### 🧪 Advanced Scripting & Testing
* **Pre-request Scripts:** Set environment variables dynamically before execution.
* **Assertion Engine:** Write JavaScript tests using a Postman-compatible syntax (`pm.test`, `pm.expect`).
* **Visual Test Results:** Real-time pass/fail indicators with detailed error reporting.

### 📋 Productivity Tools
* **Environment Variables:** Use `{{key}}` syntax in URLs, Headers, and Bodies.
* **Code Snippet Generator:** Instantly convert requests into `cURL`, `JavaScript (Fetch)`, or `Python (Requests)`.
* **Persistent Collections:** Automatic local storage for Request History and Saved Collections.
* **Modern UI:** Fully responsive design with an elegant **Dark Mode** and localized theme persistence.

---

## 🚀 Getting Started

Since **Mini Postman PRO** is entirely client-side, setup is instantaneous.

1. **Download** the `index.html` file.
2. **Open** it in any modern web browser.
3. (Optional) For the best experience with local APIs, ensure your server has **CORS** enabled.

---

## 🛠 Tech Stack

* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN for portability)
* **Logic:** Vanilla JavaScript (ES6+)
* **Data Persistence:** Browser `localStorage`
* **Icons:** SVG-based vector icons for crisp scaling

---

## 📖 Usage Examples

### Environment Interpolation
Define a variable in the **Env {}** tab:
- **Key:** `base_url`
- **Value:** `https://api.example.com`

Then, use it in the address bar: `{{base_url}}/v1/users`

### Writing a Test
```javascript
pm.test("Status code is 200", function () {
    pm.expect(pm.response.code).to.equal(200);
});

pm.test("Response is fast", function () {
    pm.expect(pm.response.responseTime).to.be.below(300);
});
