## CSS Flexbox
Flexbox stands for flexible box.
To create a flexbox you need to set the display of the container as flex

> Eg: {display: flex;}

 

This element is called the flex container, and stores the sub-elements which are known as flex items
---
### Flex container properties
1: Flex Direction
  - column
  - row (default)
  - row reverse
  - column reverse

2: Flex Wrap
- wrap
- no wrap ( default) 
  
By using this property we can make our elements responsive for different screen sizes.
 ![alt text](<Screenshot 2024-04-05 234215.png>)
3: Justify content
<br>
This property is used to set the position of content or rather align content along the main axis.
- center
- flex-end
- flex-start
- space between
- space around

4:Align Items
<br>
Just like the justify-content property, align-items define the alignment of the flex container but along the cross-axis.
- center
- flex-end
- flex-start
- space between
- space around

### Flex items properties

1. Align Self
<br>
This property allows default alignment to be overridden for the individual flex items. Try adding inline CSS to see how this property is used.

2. Order
3. <br>
4. Default order of items in flex container is 0 for all. Overriding with any vaule causes it to flow to last depending on order


---
### Other properties:
- Dont use padding in flexbox.
- Use `gap` property.
- `gap` can be `row-gap` or `column-gap` or just gap.

