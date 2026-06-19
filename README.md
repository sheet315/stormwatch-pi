# Stormwatch-Pi

This is the repo for the [project I posted to reddit](https://www.reddit.com/r/raspberry_pi/comments/1uabe2z/comment/osmvukx/?screen_view_count=4)

## How to set up:
- Download client.py to your client (Doesn't have to be a raspberry pi, but that is what I used.)
- Have a connected USB webcam.
- Find the `/dev/video` node for your USB webcam (and note down the number after video).
- Set this number in client.py line 23: `dev = 0`, replace 0 with the number after video.
- Install v4l2 on the client: `sudo apt install v4l-utils`
- Download server.py to a suitable server
- Install uvicorn: `pip install uvicorn`
- Run server: `uvicorn server:app --port (YOUR PORT HERE) --host 0.0.0.0`
- Set your server's IP and port in client.py line 9: replace `ENTER YOUR API SERVER IP:PORT HERE` with your server ip and your chosen port (previous step).

That's pretty much it.
You can go into a web browser to `http://ip:port` and press `enable stream` and you should see the webcam video, if you do, that means it worked. Enjoy.

<img width="489" height="489" alt="image" src="https://github.com/user-attachments/assets/a498cfa2-4081-419c-bd38-89da32e143eb" />
<img width="489" height="489" alt="image" src="https://github.com/user-attachments/assets/9ce2b221-10d1-4425-befd-da916ce51215" />
<img width="489" height="489" alt="image" src="https://github.com/user-attachments/assets/20cc1dad-39c8-44e2-bbe7-7a3ecb1e4cce" />
