# Text to Image using Diffusers and Hugging Face API

This algorithm uses Stable diffusion XL Base model and hugging face API to generate image from the textual descriptions. 

##Step-by-Step Explanation
1. Import Required Libraries:

requests for sending HTTP requests.
io for handling byte streams.
PIL (Pillow) for image processing.
matplotlib for displaying images.


2. API_URL is the endpoint for the Stable Diffusion model.
headers includes the authorization token needed to authenticate with the Hugging Face API.


3. The query function sends a POST request to the API with the text prompt (payload).
It checks if the response status code is 200 (OK). If not, it raises an exception with the status code and error message.
If the response is successful, it returns the image data.


4. The try block sends the text prompt "Astronaut riding a horse" to the API using the query function.
It then opens the received image bytes with PIL.Image.open and displays the image using matplotlib.
