# 2ECE - A: PA-3 - Pandas Test
<h6>
<i>About the files:</i><br>
<ins>cars.csv</ins>: A .csv file containing the table indexes and values needed for the problems below.<br>
<ins>ALCANTARA_Pandas-P1.py</ins>: A .py file that loads <i>Problem 1</i>.<br>
<ins>ALCANTARA_Pandas-P2.py</ins>: A .py file that loads <i>Problem 2</i>.<br>
</h6>
<b><h2>Problem 1:</h2></b>
<h4>A Python script that loads the given <ins>'cars.csv'</ins> file. It then displays the first and last five rows of the latter file.</h4>

```python
import pandas as pd #Imports Panda Library.

cars = pd.read_csv('cars.csv')
cars #Loads and displays the 'cars.csv'.

cars.head() #Displays the first five rows of 'cars.csv'.

cars.tail() #Displays the last five rows of 'cars.csv'.
```
<h6>With this, the desired output should be like this:</h6>
<img width="675" height="571" alt="Image" src="https://github.com/user-attachments/assets/2acf26df-c8bc-4db8-aa25-847538924647" />

<b><h2>Problem 2:</h2></b>
<h4>A Python script where we play around <i>Subsetting, Indexing, and Splicing</i>. It is splitted into four parts:</h4>

```python
import pands as pd #Imports Panda Library.

cars = pd.read_csv('cars.csv')
cars #Loads and displays the 'cars.csv'.
```
<h5>1. The code below output ONLY odd-numbered columns by splicing. It then displays the first five rows using the <i>head()</i> condition.</h5>

```python
carsodd = cars.iloc[:,1::2] #Locates via .iloc by the following format -> [none of the rows, the start of the column index::the increment to splice into two columns skipping the next column after selected splice.]
carsodd.head() #Displays the first five rows.
```
* <h6>The desired output for code above should be like this:</h6>
<img width="266" height="184" alt="Image" src="https://github.com/user-attachments/assets/abfe77ad-7fe3-41f9-a205-d62ada475caa" />

<h5>2. The code below displays the row where the value of 'Mazda RX4' is being located under the 'Model' column and displays the row where it is located at by indexing.</h5>

```python
cars.loc[cars['Model']=='Mazda RX4'] #Locates via .loc by finding the 'Mazda RX4' in the Model column and displays the row with it.
```
* <h6>The desired output for code above should be like this:</h6>
<img width="534" height="71" alt="Image" src="https://github.com/user-attachments/assets/8d9dac69-4ee8-49d3-9468-62f876d59994" />

<h5>3. The code below locates how many 'cyl' (cylinders) does the model 'Camaro Z28' have by subsetting.</h5>

```python
cars.loc[(cars['Model']=='Camaro Z28'), ['cyl']] #Locates via .loc by subsetting to find a certain element in the 'Camaro Z28' of the Mode column and the 'cyl' column.
```
* <h6>The desired output for code above should be like this:</h6>
<img width="104" height="61" alt="Image" src="https://github.com/user-attachments/assets/7d361f92-c795-4194-8028-4d1ea728c596" />

<h5>4. The code below locates how many 'cyl' (cylinders) and 'gear' does the models 'Mazda RX4 Wag', 'Honda Civic', and 'Ford Pantera L' using subsetting. It uses the <u>.iloc</u> condition and also uses its index rather than name as the condition accepts integer input.</h5>

```python
cars.iloc[[1, 18, 28], [2, 10]] 
#Locates via .iloc using specific index rows of 'Mazda 4XR Wag' (1), 'Ford Pantera L' (18), and 'Honda Civic' (28).
#In addition, it also locates the specific index with the rows by its index columns of 'cyl' (2) and 'gear' (10).
```
* <h6>The desired output for code above should be like this:</h6>
<img width="118" height="134" alt="Image" src="https://github.com/user-attachments/assets/5bd92bb9-1c58-438a-b394-a10bcb99e34d" />
