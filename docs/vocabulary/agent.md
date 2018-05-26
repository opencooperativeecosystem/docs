---
description: Description of basic agent data structures
---

# Agent

### Agent

{% tabs %}
{% tab title="Schema" %}
```javascript
{
  type: "Agent",
  id: String!,
  name: String!,
  classification: String!,
  image: String,
  primaryLocation: Location,
  note: String
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{
  type: "Agent",
  id: "503",
  name: "Maro Horta",
  classification: "Person",
  image: "https://picsum.photos/200/300"
}
```
{% endtab %}
{% endtabs %}

**Notes**  
_Classification_ is "Person" or "Organization".  
_Also might want at some point_  
user-defined relationships with other agents \(such as membership, sub-groups, etc\)  


### AgentRelationship

{% tabs %}
{% tab title="Schema" %}
```javascript
{
  type: 'AgentRelationship',
  subject: Agent!,
  object: Agent!,
  relationship: AgentRelationshipRole!    
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{
  type: 'AgentRelationship',
  subject: Agent!,
  object: Agent!,
  relationship: AgentRelationshipRole!    
}
```
{% endtab %}
{% endtabs %}

### AgentRelationshipRole

{% tabs %}
{% tab title="Schema" %}
```javascript
{
  type: 'AgentRelationshipRole',
  label: String!,
  reverseLabel: String!
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{
  type: 'AgentRelationshipRole',
  label: String!,
  reverseLabel: String!
}
```
{% endtab %}
{% endtabs %}

