# AI Image Generation with OpenAI's DALL-E

Simple API calls using OpenAI's Image Generation APIs.

## Images generated with OpenAI `DALL-E 3`

Prompt:

> "Create a wintery photo image for a horse and a skier. Include both the horse and the skier in the picture in full. The horse should run fast and pull the skier behind him with ropes. The horse should not be on skis. The skier should look like a Mongolian person from 100 years ago. The photo should look like it's 30 years old."

    Despite clear instructions, there is at least one issue with all the pictures.

|            image 1 - 2             |            image 3 - 4             |            image 5 - 6             |
| :--------------------------------: | :--------------------------------: | :--------------------------------: |
| ![skijoer1](./images/skijoer.png)  | ![skijoer3](./images/skijoer3.png) | ![skijoer5](./images/skijoer5.png) |
| ![skijoer2](./images/skijoer2.png) | ![skijoer4](./images/skijoer4.png) | ![skijoer6](./images/skijoer6.png) |

## Image Variations

I created variation images with OpenAI's `DALL-E 2` for the last image crated previously.

> The AI may have recognised the ambiguity with the horse running over skis so it removed them, or they were just lost as insignificant details. However, for all the variations, the AI decreased the image quality significantly. Variations are only available for `DALL-E 2`.

| variation 1 | variation 2 | variation 3 |
| :---------: | :---------: | :---------: |
| ![variation1](./image-variations/skijoer-variation-0.png) | ![variation2](./image-variations/skijoer-variation-1.png) | ![variation3](./image-variations/skijoer-variation-2.png) |

## Image Edits

I edited the picture with `DALL-E 2`'s `edit` functionality. (Edits are only available for `DALL-E 2`)

> For the first edit, I tried to remove the skis from under the horse.

|              original picture              |                     mask                      |                   edited picture                    |
| :----------------------------------------: | :-------------------------------------------: | :-------------------------------------------------: |
| ![original-picture](./images/skijoer6.png) | ![masked-picture](./images/skijoer6-mask.png) | ![edited-picture](./image-edits/skijoer-edit-1.png) |


> For the second time, I tried adding visible skis under the person. The last picture is finally true to the original prompt.

|              original picture              |                     mask                      |                   final picture                    |
| :----------------------------------------: | :-------------------------------------------: | :-------------------------------------------------: |
| ![original-picture2](./image-edits/skijoer-edit-1.png) | ![masked-picture2](./image-edits/skijoer-edit-1-mask.png) | ![edited-picture](./image-edits/skijoer-edit-4.png) |

---

---

## How to run this project?

0. Prerequisites:

   - Make sure Python3 is installed.
   - If you don't have an account with OpenAI, create one here: https://openai.com/
   - Create a project API key under Dashboard / API keys

1. Clone the project.

2. Create a virtual environment inside the project folder:

   `python -m venv venv`

3. Activate the virtual environment:

   Mac: `source venv/bin/activate`

   Windows: `venv\Scripts\activate`

4. Install the python dependencies:

   `pip install -r requirements.txt`

5. Create an `.env` file in the root folder and add your project's API key:

   ```
   OPENAI_API_KEY=your-unique-opanai-project-key

   ```

6. Run the Jupyter Notebook:

   - `jupyter notebook` command will open the Notebook in the browser.
   - The DALL-E-3 image generation code is in the `openai-dall-e.ipynb` file.
   - Image Variations code is in `openai-dall-e-variations.ipynb` file.
   - Image Edit code is in `openai-dall-e-edits.ipynb` file.

## Credits

- This project was adopted from Colt Steele's Walkthrough project on Udemy: [Mastering OpenAI Python APIs](https://www.udemy.com/course/mastering-openai/?couponCode=24T3MT53024).

  Changes made: I updated the API calls as per the latest documentation.

- OpenAI: https://openai.com
