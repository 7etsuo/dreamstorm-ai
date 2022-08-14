<p align="center">
  <h2 align="center">www.dreamstorm.net</h2>
</p>

Based on OpenAI's [DALL-E](https://openai.com/blog/dall-e/), based on [DALL-E Mini](https://github.com/borisdayma/dalle-mini).

## Using DALL-E Mega
DALL-E Mega is substianlly more capable than DALL-E Mini and therefore generates higher fidelity images. If you have the computing power uncomment [this line](https://github.com/saharmor/dalle-playground/blob/2cffe123325910ff266185b653841c65f227c69f/backend/app.py#L38) before running the backend.

## Local development

Follow these steps to clone and run dreamstorm locally:

1. Clone or fork this repository
2. Create a virtual environment `cd backend && python3 -m venv ENV_NAME`
3. Install requirements `pip install -r requirements.txt`
4. Make sure you have pytorch and its dependencies
   installed _[Installation guide](https://pytorch.org/get-started/locally/)_
5. Run web server `python app.py 8080` (you can change from 8080 to your own port)
6. In a different terminal, install frontend's modules `cd interface && npm install` and run
   it `npm start`
7. Copy backend's url from step 5 and paste it in the backend's url input within the web app 
8. http://localhost:3000/dreamstorm?backendUrl=https://localhost:8080

## Local development with Docker-compose

1. Make sure you have [docker](https://docs.docker.com/get-docker/) and [The NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html) installed 
2. Clone or fork this repository
3. start server `docker-compose up`, add `-d` to `docker-compose up` if you'd like to run it in the background
4. The first time will take some time to download the images, models and other dependencies. 
   models and other dependencies are downloaded only once, and then cached.
4. Copy backend's url from step 2 and paste it in the backend's url input within the web app.

   webapp at `http://localhost:3000/dreamstorm`