---
tags:
  - Teaching
  - LaTeX
  - Writing
---

# Turn your slides into lecture notes, chapter by chapter

| About this example | |
| --- | --- |
| **Author** | Vincent Mathieu |
| **Date** | 2026-10-08 |
| **Area** | Teaching (university course) |
| **Tools used** | Claude with access to a local folder, LaTeX |
| **Result** | Lecture notes in Catalan and Spanish, published on the UB Campus Virtual |

## Goal

Write proper lecture notes for my course from my lecture slides, in both languages the course is taught in (Catalan and Spanish), and publish them for students on the UB Campus Virtual.

## What I did

### 1. Put everything in one folder

I opened Claude, created a new folder, and put in it:

- the slides of my lectures,
- references: some books I had,
- the *pla docent* (the official course teaching plan).

The more context you give, the better and more refined the result.

### 2. Build the template first

Before writing any content, we created a LaTeX template together, with the style I wanted: fonts, colours, layout, everything. I only moved on once I was happy with the template.

It also works well to **give the structure yourself**: draft the LaTeX skeleton with the chapters and sections you want, and Claude fills it in.

### 3. Write chapter by chapter

I then asked Claude to write the lecture notes chapter by chapter, based on my slides and following the *pla docent*.

### 4. Review by writing comments directly in the .tex file

For each chapter, Claude wrote a first version. I opened the `.tex` file and wrote my own comments directly in it, where the change was needed. For example:

```latex
% Here I want an example.
% Here I want a figure.
% This figure is not correct.
```

Then I went back to the chat with Claude and said: *"I put comments in the file, go through them."*

I repeated this for several iterations, until I was happy with the chapter, then moved on to the next one.

### 5. One language first, then translate

I worked on only one language. When a chapter was final in that language, I asked Claude to translate it into the other one (Catalan ↔ Spanish).

### 6. Publish

The finished notes, in both languages, went on the course's page on the UB Campus Virtual.

## Result

Complete lecture notes, in my style and following my slides and the *pla docent*, in both Catalan and Spanish, available to students on the Campus Virtual.

## What to watch for

- **Template first.** Settling the style before writing saves reformatting every chapter later.
- **Give structure and context.** A LaTeX skeleton, the slides, the books and the *pla docent* all made the drafts closer to what I wanted.
- **Comments in the file work better than long chat messages.** Each comment sits exactly where the change is needed.
- **Iterate per chapter.** Finish one chapter before starting the next.
- **Finish one language before translating.** Otherwise every correction has to be made twice.
- **Check the physics.** Read every derivation and example: you remain responsible for the content.
