
# Live Session Assignment 13
# Alex Norman
## Question 1: Create a list named my_list in python with the following data points - 45.4 44.2 36.8 35.1 39.0 60.0 47.4 41.1 45.8 35.6 


```python
my_list = [45.4, 44.2, 36.8, 35.1, 39.0, 60.0, 47.4, 41.1, 45.8, 35.6]
```

### Part A: Print the 5th element in the list


```python
my_list[4]
```




    39.0



### Part B: Append 55.2 to my_list


```python
my_list.append(55.2)
```

### Part C: Remove the 6th element in the list


```python
my_list.pop(5)
```




    60.0



### Part D: Iterate over the list to print data points greater than 45


```python
for i in range(10):
    if my_list[i-1] > 45:
        print(my_list[i-1])
```

    55.2
    45.4
    47.4
    45.8


## Question 2: Introduction to numpy  
### Part A: Import the numpy library using the following command – import numpy


```python
import numpy
```

### Part B: Declare numpy array with the same data points as in my_list using numpy.array()


```python
 data = numpy.array(my_list)
```

### Part C: Compute the mean and standard deviation using numpy.mean() and numpy.std() of the above array


```python
numpy.mean(data) 
```




    42.560000000000002




```python
 numpy.std(data)
```




    5.9709630713981143



### Part D: Use logical referencing to get only those values that are less than 45


```python
numpy.array(my_list)[numpy.array(numpy.where(numpy.less(my_list, 45)))]
```




    array([[ 44.2,  36.8,  35.1,  39. ,  41.1,  35.6]])



### Part E: Compute the max and min of the array using numpy.max() and numpy.min()


```python
numpy.max(data)
```




    55.200000000000003




```python
numpy.min(data)
```




    35.100000000000001



## Question 3: Introduction to pandas
### Part A: Import the pandas library 


```python
import pandas
```

### Part B: Read the IRIS dataset into iris using pandas.read_csv(). 


```python
iris = pandas.read_csv("/Users/alexnorman/Desktop/Alex's class/Iris.csv")
```

### Part C: Using iris.head(), display the head of the dataset.


