# Spotify Shuffler
**Technologies:** *Python, HTML, CSS, Docker, Spotify Web API, OAuth 2.0*
## Purely randomized playlist ordering!
### Description
Do you ever feel frustrated about the performance of Spotify's shuffle feature? Tired of being fed the same 5 songs out of a playlist that contains more than 1000?

Then check this out.

Designed as a solution to the user pain-point of excessive reptitiveness in the Spotify shuffle algorithm, this project is an MVP prototype designed to test out a purely randomized alternative. It's a fun and useful tool for functional purposes, but also presents value as a research tool for comparing different shuffle algorithms.

**Is random ordering *truly* a desired attribute? This shuffler will be a vital component in performing further analysis to unearth the answer.**

---
### Prerequisites
- Docker [installed & running]: https://docs.docker.com/get-docker/
- A Spotify Account: https://www.spotify.com/us/signup

### Instructions
1. In your local machine's terminal, build the image by running the following Docker command:

```
docker build https://github.com/ericgadbois/Spotify-Shuffler.git -t shuffler
```

2. Run the image on your local machine using the following command:

```
docker run -p 5000:5000 shuffler
```

3. In a web browser, navigate to:

```
http://localhost:5000
```

4. You should see this screen:

![Homepage](./static/images/homepage.png)

5. Clicking the button on the homepage will redirect you to a secure, Spotify-hosted login page that will provide an authentication token to the application.

6. After logging in, select the playlist that you would like to listen to and click the "Shuffle" button (This may take a moment depending on the playlist size)

7. Voila! Your playlist will now be shuffled in your queue!
---
**Note: The Spotify Web API does not currently allow functionality to clear a user's queue. So, after your session, you will need to manually clear the remaining queue within any native Spotify interface.**