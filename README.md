# Income Predictor

The dataset used to build the predicitve model is the adult dataset form the [UCI machine learning repository](http://archive.ics.uci.edu/ml/datasets/Adult).

## Key Observations

The dataset contains two attributes specific to each row as the target value, “>50k” for income over $50,000 and “<=50k” for income under $50,000 dollars. The dataset contains 32,560 entries excluding headers and 15 columns with 24 duplicate entries.

There isn't much diversity in the dataset for features such as capital gain, capital loss, work class, native country and race.

![Screen Shot 2020-04-29 at 7 48 57 PM](https://user-images.githubusercontent.com/33552991/80635188-7a7aac80-8a53-11ea-954e-e122bdea16cb.png)

![Screen Shot 2020-04-29 at 7 50 33 PM](https://user-images.githubusercontent.com/33552991/80635144-6931a000-8a53-11ea-9045-590ed802d7f8.png)

![Screen Shot 2020-04-29 at 7 50 24 PM](https://user-images.githubusercontent.com/33552991/80635150-6c2c9080-8a53-11ea-83c7-52639dfb8d96.png)

Furthermore, it is evident from the table below there is quite a bit of deviation in the dataset for hours per week, fnlwgt, capital loss and capital gain. Additionally, the box and whiskers plot below further solidifies the fact there are a significant number of outliers in these values. This is why the the `MinMax` scaler was used instead of the `Standard` scaler as the `MinMax` scaler is not sensitive to outliers.

![Screen Shot 2020-04-29 at 7 53 47 PM](https://user-images.githubusercontent.com/33552991/80635509-dcd3ad00-8a53-11ea-99c0-cdc19456ff13.png) ![Box](https://user-images.githubusercontent.com/33552991/80635517-dfce9d80-8a53-11ea-8d92-b5e9ccff7da1.png)

## Best Model

### XGBoost

**k-Fold Validation**: 87.1%

**Logarithmic Loss**: 4.25

![Screen Shot 2020-04-29 at 7 53 13 PM](https://user-images.githubusercontent.com/33552991/80635255-8fefd680-8a53-11ea-9495-2161f465552e.png)
