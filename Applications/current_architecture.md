---
id: current_architecture
title: Current architecture
---

![Current Architecture]( https://github.com/opencooperativeecosystem/website/blob/master/Applications/ocp-state.png )

### Descriptions

#### Value Network \(original "OCP"\)

In the diagram, the rectangles inside the yellow ValueNetwork box are django apps within one django project.  There are also some user related apps not shown. There is a graphql api in development that currently supports the "new UI" work and Kispagi.  Mostly this reflects the Value Accounting app.

The Work App was created when NRP was forked to become OCP.  It has some of the original NRP pages copied there, and improved, plus new features of integration with FairCoin, membership processes, etc.  The Value Accounting App is the original NRP with a few upgrades, and being used as the "admin app" for admin people and when a function has not yet been moved to the work app.

#### Odoo

FairMarket was customized on top of Odoo.  There are no current integrations, but interoperability with OCP has been discussed.

Freedom Coop Invoicing is in process now, customizing Odoo.  It uses the agents and membership from the Value Accounting app.

#### Kispagi

Kispagi is a new app for OCW group within FairCoop, and gets work data from the Value Accounting app and Gitlab.

#### Gitlab

Gitlab is used for managing work by some groups.

#### Kanban \("New UI"\)

The "new UI" is in process, currently focused on coordinating work.  It is written in React, Apollo, and gets all of its data from the graphql api for the Value Accounting app.

#### Integral Dashboard

This is currently the same architecture as the Kanban.

#### FairCoin Wallet

#### Multicurrency Wallet
