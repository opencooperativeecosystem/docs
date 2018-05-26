# Economic Event

**Economic Event**  
 EconomicEvent is the minimum needed for recording work and distribution. EconomicEvent and Agent, plus the taxonomy, would be enough to provide a lot of the information needed for stats and accounting, if every app could provide just those.

{% tabs %} {% tab title="Schema" %}

```text
{
  type:  'EconomicEvent',
  provider: Agent!,
  receiver: Agent,
  action:  String!,
  affectedQuantity: {
    quantity: Decimal!,
    unit: String!
  },
  date: String!,
  resourceClassifiedAs: ResourceClassification!,
  note: String,
  scope: Agent
}
```

{% endtab %}

{% tab title="Example" %}

```text
{
  type:  'EconomicEvent',
  provider: {
    type: "Agent",
    id: "503",
    name: "Maro Horta",
    classification: "Person",
    image: "https://picsum.photos/200/300"
  },
  receiver: {
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
```

{% endtab %} {% endtabs %}

**Notes**

* ResourceClassification will be a taxonomy item from the taxonomy that is chosen by FairCoop to be used across apps. Right now CE is working on unifying the taxonomy, including skills.
* unit at some point will probably be from a list, instead of a string, so that units can be normalized across apps.
* action is "work" or "give", to cover just the requirements of work events and income payment events. There are other actions for when resources are being created or transported \(meaning there is a Process in addition to EconomicEvents\), like "use", "consume", "produce", and others.

_Also might want at some point_

**affects:** this is an EconomicResource, and used when something identifiable is involved, which could be a material or digital item that is recorded in inventory, or an account, say a FairCoin account\) **fulfills:** this is a Fulfillment of an Intent, or part of a plan, that is fulfilled completely or partially by the economic event\) - this would connect the plan to the work, and also add a piece of we would need to know what payment was done for what work \(what work is already paid\)

