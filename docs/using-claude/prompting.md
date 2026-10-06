# Chat and prompting

Most of what you will do with Claude is an ordinary chat. A few habits make a big difference.

## Give context

Claude knows physics and Python, but not you, your project or your audience. Say:

- **Who you are** and who the output is for.
- **What the task is**, and what you will do with the result.
- **What good looks like**: length, format, level, language.

| Instead of | Try |
|---|---|
| *Explain dark matter.* | *I give a 20-minute talk to high-school students next week. Explain the evidence for dark matter in five slides' worth of bullet points, no equations, with one everyday analogy.* |
| *Fix my code.* | *This function should return the luminosity distance in Mpc for a flat ΛCDM cosmology, but gives values 10% too high at z = 1. Find the bug.* (then paste the code) |
| *Write an email to students.* | *Write a short, friendly email in Catalan to my Física Quàntica students saying the exam moves from 12 to 19 January, same room.* |

Personal preferences you set in **Settings → Profile** are added to every chat, so you don't need to repeat who you are each time (see [Your first 30 minutes](../getting-started/first-steps.md)).

## Iterate, don't restart

The first answer is a draft. Reply with what to change: *"shorter"*, *"more formal"*, *"use numpy instead of loops"*, *"the second point is wrong because…"*. Claude keeps the whole conversation in mind.

Start a **new chat** when you change topic. Very long chats get slower, use more of your allowance, and Claude can lose track of early details.

## Show an example

If you want a specific format, paste one. *"Format the references like this: …"* or *"Write the exercise in the same style as this one: …"* works better than describing the style.

## Ask Claude to check its work

- *"Check this derivation step by step and tell me where you are least sure."*
- *"List any assumptions you made."*
- *"Which of these references are you certain exist?"*

Claude will often catch its own mistakes when asked. It will not catch all of them: you still have to verify numbers, derivations and citations. See [Tips and pitfalls](../tips/index.md).

## Useful tricks

- **Extended thinking** (model menu below the message box): turn it on for derivations, debugging and anything where a careful answer matters more than a fast one.
- **Edit your message**: hover over a message you sent and click the pencil to change it and get a new answer, instead of adding a correction.
- **Retry**: the retry button under an answer gives you a different version.
- **Ask for questions first**: *"Before you start, ask me anything you need to know."* is useful for bigger tasks like a course outline or a proposal section.
- **Language**: Claude works well in English, Spanish and Catalan. Ask in one language and request the answer in another if you need to.
