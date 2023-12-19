# Part 1

## User Stories

```
As a member of the public, so I can order a bagel when I want to, I'd like to add an item to my basket.

As a member of the public, so that I can change my order, I'd like to remove an item from my basket.
```

### Keywords

Verbs: order, add, change, remove
Nouns: member, public, bagel, item, basket

| Methods    | Inputs | Data | Scenario    | Outputs      |
|------------|--------|------|-------------|--------------|
| addItem(item)    | (item) | item: (@string), price: (@number) | if item is valid | add item to basket as a string |
||||item not valid| return "item not found"|
||||||
| removeItem(item) | (item) | item: (@string), price: (@number) | if item is valid and in basket | remove item from basket|
|||| no item added| return "item required"|

# Part 2

## User Stories

```
As a member of the public, so that I can not overfill my small bagel basket, I'd like to know when my basket is full when I try adding an item beyond my basket capacity.

As a Bob's Bagels manager, so that I can record more sales, I’d like to create baskets with larger capacity when I need to.

As a member of the public, so that I can maintain my sanity, I'd like to know if I try to remove an item that doesn't exist in my basket.
```

### Keywords

Verbs: overfill, know, adding, create, record, remove

Nouns: public, bagel, basket, manager, sales, capacity

| Methods| Inputs | Data| Scenario| Outputs|
|--------|--------|-----|---------|--------|
| basketCapacity   || totalCapacity: (@Number)| if basket equals basket full max items| return "Basket full, Please choose a bigger basket." |
||||||
| changeBasketSize | (Size) | Size: (@Number)| if changeBasketSize receives a number| change the basket size allowance|
|||| if changeBasketSize does not receive a number | return "error, set basket size"|
||||||
| removeItem| (item) | item: (@string), price: (@number) | if item does not exist in basket| return "false" and "item does not exist in basket"   |
|||| if item does exist in basket| return item.                                         |

# Part 3

## User Stories

```
As a member of the public, so that I can know how much my bagels are, I’d like to see the price of numbertem before I add it to my basket.

As a member of the public, so that I can buy many of my favorite bagels, I'd like to be able to add the same type of bagel to my basket more than once.

As a member of the public, so that I can prepare to pay, when I go to checkout, I'd like to know the total sum of the bagels in my basket.
```

### Keywords

Verbs: know, see, add, buy, pay, prepare

Nouns: member, public, bagels, price, banumbercheckout

| Methods   | Inputs | Data | Scenario| Outputs|
|-----------|--------|------|---------|--------|
| priceChecker | (item) | item: (@string)| if item in inventory exists| display item description and price |
|||| if item does not exist in inventory | return false|
||||||
| addItem   | (item) | item: (@string), price(@Number) | if item exists in basket| increase quantity by one|
|||| if item does not exist in basket| add item to basket|
||||||
| basketTotal ||totalPrice: (@Number)| if items in array| add all item prices as a number|
|||| if no items in array| return 0|