```python
iris.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
      <th>Species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
  </tbody>
</table>
</div>



### Part D: Use DataFrame.drop() to drop the id column.


```python
iris.drop('Id', axis = 1)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
      <th>Species</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>1</th>
      <td>4.9</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>2</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.3</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4.6</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5.0</td>
      <td>3.6</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>5</th>
      <td>5.4</td>
      <td>3.9</td>
      <td>1.7</td>
      <td>0.4</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>6</th>
      <td>4.6</td>
      <td>3.4</td>
      <td>1.4</td>
      <td>0.3</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>7</th>
      <td>5.0</td>
      <td>3.4</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>8</th>
      <td>4.4</td>
      <td>2.9</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>9</th>
      <td>4.9</td>
      <td>3.1</td>
      <td>1.5</td>
      <td>0.1</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>10</th>
      <td>5.4</td>
      <td>3.7</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>11</th>
      <td>4.8</td>
      <td>3.4</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>12</th>
      <td>4.8</td>
      <td>3.0</td>
      <td>1.4</td>
      <td>0.1</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>13</th>
      <td>4.3</td>
      <td>3.0</td>
      <td>1.1</td>
      <td>0.1</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>14</th>
      <td>5.8</td>
      <td>4.0</td>
      <td>1.2</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>15</th>
      <td>5.7</td>
      <td>4.4</td>
      <td>1.5</td>
      <td>0.4</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>16</th>
      <td>5.4</td>
      <td>3.9</td>
      <td>1.3</td>
      <td>0.4</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>17</th>
      <td>5.1</td>
      <td>3.5</td>
      <td>1.4</td>
      <td>0.3</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>18</th>
      <td>5.7</td>
      <td>3.8</td>
      <td>1.7</td>
      <td>0.3</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>19</th>
      <td>5.1</td>
      <td>3.8</td>
      <td>1.5</td>
      <td>0.3</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>20</th>
      <td>5.4</td>
      <td>3.4</td>
      <td>1.7</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>21</th>
      <td>5.1</td>
      <td>3.7</td>
      <td>1.5</td>
      <td>0.4</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>22</th>
      <td>4.6</td>
      <td>3.6</td>
      <td>1.0</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>23</th>
      <td>5.1</td>
      <td>3.3</td>
      <td>1.7</td>
      <td>0.5</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>24</th>
      <td>4.8</td>
      <td>3.4</td>
      <td>1.9</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>25</th>
      <td>5.0</td>
      <td>3.0</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>26</th>
      <td>5.0</td>
      <td>3.4</td>
      <td>1.6</td>
      <td>0.4</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>27</th>
      <td>5.2</td>
      <td>3.5</td>
      <td>1.5</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>28</th>
      <td>5.2</td>
      <td>3.4</td>
      <td>1.4</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>29</th>
      <td>4.7</td>
      <td>3.2</td>
      <td>1.6</td>
      <td>0.2</td>
      <td>Iris-setosa</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>120</th>
      <td>6.9</td>
      <td>3.2</td>
      <td>5.7</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>121</th>
      <td>5.6</td>
      <td>2.8</td>
      <td>4.9</td>
      <td>2.0</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>122</th>
      <td>7.7</td>
      <td>2.8</td>
      <td>6.7</td>
      <td>2.0</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>123</th>
      <td>6.3</td>
      <td>2.7</td>
      <td>4.9</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>124</th>
      <td>6.7</td>
      <td>3.3</td>
      <td>5.7</td>
      <td>2.1</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>125</th>
      <td>7.2</td>
      <td>3.2</td>
      <td>6.0</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>126</th>
      <td>6.2</td>
      <td>2.8</td>
      <td>4.8</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>127</th>
      <td>6.1</td>
      <td>3.0</td>
      <td>4.9</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>128</th>
      <td>6.4</td>
      <td>2.8</td>
      <td>5.6</td>
      <td>2.1</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>129</th>
      <td>7.2</td>
      <td>3.0</td>
      <td>5.8</td>
      <td>1.6</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>130</th>
      <td>7.4</td>
      <td>2.8</td>
      <td>6.1</td>
      <td>1.9</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>131</th>
      <td>7.9</td>
      <td>3.8</td>
      <td>6.4</td>
      <td>2.0</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>132</th>
      <td>6.4</td>
      <td>2.8</td>
      <td>5.6</td>
      <td>2.2</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>133</th>
      <td>6.3</td>
      <td>2.8</td>
      <td>5.1</td>
      <td>1.5</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>134</th>
      <td>6.1</td>
      <td>2.6</td>
      <td>5.6</td>
      <td>1.4</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>135</th>
      <td>7.7</td>
      <td>3.0</td>
      <td>6.1</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>136</th>
      <td>6.3</td>
      <td>3.4</td>
      <td>5.6</td>
      <td>2.4</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>137</th>
      <td>6.4</td>
      <td>3.1</td>
      <td>5.5</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>138</th>
      <td>6.0</td>
      <td>3.0</td>
      <td>4.8</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>139</th>
      <td>6.9</td>
      <td>3.1</td>
      <td>5.4</td>
      <td>2.1</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>140</th>
      <td>6.7</td>
      <td>3.1</td>
      <td>5.6</td>
      <td>2.4</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>141</th>
      <td>6.9</td>
      <td>3.1</td>
      <td>5.1</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>142</th>
      <td>5.8</td>
      <td>2.7</td>
      <td>5.1</td>
      <td>1.9</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>143</th>
      <td>6.8</td>
      <td>3.2</td>
      <td>5.9</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>144</th>
      <td>6.7</td>
      <td>3.3</td>
      <td>5.7</td>
      <td>2.5</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>145</th>
      <td>6.7</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>146</th>
      <td>6.3</td>
      <td>2.5</td>
      <td>5.0</td>
      <td>1.9</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>147</th>
      <td>6.5</td>
      <td>3.0</td>
      <td>5.2</td>
      <td>2.0</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>148</th>
      <td>6.2</td>
      <td>3.4</td>
      <td>5.4</td>
      <td>2.3</td>
      <td>Iris-virginica</td>
    </tr>
    <tr>
      <th>149</th>
      <td>5.9</td>
      <td>3.0</td>
      <td>5.1</td>
      <td>1.8</td>
      <td>Iris-virginica</td>
    </tr>
  </tbody>
