# Insternship-Projects
#Web scraping and saving data in csv format
# using website "https://www.worldometers.info/world-population/india-population" to scrape the data
# import required python libraries
import requests
import pandas as pd
from bs4 import BeautifulSoup
url="https://www.worldometers.info/world-population/india-population/" # scraping the url to collect data about India's census over past few deacades
response=requests.get(url)
htmlcontent=response.content
soup=BeautifulSoup(htmlcontent,'html.parser' )
tests=soup.find("tbody")
table=tests.find_all("tr")
year=[]   #Parameters we are going to obtain from the scraped data
population=[]
year_per_change=[]
yearly_change=[]
migrant=[]
median_age=[]
fertility_rate=[]
density=[]
urban_pop=[]
urban_population=[]
world_pop=[]
world_population=[]
for i in range(len(table)):
    data=table[i].get_text().split(' ')
    year.append(data[1])   # entering the data in the list
    population.append(data[2])
    year_per_change.append(data[3])
    yearly_change.append(data[5])
    migrant.append(data[6])
    median_age.append(data[7])
    fertility_rate.append(data[8])
    density.append(data[9])
    urban_pop.append(data[10])
    urban_population.append(data[12])
    world_pop.append(data[13])
    world_population.append(data[15])
dict ={'Year' : year, 'Yearly_ChaNGE' : yearly_change ,'Yearly_%_Change' : year_per_change,'Migrant' : migrant , 'Median_Age' : median_age, 'Fertility_Rate' : fertility_rate,
       'Density' : density, 'Urban_Pop' : urban_pop , 'Urban_Population ' : urban_population,'World_Pop' : world_pop ,'World_Population ': world_population}
df=pd.DataFrame(dict)
df.to_csv('Population_start_India.csv')  # saving the scraped data in csv format[Population_start_India.csv]
print (df)

[Population_start_India.csv](https://github.com/Akanksha7254/Insternship-Projects/files/12874136/Population_start_India.csv)![csv output](https://github.com/Akanksha7254/Insternship-Projects/assets/146561059/235054c3-d2f2-4883-aee3-f5704ea969a8)


