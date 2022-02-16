# The Power of the Calculated Field

While making applications, you will undoubtedly use constants or pre-defined default settings. Items that have a special meaning and a specific value that does not change. Well… at least not for a while, or not very often. So you might be inclined to just “hardcode” these values whenever applicable.\
But when they do need to be changed, you’ll have a hard time finding all the situations where they are hardcoded in the expressions and labels in your application.

Do you recognize any of the following?

* The email address you want to use as the default sender for all emails in the application.&#x20;
* The VAT-percentage in your financial calculations.&#x20;
* The API-key or token for external applications you use, like Google APIs.&#x20;
* Any pre-defined number or date to be used in some context.

In WEM, you can use a Calculated Field to hold these “constant” values and use this field in your expressions, templates, flows and calculations.\
This way, if the value needs to be changed, there is only one place in WEM where this needs to be done: the expression of the Calculated Field in the Data Model.

A Calculated Field can be any of the available WEM-Types (Text, Number, Date, Boolean, Single/Multi-select and even a File or Referenced list item).

![](https://github.com/zoombim/Public-Documentation/tree/09466aea1b73d2e87a60fac4ae6557406b4c032f/public-documentation/.gitbook/assets/tips-and-tricks.data.calculated-fields.png)

Calculated Fields can be used in the expressions of other calculated fields. This makes way for some powerful stuff, so be smart and don’t go circular…

Advantage 1: you can find all the usages of a Calculated Field throughout your project with one click on button `Find Usages`.

Advantage 2: if you know a change is coming in the future, you can put this in the calculation expression. So you can prepare the change in advance and not worry when the time comes to make the changes.

So, whenever you feel the urge to put a seemingly constant value directly into an expression, stop and think whether a Calculated Field might be the better option.

Don’t forget to organize your Calculated Fields cleverly: put them in a logical place within your Data Model and give them names that instantly clarifies their intended purpose.
