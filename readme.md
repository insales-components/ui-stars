
```twig
<div class="star-rating-wrapper">
  <div class="star-rating">
    {% assign r = 5 %}
    {% for i in (1..5) %}
      <input name="review[rating]" id="star{{ r }}-{{ product.id }}" type="radio" name="reviewStars" class="star-radio"
             value="{{ r }}"/>
      <label title="{{ r }}" for="star{{ r }}-{{ product.id }}" class="star-label"></label>
      {% assign r = r | minus: 1 %}
    {% endfor %}
  </div>
</div>
```
