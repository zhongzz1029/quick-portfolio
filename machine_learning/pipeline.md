# Pipeline 

Pipeline simplifies the process of building chains of data transformation and models. 

```python
from sklearn.pipeline import Pipeline 
pipe = Pipeline([('scalar', MinMaxScaler()), ('svm', SVC())]) 
pipe.fit(x_train, y_train)
pipe.score(x_test, y_test)
# a simple class: make_pipeline  
```

### Pipeline with gridsearch for best hyperparameters 

```python
grid = GridSearchCV(pipe, param_grid=param_grid, cv=5)
grid.fit(x_train, y_train)
grid.score(x_test, y_test) 
# There is more of attributes of grid 
```

### Pipeline with gridseach for the best model 

```python
pipe = [
	{'classifier': [SVC()], 'preprocessing': [StandardScaler(), None],
	 'classifier_gamma': [0.001, 0.01, 0.1, 1, 10, 100], 
	 'classifier_C': [0.001, 0.01, 0.1, 1, 10, 100]}, 
	{'classifier': [RandomForestClassifier()],
	 'preprocessing': [None],
	 'classifier_max_features': [1, 2, 3]}
]
grid = GridSearchCV(pipe, param_grid=param_grid, cv=5)
grid.fit(x_train, y_train)
grid.score(x_test, y_test) 
``` 
