
![Logo](https://logos-world.net/wp-content/uploads/2020/09/Spotify-Logo-700x394.png)

    
# The Analysis of Changes in Spotify Users' Music Taste and Song Recommendation System

This project's aim is to analyze whether users' taste of music
has changed due to COVID-19. Furthermore, a model is built in
order to suggest similar songs based on characteristics given 
by Spotify.

## Description

### Context and Content
COVID-19 has changed people's lives in many ways. Therefore,
we want to analyze if listeners' music taste has changed
due to the pandemic. Furthermore, a model was built in order
to suggest 10 songs with similar characteristics.

Data retrieved was the weekly top 200 global songs on
[Spotify chart](https://spotifycharts.com/regional) from 
12/28/2018 to 12/04/2020.

### Features
More features and features' definitions can be found on
[Spotify API website](https://developer.spotify.com/documentation/web-api/reference/#category-artists)

|variable                       |description |
|:---|:-----------|
|track_name                     | Song Name|
|track_artist                   | Song Artist|
|danceability                   | Danceability describes how suitable a track is for dancing based on a combination of musical elements including tempo, rhythm stability, beat strength, and overall regularity. A value of 0.0 is least danceable and 1.0 is most danceable. |
|energy                         | Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity. Typically, energetic tracks feel fast, loud, and noisy. For example, death metal has high energy, while a Bach prelude scores low on the scale. Perceptual features contributing to this attribute include dynamic range, perceived loudness, timbre, onset rate, and general entropy. |
|speechiness                    | Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value. Values above 0.66 describe tracks that are probably made entirely of spoken words. Values between 0.33 and 0.66 describe tracks that may contain both music and speech, either in sections or layered, including such cases as rap music. Values below 0.33 most likely represent music and other non-speech-like tracks. |
|acousticness                   | A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.|
|instrumentalness               | Predicts whether a track contains no vocals. “Ooh” and “aah” sounds are treated as instrumental in this context. Rap or spoken word tracks are clearly “vocal”. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0. |
|liveness                       | Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live. |
|valence                        | A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry). |
|tempo                          | The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration. |
|duration_ms                    | Duration of song in milliseconds |
|track_popularity               | Song Popularity (0-100) where higher is better |


## Software/Language

This project requires **Python** and was coded on **[Google Colab](https://colab.research.google.com/notebooks/intro.ipynb#recent=true).**

## Appendix

Packages used:

```{py}
!pip install spotipy
import spotipy
from spotipy.oauth2 import SpotifyClientCredentials #To access authorised Spotify data
import csv
import pandas as pd
import glob
from scipy import stats
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
from sklearn import preprocessing
from sklearn.cluster import KMeans
from scipy.spatial.distance import euclidean
```

  
## Acknowledgements

 - [Web API | Spotify for Developers](https://developer.spotify.com/documentation/web-api/)
 - [t-test independent](https://github.com/bhattbhavesh91/GA_Sessions/blob/master/t_test_independence/T_Test_Sales.ipynb)
  
