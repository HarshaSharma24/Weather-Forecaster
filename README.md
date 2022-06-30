# Weather-Forecast-App ⛅
## Introduction:
A weather forecast app is web-based application to get weather updates and any other climatic changes.
In this project, I've made a weather forecast application using **Streamlit**  and **PYOWM** libraries in Python. 

>**Concepts used in this project:**
* Application Development
* API calls
* Data Visualisation


## Features:
* Getting Weather forecast using Open Weather API
* City name based querying
* Parameters: Temperature, Wind speed, Cloud coverage, Sunrise & Sunset time, Graphical representation

## Prerequisites:
>**Tools & Technologies used:**
* Python 
* [Streamlit](https://streamlit.io/)
* [Open Weather Map](https://openweathermap.org/)
* Matplotlib
* [PYOWM]((https://pyowm.readthedocs.io/en/latest/))


>Installation Guide:

pip install streamlit
pip install pyowm
pip install matplotlib

## Steps:

`` Scripting in Python``
```
Step1: Firstly, Install all the required packages mentioned above and go through the respective documentation.
Step2: We have to register an account on https://openweathermap.org/ and generate an API Key.
       Note: I have used Current Weather Data, But you can use different kinds of API's and upgrade your app.
Step3: Here we initialize Pyowm with an API key.
Step4: We take the city Name as input and call the weather_manager() instance to fetch the weather data for that place.
       -Unlike the previous step where we called the temperature values, now we call the clouds and the wind functions.
       -Similarly, like the previous ones, to get the sunset and sunrise time,
        we call the sunset_time(‘iso’) and sunrise_time(‘iso’) functions of the weather object.
Step5: Now, let’s start with the FUN Part: Making the Python Web App using streamlit.
       -Streamlit has various unique methods to call for like title, header, textbox, buttons etc.
       -Read the streamlit documentation and explore other options and try to make it more interactive.
Step6: Plotting Graphs and Calculations using matplotlib.
       -The plot_line() and plot_bar() function is called by the our weather_detail() function.
       -The ‘days’ list that is passed contains the values in an encoded representation which we won’t understand. 
       -Hence to convert it into human- perceivable format, we use the dates.date2num and the set_major_formatter() function.
       -Now as per the user input we get the graphs plotted using the plt.plot(for line graph) and plt.bar(for bar graph). 
       -To print the graphs in Streamlit we use the st.pyplot() just like our standard plt.show(). 
       -At the end plt.clf() is used to clear the graphs making space for the next graph to be printed.
```

## References:
- [Open Weather Map](https://openweathermap.org/)
- [Streamlit docs](https://docs.streamlit.io/en/stable/)
- [Pyowm docs](https://pyowm.readthedocs.io/en/latest/pyowm.weatherapi25.html)
