# Notes

Personal engineering notes — mostly Java, Spring Boot and the things around them.
Written to be re-read quickly before interviews, design discussions and reviews.

## Contents

| Topic | What's in it |
|---|---|
| [devops/](devops/) | Docker, CI/CD, deployment, infrastructure |
| [java/](java/) | Core Java, collections, concurrency, JVM |
| [spring-boot/](spring-boot/) | Spring Framework, Spring Boot, Spring Data, testing |
| [databases/](databases/) | SQL, Postgres, MySQL, MongoDB, query tuning |
| [system-design/](system-design/) | Architecture, scalability, design patterns |

### Latest notes

- [Docker — interview revision](devops/docker/docker-interview-revision.md) — Docker for Java/Spring Boot interviews: concepts, commands, layered jars, JVM in containers, Q&A

## How this repo is organised

```
Notes/
├── README.md                 <- you are here (index)
├── templates/
│   └── note-template.md      <- copy this when starting a new note
├── devops/
│   ├── README.md             <- index for this topic
│   └── docker/
│       ├── README.md
│       ├── docker-interview-revision.md
│       └── exports/          <- rendered PDF / HTML of the note
├── java/
├── spring-boot/
├── databases/
└── system-design/
```

**Rules I'm following here**

1. One topic per folder. If a topic grows past ~3 notes, give it a subfolder.
2. Every folder has a `README.md` that lists what's inside, so browsing on GitHub works.
3. Note filenames are lowercase with hyphens: `docker-interview-revision.md`.
4. Rendered files (PDF, HTML) go in an `exports/` folder next to the note, never mixed with the markdown.
5. The source of truth is always the markdown. Exports are regenerated from it.

## Adding a new note

```bash
cp templates/note-template.md java/collections-deep-dive.md
```

Then add a line for it in the topic's `README.md` and in **Latest notes** above.

## Regenerating a PDF from a note

Open the HTML export in Chrome and print to PDF, or from the terminal:

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new --disable-gpu --no-pdf-header-footer --print-to-pdf="out.pdf" "file:///absolute/path/to/note.html"
```
