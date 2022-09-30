### Trgn_assignment4¶

## Usage
To determine if there a correlation between number of hospital beds and COVID mortality.

## Description
I explore whether there is obvious evidence for a correlation b/t number of hospital beds and COVID mortality. Intuitively, one might think that more hospital beds improve mortality within a region.

The API Docs are here: https://covid-19-apis.postman.com/). Here is an example unit test where you can see a JSON result. https://api.covid19api.com/

How do we determine countries? Well we read the API manual and see: https://api.covid19api.com/countries

Call API: https://www.communitybenefitinsight.org/api/get_hospitals.php

API Documents: https://www.communitybenefitinsight.org/?page=info.data_api

## Answer

```import requests 
import pandas as pd
import json
import numpy as np
req=requests.get("https://api.covid19api.com/live/country/united-states").json()
covid=pd.DataFrame(req)```

```covid.info()```

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 24480 entries, 0 to 24479
Data columns (total 13 columns):
 #   Column       Non-Null Count  Dtype 
---  ------       --------------  ----- 
 0   ID           24480 non-null  object
 1   Country      24480 non-null  object
 2   CountryCode  24480 non-null  object
 3   Province     24480 non-null  object
 4   City         24480 non-null  object
 5   CityCode     24480 non-null  object
 6   Lat          24480 non-null  object
 7   Lon          24480 non-null  object
 8   Confirmed    24480 non-null  int64 
 9   Deaths       24480 non-null  int64 
 10  Recovered    24480 non-null  int64 
 11  Active       24480 non-null  int64 
 12  Date         24480 non-null  object
dtypes: int64(4), object(9)
memory usage: 2.4+ MB