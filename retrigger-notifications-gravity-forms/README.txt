=== Retrigger Notifications Gravity Forms ===
Contributors: wpspin
Donate link: https://wpspins.com/support-our-work/
Tags: gravity forms, zapier, webhooks, resend notifications, gravity forms addon
Requires at least: 4.0.0
Tested up to: 6.9
Stable tag: 1.3
Requires PHP: 7.0
License: GPLv2 or later
License URI: http://www.gnu.org/licenses/gpl-2.0.html

Resend Gravity Forms entry data to Zapier and Webhook feeds with one click -- no need to resubmit the form.

== Description ==

**Retrigger Notifications Gravity Forms** lets you manually re-send Gravity Forms entry data to external Zapier and Webhook API feeds -- directly from the WordPress admin, without resubmitting the form.

Whether a webhook failed silently, Zapier missed a trigger, or you simply need to push historical entries to a new integration, this plugin has you covered.

---

### 🔄 What It Does

When Gravity Forms sends entry data to Zapier or Webhooks, things don't always go right. Endpoints go down, APIs timeout, and integrations break. Instead of asking users to resubmit, this plugin lets you **retrigger the feed** for any entry -- individually or in bulk.

---

### ✅ Use Cases

1. **🔁 Resend failed Zapier triggers** -- A Zap didn't fire? Retrigger it from the entry detail page without asking the user to resubmit.
2. **🌐 Resend failed Webhook deliveries** -- Push entry data again to your Webhook endpoint when the first attempt failed or timed out.
3. **📦 Bulk resend entries to Zapier** -- Select multiple entries from the Entries list and resend them all to Zapier feeds in one action.
4. **📦 Bulk resend entries to Webhooks** -- Select multiple entries and push them all to Webhook endpoints at once.
5. **🐛 Debug API integrations** -- Use the built-in test endpoint and GF logging to troubleshoot why data isn't reaching your external service.
6. **🔗 Connect a new Zapier integration to old entries** -- Set up a new Zap and retrigger historical entries so they flow into the new workflow.
7. **🔗 Connect a new Webhook to old entries** -- Added a new Webhook feed? Push past entries through it without resubmission.
8. **🛠️ Test Zapier/Webhook setup during development** -- Quickly retrigger entries while building and testing your automation pipeline.
9. **📊 Sync data after downtime** -- If your external service was down during form submissions, retrigger all affected entries once it's back online.
10. **🔍 Verify data delivery** -- Retrigger a single entry and check GF logs to confirm data was sent and received correctly.

---

### ⚙️ Settings & Usage

This plugin works seamlessly within the existing Gravity Forms interface -- no separate settings page required.

**Single Entry Resend:**

1. Go to **Forms → Entries** in your WordPress admin.
2. Click on any entry to open the **Entry Detail** page.
3. In the right sidebar, you'll see **"Resend Zapier Feeds"** and/or **"Resend Webhook Feeds"** panels.
4. Check the feeds you want to retrigger.
5. Click the **Resend** button. Done!

**Bulk Resend:**

1. Go to **Forms → Entries** and select the entries you want to resend.
2. Choose **"Resend Zapier Feeds"** or **"Resend Webhook Feeds"** from the **Bulk Actions** dropdown.
3. Click **Apply**. Confirm the action in the popup dialog.
4. All selected entries will be resent to the configured feeds.

**Debugging:**

- Enable **Gravity Forms Logging** under Forms → Settings → Logging.
- Use the built-in test endpoint (`/wp-json/gf/v1/test-webhook-api`) to verify webhook delivery.
- All retrigger operations are logged to the GF debug log.

---

### 🧩 Works Great With These Plugins

- **[Gravity Forms](https://www.gravityforms.com/)** -- Required. The form plugin this addon extends.
- **[Gravity Forms Zapier Add-On](https://www.gravityforms.com/add-ons/zapier/)** -- Required for Zapier retrigger features.
- **[Gravity Forms Webhooks Add-On](https://www.gravityforms.com/add-ons/webhooks/)** -- Required for Webhook retrigger features.
- **[GravityView](https://www.gravitykit.com/products/gravityview/)** -- Display entries on the frontend; use Retrigger to fix API issues behind the scenes.
- **[Gravity Perks](https://gravitywiser.com/)** -- Advanced Gravity Forms snippets and utilities that complement this plugin.
- **[Gravity Flow](https://gravityflow.io/)** -- Workflow automation for Gravity Forms; retrigger feeds at any workflow step.
- **[WP Webhooks](https://wp-webhooks.com/)** -- Extend your webhook capabilities beyond Gravity Forms.
- **[Zapier](https://zapier.com/)** -- The automation platform this plugin integrates with for retriggering Zaps.
- **[Make (formerly Integromat)](https://www.make.com/)** -- Use with Gravity Forms Webhooks to push data to Make scenarios.
- **[Gravity SMTP](https://www.gravityforms.com/add-ons/smtp/)** -- Reliable email delivery alongside your retriggered API feeds.

---

### 📋 Requirements

- WordPress 4.0 or higher
- Licensed **Gravity Forms** plugin (active)
- **Zapier Add-On** enabled (for Zapier features)
- **Webhooks Add-On** enabled (for Webhook features)

== Installation ==

1. Upload the `gravityforms-retrigger-notifications` folder to `/wp-content/plugins/`.
2. Activate the plugin through **Plugins → Installed Plugins** in WordPress.
3. Make sure Gravity Forms and at least one of the Zapier or Webhooks add-ons are active.
4. Navigate to **Forms → Entries**, open any entry, and look for the **Resend** panels in the sidebar.

== Screenshots ==

1. Resend Zapier and Webhook feeds panels on the Entry Detail sidebar.
2. Resend feeds panels with checkboxes for selecting individual feeds.
3. Bulk resend actions in the Entries list dropdown.

== Frequently Asked Questions ==

= Do I need both Zapier and Webhooks add-ons? =

No. The plugin detects which add-ons are active and only shows the relevant resend panels. You can use it with just Zapier, just Webhooks, or both.

= Will this create duplicate entries? =

No. This plugin only resends the existing entry data to external feeds. It does not create new form entries.

= Does it work with the latest Gravity Forms Zapier add-on? =

Yes. The plugin automatically detects whether you are using Zapier add-on version below 4.0 or 4.0+ and uses the correct methods.

= Where can I see logs? =

Enable Gravity Forms Logging under **Forms → Settings → Logging**. All retrigger actions are logged to the Gravity Forms debug log.

== Changelog ==

= 1.3 =
* Compatible with WordPress 6.9
* Updated plugin tags and description
* Added support contact banner in retrigger panels

= 1.2 =
* Check compatible with WordPress 6.2
* Added bulk action to resend feeds in entries page.
* Added logging messages in gravity forms test mode.

= 1.1.5 =
* Check compatible with WordPress 6.1.1

= 1.1.4 =
* Check compatible with WordPress 6.0.1

= 1.1.3 =
* Add donation URL

= 1.1.2 =
* Check compatible with WordPress 5.8.2
* Update author URI.

= 1.1.1 =
* Check compatible with WordPress 5.7.2

= 1.1.0 =
* Check compatible with WordPress 5.7
* Fix the error of missing Zapier resend hook box on plugin `gravityformszapier` 4.0

= 1.0.3 =
* Check compatible with WordPress 5.6.2

= 1.0.2 =
* Check compatible with WordPress 5.6
* Add more plugin screenshot, logo, banner.

= 1.0.1 =
* Corrections in the plugin description.

= 1.0 =
* First version of the plugin.
