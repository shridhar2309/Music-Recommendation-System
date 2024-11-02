🎶 Music Recommendation System Using Spotify Data

This project is a music recommendation system that uses machine learning to recommend songs based on their audio features, such as danceability, energy, tempo, and valence. By analyzing these attributes from the Spotify dataset, this system makes content-based recommendations, helping users discover similar songs.

📋 Project Overview

Objective: Build a content-based recommendation system using Spotify audio features.
Model: K-Nearest Neighbors (KNN) is used to find songs similar to the input track based on its features.
Dataset: Audio features dataset obtained using the Spotify API, including features like danceability, energy, tempo, loudness, and valence.
Recommendations: Based on feature similarity, the system suggests songs that match the input track's characteristics.

📂 Table of Contents

Installation
Spotify API Setup
Data Collection
How It Works
Usage
Future Enhancements
Contributing


🛠️ Installation

Clone the Repository:

bash
git clone https://github.com/shridhar2309/Music-Recommendation-System/tree/main
cd music-recommendation-system
Install Dependencies:

bash
pip install -r requirements.txt
Note: If using Google Colab, install dependencies in a Colab cell.

Spotify API Credentials:

Sign up for a Spotify Developer account and create an app to get API credentials.
Add the Client ID and Client Secret to a .env file in the project directory:
plaintext
Copy code
SPOTIPY_CLIENT_ID='3d627552a7404b4b9b4db42bd08581d5'
SPOTIPY_CLIENT_SECRET='3a68d462cba64a898397ebb332811342'

🎧 Spotify API Setup

Register an Application on the Spotify Developer Dashboard.
Obtain your Client ID and Client Secret from the app settings.
Add the credentials to a .env file or use environment variables in your code.

📊 Data Collection

Authentication: Use the Spotify API to authenticate and access track features.
Data Download: Run the provided data collection script to download track features (danceability, energy, tempo, etc.) into spotify_tracks.csv.

🚀 How It Works

Data Preprocessing:

Prepares the Spotify audio features data for model training.
Splits the data into training and testing sets.
KNN Model:

A K-Nearest Neighbors model is trained on audio features to find songs with similar characteristics.
When a track is given, KNN finds songs with the closest feature vectors to recommend similar tracks.
Recommendation Function:

Takes a track's features as input and returns a set of recommended tracks based on similarity.
Evaluation:

Calculates the average popularity of recommended tracks to gauge how well the recommendations align with user preferences.

📌 Usage

Recommend Songs: Use the recommend_tracks() function to get song recommendations for a specific track.

python

recommended_tracks = recommend_tracks(track_index=0)  # Change track index as needed
print("Recommended Tracks:")
print(recommended_tracks)
Evaluate Recommendations: Use the evaluate_recommendation() function to check the popularity of recommended songs for a given track.

python

evaluate_recommendation(track_index=0)  # Change track index as needed
Optional - Run a Web Interface: Run a Streamlit or Gradio app for user-friendly recommendations.

Streamlit:
bash
streamlit run app.py
Gradio (useful for Google Colab):
python

import gradio as gr

def recommend_interface(track_index):
    return recommend_tracks(track_index)

gr.Interface(fn=recommend_interface, inputs="number", outputs="dataframe").launch()

🌟 Future Enhancements

Collaborative Filtering: Incorporate user-based collaborative filtering for more personalized recommendations.
Improved User Interface: Build a more interactive and visually appealing UI.
Expanded Features: Include genre or artist data to improve recommendation accuracy.

🤝 Contributing

Contributions are welcome! Feel free to open issues or submit pull requests to enhance the project.


📧 Contact
For any questions, reach out to me at your-shridharhappy23@gmail.com

