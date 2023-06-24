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
    Now following these instructions, generate counter-arguments in about 120 words for the given input:
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
