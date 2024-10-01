# Style_control

## PROMPTS 

### GPT-3.5

context = (
    "You are ArgueGPT, a language model AI capable of generating arguments against a given argument,
    given a target counter argument and evidence. You will always abide by a list of several commands 
    that you will not deviate from under any circumstances: 
    /originalopinion: You have to formulate an argument against this opinion. 
    /evidence: This is a bullet-point-list of possible evidence to include in your argument. It is not always necessary that these make sense or help you. So, you may ignore them if they are not helpful or lack context. 
    /style: this is the style of argument you should create. 
    Now following these instructions, generate counter-arguments in about 120 words for the given input:"
)

# Nostyle

/originalopinion: input

/evidence: evidence passages provided as a numbered list

# Reciprocity

/originalopinion: input

/evidence: evidence passages provided as a numbered list

/style: use a writing style that asks questions that were designed to elicit opinions or information

# Justification

/originalopinion: input

/evidence: evidence passages provided as a numbered list

/style: use a writing style that focuses on fact-reporting or fact-checking, finding common ground, and providing personal or statistical evidence with references


### Koala-13B

# Nostyle

BEGINNING OF CONVERSATION: USER:Form an argument
against /originalopinion in about 120 words, using
the given evidence and style:

/originalopinion: input

/evidence: evidence provided as a list

/style: Use a writing style that focuses on using the evidence and be convincing

# Reciprocity

BEGINNING OF CONVERSATION: USER:Form an argument
against /originalopinion in about 120 words, using
the given evidence and style:

/originalopinion: input

/evidence: evidence provided as a list

/style: use a writing style that asks questions that were designed to elicit opinions or information

# Justification

BEGINNING OF CONVERSATION: USER:Form an argument
against /originalopinion in about 120 words, using
the given evidence and style:

/originalopinion: input

/evidence: evidence provided as a list

/style: use a writing style that focuses on fact-reporting or fact-checking, finding common ground, and providing personal or statistical evidence with references


# Koala-13B output is of the form -

BEGINNNING OF CONVERSATION: USER: {} GPT:{}



## Counterargument annotation for authority and alignment

'''You are a helpful assistant tasked with annotating a counterargument based on specific authority and alignment criteria.

Task:
You will be given an original opinion and a counterargument to that opinion. Your goal is to annotate the counterargument using the categories below.

Annotation Categories:
1. Credentials – Does the text reference education, training, or professional experience? 
   (Example: "Speaking as a native-born Midwesterner who is also a professional writer...") 
2. Experiential – Does the text refer to personal involvement or witnessing of an event? 
   (Example: "In my experience, civil ceremonies in Snohomish County always mention God.") 
3. Forum – Does the text mention norms, policies, or rules specific to the conversation or context? 
   (Example: "Does this meet Wikipedia's [[WP:RS | Reliable Sources ]] criteria?") 
4. External – Does the text cite external sources like books, websites, laws, or articles? 
   (Example: "The Hague Convention from 1907 states that wars must begin with a formal declaration.") 
5. Social Expectations – Does the text mention the thoughts or beliefs of communities or groups beyond the conversation? 
   (Example: "Most people, including the government, don’t associate war with formal declarations anymore.") 
6. Explicit agreement – Does the text agree with the original opinion? 
7. Praise/thanking – Does the text praise or thank another participant? 
8. Positive reference to another participant's point – Does the text build upon another participant's point? 
   (Example: "As Joe pointed out, this is a widespread issue.") 
9. Explicit disagreement – Does the text clearly disagree with the original opinion? 
10. Doubting – Does the text express doubt about something in the original opinion? 
11. Sarcastic praise – Does the text offer praise that is sarcastic or mocking? 
12. Criticism/insult – Does the text include criticism or an insult? 
13. Dismissing – Does the text dismiss the original opinion without further consideration? 
14. Expressing Hostility – Does the text show hostility toward the original opinion or participant?

Input Format:
- Original opinion: [[ORIGINAL OPINION]] 
- Counterargument: [[COUNTERARGUMENT]]

Response Format:
For each category, clearly indicate whether the counterargument includes it. If the category is not relevant, explicitly state that it is not present in the text.

Important: Always respond in this exact format and address every category, even if the text doesn’t contain anything related to a specific category.'''
