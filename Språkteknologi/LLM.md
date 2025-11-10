
är som mycket större [[neural networks]] för att predicta nästa ord osv
- left to right word prediction kallas *casual/autoregressive*

finns tre arkitekturer:
- Decoder: input token, output token
	- genererar text
- Encoders: ta tokens som input, genererar vector encoding av varje token
	- Ex för skapa classifiers
- encoder-decoder take tokens as input and generate a series of tokens as output.
	- mycket mer loose relationsship mellan input och output tokens; kan vara ex machine translation

### Decoders
- m¨ånga NLP tasks kan ådstakommas av dessa
- ex sentiment analysis: ![[Pasted image 20251108125206.png]]
- conditiona på tidiagare och och på prob distribution över nästa ord
- instruction tuning: fortsätta träna pre trained llm på instriuctions och deras responses

**hur välja nästa ord**?
- tar softmax av alla logits från output layer
- greedy decoding = alltid ta mest likely token
	- blir för generic, deterministiskt i samma kontext
	- använder istället ofta random sampling
- samplingen kallas random sampling/multinomial sampling
- ![[Pasted image 20251108131929.png]]
- har dock för hög randomness för finns många low prob ord
- använder därför *temperature sampling*
	- Resvala prob dist så mer likely tokens blir ännu mer likely, mindre likely ännu indre
	- har en temprature factor $\tau$
	- ![[Pasted image 20251108132320.png]]

### Training llm
- tre steg:
	- pretraining: träna generelt med cross entropy loss function på stor corpora. Kan generera text
	- instgruction tuning: träna igen på corpus med frågor och korrekt svar
	- alginment: ge context och två potentiella continuations, en labeled accepted, den andra rejected
- loss function: skillnad actual och predicted prob dist ![[Pasted image 20251108133122.png]]
- eftersom one-hot: ![[Pasted image 20251108133229.png]]
- vi använder aldrig predicted word för den fortsatta sequencen under training, kallas teacher forcing
- i batch tar vi average
	- ![[Pasted image 20251108133811.png]]

### Evaluating llms
- använd hur hög log prob model assignar till en given text
- ![[Pasted image 20251108134600.png]]
- ![[Pasted image 20251108134629.png]]
- ett problem med detta är att probabilityn blir mindre och mindre desto fler ord vi lägger till
	- perplexity är en sådan length normalized function:
		- ![[Pasted image 20251108134828.png]]
		- ![[Pasted image 20251108134833.png]]
	- kan bli väldigt olika om olika model har olika tokenizers, bäst jämföra på sådana med samma
- kan också testa performance på downstream tasks: exempelvis MMLU (Massive Multitask Language Understanding) dataset, frågor i olika områden