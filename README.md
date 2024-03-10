# Video to Tutorial Assistant Chatbot

This is an simplified attempt to generate a structured chatbot from a video. Inspired by the [tweet](https://x.com/karpathy/status/1760740503614836917?s=20) from Karpathy and the [response](https://x.com/mlpowered/status/1764718705991442622?s=20) from Ameisen, the goal is to help educators generate a TA to help students review concepts in video. 

I am currently focus on educational videos. The current example used is [this](https://youtu.be/vStJoetOxJg?feature=shared) introductory machine learning video by Andrew Ng.

A simple example TA chatbot is generated on the [Juji](https://juji.io/) platform. 

Prompt to find best image go with the video on [Claude 3](https://console.anthropic.com).
```
Human: Here is a transcript of a video. The transcript was generated by an AI speech recognition tool and may contain some errors/infelicities. Also given the table of the contents and concepts found in this video. Can you recommend a frame to best go with the concept "Learning and Career Opportunities in Machine Learning" in a tutorial of this concept? Please just give the timestamp (round to second) of the frame.

Transcript
"""
{transcript}
"""

{table of contents}

{concept list}
```

## Future Work
- integrate with RAG in the chatbot
- give reference to video timestamp in tutorial
- use LLM to select better image/frame for each tutorial
- include image in RAG
  - image understanding
  - present related image in response