</table>
<p>150 rows × 5 columns</p>
</div>



### Part E: Subset dataframe to create a new data frame that includes only the measurements for the setosa species.


```python
setosa = iris[iris.Species == 'Iris-setosa']
```

### Part F: Use DataFrame.describe() to get the summary statistics


```python
iris.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>150.000000</td>
      <td>150.000000</td>
      <td>150.000000</td>
      <td>150.000000</td>
      <td>150.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>75.500000</td>
      <td>5.843333</td>
      <td>3.054000</td>
      <td>3.758667</td>
      <td>1.198667</td>
    </tr>
    <tr>
      <th>std</th>
      <td>43.445368</td>
      <td>0.828066</td>
      <td>0.433594</td>
      <td>1.764420</td>
      <td>0.763161</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.000000</td>
      <td>4.300000</td>
      <td>2.000000</td>
      <td>1.000000</td>
      <td>0.100000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>38.250000</td>
      <td>5.100000</td>
      <td>2.800000</td>
      <td>1.600000</td>
      <td>0.300000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>75.500000</td>
      <td>5.800000</td>
      <td>3.000000</td>
      <td>4.350000</td>
      <td>1.300000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>112.750000</td>
      <td>6.400000</td>
      <td>3.300000</td>
      <td>5.100000</td>
      <td>1.800000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>150.000000</td>
      <td>7.900000</td>
      <td>4.400000</td>
      <td>6.900000</td>
      <td>2.500000</td>
    </tr>
  </tbody>
</table>
</div>




```python
setosa.describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Id</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>count</th>
      <td>50.00000</td>
      <td>50.00000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.00000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>25.50000</td>
      <td>5.00600</td>
      <td>3.418000</td>
      <td>1.464000</td>
      <td>0.24400</td>
    </tr>
    <tr>
      <th>std</th>
      <td>14.57738</td>
      <td>0.35249</td>
      <td>0.381024</td>
      <td>0.173511</td>
      <td>0.10721</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.00000</td>
      <td>4.30000</td>
      <td>2.300000</td>
      <td>1.000000</td>
      <td>0.10000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>13.25000</td>
      <td>4.80000</td>
      <td>3.125000</td>
      <td>1.400000</td>
      <td>0.20000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>25.50000</td>
      <td>5.00000</td>
      <td>3.400000</td>
      <td>1.500000</td>
      <td>0.20000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>37.75000</td>
      <td>5.20000</td>
      <td>3.675000</td>
      <td>1.575000</td>
      <td>0.30000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>50.00000</td>
      <td>5.80000</td>
      <td>4.400000</td>
      <td>1.900000</td>
      <td>0.60000</td>
    </tr>
  </tbody>
</table>
</div>



### Part G: Use DataFrame.groupby() to create grouped data frames by Species and compute summary statistics using DataFrame.describe()


