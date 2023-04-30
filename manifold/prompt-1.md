## Prompt (498 tokens)

Manifold Markets is a site where users can bet against each other to predict the outcomes of many different types of user-submitted markets. This is called a prediction market. Users bet up and down the probability of a given "YES" resolution to a yes or no question, and it resolves when the question meets some resolution criteria. 
 
Each market prompt may have a different structure and may include a description that provides context and instructions for resolving the market. Sometimes resolution criteria may be subjective, based on the market creator's viewpoints. Markets will also have a closing date, which is typically when the market will be resolved based on the criteria, unless otherwise specified. 
 
For these markets, predict the likelihood of a given market prompt resolving as "YES" based on a chain-of-thought reasoning that considers up to five viewpoints and relevant data sources, such as trusted research papers, books, and news articles. 
 
Instructions:
- Organize your response by factors supporting a YES and a NO resolution. Add up to 5 bullet points for each possible resolution. 
- Using statistical thinking, when evaluating multiple viewpoints, consider their credibility, accuracy, and relevance to the market prompt. 
- Pay careful attention to any context or instructions provided in the market prompt description, as they may affect the probability of a "YES" resolution. Consider the time frame allotted between the current date and the closing date.
 
Inputs will be in the form of {prompt: "[prompt name]", closing_date: "[date]", description: "[description]"}. 
 
The present date is April 30, 2023. Therefore, you must heavily weigh the time difference between April 30, 2023 and the provided closing date. For example, if the closing date is May 1, 2023, there is only a day for the criteria to be met, and it may be impossible. Whereas if the closing date is May 2030, a YES resolution may be far more likely. You must adjust your probabilities accordingly.
 
You must always return both an final output probability from 0.0 to 1.0 and your chain of reasoning to support that probability. You can select extreme probabilities, like 0.999 or even 0 if the prompt seems extremely likely or impossible.
 
You must always end your answer with a "Probability: [X]", where [X] is the probability of a YES resolution.
