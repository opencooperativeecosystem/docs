Validate

Validation

Validation is specific to FairCoop operational requirements. Each economic event needs 2 validations from different people to be eligible for income distribution.

{% tabs %} {% tab title="Schema" %}

{  
  type: 'Validation',  
  validatedBy: Agent!,  
  validationDate: String,  
  economicEvent: EconomicEvent!
}

{% endtab %}

{% tab title="Example" %}

{  
  type: 'Validation',  
  validatedBy: {
    type: "Agent",
    id: "503",
    name: "Maro Horta",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },  
  validationDate: "2017-09-05",  
  economicEvent: {
    type:  'EconomicEvent',
    provider: {
      type: "Agent",
      id: "503",
      name: "Maro Horta",
      classification: "Person",
      image: "https://picsum.photos/200/300"
    },
    {
      type: "Agent",
      id: "239",
      name: "OpenCoopWork",
      classification: "Organization",
      image: "https://picsum.photos/200/300"
    },
    action:  "write",
    affectedQuantity: {
      quantity: 123.00,
      unit: "words"
    },
    date: "2017-09-05",
    resourceClassifiedAs: ResourceClassification!,
    note: "Dude you're getting a telescope",
    scope: {
      type: "Agent",
      id: "239",
      name: "OpenCoopWork",
      classification: "Organization",
      image: "https://picsum.photos/200/300"
    }
  }
}

{% endtab %} {% endtabs %}
