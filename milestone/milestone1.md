## Milestone 1 (7th of April, 5pm)

**10% of the final grade**

This is a preliminary milestone to let you set up goals for your final project and assess the feasibility of your ideas.
Please, fill the following sections about your project.

*(max. 2000 characters per section)*

### Dataset
We have decided to use our own [personal data](https://support.spotify.com/us/article/data-rights-and-privacy-settings/) (which is available under the GDPR data rights) from Spotify and mix with other API sources, such as [Spotfiy API](https://developer.spotify.com/documentation/web-api) and [Spotipy](https://spotipy.readthedocs.io/en/2.22.1/).

We have first downloaded a copy of our Streaming History. The file is  around 500 kb of size, with more than 3000 records of playing history. It contains records with the following structure:



	{

	"endTime": date,

	"artistName":  string,

	"trackName": string,

	"msPlayed": string

}

	,

	With this information we were able to query the Spotify web API to get the album release date, its popularity following Spotify's criteria, its associated genres and the track's duration.  

In addition, we are using spotify's API audio features route. It returns a list of audio features for every track.  

	{

	"danceability": number,

	"energy":  number,

	"key": number,

	"loudness": number,

	"acousticness": number,

	"intrumentalness" : number,

	"livenes": number,

	"valence": number,

	"tempo": number

}

Finally, we may gather the music lyrics together with musixmatch api for example. However it is limited to 30% of the track.


## Problematic

We are looking to deliver some personal and original insights about your music consumption. We have temporal data such as the date the track has been played and for how long, coupled with track information and its audio features such as danceability, valence and loudness.

We think this might be a relevant platform to be released online, so a user may download its own data from spotify, upload it and get an analysis for a reduced part of it. (For example 150 most listened songs?)

We are targeting every music listener that uses Spotify regularly and are interested in knowing more about their own music listening behavior.

With this data, we can try to answer to the following questions:




    How do the periods of the year influence your music tastes?


    What music do you listen to more on weekends compared to weekdays?


    What is your expected sentiment of the day or week by listening to these tracks?


## Exploratory Data Analysis

Analysis and exploration of dataset can be found in the [notebooks/Analysis.ipynb](../notebooks/Analysis.ipynb)

Below are some examples of visualizations we have found relevant.

<img src="../images/plot4.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot5.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot6.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot1.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot2.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot3.png" alt="alt text" width="50%" height="50%" />
<img src="../images/plot7.png" alt="alt text" width="50%" height="50%" />




## 4-Related Work

We think the originality of our approach is to actually leverage the fact that companies have legal obligations to deliver to a user their data usage in order to show personal insights.  

We were inspired by this [project](https://towardsdatascience.com/spotify-sentiment-analysis-8d48b0a492f2) we have found online by Lowri Williams. The project consists of doing sentiment analysis on Spotify data with lyrics information. We really liked the idea behind and the fact that it is a public tool that can be accessed by anyone.

However, we want to show some different insights using the track's playing times that weren't used in her project. Also we don't wish to focus much on sentiment analysis as her project does.

Her [radar chart](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*0xKnvDtAV5u8pKV7xbnOJw.png) inspired us to do a similar one, but instead of having "positive", "negative" and "neutral". We will use the track features and also other date metrics instead of month, such as days of the week, years or time range in a day.

On top of that we want to add some moer basic charts, such as time series line charts, pie charts with information about most played songs, artists. And also, more creative ones, such as bubble charts with the song features and an interactive timeline, so the user can scroll through time and visualize how their song features evolve.
