---
layout: post
title: "Entity Relationship Reflection"
author: JC Ntambara
---

## Description: 

"Your local grocery store would like your help in creating an online grocery shopping web application. The owner of the store will be able to list items for sale, where the items have a name, price, description, quantity available, and a manufacturer. Customers will be able to go to the site and register to create an account, entering in their name, address, and phone number. Once registered, customers will be able to start an order for pickup or delivery. The customer can select from the food items the store has for sale. When an item is selected, the customer will note the quantity desired, any special instructions, and if this item can be substituted if the store is out of stock. Finally, when the customer finalizes their order, they will be able to choose a time and date for their order to be fulfilled. Finalized orders can no longer be changed by the customer."


### ER Implementation Assumptions

From the given description above, I assumed that the entire model is going to be based on the store, which resulted in me not including the store or the store owner as entities. I considered the idea that this whole process is going to involve customers, items, and orders connected with each other based on their relationship. Therefore, my assumption was that it was probably important to create three entities, with each entity having it's own given attributes. There are some extra information that I considered leaving out because I didn't figure out where they should fit in my three entities, and I assumed they are not necessary as long as the important information in regards to the connection was included.

### LucidChat ER Diagram

![ER-Modeling]({{"/assets/images/LAB6-ERM.png" | relative_url}}){:width="100%"}

The above Entity RElationship Diagram shows the aforementioned three entities. The first entity being Item, has all the given attributes and as shown, it is connected to Order entity which also has its attributes. An order can include zero or many item and some items can be ordered as well. Notice that we have quantity available in the Item entity, but we also need to have quantity ordered as shown as an attribute to Includes. Finally, customer as a third entity should also have its attribute as provided in the description. A customer should be able to create zero to many orders, and if there is an order, there must be a customer who ordered it. 

### Vertabelo Schema

![Schema]({{"/assets/images/ER-schema.png" | relative_url}}){:width="100%"}

This vertabelo schema is also the exact same representation of the things I mentioned about the ER-Diagram, except that it's represented in tables. The Item is connected to the Order by Includes which brings in all the primary keys of both Item and Order as Foreign Keys. Additionally, Customer table is also connected to Order because as I mentioned earlier, a customer should be able to create an order and zero or many orders should belong to a customer. 

### How I feel about the resulting data representation and some complications I could encounter implementing this model

From my point of view, I feel like the represented data above makes more sense at least enough to meet the interaction between the store, customers, items, and orders. If anything goes wrong in the implementation, that could probably be due to some missing information, but other than that I am not able to notice a lot of complications from the representations above. 



