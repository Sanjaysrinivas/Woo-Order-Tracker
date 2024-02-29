# Woo Order Tracker

Woo Order Tracker is a WordPress plugin that extends WooCommerce by allowing you to track orders and send notifications via webhooks. When enabled, it posts JSON formatted order details to a specified webhook URL during various order events.

## Features

- Enable or disable tracking on demand.
- Set a custom destination URL for outgoing webhooks.
- Send webhooks on various WooCommerce order events:
  - Order creation
  - Order status changes
  - Order cancellation
  - Order deletion
  - Order note addition
  - Order completion
- Responsive settings page.
- Support for English and Italian language localizations.

## Installation

1. **Upload Plugin**: Download the `woo-order-tracker.zip` file and upload it to your WordPress website via the Plugins > Add New > Upload Plugin

2. **Activate Plugin**: Once uploaded, activate the plugin through the 'Plugins' menu in WordPress.

3. **Configure Settings**: Navigate to the 'Woo Order Tracker' item in the sidebar within your WordPress admin panel. Here you can enable tracking, set the destination URL webhook, and save your settings.

4. **Webhook URL**: Input the URL where the JSON data should be sent when order events occur.

5. **Save Settings**: Click the 'Save Settings' button to apply your configuration.

## Usage

Once installed and configured, the plugin will automatically send webhooks to the specified URL(s) when the configured WooCommerce order events are triggered. The JSON data structure will include information such as the order ID, total, currency, status, billing email, and customer note.

Ensure that the destination URL is capable of receiving POST requests with JSON formatted bodies.

## Webhook Events

The webhook URL - https://webhook.site/5c031f97-33e9-4217-9a3e-d67ff12a9fa8

The plugin hooks into the following WooCommerce actions:

- `woocommerce_checkout_update_order_meta`
- `woocommerce_order_status_changed`
- `woocommerce_cancelled_order`
- `woocommerce_trash_order`
- `woocommerce_order_note_added`
- `woocommerce_order_status_completed`


