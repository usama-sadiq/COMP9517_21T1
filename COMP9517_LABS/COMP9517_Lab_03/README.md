# COMP9517 COMPUTER VISION LAB-03 YEAR: 2021 TERM: 01

# AIM

- The aim of this lab is to learn and implement pattern recognition.

# DATASET

- The dataset used for this entire lab is the fashion-MNIST dataset available through tensorflow 2.
- Fashion-MNIST is a dataset of Zalando's articles images.
- Training set size: 60,000.
- Test set size: 10,000.
- Each example is 28x28 grayscale images.
- The dataset has 10 classes.
- The dataset is available at https://github.com/zalandoresearch/fashion-mnist. Credit to the owners.

## LABELS

- Each training and test example is assigned to one of the following labels:

<table>
    <tr>
        <th>Label</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>0</td>
        <td>T-shirt/top</td>
    </tr>
     <tr>
        <td>1</td>
        <td>Trouser</td>
    </tr>
     <tr>
        <td>2</td>
        <td>Pullover</td>
    </tr>
     <tr>
        <td>3</td>
        <td>Dress</td>
    </tr>
     <tr>
        <td>4</td>
        <td>Coat</td>
    </tr>
     <tr>
        <td>5</td>
        <td>Sandal</td>
    </tr>
     <tr>
        <td>6</td>
        <td>Shirt</td>
    </tr>
     <tr>
        <td>7</td>
        <td>Sneaker</td>
    </tr>
     <tr>
        <td>8</td>
        <td>Bag</td>
    </tr>
     <tr>
        <td>9</td>
        <td>Ankle boot</td>
    </tr>
</table>

# OBJECTIVE

- Develop a program to perform pattern recognition for the dataset.

- Classify the 10 fashion items using the three classifiers 
    - KNeighboursClassifier with parameter k=3. 
    - SGDClassifier with parameter max_iter=250.
    - DecisionTreeClassifier.
    - Compare their results.

# IMEPLEMENTATION

## KNN Model

- Import the Fashion_MNIST dataset from tensorflow. 
- Split the train dataset to 2000 and test dataset to 500.
- Change the shape of the train dataset to 2-dimension from 3-dimension. (Shape after reshaping 2000*784).
- Initilize KNN model with parameter value n_neigbours = 2.
- Train the KNN model and make predictions.
- Evaluate the model on train and test data.

## RESULT

<table>
    <tr>
        <th colspan="5">KNN Classification Report</th>
    </tr>
    <tr>
        <td>Precision</td>
        <td>Recall</td>
        <td>F1-Score</td>
        <td>Support</td>
    </tr>
    <tr>
        <td></td>
        <td>T_shirt/top</td>
        <td>0.78</td>
        <td>0.84</td>
        <td>0.81</td>
        <td>55</td>
    </tr>
    <tr>
        <td>Trouser</td>
        <td>0.89</td>
        <td>0.98</td>
        <td>0.94</td>
        <td>52</td>
    </tr>
    <tr>
        <td>Pullover</td>
        <td>0.62</td>
        <td>0.77</td>
        <td>0.69</td>
        <td>65</td>
    </tr>
    <tr>
        <td>Dress</td>
        <td>0.71</td>
        <td>0.78</td>
        <td>0.74</td>
        <td>46</td>
    </tr>
    <tr>
        <td>Coat</td>
        <td>0.75</td>
        <td>0.63</td>
        <td>0.69</td>
        <td>57</td>
    </tr>
    <tr>
        <td>Sandal</td>
        <td>0.94</td>
        <td>0.87</td>
        <td>0.91</td>
        <td>39</td>
    </tr>
    <tr>
        <td>Shirt</td>
        <td>0.61</td>
        <td>0.40</td>
        <td>0.49</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Sneaker</td>
        <td>0.81</td>
        <td>0.94</td>
        <td>0.87</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Bag</td>
        <td>1.00</td>
        <td>0.91</td>
        <td>0.95</td>
        <td>44</td>
    </tr>
    <tr>
        <td>Ankle boot</td>
        <td>0.93</td>
        <td>0.85</td>
        <td>0.89</td>
        <td>48</td>
    </tr>
    <tr>
    </tr>
    <tr>
        <td>accuracy</td>
        <td></td>
        <td></td>
        <td>0.79</td>
        <td>500</td>
    </tr>
    <tr>
        <td>macro average</td>
        <td>0.81</td>
        <td>0.80</td>
        <td>0.80</td>
        <td>500</td>
    </tr>
     <tr>
        <td>weight average</td>
        <td>0.80</td>
        <td>0.79</td>
        <td>0.79</td>
        <td>500</td>
    </tr>    
