# Vippy Template

Vippy is a template designed for building your own virtual-photography portfolio (I mean.. it could also be IRL photography) and personal website. Built with a modular architecture, it offers seamless configuration through an intuitive admin panel, allowing for deep customization to match your unique style and specific needs.

The admin dashboard also features a management system for virtual photography portfolios, utilizing Backblaze integration for image hosting.

## Setup Guide

### Prerequisites
- **Ruby & Jekyll**: For the static site generation.
- **Node.js**: For the admin panel.

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/vippy.git
   cd vippy
   ```

2. **Install Jekyll Dependencies**
   ```bash
   bundle install
   ```

3. **Install Admin Panel Dependencies**
   ```bash
   cd vippy-admin
   npm install
   ```

## Running the Project

To fully utilize the template, you need to run both the Jekyll server (for the site) and the Node.js server (for the admin panel).

1. **Start the Website**
   In the root directory:
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at `http://localhost:4000`.

2. **Start the Admin Panel**
   In the `vippy-admin` directory:
   ```bash
   npm start
   ```
   The admin dashboard will be available at `http://localhost:3001/vippy`.

## Configuration

### Managing Modules
Navigate to `http://localhost:3001/vippy` to see your active modules.
- **Toggle**: Use the switch to enable or disable a module. Disabled modules will disappear from the site navigation.
- **Reorder**: Drag and drop modules to change their order in the navigation menu.
- **Important**: After making changes to modules (toggling or reordering), you must restart your Jekyll server (`bundle exec jekyll serve`) for changes to take effect on the live site.

### Backblaze B2 Setup (Image Uploads)
To enable image uploading functionality for the Virtual Photography module, you need to connect your Backblaze B2 account.

1. Log in to Backblaze B2 and create a new **Public Bucket**.
2. Go to **App Keys** and create a new key with read/write access to that bucket.
3. Access the Virtual Photography module inside the admin dashboard and configure your Storage settings.
- **use_cdn**: Set to `true` if you are using a CDN (like Cloudflare) in front of B2.
- **cdn_domain**: If `use_cdn` is true, enter your CDN URL (e.g., `https://cdn.yoursite.com`).

Once configured, the admin panel will automatically handle image uploads to your bucket.

## Credits
A special thanks to nico for the initative and recomandations + yousinix for his portfolYOU theme which this template is based one.