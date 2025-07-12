NOTE: _**THIS WILL WORK IN input HTML TAG ONLY !**_
1. In the root folder of your project install brq-smart-popup using following command

    **npm install https://github.com/brqsiva/brq-smart-popup**

2. Suppose you want to show data from JSON in your input field as suggestion, where the JSON data extracted from _https://dummyjson.com/products_ is structured like as follows,
    _<pre>{products": [
        {
          "id": 1,
          "title": "Essence Mascara Lash Princess",
          "description": "The Essence Mascara Lash Princess is a popular mascara known for its volumizing and lengthening effects. Achieve dramatic lashes with this long-lasting and cruelty-free formula.",
          "category": "beauty",
          "price": 9.99,
          "tags": [
            "beauty",
            "mascara"
          ]
        },
        {
          "id": 2,
          "title": "Eyeshadow Palette with Mirror",
          "description": "The Eyeshadow Palette with Mirror offers a versatile range of eyeshadow shades for creating stunning eye looks. With a built-in mirror, it's convenient for on-the-go makeup application.",
          "category": "beauty",
          "price": 19.99,
          "tags": [
            "beauty",
            "eyeshadow"
          ]
        }
      ]
    }</pre>_
   
and you want to show
 _title_, _description_, _category_, and _price_ 
in suggestion drop of the input, then you can call the component **brq-smart-popup** as below:
_**<pre><code>
&lt;BRQSmartPopup
  api="https://dummyjson.com/products"
  dataKey="products"
  displayFields={["title", "description", "category", "price"]}
  bindFields={{
    title: "title",
    description: "description",
    category: "category",
    price: "price"
  }}
/&gt;
</code></pre>**_

Here is the params explained!:  
_**api**_: The url which returns JSON data to bind.  
_**dataKey**_: The name of root node of JSON data.  
_**displayFields**_: List of fields in JSON to display in suggestian drop as array.  
_**bindFields**_: Pairing of input html with id to json data field as object.   