</table>

### KNN Classifier COnfusion Matrix

<p>[[46  2  4  2  0  0  1  0  0  0]</p>
<p>[ 0 51  0  1  0  0  0  0  0  0]</p>
<p>[ 3  0 50  1  6  0  5  0  0  0]</p>
<p>[ 3  3  1 36  2  0  1  0  0  0]</p>
<p>[ 0  1  9  6 36  0  5  0  0  0]</p>
<p>[ 0  0  0  0  0 34  0  3  0  2]</p>
<p>[ 6  0 14  4  4  0 19  0  0  0]</p>
<p>[ 0  0  0  0  0  2  0 44  0  1]</p>
<p>[ 1  0  2  1  0  0  0  0 40  0]</p>
<p>[ 0  0  0  0  0  0  0  7  0 41]]</p>

## Stochastic Gradient Descent Classifier

- Initilize SGD model with parameter value max_iter = 250.
- Train the SGD model and make predictions.
- Evaluate the model on train and test data.

## RESULT

<table>
    <tr>
        <th colspan="5">SGD Classification Report</th>
    </tr>
    <tr>
        <td>Precision</td>
        <td>Recall</td>
        <td>F1-Score</td>
        <td>Support</td>
    </tr>
    <tr>
        <td>T_shirt/top</td>
        <td>0.92</td>
        <td>0.80</td>
        <td>0.85</td>
        <td>55</td>
    </tr>
    <tr>
        <td>Trouser</td>
        <td>0.96</td>
        <td>0.98</td>
        <td>0.97</td>
        <td>52</td>
    </tr>
    <tr>
        <td>Pullover</td>
        <td>0.72</td>
        <td>0.68</td>
        <td>0.70</td>
        <td>65</td>
    </tr>
    <tr>
        <td>Dress</td>
        <td>0.92</td>
        <td>0.78</td>
        <td>0.85</td>
        <td>46</td>
    </tr>
    <tr>
        <td>Coat</td>
        <td>0.92</td>
        <td>0.58</td>
        <td>0.71</td>
        <td>57</td>
    </tr>
    <tr>
        <td>Sandal</td>
        <td>0.82</td>
        <td>0.92</td>
        <td>0.87</td>
        <td>39</td>
    </tr>
    <tr>
        <td>Shirt</td>
        <td>0.43</td>
        <td>0.79</td>
        <td>0.55</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Sneaker</td>
        <td>0.83</td>
        <td>0.94</td>
        <td>0.88</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Bag</td>
        <td>1.00</td>
        <td>0.89</td>
        <td>0.94</td>
        <td>44</td>
    </tr>
    <tr>
        <td>Ankle boot</td>
        <td>0.97</td>
        <td>0.81</td>
        <td>0.89</td>
        <td>48</td>
    </tr>
    <tr>
    </tr>
    <tr>
        <td>accuracy</td>
        <td></td>
        <td></td>
        <td>0.81</td>
        <td>500</td>
    </tr>
    <tr>
        <td>macro average</td>
        <td>0.85</td>
        <td>0.82</td>
        <td>0.82</td>
        <td>500</td>
    </tr>
     <tr>
        <td>weight average</td>
        <td>0.85</td>
        <td>0.81</td>
        <td>0.81</td>
        <td>500</td>
    </tr>    
</table>

### SGD Classifier COnfusion Matrix

