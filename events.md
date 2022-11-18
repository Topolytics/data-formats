# PragmatIC TRACE API Events

> This document describes the API Events expected within the material movement and transformation flow.
Introduction

To understand how the flow of material operates a simulation was created. Locations were identified and categorised, with different types of activities (events) being undertaken at these locations.

## Location Categories & Activities
The following is a list of location categories and activities (event types), which translate into API events:

### Manufacturer of the packaging, e.g. Sharpak
- Category: `package_manufacturer`
- Activities: `make`

### Manufacturer of the filled product, e.g. PrimaFruit
- Category: `package_manufacturer`
- Activities: `fill`

### Processor site that washes packaging, e.g. IFCO, Bracknell
- Category: `processor`
- Activities: `wash`

### Distributer of the product, e.g. Waitrose Customer Fulfilment Centre
- Category: `retail`
- Activities: `distribute`

### Retailer of the product e.g. Waitrose & Partners
- Category: `retail`
- Activities: `sell`

## Untracked Activities
Additional activities occur although these may not be captured directly by devices. For example material will leak out of the system, and consumers will not log the purchasing of products.

At some later stage it may be possible to track these activities, however the simulation of material and product flow requires that these activities occur.

### Consumers purchase and consume products
- Category: `consume`
- Activities: `consume`

### Material / products leak out of the system
- Category: `destroy`
- Activities: `destroy`