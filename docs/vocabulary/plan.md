---
description: >-
  Planning could include Plans, Processes, Intents.  Planning is basically work
  to be done.  (Later planning might also be for production, distribution,
  exchanging of goods and services.)
---

# Plan

### Intent

An Intent is the minimal way of planning some work. 

{% tabs %}
{% tab title="Schema" %}
```javascript
{
  type: 'Intent',
  scope: Agent!,
  action:  String!,
  affectedQuantity: {
    quantity: Decimal,
    unit: String
  },
  due: String!,
  resourceClassifiedAs: ResourceClassification!,
  note: String,
  isFinished: Bool,
  inputOf: Process
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{
  type: 'Intent',
  scope: {
    type: "Agent",
    id: "239",
    name: "OpenCoopWork",
    classification: "Organization",
    image: "https://picsum.photos/200/300"
  },
  action:  "work",
  affectedQuantity: {
    quantity: "3.5",
    unit: "Hour"
  },
  dueDate: "2017-09-05",
  resourceClassifiedAs: ResourceClassification!,
  note: "Minor fixes on the responsive version",
  isFinished: false,
  inputOf: {  
    type: 'Process',
    name: 'Draft a new blog post',  
    note: 'Write about new roadmap and deadlines agreed on the 23 global assemblies',  
    plannedStart: '2017-09-03',  
    plannedDuration: '2017-09-05',  
    isFinished: true,  
    scope: {
      type: "Agent",
      id: "239",
      name: "OpenCoopWork",
      classification: "Organization",
      image: "https://picsum.photos/200/300"
    }
  }
}
```
{% endtab %}
{% endtabs %}

**Notes**

* **scope** is the agent that is the area, sub-area, or project
* **ResourceClassification** will be a taxonomy item from the taxonomy used across apps.
* **outputOf** Process, when a deliverable of a process is important in the planning

_Also might want at some point:_        
We might want at some point to also include _Commitment_, which is an Intent that someone has committed to do.    

### Process

Intents can be grouped into a process, although they wouldn't need to be.  A Process is an activity that transforms inputs into outputs. The outputs might then become inputs to other processes, forming networks and chains.  A process more minimally can just group work Intents, which are inputs.  \(In some apps, a Process might be Task, or might group Tasks.\)

{% tabs %}
{% tab title="Schema" %}
```javascript
{  
  type: 'Process',
  name: String!,  
  note: String,  
  plannedStart: String!,  
  plannedDuration: Int!,  
  isFinished: Bool,  
  scope: Agent!
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{  
  type: 'Process',
  name: 'Draft a new blog post',  
  note: 'Write about new roadmap and deadlines agreed on the 23 global assemblies',  
  plannedStart: '2017-09-03',  
  plannedDuration: '2017-09-05',  
  isFinished: true,  
  scope: {
    type: "Organization",
    id: "239",
    name: "OpenCoopWork",
    classification: "Organization",
    image: "https://picsum.photos/200/300"
  }
}
```
{% endtab %}
{% endtabs %}

**Notes**

* scope is the agent that is the area, sub-area, or project
* plannedStart is a date

### Plan

Processes can be grouped into a plan. A plan is a structured series of processes created to organize people and resources to obtain a specific result.  Plans can be simple or complex, say facilitation for a month, or a campaign including much connected work done across different projects

{% tabs %}
{% tab title="Schema" %}
```javascript
{
  type: 'Plan',
  name: String!,  
  note: String,  
  due: String
}
```
{% endtab %}

{% tab title="Example" %}
```javascript
{
  type: 'Plan',
  name: 'Develop and test the xyz feature and make a pull request',  
  note: 'When you browse through videos at YouTube, which do you usually click first: one with around 10 views or one with around 75,000 views? If you’re normal, then you’re much more likely to click on YouTube videos that have a lot of clicks already. The logic is simple. The more views a video has, the more interesting the video must be.',  
  due: '2017-09-05'
}
```
{% endtab %}
{% endtabs %}

**Notes**

* due is a date, and could also be derived from the due dates of the processes

_Also might want at some point_:        
A plan can include more than one deliverable, each of which contributes to the goal or outcome of the plan.    
Each deliverable can be produced by a chain of processes, where output \(an economic resource\) from one process is input to the next process.