<p>[[44  0  0  1  0  0 10  0  0  0]</p>
<p>[ 0 51  0  1  0  0  0  0  0  0]</p>
<p>[ 0  0 44  0  3  0 18  0  0  0]</p>
<p>[ 1  2  0 36  0  0  7  0  0  0]</p>
<p>[ 0  0 11  0 33  0 12  1  0  0]</p>
<p>[ 0  0  0  0  0 36  0  2  0  1]</p>
<p>[ 3  0  6  1  0  0 37  0  0  0]</p>
<p>[ 0  0  0  0  0  3  0 44  0  0]</p>
<p>[ 0  0  0  0  0  2  3  0 39  0]</p>
<p>[ 0  0  0  0  0  3  0  6  0 39]]</p>

## Decision Tree Classifier

- Initilize DT model.
- Train the SGD model and make predictions.
- Evaluate the model on train and test data.

## RESULT

<table>
    <tr>
        <th colspan="5">DT Classification Report</th>
    </tr>
    <tr>
        <td>Precision</td>
        <td>Recall</td>
        <td>F1-Score</td>
        <td>Support</td>
    </tr>
    <tr>
        <td>T_shirt/top</td>
        <td>0.85</td>
        <td>0.82</td>
        <td>0.83</td>
        <td>55</td>
    </tr>
    <tr>
        <td>Trouser</td>
        <td>0.88</td>
        <td>0.88</td>
        <td>0.88</td>
        <td>52</td>
    </tr>
    <tr>
        <td>Pullover</td>
        <td>0.57</td>
        <td>0.51</td>
        <td>0.54</td>
        <td>65</td>
    </tr>
    <tr>
        <td>Dress</td>
        <td>0.56</td>
        <td>0.76</td>
        <td>0.65</td>
        <td>46</td>
    </tr>
    <tr>
        <td>Coat</td>
        <td>0.56</td>
        <td>0.44</td>
        <td>0.49</td>
        <td>57</td>
    </tr>
    <tr>
        <td>Sandal</td>
        <td>0.86</td>
        <td>0.82</td>
        <td>0.84</td>
        <td>39</td>
    </tr>
    <tr>
        <td>Shirt</td>
        <td>0.43</td>
        <td>0.45</td>
        <td>0.44</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Sneaker</td>
        <td>0.84</td>
        <td>0.91</td>
        <td>0.88</td>
        <td>47</td>
    </tr>
    <tr>
        <td>Bag</td>
        <td>0.79</td>
        <td>0.75</td>
        <td>0.77</td>
        <td>44</td>
    </tr>
    <tr>
        <td>Ankle boot</td>
        <td>0.84</td>
        <td>0.90</td>
        <td>0.87</td>
        <td>48</td>
    </tr>
    <tr>
    </tr>
    <tr>
        <td>accuracy</td>
        <td></td>
        <td></td>
        <td>0.71</td>
        <td>500</td>
    </tr>
    <tr>
        <td>macro average</td>
        <td>0.72</td>
        <td>0.72</td>
        <td>0.72</td>
        <td>500</td>
    </tr>
     <tr>
        <td>weight average</td>
        <td>0.71</td>
        <td>0.71</td>
        <td>0.71</td>
        <td>500</td>
    </tr>    
</table>


### DT Classifier COnfusion Matrix

<p>[[45  0  0  4  2  0  4  0  0  0]</p>
<p>[ 1 46  0  4  0  1  0  0  0  0]</p>
<p>[ 1  1 33  3 12  2  9  1  2  1]</p>
<p>[ 2  2  3 35  1  0  3  0  0  0]</p>
<p>[ 0  2 13  6 25  0  9  0  2  0]</p>
<p>[ 1  0  0  0  0 32  0  3  2  1]</p>
<p>[ 2  1  8 10  2  0 21  0  3  0]</p>
<p>[ 0  0  0  0  0  1  0 43  0  3]</p>
<p>[ 1  0  1  0  3  0  3  0 33  3]</p>
<p>[ 0  0  0  0  0  1  0  4  0 43]]</p>