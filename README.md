# LandOfHolisticPets

**Fix for NoIndexing of Collections with Tags**

Changed the following from line 47 of theme.liquid:
```
{% if template contains 'collection' and current_tags %}
      <meta name="robots" content="noindex" />
      <link rel="canonical" href="{{ shop.url }}{{ collection.url }}" />
    {% else %}
      <link rel="canonical" href="{{ canonical_url }}" />
    {% endif %}
```

To
```
{% if template contains 'collection' and current_tags %}
      <link rel="canonical" href="{{ shop.url }}{{ collection.url }}" />
    {% else %}
      <link rel="canonical" href="{{ canonical_url }}" />
    {% endif %}
```

**Fix sitewide broken JS**
Remove the following from line 140 of theme.liquid:
```
{% render 'upsell-now', customer: customer, product: product, template: template, cart: cart %}
```
