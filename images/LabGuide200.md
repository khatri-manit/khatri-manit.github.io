
# Lab 200

## Introduction


### Machine learning in ADWC

The first Machine learning model will help in deducing what are the chances of a particular Product in the inventory getting Perished.

Start the model by dropping off the previous tables which will be used in building the models.
Once the tables are dropped create the CUSTOMERS360 table which contains the featured information from the original l_marketbasket table.

![](./Capture1b.png)

Once the tables has been dropped the previous models as well as their settings has to be dropped.

![](./Capture2b.png)

Next the requisite algorithm and the corresponding parameters has to be imported in order to build the model. In this scenario Algorithm used is 'Support Vector Machines'. Explicitly the tables its corresponding featured column, on which the algorithm is applied, has to be mentioned. Based on all this informations the model is created.

![](./Capture3b.png)
![](./Capture4.png)

Once the model has been built , in order to find the top 5 perishable Product enter the following SQL command in a new paragraph of the notebook

![](./Capture5b.png)

The most perishable product in a particular day of the week can be found out using the following SQL command 

![](./Capture6b.png)

The Second model is built with Classification algorithm, tells us which products have the least probability of a sale. 

First step is to drop any pre configured table or settings

![](./Capture7b.png)

Then we start off with building the classification model and then generate a lift test and an apply test result

![](./Capture10.png)

The apply test result will give the products and with the least chances of them getting sold that particular day of the week .

![](./Capture9b.png)

Combining both prediction results and one can come up with a list of products that should be offered as a flash sale or similar promotional activities. 

![](./Capture11b.png)