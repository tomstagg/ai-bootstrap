	Pretraining
- Download and process the internet
	- FineWeb - curated text data at scale, currated by Hugging Face: https://huggingface.co/spaces/HuggingFaceFW/blogpost-fineweb-v1
	- hugh quantity of very large with hugh diversity and high quality
	- 44TB of filter data - 16GB Hard drive for £250 today
	- Data from common crawl - 2.7 Billion web pages, crawls via seed links to other pages
	- Blocked list: malware, marketing, adult, gambling, etc
	- Text is extracted and filters : remove tags, code, PII removals, filtered to english
	- dataset is shown here: https://huggingface.co/datasets/HuggingFaceFW/fineweb
- Tokenization - convert text to symbols
	- chunk of text - a word or partial word
	- used for efficiency - smaller more manageable chunks that a model can handle
	- show text file and tokeniser https://tiktokenizer.vercel.app/] cl100k_base
	- show hello world - uses two tokens
	- demo show a chunk of text  and conversion to tokens. 
	- 100,277 possible tokens 
- neural network training
	- take windows of tokens between 0 and 8000 - we attempt to predict the next token which comes in the sequence
	- we get the initial neural network to predict the word/token which comes next
	- initially randomly initialised
	- we know what comes next and we can update the nn and tuning it many many times, updating the parameters
	- takes a lot of compute and long training runs to reduce the loss - how well it is performing. Low is good
- nn internals
	- weights of parameters - which are sets of knobs on dj set to adjust
	- a neural net is just a list of numbers with Billions of parameters, 8,70,450, Trillion
	- All it is doing is * / exp() + - a giant mathemticaly expression.
	- An example is here: https://bbycroft.net/llm
	- network is called the transformer - information flows from input the tokens, to the ouput the next token prediction
		- embeddings - a vector for each token
		- matric multiplications, etc
	- like a synthetic neurons  - similar to brain tissue in some ways
- inference
	- token at a time
	- context length 
- Chat GPT-2 example
- GPUs - computer power
	- driven NVIDA to be the 3rd largest compnay in the world

- post training
	- questions and answers: https://huggingface.co/datasets/OpenAssistant/oasst1/viewer/default/train?views%5B%5D=train
	- model imitates a human labeller
	- hallucinations
		- even if some part of the networks doesn't know the answer, some form of it's training set confidently answer it
		- it will try and do it's best and imitate
		- https://huggingface.co/spaces/huggingface/inference-playground "who is Zarellin Vexmoor?"




links
fineweb https://huggingface.co/spaces/HuggingFaceFW/blogpost-fineweb-v1
Tiktokenizer: [https://tiktokenizer.vercel.app/]
llm visualisation https://bbycroft.net/llm
inference playground: https://huggingface.co/spaces/huggingface/inference-playground
sesame AI demo: https://youtu.be/fgvRn86B5X0?t=84
text: /Users/x2027763/personal/ai-bootstrap/text.txt
tokens: /Users/x2027763/personal/ai-bootstrap/tokens.txt