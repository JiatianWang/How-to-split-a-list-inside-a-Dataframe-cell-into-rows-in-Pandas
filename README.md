# How-to-split-a-list-inside-a-Dataframe-cell-into-rows-in-

## This short tutorial is about how to split a list in a dataframe in to rows.

The csv file is from my personal project TED talk analysis.

What is going to be dealt with is showing down below

![Capture1](https://user-images.githubusercontent.com/32876600/89109487-7d4cbb00-d40f-11ea-9aa7-555b735bfce0.JPG)

The libiary I used here are Pandas, Numpy, ast

ast.literal_eval is used to raise an exception if the input isn't a valid Python datatype, so the code won't be executed if it's not.

## Steps:
1, Ignore invalid python datatype

2, Use df.apply(pd.Series) to split the lists(which contains a list of values) into new columns. and the output preserves the index

![Capture2](https://user-images.githubusercontent.com/32876600/89109489-7f167e80-d40f-11ea-8828-9ac2c90ddb3e.JPG)

3, use stack method to make it to one column record

![Capture3](https://user-images.githubusercontent.com/32876600/89109490-8047ab80-d40f-11ea-8bee-dc33d141f659.JPG)

4, merge the columns with the rest of dataset,using the same index attribute(left_index = True,right_index = True)

![Capture4](https://user-images.githubusercontent.com/32876600/89109491-82116f00-d40f-11ea-9a89-da980572f231.JPG)
