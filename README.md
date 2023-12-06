# Speech to Blog Converter
The Speech to Blog Converter project is designed to transform spoken content, such as lectures, into well-formatted blog posts. The key architecture leverages the Longformer Encoder Decoder (LED) model, fine-tuned for two crucial tasks: generating the main content of the blog and creating headings for paragraphs.

## Project Process:

### Speech Recognition:
Utilizes OpenAI's Whisper API for accurate speech-to-text conversion.
The resulting transcript is meticulously formatted with punctuations for enhanced readability.

### Extractive Summarization:
Leverages NLTK and Gensim libraries for extractive summarization of the transcript.
The summary becomes the input for fine-tuned Model 1, generating fresh blog content. This content includes key sentences from the input summary.

### Paragraph Formation:
Utilizes sentence transformers to break the generated content into multiple paragraphs.
Ensures improved readability and structure for the blog post.

### Subheading Generation:
Fine-tuned Model 2 takes small paragraphs as input and generates relevant subheadings.
Enhances the organization and navigability of the blog post.

## Fine-Tuned Models:
### Model 1: Content Generation
- To generate comprehensive and coherent blog content based on the input summary.
- The model is fine-tuned using a dataset containing summaries and corresponding full-length blog posts.
- Takes a summarized transcript as input and produces a well-articulated blog content output.

### Model 2: Subheading Generation
- To create subheadings for small paragraphs, improving the overall structure of the blog post.
- Utilizes a dataset comprising paragraphs and their corresponding headings from diverse sources.
- Accepts small paragraphs as input and generates relevant subheadings, enhancing the readability and organization of the blog.

## Note:
Complete code files are available in the "all code" folder.
The project's success relies on the fine-tuned Longformer Encoder Decoder model, emphasizing its versatility in both generating blog content and crafting headings for enhanced structure.
