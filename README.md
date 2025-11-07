# geomarketing-moscow-retail

The training project "Identifying Promising Territories for Opening Grocery Stores Using Machine Learning Methods" was presented as part of the professional retraining program "Development of Geoinformation Solutions Using Artificial Intelligence Methods."

##  Структура проекта

geomarketing-moscow-retail/
├── data/                          
│   ├── raw/                       
│   │   ├── moscow_bbox.geojson    
│   │   └── existing_stores.csv    
│   └── processed/                 
│       └── h3_features.csv        
├── notebooks/                     
│   ├── 01_data_collection.ipynb      
│   ├── 02_feature_engineering.ipynb  
│   ├── 03_model_training.ipynb       
│   └── 04_visualization.ipynb        
├── src/                           
│   ├── __init__.py
│   ├── data_loader.py            
│   ├── h3_utils.py               
│   ├── feature_engineering.py    
│   ├── models/                   
│   │   ├── __init__.py
│   │   ├── classifier.py         
│   │   └── clustering.py         
│   └── visualization/            
│       ├── __init__.py
│       ├── maps.py               
│       └── plots.py              
├── results/                      
│   ├── models/                   
│   │   ├── random_forest.pkl
│   │   └── gradient_boosting.pkl
│   ├── maps/                     
│   │   ├── potential_map.html
│   │   └── top_locations.html
│   └── exports/                  
│       └── top_locations.csv
├── docs/                         
│   ├── methodology.md            
│   └── api_reference.md          
├── tests/                        
├── requirements.txt              
├── environment.yml               
├── Dockerfile                    
└── README.md                     

##  Описание директорий

### **data/** - Данные исследования
- `raw/` - Исходные данные из OpenStreetMap
- `processed/` - Обработанные данные для анализа

### **notebooks/** - Jupyter notebooks
- `01_data_collection.ipynb` - Сбор и первичная обработка данных
- `02_feature_engineering.ipynb` - Создание пространственных признаков
- `03_model_training.ipynb` - Обучение моделей машинного обучения
- `04_visualization.ipynb` - Визуализация результатов и создание карт

### **src/** - Исходный код Python
- `data_loader.py` - Загрузка и обработка геоданных
- `h3_utils.py` - Утилиты для работы с гексагональной сеткой H3
- `feature_engineering.py` - Создание пространственных признаков
- `models/` - Модели машинного обучения
- `visualization/` - Визуализация результатов

### **results/** - Результаты исследования
- `models/` - Сохраненные обученные модели
- `maps/` - Интерактивные карты в HTML формате
- `exports/` - Экспортированные данные для анализа

##  Быстрый старт

### Установка зависимостей
```bash
pip install -r requirements.txt

# Запуск Jupyter notebook
jupyter notebook notebooks/01_data_collection.ipynb
