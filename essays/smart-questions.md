---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2025-09-11
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">






## What’s a smart question?

Effective communication is essential in software engineering. Eric Raymond's "How to Ask Questions the Smart Way" reminds us that well-formulated, precise questions maximize the chances of receiving helpful answers and promote an open society.

Stack Overflow, a Q&A site for programmers, is a great resource for any individual who may be having issues with code or who just wants to find new or different methods of accomplishing something. There I found examples of bad questions and good questions, which could probably be improved.

A developer asked about this C/C++ snippet: <a href="https://stackoverflow.com/questions/1642028/what-is-the-operator-in-c-c"><i class="large github icon "></i>here</a>

```
Q: What is the '-->' operator in C/C++?

After reading [Hidden Features and Dark Corners of C++/STL](http://groups.google.com/group/comp.lang.c++.moderated/msg/33f173780d58dd20) on comp.lang.c++.moderated, I was completely surprised that the following snippet compiled and worked in both Visual Studio 2008 and G++ 4.4. I would assume this is also valid C since it works in GCC as well.

Here's the code:

#include <stdio.h>
int main()
{
    int x = 10;
    while (x --> 0) // x goes to 0
    {
        printf("%d ", x);
    }
}

Output:

9 8 7 6 5 4 3 2 1 0

Where is this defined in the standard, and where has it come from?
```
Analysis of Smartness

This question demonstrates several principles from Raymond’s guidelines: Clarity and specificity: The developer provides the exact code, observed output, and the context of their confusion. Prior research: They reference reading Hidden Features and Dark Corners of C++/STL, showing they attempted to understand the behavior before asking. Conciseness with context: The question is short but gives enough detail for an expert to analyze. Open-ended yet focused: They seek a precise explanation about the language standard and compiler behavior.

```
A: --> is not an operator.
It is in fact two separate operators, -- and >.

The code in the condition decrements x, while returning x's original (not decremented) value, and then compares the original value with 0 using the > operator.
To better understand, the statement could be written as follows: while( (x--) > 0 )

```

This concise explanation not only addressed the developer's query but also instructed others in a subtle point of C/C++ syntax. It shows how well-posed questions engender clear, actionable, and accurate answers.


## A not so smart question

In contrast, let us look at a hypothetical "not-so-smart" question:

```

“My program isn’t working. Can someone fix it?”

```

This question is vague: it provides no programming language, no code snippet, and no error message. It does not demonstrate any research, giving no information about what the asker has tried or observed. The default response of the community is to request clarification, asking for code or error messages. While such requests do eventually push the asker towards the inclusion of necessary information, they do not lead to immediate solutions and frustrate the asker and the potential responders as well. This highlights that poorly prepared questions are a waste of time and lead to low-quality interaction.

A contrast between these two examples points to the value of smart questions. Preparation, clear explanation of the problem, giving proper context, and demonstrating work already done saves time, gets beneficial answers, and promotes a sense of community. Conversely, ill-defined questions cause confusion, delay progress, and produce inefficiency, which ultimately get in the way of learning and problem-solving.


## Conclusion

In conclusion, smart questioning is an essential skill for software engineers. The C/C++ --> example illustrates how specificity, context, and background research allow communities to provide precise and instructive answers. The fictional "not-so-smart" example illustrates the result of inadequate preparation and clarity. By internalizing these principles, software engineers can strengthen problem-solving abilities, make meaningful contributions to collaborative communities, and further their career progression.

With the last essay as well, I had procrastinated hard on this one and had to use chatgpt to help me bulk out the essay and help with formating and such. 
