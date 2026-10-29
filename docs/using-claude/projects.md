# Projects

A Project is a folder for chats that share the same files and instructions. Use one per course, paper, proposal or long task.

## Why use one

- **Files once**: upload the syllabus, the draft or the data description once; every chat in the Project can use it.
- **Instructions once**: tell Claude the audience, style and rules once, not in every chat.
- **Tidy history**: all chats about one topic in one place.

Pro gives you as many Projects as you want. Large Projects are handled automatically: Claude searches the Project's files and pulls in the relevant parts.

## Create one

1. Click **Projects** in the left sidebar, then **+ New project**.
2. Give it a name and, optionally, a description.
3. Add files under **Project knowledge**: PDFs, text, code, notes.
4. Click **Set project instructions** and write them (see below).
5. Start a chat inside the Project.

## Write good instructions

Instructions are added to every chat in the Project. Keep them short and concrete.

```text
This Project is for the course "Astrofísica Extragalàctica" (4th year,
Grau en Física, UB). Students know undergraduate physics and basic Python.
- Write course material in Catalan unless I ask otherwise.
- Use the notation from the attached lecture notes.
- Exercises: give a statement, then a full solution in a separate section.
- Never invent references. If you cite something, say whether you are sure it exists.
```

## Ideas for ICCUB

| Project | What to put in it |
|---|---|
| A course | Syllabus, lecture notes, past exams, notation conventions |
| A paper in progress | Your draft, key references, the collaboration's style rules (if sharing is allowed) |
| A grant proposal | The call text, evaluation criteria, your CV, previous proposals |
| Your group's code | README, a description of the pipeline, coding conventions |
| Outreach | Your target audience, past talks, the venue's format |

## Project memory

Each Project has its own [memory](../getting-started/data-and-privacy.md#memory): what Claude learns in that Project's chats stays there and is not used in other Projects. Inside a Project, Claude also uses your general memory. For a confidential Project (a proposal you are evaluating, a paper under embargo), turn off **Use account memory** on the Project page so nothing flows in or out.

Chats in the same Project don't see each other's content unless it is in the Project files.

!!! note
    On a Pro plan, Projects are private to you. You cannot share a Project with a colleague; share the files and the instructions instead.
