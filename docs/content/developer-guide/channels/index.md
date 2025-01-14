---
title: "Channels"
showtoc: true
---

# Channels

Channels are a feature of Vendure which allows multiple sales channels to be represented in a single Vendure instance. A Channel allows you to:

* Set a channel-specific currency, tax and shipping defaults
* Assign only specific Products to the Channel (with Channel-specific prices)
* Create Administrator roles limited to the Channel
* Assign only specific Promotions, Collections, ShippingMethods to the Channel
* Have Orders and Customers associated with specific Channels.

Every Vendure server always has a **default Channel**, which contains _all_ entities. Subsequent channels can then contain a subset of the above entities.

{{< figure src="channels_diagram.png" >}}

Use-cases of Channels include:

* Multi-region stores, where there is a distinct website for each territory with its own available inventory, pricing, tax and shipping rules.
* Creating distinct rules and inventory for different sales channels such as Amazon.
* Specialized stores offering a subset of the main inventory.

## How to set the channel when using the GraphQL API

To specify which channel to use when making an API call, set the `'vendure-token'` header to match the token of the desired Channel.

## Multi-Tenant (Marketplace) Support

Channels can also be used to implement a multi-tenant or marketplace application. In such a setup, each merchant would have their own dedicated Channel and would be granted permissions on that Channel only.
 
For a detailed guide on how this would be set up, see our [Multi-Tenant guide]({{< relref "multi-tenant" >}}).
