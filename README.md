# Europe Travel Website - Static Deployment Ready

This repository contains all the necessary resources and dependencies to deploy a static Europe Travel Website on a web server. This is a fully self-contained static website built using HTML, CSS, and JavaScript.

**Original GitHub Repository:** [https://github.com/GNiruthian/Europe-Travel-Website-html-css-js](https://github.com/GNiruthian/Europe-Travel-Website-html-css-js)

## Static Website Nature

This website is entirely static. This means:

* **No server-side processing:** All the website's logic and content are handled directly by the user's browser.
* **Pre-rendered content:** The HTML, CSS, and JavaScript files are delivered as they are, without any dynamic generation on the server.
* **Simplified deployment:** Deploying a static website is generally straightforward as it only requires serving static files.

## Contents

This repository includes all the assets required for the website to function correctly:

* **HTML files (`.html`):** The structure and content of each page.
* **CSS files (`.css`):** The styling and visual presentation of the website.
* **JavaScript files (`.js`):** Any client-side interactivity and dynamic behavior.
* **Image files (`.jpg`, `.png`, etc.):** All the images used on the website.
* **Font files (if any):** Custom fonts used for the website's typography.
* **Any other static assets:** This might include icons, or other media files.

**You do not need to install any dependencies or run any build processes to deploy this website.** Simply copy the contents of this repository to your web server's document root.

## Deployment Options on Google Cloud

This static website can be easily deployed on various Google Cloud Platform (GCP) services:

* **Google Compute Engine (GCE):**
    1.  Create a virtual machine instance.
    2.  Install a web server (e.g., Nginx, Apache) on the instance.
    3.  Configure the web server to serve the files from this repository.
    4.  Ensure the necessary firewall rules are in place to allow HTTP/HTTPS traffic.

* **Google Kubernetes Engine (GKE):**
    1.  Create a Kubernetes cluster.
    2.  Create a Deployment to manage a Pod running a container that serves the static files (e.g., using an Nginx image configured to serve the content).
    3.  Create a Service (e.g., LoadBalancer) to expose the website to the internet.

* **Cloud Run:**
    1.  Containerize the static website files using a simple web server (e.g., Nginx, httpd) in a Dockerfile.
    2.  Deploy the container image to Cloud Run. Cloud Run automatically handles scaling and infrastructure.

* **App Engine (Static Files):**
    1.  Create an `app.yaml` file in the root directory of this repository to configure static file serving.
    2.  Deploy the application using the `gcloud app deploy` command. App Engine's static file handlers are optimized for serving static content efficiently.

**For all deployment options, ensure that the web server or service is configured to correctly serve the files located in this repository.**

This README provides the essential information for deploying this static Europe Travel Website. Good luck!
