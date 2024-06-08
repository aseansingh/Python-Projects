# Titanic-Dataset
By Considering the data provided in the titanic dataset tried to made some conclusions by using python language and jupiter notebook on how there was much survival or no survival using visualisations for  age, Pclass, Sex Fare.

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
%matplotlib inline
import seaborn as sns

df_titanic = pd.read_csv("titanic.csv")

sns.set(style="whitegrid")

plt.figure(figsize=(10, 6))
sns.histplot(data=df_titanic, x='Age', hue='Survived', multiple='stack', kde=True)
plt.title('Survival based on Age')
plt.xlabel('Age')
plt.ylabel('Count')
plt.show()

plt.figure(figsize=(10, 6))
sns.countplot(data=df_titanic, x='Pclass', hue='Survived')
plt.title('Survival based on Pclass')
plt.xlabel('Pclass')
plt.ylabel('Count')
plt.show()

plt.figure(figsize=(10, 6))
sns.countplot(data=df_titanic, x='Sex', hue='Survived')
plt.title('Survival based on Sex')
plt.xlabel('Sex')
plt.ylabel('Count')
plt.show()

plt.figure(figsize=(10, 6))
sns.scatterplot(data=df_titanic, x='Age', y='Fare', hue='Survived')
plt.title('Survival based on Fare and Age')
plt.xlabel('Age')
plt.ylabel('Fare')
plt.show()