```python
iris.groupby(iris['Species']).describe()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th></th>
      <th>Id</th>
      <th>PetalLengthCm</th>
      <th>PetalWidthCm</th>
      <th>SepalLengthCm</th>
      <th>SepalWidthCm</th>
    </tr>
    <tr>
      <th>Species</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="8" valign="top">Iris-setosa</th>
      <th>count</th>
      <td>50.00000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>25.50000</td>
      <td>1.464000</td>
      <td>0.244000</td>
      <td>5.006000</td>
      <td>3.418000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>14.57738</td>
      <td>0.173511</td>
      <td>0.107210</td>
      <td>0.352490</td>
      <td>0.381024</td>
    </tr>
    <tr>
      <th>min</th>
      <td>1.00000</td>
      <td>1.000000</td>
      <td>0.100000</td>
      <td>4.300000</td>
      <td>2.300000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>13.25000</td>
      <td>1.400000</td>
      <td>0.200000</td>
      <td>4.800000</td>
      <td>3.125000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>25.50000</td>
      <td>1.500000</td>
      <td>0.200000</td>
      <td>5.000000</td>
      <td>3.400000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>37.75000</td>
      <td>1.575000</td>
      <td>0.300000</td>
      <td>5.200000</td>
      <td>3.675000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>50.00000</td>
      <td>1.900000</td>
      <td>0.600000</td>
      <td>5.800000</td>
      <td>4.400000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">Iris-versicolor</th>
      <th>count</th>
      <td>50.00000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>75.50000</td>
      <td>4.260000</td>
      <td>1.326000</td>
      <td>5.936000</td>
      <td>2.770000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>14.57738</td>
      <td>0.469911</td>
      <td>0.197753</td>
      <td>0.516171</td>
      <td>0.313798</td>
    </tr>
    <tr>
      <th>min</th>
      <td>51.00000</td>
      <td>3.000000</td>
      <td>1.000000</td>
      <td>4.900000</td>
      <td>2.000000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>63.25000</td>
      <td>4.000000</td>
      <td>1.200000</td>
      <td>5.600000</td>
      <td>2.525000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>75.50000</td>
      <td>4.350000</td>
      <td>1.300000</td>
      <td>5.900000</td>
      <td>2.800000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>87.75000</td>
      <td>4.600000</td>
      <td>1.500000</td>
      <td>6.300000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>100.00000</td>
      <td>5.100000</td>
      <td>1.800000</td>
      <td>7.000000</td>
      <td>3.400000</td>
    </tr>
    <tr>
      <th rowspan="8" valign="top">Iris-virginica</th>
      <th>count</th>
      <td>50.00000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>mean</th>
      <td>125.50000</td>
      <td>5.552000</td>
      <td>2.026000</td>
      <td>6.588000</td>
      <td>2.974000</td>
    </tr>
    <tr>
      <th>std</th>
      <td>14.57738</td>
      <td>0.551895</td>
      <td>0.274650</td>
      <td>0.635880</td>
      <td>0.322497</td>
    </tr>
    <tr>
      <th>min</th>
      <td>101.00000</td>
      <td>4.500000</td>
      <td>1.400000</td>
      <td>4.900000</td>
      <td>2.200000</td>
    </tr>
    <tr>
      <th>25%</th>
      <td>113.25000</td>
      <td>5.100000</td>
      <td>1.800000</td>
      <td>6.225000</td>
      <td>2.800000</td>
    </tr>
    <tr>
      <th>50%</th>
      <td>125.50000</td>
      <td>5.550000</td>
      <td>2.000000</td>
      <td>6.500000</td>
      <td>3.000000</td>
    </tr>
    <tr>
      <th>75%</th>
      <td>137.75000</td>
      <td>5.875000</td>
      <td>2.300000</td>
      <td>6.900000</td>
      <td>3.175000</td>
    </tr>
    <tr>
      <th>max</th>
      <td>150.00000</td>
      <td>6.900000</td>
      <td>2.500000</td>
      <td>7.900000</td>
      <td>3.800000</td>
    </tr>
  </tbody>
</table>
</div>



### Part H: Use DataFrame.boxplot() to plot boxplots by Species


```python
iris.groupby(iris['Species']).boxplot()
```

    //anaconda/lib/python3.5/site-packages/pandas/tools/plotting.py:3082: FutureWarning: 
    The default value for 'return_type' will change to 'axes' in a future release.
     To use the future behavior now, set return_type='axes'.
     To keep the previous behavior and silence this warning, set return_type='dict'.
      rot=rot, grid=grid, **kwds)





    OrderedDict([('Iris-setosa',
                  {'boxes': [<matplotlib.lines.Line2D at 0x1153325c0>,
                    <matplotlib.lines.Line2D at 0x11535d278>,
                    <matplotlib.lines.Line2D at 0x11536eba8>,
                    <matplotlib.lines.Line2D at 0x115383518>,
                    <matplotlib.lines.Line2D at 0x115395e48>],
                   'caps': [<matplotlib.lines.Line2D at 0x1153549e8>,
                    <matplotlib.lines.Line2D at 0x11533a128>,
                    <matplotlib.lines.Line2D at 0x115363b70>,
                    <matplotlib.lines.Line2D at 0x115368a58>,
                    <matplotlib.lines.Line2D at 0x115379b70>,
                    <matplotlib.lines.Line2D at 0x115379cf8>,
                    <matplotlib.lines.Line2D at 0x11538ae10>,
                    <matplotlib.lines.Line2D at 0x115390cf8>,
                    <matplotlib.lines.Line2D at 0x1153a0e10>,
                    <matplotlib.lines.Line2D at 0x1153a0f98>],
                   'fliers': [<matplotlib.lines.Line2D at 0x115358ac8>,
                    <matplotlib.lines.Line2D at 0x11536eac8>,
                    <matplotlib.lines.Line2D at 0x11537fd68>,
                    <matplotlib.lines.Line2D at 0x115395d68>,
                    <matplotlib.lines.Line2D at 0x1153a8f98>],
                   'means': [],
                   'medians': [<matplotlib.lines.Line2D at 0x1153582b0>,
                    <matplotlib.lines.Line2D at 0x115368be0>,
                    <matplotlib.lines.Line2D at 0x11537f550>,
                    <matplotlib.lines.Line2D at 0x115390e80>,
                    <matplotlib.lines.Line2D at 0x1153a87f0>],
                   'whiskers': [<matplotlib.lines.Line2D at 0x115332e80>,
                    <matplotlib.lines.Line2D at 0x11533e898>,
                    <matplotlib.lines.Line2D at 0x11535db00>,
                    <matplotlib.lines.Line2D at 0x1153639e8>,
                    <matplotlib.lines.Line2D at 0x115375b00>,
                    <matplotlib.lines.Line2D at 0x115375c88>,
                    <matplotlib.lines.Line2D at 0x115383da0>,
                    <matplotlib.lines.Line2D at 0x11538ac88>,
                    <matplotlib.lines.Line2D at 0x11539cda0>,
                    <matplotlib.lines.Line2D at 0x11539cf28>]}),
                 ('Iris-versicolor',
                  {'boxes': [<matplotlib.lines.Line2D at 0x1152397f0>,
                    <matplotlib.lines.Line2D at 0x1153b6eb8>,
                    <matplotlib.lines.Line2D at 0x1153d0828>,
                    <matplotlib.lines.Line2D at 0x1153e6198>,
                    <matplotlib.lines.Line2D at 0x1153f7ac8>],
                   'caps': [<matplotlib.lines.Line2D at 0x11533ea90>,
                    <matplotlib.lines.Line2D at 0x1153179e8>,
                    <matplotlib.lines.Line2D at 0x1153c6e80>,
                    <matplotlib.lines.Line2D at 0x1153c6f98>,
                    <matplotlib.lines.Line2D at 0x1153da7f0>,
                    <matplotlib.lines.Line2D at 0x1153daef0>,
                    <matplotlib.lines.Line2D at 0x1153eca90>,
                    <matplotlib.lines.Line2D at 0x1153f3978>,
                    <matplotlib.lines.Line2D at 0x115401a90>,
                    <matplotlib.lines.Line2D at 0x115401c18>],
                   'fliers': [<matplotlib.lines.Line2D at 0x1152ffda0>,
                    <matplotlib.lines.Line2D at 0x1153d0748>,
                    <matplotlib.lines.Line2D at 0x1153e1f98>,
                    <matplotlib.lines.Line2D at 0x1153f79e8>,
                    <matplotlib.lines.Line2D at 0x115408c88>],
                   'means': [],
                   'medians': [<matplotlib.lines.Line2D at 0x11526a7b8>,
                    <matplotlib.lines.Line2D at 0x1153ca860>,
                    <matplotlib.lines.Line2D at 0x1153e11d0>,
                    <matplotlib.lines.Line2D at 0x1153f3b00>,
                    <matplotlib.lines.Line2D at 0x115408470>],
                   'whiskers': [<matplotlib.lines.Line2D at 0x115226da0>,
                    <matplotlib.lines.Line2D at 0x1153b1358>,
                    <matplotlib.lines.Line2D at 0x1153bee10>,
                    <matplotlib.lines.Line2D at 0x1153bef98>,
                    <matplotlib.lines.Line2D at 0x1153d6780>,
                    <matplotlib.lines.Line2D at 0x1153d6f98>,
                    <matplotlib.lines.Line2D at 0x1153e6fd0>,
                    <matplotlib.lines.Line2D at 0x1153ec908>,
                    <matplotlib.lines.Line2D at 0x1153fda20>,
                    <matplotlib.lines.Line2D at 0x1153fdba8>]}),
                 ('Iris-virginica',
                  {'boxes': [<matplotlib.lines.Line2D at 0x115286a58>,
                    <matplotlib.lines.Line2D at 0x11542a198>,
                    <matplotlib.lines.Line2D at 0x11543aac8>,
                    <matplotlib.lines.Line2D at 0x115452438>,
                    <matplotlib.lines.Line2D at 0x115462d68>],
                   'caps': [<matplotlib.lines.Line2D at 0x11541d7f0>,
                    <matplotlib.lines.Line2D at 0x11541def0>,
                    <matplotlib.lines.Line2D at 0x11542ea90>,
                    <matplotlib.lines.Line2D at 0x115435978>,
                    <matplotlib.lines.Line2D at 0x115446a90>,
                    <matplotlib.lines.Line2D at 0x115446c18>,
                    <matplotlib.lines.Line2D at 0x115455d30>,
                    <matplotlib.lines.Line2D at 0x11545bc18>,
                    <matplotlib.lines.Line2D at 0x11546ed30>,
                    <matplotlib.lines.Line2D at 0x11546eeb8>],
                   'fliers': [<matplotlib.lines.Line2D at 0x115424f98>,
                    <matplotlib.lines.Line2D at 0x11543a9e8>,
                    <matplotlib.lines.Line2D at 0x11544cc88>,
                    <matplotlib.lines.Line2D at 0x115462c88>,
                    <matplotlib.lines.Line2D at 0x115473f28>],
                   'means': [],
                   'medians': [<matplotlib.lines.Line2D at 0x1154241d0>,
                    <matplotlib.lines.Line2D at 0x115435b00>,
                    <matplotlib.lines.Line2D at 0x11544c470>,
                    <matplotlib.lines.Line2D at 0x11545bda0>,
                    <matplotlib.lines.Line2D at 0x115473710>],
                   'whiskers': [<matplotlib.lines.Line2D at 0x1152867f0>,
                    <matplotlib.lines.Line2D at 0x115418f98>,
                    <matplotlib.lines.Line2D at 0x11542afd0>,
                    <matplotlib.lines.Line2D at 0x11542e908>,
                    <matplotlib.lines.Line2D at 0x115440a20>,
                    <matplotlib.lines.Line2D at 0x115440ba8>,
                    <matplotlib.lines.Line2D at 0x115452cc0>,
                    <matplotlib.lines.Line2D at 0x115455ba8>,
                    <matplotlib.lines.Line2D at 0x115467cc0>,
                    <matplotlib.lines.Line2D at 0x115467e48>]})])



### Part I:  Plot a scatter matrix plot using the seaborn library. Use the following to load and plot. 


```python
import seaborn  
```


```python
 seaborn.pairplot(iris, hue='Species')
```




    <seaborn.axisgrid.PairGrid at 0x117b0f978>


