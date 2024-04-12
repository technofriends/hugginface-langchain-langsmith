# Text Generation with Falcon-7B Language Model

This project demonstrates how to use the Falcon-7B language model from the Hugging Face Hub to generate text based on a given prompt. The code is written in Python and utilizes the Langchain and Langchain Community libraries.

## Prerequisites

Before running the code, make sure you have the following:

- Python 3.x installed
- Hugging Face API token
- Langchain API token

## Setup

1. Install the required dependencies by running the following command:

   ```bash
   pip install langchain langchain_community python-dotenv
   ```

2. Obtain your Hugging Face API token:
   - Go to the [Hugging Face website](https://huggingface.co/) and sign up for an account if you don't have one already.
   - Navigate to your [Hugging Face profile settings](https://huggingface.co/settings/token) and generate a new API token.
   - Copy the generated token.

3. Obtain your Langchain API token:
   - Go to the [Langchain website](https://langchain.com/) and sign up for an account if you don't have one already.
   - Navigate to your [Langchain API settings](https://langchain.com/account/api-keys) and generate a new API token.
   - Copy the generated token.

4. Create a `.env` file in the project directory and add the following keys and their corresponding values:

   ```
   LANGCHAIN_API_KEY=<your_langchain_token>
   HUGGINGFACEHUB_API_TOKEN=<your_huggingface_token>
   LANGCHAIN_TRACING_V2="true"
   LANGCHAIN_PROJECT="generativegeekdemo"
   ```

   Replace `<your_langchain_token>` with your actual Langchain API token and `<your_huggingface_token>` with your actual Hugging Face API token.

## Usage

1. Open the Python script or Jupyter Notebook containing the code.

2. Make sure the `.env` file is in the same directory as the script or notebook.

3. Run the code cells or execute the script.

4. The code will load the Falcon-7B language model from the Hugging Face Hub using the provided API token.

5. You can modify the `query` variable to specify the initial text prompt for text generation. For example:

   ```python
   query = "A boy went to school and he "
   ```

6. The language model will generate text based on the provided prompt, and the generated text will be printed as output.

## Customization

- You can experiment with different text prompts by modifying the `query` variable in the code.

- If you want to use a different language model from the Hugging Face Hub, you can change the `repo_id` parameter in the following line of code:

  ```python
  llm = HuggingFaceHub(repo_id="tiiuae/falcon-7b-instruct")
  ```

  Replace `"tiiuae/falcon-7b-instruct"` with the desired model repository ID.

## Troubleshooting

- If you encounter any issues related to missing dependencies, make sure you have installed the required libraries mentioned in the setup section.

- If you face authentication errors, double-check your API tokens and ensure they are correctly set in the `.env` file.

- For any other issues or questions, please refer to the documentation of the respective libraries (Langchain and Langchain Community) or seek support from their respective communities.

## License

This project is licensed under the [MIT License](LICENSE).

Feel free to modify and adapt the code to suit your needs. Happy text generation!
