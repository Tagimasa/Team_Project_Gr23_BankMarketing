# Client forecasting tool#

The purpose of this folder is to create a reproducible approach for "bank manager" to generate a list of "Yes" clients for future promotional or subscription campaigns.

What does this mean?

1/ We create the "Template Dataset" – *02_Template_Dataset_for_y_prediction.csv*, which any manager can fill with new data (the only requirement is to use the same columns with the same features).

2/ After that, the "manager" simply runs the code in *01_Prediction_code.ipynb*.

3/ The result will be an automatically created file with the predicted "Yes" or "No" for every client - an example is *03_Predicted _yes_no_clients.csv*.

Of course, it would be great to provide a special user interface, but that is not the goal of this project.

The same approach and the tools used could easily be adapted for many small and medium-sized businesses here in Canada (such as convenience stores, pet food retailers, artisanal products, bookstores, souvenirs, arts, farmers’ markets, etc.) to help increase their competitiveness against larger, monopolistic networks.