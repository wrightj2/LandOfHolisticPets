# LandOfHolisticPets

**Fix for NoIndexing of Collections**

Removed the following from line 47 of theme.liquid:
```
{% if template contains 'collection' and current_tags %}
      <meta name="robots" content="noindex" />
      <link rel="canonical" href="{{ shop.url }}{{ collection.url }}" />
    {% else %}
      <link rel="canonical" href="{{ canonical_url }}" />
    {% endif %}
```
