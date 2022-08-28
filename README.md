<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a>
    <img src="ai_campers1.png" alt="Logo" width="150" height="150">
  </a>

  <h3 align="center">AI CAMPERS</h3>

  <p align="center">
    AI Summer Camp '22 - Medical Cost Analysis
    
  </p>
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#project-content">Project Content</a></li>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#model-selection">Model Selection</a>
      <ul>
        <li><a href="#best-performing-model---polynomial-regression">Best Performing Model - Polynomial Regression</a></li>
      </ul>
    </li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

  <a>
    <img src="ai_campers_team.png" alt="Team">
  </a>

Hande ÇELEBİ - [Linkedin](https://www.linkedin.com/in/hande-%C3%A7elebi-5572461b8/)

Anıl Can ÖZGÖK - [Linkedin](https://www.linkedin.com/in/an%C4%B1l-can-%C3%B6zg%C3%B6k/)

Azime ARIKAYA - [Linkedin](https://www.linkedin.com/in/azime-arikaya-69a766219/)

Emre ÖZ - [Linkedin](https://www.linkedin.com/in/emre-oz/)

 ### Project Content
 
The aim of the project is to estimate the approximate cost of a person's health insurance based on the given variables. For this purpose, we built the infrastructure of the project with python. It is because python has library support and is easy to use. We performed exploratory data analysis with the data set given to us. We chose the most suitable model according to the data obtained afterwards.

### Built With

This section contains all libraries used in the project.

* Pandas
  ```sh
  import pandas as pd
  ```
* Numpy
  ```sh
  import numpy as nm
  ``` 
* Seaborn
  ```sh
  import seaborn as sb
  ```
* Matplot
  ```sh
  import pandas as pd
  ```
* Sklearn
  ```sh
  import sklearn as sk
  ```

<!-- GETTING STARTED -->
## Model Selection

At this stage, we tried a total of 4 models. These are: Linear Regression, Polynomial Regression, Lasso Regression and Ridge Regression. As a result, the model with the highest R2 value was Polynomial Regression.

### Best Performing Model - Polynomial Regression

* R2: 0.8411925923335958
  ```sh
  from sklearn.preprocessing import PolynomialFeatures

  poly_reg = PolynomialFeatures(degree=5)

  X_poly = poly_reg.fit_transform(X)
  pol_reg = LinearRegression()
  poly = pol_reg.fit(X_poly, y)

  y_poly_pred = pol_reg.predict(X_poly)

  print(f"R2: {r2_score(y,y_poly_pred)}")
  print(f"MAE: {mean_absolute_error(y,y_poly_pred)}")
  print(f"MSE: {mean_squared_error(y,y_poly_pred)}")
  ```

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Here are the resources we used in the construction of this project. Thank you very much.

* [Global AI Hub](https://globalaihub.com/ai-summer-camp-22/)
* [Gülcan Öğündür](https://medium.com/@gulcanogundur/model-se%C3%A7imi-k-fold-cross-validation-4635b61f143c)
* [Yasin Güneş](https://www.linkedin.com/in/yasin-g%C3%BCne%C5%9F-3864631b5/)
* [Günel Alizada](https://www.linkedin.com/in/gunelalizada/)
* [Kaggle Data Set](https://www.kaggle.com/datasets/mirichoi0218/insurance)
