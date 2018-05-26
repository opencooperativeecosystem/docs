Resources
ResourceClassification

This is a global taxonomy. Data structure to be determined, but here is a simple possibility.

{% tabs %} {% tab title="Schema" %}

{
  type: 'ResourceClassification',
  name: String!,
  parent: ResourceClassification
}

{% endtab %}

{% tab title="Example" %}

{
  type: 'ResourceClassification',
  name: String!,
  parent: ResourceClassification
}

{% endtab %} {% endtabs %}
EconomicResource

A resource which is useful to people or the ecosystem.

{% tabs %} {% tab title="Schema" %}

{
  type: 'EconomicResource',
  resourceClassifiedAs: ResourceClassification!,
  trackingIdentifier: String,
  currentQuantity: {
    quantity: Decimal!,
    unit: Unit!
  },
  note: String,
  currentLocation: Location
}

{% endtab %}

{% tab title="Example" %}

{
  type: 'EconomicResource',
  resourceClassifiedAs: ResourceClassification!,
  trackingIdentifier: String,
  currentQuantity: {
    quantity: Decimal!,
    unit: Unit!
  },
  note: String,
}

{% endtab %} {% endtabs %}
Location

{% tabs %} {% tab title="Schema" %}

{
  type: 'Location',
  longitude: Decimal!,
  latitude: Decimal!
}

{% endtab %}

{% tab title="Example" %}

{
  type: 'Location',
  longitude: Decimal!,
  latitude: Decimal!
}

{% endtab %} {% endtabs %}
