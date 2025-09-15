# Uber-Sales-Analytics
This comprehensive dataset contains detailed ride-sharing data from Uber Operations for the year 2024, providing rich insights into booking patterns , vehicle performance, revenue streams , cancellation behaviours , and customer satisfaction metrics.

The goal of this analytics is to uncover insights from the data and make valuable recommendation for the company.

##### Objectives of the analysis
1. DATA IMPORTATION
2. DATA EXPLORATION
3. DATA CLEANING
4. BOOKING PATTERNS
5. CUSTOMER RATINGS
6. DISTRIBUTION OF VEHICLE TYPES


   ## Data and Library Importation
   ```python
   # importing the necessary Libraries

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')
```

```python
# importing he dataset
df = pd.read_csv("/content/drive/MyDrive/Colab Notebooks/UBER ANALYTICS/ncr_ride_bookings.csv")
```

# Data Exploration 
Before the commencement of the analysis, the data was examined which included process like checking shapes of the data , the data types and missing values.The results of the exploration revealed that the dataset has about 150,000 rows .Certain data fields like <Avg VTAT> , 
```

## Data Exploration


