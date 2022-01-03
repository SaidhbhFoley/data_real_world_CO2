# data_real_world_CO2
# CO2 Emissions

## Introduction

For this project I have choosen to look at the global Carbon dioxide (CO<sub>2</sub>) emissions, I have taken the data from owid co2data.

CO<sub>2</sub> emissions have risen dramatically since the start of the industrial revolution. Most of the world's greenhouse gas emissions come from a relatively small number of countries. China, the United States, Russia and the European Union are the largest emittors on an absolute basis. However when you look at per capita the United State are the largest emittors. 

In this notebook I will examine these countries along with others to examine if there is any correlation between CO<sub>2</sub> emissions and other variables such as population and GDP.

I have included data on the increase in temperature to show the correlation between CO<sub>2</sub> and the increase in global temperatures. As this is a well known phenomenon it will not be explored in this notebook. It is here for illustrative purposes and to highlight the need to change CO<sub>2</sub> emissions if we are to halt climate change.

I have included the codebook from Our World in Data, for information on all the columns and the meanings of each column.

## Libraries Imported
import pandas as pd

import matplotlib.pyplot as plt

import numpy as np

import seaborn as sns

import os

## Why CO2 Emissions Matter
I have included the data for the global increase in temperature to show how the world's temperature has been rising since the indutrial revolution. This data was taken from Our World in Data.

## Examining the Data
The dataset obtained from Our World in Data is an extremely thorough and large dataset. Therefore throughout this notebook it will be broken down into more accessible dataframes, that will allow for analysis.
Before I begin the analysis the data will be examined, it is important to examine a dataset before analysis. I will examine the data using .head(), .info() and .describe(). I will also ascertain the percentage of NaN in the data as this will limit the analysis if it is extremely prevailant in a variable that variable will not be used.

As this dataset is too large to even ascertain which countries are the largest emitters of both absolute CO2 and per capita CO2, I will start by looking into continents as a whole and then specific countries in relation to population and GDP.

Absolute CO2 emissions are largely made up by Asia, accounting for over 20,000 million tonnes in 2020 with Europe accounting for ~5000 million tonnes and North America for ~6000 million tonnes (5775 taken from the dfnamerica dataframe).

In Central America Guatemala is the biggest emitter of CO2, having doubled it's emissions in the last 20 years. It also has the largest population of the countries in Central America followed by Honduras and Nicaragua. Despite Nicaragua being the third dentist in terms of population it is the second lowest emitter. Belize is lowest emitter of CO2 and has the lowest population of all countries in Central America, with a population of 397,621 in 2020.

## Exmaining Countries in Europe
I created a dataframe containing each country in Europe, I choose to focus on the continent Europe and not the European Union.

I then used population data taken from worldometer to get the the highest populated countries and lowest populated countries4 in Europe. In order to cross reference that the countries on this list were also in the data set I searched for the countries to ensure they were present.

I then choose to look at the countries with the highest level of GDP and the lowest level of GDP. As the data for GDP was patchy in the original dataset I took the information from eurostat.

As it is difficult to see the data presented I narrowed down the countries represented. First to the ten highest populated countries and then to the ten lowest populated countries.

By combining the highest population data with the lowest population data it is possible to see the difference clearer than when they are plotted on different plots.
The plot for the lowest population countries did not reach 40 on the y-axis, whereas the highest populations reached over 2500, for one Russia alone.

## GDP and CO<sub>2</sub> Emissions
I will examine below if there is a correlation between GDP and CO2. Iw ould expect there to be a positive correlation between emissions on GDP, as it well understood that the richest countries are the largest emitters of CO2.

Developed countries as a whole are responsible to 79% of emissions according to the Center for Global Development.

I wanted to examine this first on Europe and then expand it out across the global data.

### Europe
Luxembourg, Ireland and Switzerland are the top three countries in terms of GDP per capita. Luxembourg is one of the lowest emitters with only Iceland emitting less CO2. Germany is by far the largest emitter of CO2 followed by the Netherlands. The Netherlands ranks 6th in terms of GDP per capita and Germany 9th.

Germany emitts the most absolute CO2 with Luxembourg being the secondest smallest emitter. But when you look at CO2 per capita Luxembourg emits far more than the other countries, emitting over 25 million tonnes, with Iceland in second place emitting ~7 million tonnes.

### Countries with the Highest GDP
As the GDP in the dataset was sparse with ~50% NaN I used worldometer to get the countries with the highest GDP7 I choose to focus on the top 10 countries in terms of nominal GDP.

First I plotted absolute emissions, I then focused on per capita emissions.

In terms of absolute emissions China is the largest emitter followed by the United States and India. The United States is the country with the largest nomial GDP followed by China, India is fifth in the world for nominal GDP.

In terms of per capita emissions the United States is the largest emitter followed by Canada and then Germany. Germany is fourth in terms of nominal GDP with Canada coming 10th. India is the lowest per capita emitter depsite being in the top three for absolute emissions.

### Countries with the Lowest GDP
As the GDP in the dataset was sparse with ~50% NaN I used worldometer to get the countries with the lowest GDP. I choose to focus on the lowest 10 countries in terms of nominal GDP.

First I plotted absolute emissions as seen below. I then focused on per capita emissions.

The comaprison between the lowest and highest emitters is stark, particularly when it comes to absolute emissions. In order to present this data in a more visually appealing way I will next look into creating Bar Charts.

### Bar Charts for GDP and CO2 Emissions
For these Bar Charts I will focus on certain years and not the changes in emissions over time. I will look at 3 different years, first 2020 as it is the most recent year, then 2007 as it is the year before the economic collapse and finally 2009 as it was the year after the economic collapse.

There was little difference across the countries that emitted the most and least CO<sub>2</sub> across these three years.

## Three Largest Emitters
Here I will examine the three largest emitters of CO2. The three largest emitters are United States, China and Russia.

## Conclusion
I believe I have shown in this notebook the link between high GDP and CO2 emissions both in terms of absolute and per capita.