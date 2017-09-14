# -*- coding: utf-8 -*-
"""
Created on Tue Sep 05 14:02:17 2017

@author: Emily
"""

import requests
from lxml import objectify

#https://www.ncdc.noaa.gov/temp-and-precip/climatological-rankings/download.xml?parameter=tavg&state=44&div=0&month=6&periods[]=6&year=2017
period='6'
S_R_AgBelt='44'
climate='0'
month='8'
year='2016'

url = 'https://www.ncdc.noaa.gov/temp-and-precip/climatological-rankings/download.xml?parameter=tavg&state=%s&div=%s&month=%s&periods[]=%s&year=%s' %(S_R_AgBelt, climate, month, period, year)
response = requests.get(url).content
response = objectify.fromstring(response)
data=response.data

my_wm_username = 'elane'
print my_wm_username
print data.value
print data.twentiethCenturyMean
print data.lowRank
print data.highRank
