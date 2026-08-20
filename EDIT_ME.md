# Editing Amogh Anakru's website

The public site is a single file, `index.html`, styled by `styles.css`. Search for `EDIT AREA` inside `index.html`; every section that is meant to be expanded is clearly marked.

## 1. Replace the portrait

Replace this file with a real photo while keeping the same filename:

```text
assets/headshot.jpg
```

A portrait-oriented image works best. The displayed crop uses a 4:5 aspect ratio.

## 2. About / biography

Search for:

```html
EDIT AREA: ABOUT
```

Suggested draft space:

### Short biography

[Write 1–2 paragraphs here.]


### Current appointment

[Write the current title, department, institution, and advisor here.]


### Optional personal sentence

[Add interests outside physics, mentoring information, or an invitation to contact you.]


## 3. Research overview

Search for:

```html
EDIT AREA: RESEARCH
```

Suggested draft space:

### Research overview

[Write 1–3 paragraphs explaining the central questions that connect your work.]


### Research direction 1

**Title:**

**Description:**

**Representative papers or links:**


### Research direction 2

**Title:**

**Description:**

**Representative papers or links:**


### Research direction 3

**Title:**

**Description:**

**Representative papers or links:**


## 4. Publication descriptions

Each publication already contains a commented template like this:

```html
<!-- <p class="pub-note">Add a short description of the paper here.</p> -->
```

Remove `<!--` and `-->`, then replace the placeholder sentence.

To add a new publication, copy this inside `<ol class="publication-list">`:

```html
<li>
  <p class="pub-title">Paper title</p>
  <p class="pub-authors"><strong>Amogh Anakru</strong>, Coauthor One, and Coauthor Two</p>
  <p class="pub-venue"><em>Journal</em> volume, page (year) · <a href="URL">journal</a> · <a href="URL">arXiv</a></p>
  <p class="pub-note">Optional one- or two-sentence description.</p>
</li>
```

## 5. Profile links

The visible links near the top currently include email, Google Scholar, ORCID, Penn State, and the CV. Add GitHub or other profiles by inserting:

```html
<span aria-hidden="true">/</span>
<a href="YOUR-URL">github</a>
```

## 6. Talks, teaching, and activities

Search for:

```html
EDIT AREA: TALKS AND ACTIVITIES
```

and

```html
EDIT AREA: EDUCATION, TEACHING, AND SKILLS
```

Copy an existing list item, replace the title, and update the year. Links to slides can be added directly after the venue.

## 7. Publish on GitHub Pages

1. Create a repository named `USERNAME.github.io`.
2. Upload everything in this folder to the repository root.
3. In GitHub, open **Settings → Pages**.
4. Choose **Deploy from a branch**, select `main`, and select the root folder.
5. The site will appear at `https://USERNAME.github.io/`.
