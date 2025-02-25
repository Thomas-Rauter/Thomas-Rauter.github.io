# My Personal Website

This repository contains my personal website built with **Jekyll** using the 
**Minima** theme. This guide explains how to **set up the website locally**, 
install dependencies, and run Jekyll to preview changes.

---

## **🚀 How to Set Up This Website Locally**

Follow these steps to clone and set up the website on a **new computer**.

### **1️⃣ Install Required Dependencies**
Ensure your system has the following installed:

- **Ruby** (version 3.x recommended)
- **Bundler** (Ruby package manager)
- **Jekyll**

#### **🔹 Install Ruby & Bundler**
- **On macOS (with Homebrew)**:
  ```bash
  brew install ruby
  gem install bundler
  ```

- **On Ubuntu / Debian**:
  ```bash
  sudo apt update
  sudo apt install ruby-full build-essential zlib1g-dev
  gem install bundler
  ```

- **On Windows**:
  - Install **RubyInstaller** from [rubyinstaller.org](https://rubyinstaller.org/)
  - After installation, open a terminal and run:
    ```powershell
    gem install bundler
    ```

---

### **2️⃣ Clone the GitHub Repository**
```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

---

### **3️⃣ Install Jekyll and Dependencies**
Inside the project directory, run:
```bash
bundle install
```

This installs all required **Jekyll plugins and dependencies**.

---

## **🛠️ Running the Website Locally**
To preview the website on `localhost:4000`, use:

```bash
bundle exec jekyll serve
```

If successful, you should see output like:
Server address: http://127.0.0.1:4000


Open your **browser** and visit `http://127.0.0.1:4000`.

---

## **🔎 Testing & Troubleshooting**
### **Test a Clean Build**
To test the website as a **fresh build**, use:
```bash
bundle exec jekyll build --clean
```

This regenerates the site and removes old cached files.

### **Check for Dependency Issues**
If `jekyll serve` fails, try:
```bash
bundle update
bundle exec jekyll serve
```

If Sass-related warnings appear (e.g., deprecation messages for `darken()` and
`lighten()`), downgrade `sassc` with:
```bash
gem install sassc -v "~> 2.0"
bundle update jekyll-sass-converter
```

---

## **🌍 Deploying Updates**
If making changes, commit and push to GitHub:
```bash
git add .
git commit -m "Updated content"
git push origin main
```

If hosting via **GitHub Pages**, the site will automatically update.

---

## **🔁 Resetting Everything (If Needed)**
If anything goes wrong, **reset your local setup**:
```bash
rm -rf _site .jekyll-cache
bundle exec jekyll clean
bundle install
bundle exec jekyll serve
```

---

## **💡 Notes**
- If you switch computers, just **clone the repo and repeat steps 1-3**.
- Always run `bundle install` after pulling new changes.
- To ensure compatibility, use **Ruby 3.x** and avoid unnecessary Sass updates.

---

**✅ Now your setup is documented!** If you ever switch to a new computer, just follow these steps. 🚀


