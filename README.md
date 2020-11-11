## MARKET BASKET ANALYSIS
We all have been shopping more from online e-commerce sites recently, probably due to the lock-down imposed in most parts of the world. You must have noticed an up-sell feature named ‘frequently bought together’ in most of these sites, for instance Amazon where it predicts what all items would go-along with the item that you have just added to the cart. Customers are given the choice of adding all the items shown under this feature to the cart or select the required ones. Amazon does it thorough what they call ‘item-to-item collaborative filtering’ where it runs recommendation algorithms based on the item-search history of the customer to improve the shopping experience. In the case of offline retailers, it works pretty much the same. Let us consider the basic example of Bread and Jam. If the retailer finds that there is an increase in the sales of bread, he can further up-sell by giving a discount in the price of jam, so that more customers are bound to buy them together.
This entire process of analyzing the shopping trends of customers is called ‘Market Basket Analysis’. It is an analyzing technique based on the idea that if we buy an item then we are bound to buy or not-buy a group (or single) items. For example, if a customer is buying bread then the chances of him/her buying jam is more. This is represented by the following equation:
# A->B(Association Mining Rule)
This equation is called the Association Mining Rule. This can be thought of as an IF-THEN relationship. If item A is bought by a customer then the chances of item B being bought by the same user in the same transaction is found out. Here A is called the Antecedent and B the consequent. Antecedents are primary item that are found in the basket and consequents are the items that are found with an antecedent/group of antecedents. 
The metrics for measuring association are:
# Support: It tells us about the combination of items bought together frequently. It gives the part of transactions that contain both A and B. We can filter out the less frequently occurring items-sets using support.
# Confidence: It tells us how frequently the items A and B are bought together, for the no. of times A is bought.
# Lift: It indicates the strength of a rule over the randomness of A and B being bought together. It basically measures the strength of any association rule(we will talk about association rules below).
More the lift more is the strength of the rule. If the lift is 3 for A -> B then it means if we buy A, the chances of buying B is 3 times.
So the process is to make rules for each item-set to figure out the metrics of its association so as to decide whether to include it in the analysis or not. But consider a large data-set having millions of user and transactions, thereby producing a large amount of item-sets. So to make rules for all of these would be a humongous task. This is where Apriori algorithm enters the scene.
# Apriori algorithm uses frequently bought item-sets to generate association rules. It is built on the idea that the subset of a frequently bought items-set is also a frequently bought item-set. Frequently bought item-sets are decided if their support value is above a minimum threshold support value.
