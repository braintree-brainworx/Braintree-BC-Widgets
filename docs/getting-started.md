---
layout: page
title: Getting Started
permalink: /docs/getting-started/
---

# Getting Started

This guide walks you through the initial setup of the Braintree BigCommerce Widgets.

## Prerequisites

- A BigCommerce store running the Stencil theme framework
- A [Braintree](https://www.braintreepayments.com/) merchant account
- Access to your BigCommerce control panel

## Installation

### 1. Add the Widget Script

Include the Braintree BC Widgets script in your Stencil theme's `templates/layout/base.html`:

```html
<script src="https://braintree-by-vox.github.io/Braintree-BC-Widgets/assets/js/braintree-bc-widgets.js"></script>
```

### 2. Configure Your Braintree Credentials

Add your Braintree tokenization key to your theme's `config.json`:

```json
{
  "settings": {
    "braintree_tokenization_key": "your_tokenization_key_here"
  }
}
```

### 3. Initialize a Widget

```javascript
BraintreeBCWidgets.init({
  container: '#payment-container',
  tokenizationKey: '{{theme_settings.braintree_tokenization_key}}',
  paymentMethods: ['card', 'paypal']
});
```

## Next Steps

- [Configuration Options](../configuration) – Customise widget behaviour
- [Widgets Reference](../widgets) – Explore all available widgets
