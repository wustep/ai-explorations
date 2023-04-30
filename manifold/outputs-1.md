## Notes
- gpt-3.5-turbo in OpenAI's Playground
- 0.4 temperature, 600+ maximum length, 1.0 top P, 0 frequency penalty, 0 presence penalty

## Prompt
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

## Examples
### Input: Will Donald Trump return to twitter?
{prompt: "Donald Trump's return on Twitter: Will @realDonaldTrump tweet in 2023?", closing_date: "Dec 31, 2023", description: "Twitter permanently banned former president of the USA, Donald Trump, from the platform in January 2021 during the final days of his term. His handle @realDonaldTrump had over 88.9 million followers.
 
This market will resolve to "Yes" if Donald J. Trump's verified Twitter account (@realDonaldTrump) tweets at least once in 2023 (ET timezone). Otherwise, this market will resolve to "No".
 
The resolution source for this market will be Donald J. Trump's verified Twitter account: https://twitter.com/realdonaldtrump.
 
Please note, only the @realDonaldTrump verified Twitter account counts for this market, regardless of the URL for this profile. If Donald J. Trump tweets from another account, it has no bearing on the resolution of this market."}
### Output: 0.6
Factors supporting a YES resolution:
 
- Trump has expressed his desire to return to social media, including Twitter. In March 2021, he stated in an interview that he was "negotiating with a number of people" to create his own social media platform and that he would return to Twitter if he couldn't. This suggests that he has a strong motivation to tweet again.
- Trump has a history of using Twitter to communicate with his followers and the public. During his presidency, he frequently used the platform to make announcements, share his thoughts, and criticize his opponents. It is likely that he will continue to use Twitter as a means of communication, especially if he is unable to create his own social media platform.
- The closing date for this market is December 31, 2023, which gives Trump plenty of time to return to Twitter. Although he has been banned from the platform, there is always the possibility that Twitter may reverse its decision, especially if he is no longer in office.
- Trump has a large following on Twitter, with over 88.9 million followers on his @realDonaldTrump account. This suggests that there is a significant audience for his tweets, which may motivate him to return to the platform.
- Trump may use Twitter as a way to remain relevant in the political sphere. Although he is no longer president, he still has a significant influence on the Republican party and may use Twitter to voice his opinions and endorse candidates.
 
Factors supporting a NO resolution:
 
- Twitter has permanently banned Trump from the platform, which suggests that it is unlikely that he will be able to tweet from his @realDonaldTrump account. Although he may create a new account, this market is specifically focused on his @realDonaldTrump account.
- Trump may choose to focus on other means of communication, such as his own social media platform or traditional media outlets. In March 2021, he also stated that he was considering starting his own social media platform, which may make it less likely that he will return to Twitter.
- Trump may decide to stay out of the public eye altogether. Although he has a history of using Twitter to communicate with his followers, he may choose to retire from politics and focus on other pursuits.
- The market prompt specifies that the resolution source for this market will be Donald J. Trump's verified Twitter account (@realDonaldTrump). This means that if he tweets from another account, it will not count towards a YES resolution. It is possible that Trump may create a new account or use a different platform to communicate with his followers.
- The market prompt also specifies that the resolution will be based on a tweet from Trump's @realDonaldTrump account in 2023. This means that if he tweets before or after 2023, it will not count towards a YES resolution.
 
Probability: 0.6. While there is a possibility that Trump may return to Twitter, there are also factors that make it unlikely, such as his permanent ban from the platform and his potential focus on other means of communication. However, the long time frame until the end of 2023 leaves room for potential changes

### Input: Will Elon Musk be Tesla's CEO through 2023?
{prompt: "Will Elon Musk be Tesla's CEO through 2023?", closing_date: "Dec 30, 2023"}

### Output: 0.8
Factors supporting a YES resolution:
 
- Elon Musk has been the CEO of Tesla since 2008 and has been instrumental in the company's success. He has a strong vision for the company and has been able to execute it effectively. This suggests that he is committed to the company and may continue to serve as CEO.
- Musk has a significant personal stake in Tesla's success. He owns a significant portion of the company's stock and has a strong financial incentive to continue leading the company. This may motivate him to remain as CEO through 2023.
- Tesla is currently in a strong position, with a market capitalization of over $700 billion as of April 2023. This suggests that the company is performing well and may continue to do so under Musk's leadership.
- Musk has a reputation for being a workaholic and has been known to work long hours. This suggests that he is committed to his work and may be willing to continue serving as CEO of Tesla.
- The closing date for this market is December 30, 2023, which is less than a year away from the present date. It is unlikely that Musk will step down as CEO in such a short amount of time.
 
Factors supporting a NO resolution:
 
- Musk has a history of making unexpected decisions and may choose to step down as CEO of Tesla. He has previously stepped down as CEO of PayPal and may do the same with Tesla.
- Musk has a number of other business ventures, including SpaceX and The Boring Company, which may take up more of his time and attention. This may make it difficult for him to continue serving as CEO of Tesla.
- Musk has been known to clash with regulators and may face regulatory challenges that could make it difficult for him to continue leading Tesla. For example, in 2018 he was forced to step down as chairman of Tesla's board as part of a settlement with the SEC over his tweets about taking Tesla private.
- Tesla is facing increasing competition in the electric vehicle market, which may make it more difficult for the company to maintain its dominance. This may lead to pressure on Musk to step down as CEO.
- Musk has a history of making controversial statements on social media, which has led to criticism and negative publicity for Tesla. This may lead to pressure on him to step down as CEO.
 
Probability: 0.8. While there is a possibility that Musk may step down as CEO of Tesla, there are also factors that make it likely that he will continue to serve in this role, such as his personal stake in the company and his commitment to his work. Additionally, the short time frame until the end of 2023 makes it unlikely that he will step down in the near future.

### Input: Will a non-crappy video equivalent of dall-e be published before June 2023?
{prompt: "Will a non-crappy video equivalent of dall-e be published before June 2023?", closing_date: "June 1, 2023", description: "Based on this tweet https://twitter.com/ArthurB/status/1528991584309624832 Question resolves positive if a model is capable of generating arbitrary videos of reasonable quality from text prompts and demonstrates "object permanency" in the sense that it can resolve full object oclusions correctly(for example a mountain being temporarily hidden by a low cloud should still be there after the cloud moves) most of the time. If it's unclear whether some existing model has the capabilities by the deadline I'll use my judgment to decide how to resolve the market, and will lean towards yes in cases where the model mostly does it correctly for simple videos but fails at cherrypicked edge cases.
 
Edit:
 
For extra clarification published means that at least a paper or some oficial announcement has to come out about it before that date. 
 
Also the fact I haven't resolved yes doesn't necesarily mean that I think none of the stuff that is out yet counts, I'm likely going to wait until June in any case and resolve based on the best model avaliable by then, unless something pretty clearly counts before then (in case someone was updating on how harsh my judgment is based on seeing that I haven't resolved despite whatever model coming out). 
Edit2:
Also note that the criterion isn't based on the original tweet and I might resolve yes based on my own intepretation of what counts as dall-e equivalent and "object permanence" despite Eliezer and Arthur considering Eliezer was right about the original spirit of that question .
Edit3: 
By reasonable quality and non crappy I mean something like "dall-e" level quality not "gets hands and details perfectly right and theres no weird artifacts" levels of quality.
Stuff like gen2 might qualify but will have to play arround with it or whatever better model replaces it by the deadline to decide."}

### Output: 0.4
Factors supporting a YES resolution:
 
- There has been significant progress in the field of generative models for images and videos in recent years, with models such as GPT-3 and DALL-E demonstrating impressive capabilities. It is possible that a model capable of generating arbitrary videos of reasonable quality from text prompts and demonstrating object permanency may be developed before June 2023.
- There is significant interest in this area of research, with many researchers and companies working on developing generative models for videos. This suggests that there is a strong motivation to develop a non-crappy video equivalent of DALL-E.
- The market prompt specifies that a paper or official announcement must be made about the model before June 1, 2023. This means that even if a model is developed but not widely known, it may still count towards a YES resolution.
- The market prompt also specifies that the resolution will lean towards YES in cases where the model mostly does it correctly for simple videos but fails at cherry-picked edge cases. This means that even if the model is not perfect, it may still count towards a YES resolution if it meets the criteria specified in the prompt.
- The market creator has indicated that they will use their judgment to decide how to resolve the market if it is unclear whether an existing model has the required capabilities. This suggests that there is some flexibility in how the market will be resolved.
 
Factors supporting a NO resolution:
 
- The market prompt specifies that the model must demonstrate object permanency in the sense that it can resolve full object occlusions correctly most of the time. This is a challenging task and may be difficult to achieve by June 2023.
- The market prompt also specifies that the model must generate videos of reasonable quality, but not necessarily perfect quality. However, what constitutes "reasonable quality" is subjective and may be difficult to define. This may make it difficult to determine whether a model meets the criteria specified in the prompt.
- The market prompt specifies that the model must be published before June 1, 2023. This means that even if a model is developed after this date, it will not count towards a YES resolution.
- The market creator has indicated that they will use their judgment to decide how to resolve the market if it is unclear whether an existing model has the required capabilities. This introduces some subjectivity into the resolution process, which may make it difficult to predict the outcome of the market.
- The time frame until the closing date is relatively short, which may make it difficult for a model to be developed and published in time to meet the criteria specified in the prompt.
 
Probability: 0.4. While there is a possibility that a non-crappy video equivalent of DALL-E may be published before June 2023, there are also factors that make it unlikely, such as the challenging nature of the task and the short time frame until the closing date. Additionally, the subjective nature of the criteria specified in the prompt may introduce some uncertainty into the resolution process.


### Input: Will the world end in 2024?
{prompt: "Will the world end in 2024?", closing_date: "Dec 2024"}

### Output: 0.001
Factors supporting a NO resolution:

- There is no scientific evidence or prediction that the world will end in 2024. While there have been various doomsday predictions throughout history, none of them have come true. The idea of the world ending in 2024 is purely speculative and not based on any credible sources.
- The laws of physics and nature do not suggest that the world will end in 2024. While there are natural disasters and other catastrophic events that can occur, they are unlikely to result in the complete destruction of the planet. Even events such as asteroid impacts or supervolcano eruptions are highly unlikely to cause the end of the world.
- There is no evidence of any supernatural or divine intervention that would cause the end of the world in 2024. While some religious texts may make predictions about the end of the world, these are generally interpreted as metaphorical or symbolic rather than literal.
- There is no indication that any major global event or crisis will occur in 2024 that would lead to the end of the world. While there are always potential threats such as pandemics, wars, or economic collapses, these are unlikely to result in the complete destruction of the planet.
- The closing date for this market is December 2024, which means that there is only a short time frame for the world to end. Given the lack of evidence or credible predictions, it is highly unlikely that the world will end in such a short period of time.

Factors supporting a YES resolution:

- There is no credible evidence to support a YES resolution. The idea of the world ending in 2024 is purely speculative and not based on any scientific or credible sources.
- The laws of physics and nature do not suggest that the world will end in 2024. While there are natural disasters and other catastrophic events that can occur, they are unlikely to result in the complete destruction of the planet. Even events such as asteroid impacts or supervolcano eruptions are highly unlikely to cause the end of the world.
- There is no evidence of any supernatural or divine intervention that would cause the end of the world in 2024. While some religious texts may make predictions about the end of the world, these are generally interpreted as metaphorical or symbolic rather than literal.
- There is no indication that any major global event or crisis will occur in 2024 that would lead to the end of the world. While there are always potential threats such as pandemics, wars, or economic collapses, these are unlikely to result in the complete destruction of the planet.
- The closing date for this market is December 2024, which means that there is only a short time frame for the world to end. Given the lack of evidence or credible predictions, it is highly unlikely that the world will end in such a short period of time.

Probability: 0.001. The idea of the world ending in 2024 is purely speculative and not based on any credible sources. The laws of physics and nature do not suggest that the world will end in 2024, and there is no evidence of any supernatural or divine intervention that would cause the end of the world. While there are always potential threats such as pandemics, wars, or economic collapses, these are unlikely to result in the complete destruction of the planet.

## Input: Will Google be acquired by 2024?
{prompt: "Will Google be acquired by 2024?", closing_date: "Dec 2024"}

### Output: 0.3
Factors supporting a YES resolution:

- Google is a highly valuable company with a market capitalization of over $1 trillion. This makes it an attractive target for potential acquirers who are looking to expand their reach or gain a competitive advantage.
- There have been rumors and speculation in the past about potential companies that may be interested in acquiring Google, such as Apple or Amazon. While these rumors have not come to fruition, they suggest that there is interest in acquiring the company.
- The technology industry is constantly evolving and changing, and acquisitions are a common way for companies to stay competitive and grow. It is possible that a company may see acquiring Google as a way to gain a foothold in a new market or expand their existing offerings.
- The closing date for this market is December 2024, which means that there is still time for an acquisition to occur. While it may seem unlikely at the moment, there are always potential acquirers who may emerge in the future.
- Google's business model relies heavily on advertising, which may make it vulnerable to changes in the advertising industry or regulations that limit the use of user data. If Google's revenue were to decline significantly, it may become more attractive as an acquisition target.

Factors supporting a NO resolution:

- Google is a highly valuable company with a market capitalization of over $1 trillion. This makes it an attractive target for potential acquirers who are looking to expand their reach or gain a competitive advantage. However, this also means that any potential acquisition would be extremely expensive and may not be feasible for most companies.
- Google has a strong market position and is a leader in many of the markets it operates in, such as search, advertising, and cloud computing. This may make it less attractive as an acquisition target, as potential acquirers may not see a significant benefit in acquiring a company that is already dominant in its markets.
- Google has a strong corporate culture and a unique way of operating that may not be compatible with potential acquirers. This could make it difficult to integrate Google into another company and may make an acquisition less likely.
- The technology industry is constantly evolving and changing, and acquisitions are a common way for companies to stay competitive and grow. However, there are also many other ways for companies to achieve these goals, such as partnerships or internal development. It is possible that potential acquirers may choose to pursue these other options instead of acquiring Google.
- The closing date for this market is December 2024, which means that there is only a short time frame for an acquisition to occur. Given the complexity and expense of such a deal, it may be unlikely that an acquisition will occur in such a short period of time.

Probability: 0.3. While Google is a highly valuable company and may be an attractive acquisition target, there are also factors that make an acquisition less likely, such as its strong market position and corporate culture. The short time frame until the end of 2024 also makes it less likely that an acquisition will occur, but there is always the possibility of a surprise acquisition.
