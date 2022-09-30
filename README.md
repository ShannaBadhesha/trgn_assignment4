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