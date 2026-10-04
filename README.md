# Assignment 3. Responsive Web Design (Media Queries + Bootstrap Grid)

## Part 1. Media Queries

### Task 0. Responsive Typography

**Task:** Create a simple webpage with headings and paragraphs. Use media queries to change font sizes for mobile, tablet and desktop.

**What I did:** I wrote a text block with headings (`h3`, `h4`, `h5`) and paragraphs. Base styles are for mobile (small fonts). Two `min-width` media queries increase the font sizes for tablet and desktop.

| Element | Mobile | Tablet | Desktop |
|---|---|---|---|
| Main heading | 20px | 28px | 38px |
| Subheading | 17px | 22px | 28px |
| Paragraph | 14px | 17px | 20px |

**Mobile (375px)**

<img width="485" height="888" alt="image" src="https://github.com/user-attachments/assets/59764072-c688-4c03-a89d-21c2eb1e3076" />
)

**Tablet (800px)**

<img width="1023" height="807" alt="image" src="https://github.com/user-attachments/assets/cdb0dfec-8760-442b-ab48-67e8ec6f8386" />

**Desktop (1280px)**

<img width="1135" height="627" alt="image" src="https://github.com/user-attachments/assets/7d4448bf-33c4-489e-87f0-c7c2ec503cf3" />


### Task 1. Responsive Layout with Media Queries

**Task:** Create a webpage with three boxes in a row. Desktop: three side by side. Tablet: two in a row. Mobile: stacked vertically. Use only CSS media queries (no Bootstrap).

**What I did:** The boxes are inside a flex container with `flex-wrap: wrap` and `gap: 20px`. On mobile each box has `width: 100%`. On tablet the width is `calc((100% - 20px) / 2)`, and on desktop `calc((100% - 40px) / 3)`. The `calc()` takes the gaps into account. Bootstrap classes are not used in this section.

**Mobile (375px)**

<img width="480" height="801" alt="image" src="https://github.com/user-attachments/assets/3c765f3a-ab62-4469-9ec2-67c4f5920450" />

**Tablet (800px)**

<img width="1026" height="551" alt="image" src="https://github.com/user-attachments/assets/74f122f5-6394-4d89-9077-c7f0f400be6f" />


**Desktop (1280px)**

<img width="1135" height="251" alt="image" src="https://github.com/user-attachments/assets/5dab7a6c-df8f-4274-8926-6effe6f20bf4" />


## Part 2. Bootstrap Grid System

### Task 2. Bootstrap Responsive Columns

**Task:** Build a responsive layout using Bootstrap's 12-column grid with three columns. Desktop: each column takes 4 columns. Tablet: two columns on the first row and one on the second. Mobile: all columns stacked.

**What I did:** I used `container`, `row g-3` and three columns with the classes `col-12 col-md-6 col-lg-4`:

- `col-12` - on mobile each column takes all 12 parts (stacked);
- `col-md-6` - from 768px each column takes 6 parts (two per row, the third wraps to the second row);
- `col-lg-4` - from 992px each column takes 4 parts (three per row).

**Mobile (375px)**

<img width="492" height="752" alt="image" src="https://github.com/user-attachments/assets/476920c3-2078-4ae2-b5c2-8cce827a1a8c" />

**Tablet (800px)**

<img width="1017" height="556" alt="image" src="https://github.com/user-attachments/assets/21f593b6-a36c-4e04-b70f-32d8be69264d" />


**Desktop (1280px)**

<img width="1133" height="242" alt="image" src="https://github.com/user-attachments/assets/2b3179db-dbb0-4805-acda-05436b3b514b" />


### Task 3. Bootstrap Navigation Bar

**Task:** Create a responsive navigation bar using Bootstrap components: a logo on the left, links on the right, collapse into a hamburger menu on smaller screens.

**What I did:** I used `navbar navbar-expand-lg` with `navbar-brand` (logo on the left), `navbar-toggler` (hamburger button) and `collapse navbar-collapse` with a `navbar-nav ms-auto` list (links pushed to the right). The hamburger button works because of `bootstrap.bundle.min.js` connected at the end of the page.

**Desktop (1280px)**

<img width="401" height="42" alt="image" src="https://github.com/user-attachments/assets/a4778590-a58b-41cd-aa38-626dfcf6cdd7" />


**Mobile, menu closed (375px)**

<img width="490" height="63" alt="image" src="https://github.com/user-attachments/assets/aad5f598-2421-4599-8240-11d5a48a1466" />

**Mobile, menu open (375px)**

<img width="492" height="331" alt="image" src="https://github.com/user-attachments/assets/16575310-5959-4dc7-9d6e-fc3ec47a3c10" />


## Part 3. Combined Project

### Task 4. Responsive Portfolio Page

**Task:** Create a portfolio page using both media queries and the Bootstrap grid: a header with a Bootstrap navbar, a main section with projects on the left and a sidebar with personal info and contacts on the right, and a footer. Apply custom media queries to adjust font sizes, spacing and element visibility.

**What I did:**

- **Header:** Bootstrap navbar (collapses into a hamburger menu) and an intro banner.
- **Main left side:** `col-12 col-lg-8` with project cards. Cards are arranged with the grid: `col-12 col-sm-6` (one card per row on mobile, two per row from 576px).
- **Main right side:** `col-12 col-lg-4` with the sidebar (avatar, name, group, skills, contacts). On mobile the sidebar goes under the projects.
- **Footer:** at the bottom of the page.
- **Custom media queries (768px and 992px):**
  - font sizes of the banner, titles and cards grow on tablet and desktop;
  - paddings and spacing grow on tablet and desktop;
  - the height of the card covers grows;
  - element visibility: the extra banner line and the "Skills" block are hidden on mobile and shown from tablet;
  - on desktop the sidebar is `position: sticky`.

**Mobile (375px)**

<img width="490" height="908" alt="image" src="https://github.com/user-attachments/assets/571903f4-7e3e-4502-ab10-6e1bb11a3e8a" />

**Mobile, menu open (375px)**

<img width="472" height="397" alt="image" src="https://github.com/user-attachments/assets/4550533d-5ba9-4404-824d-9c9c4c0124fd" />

**Tablet (800px)**

<img width="1022" height="917" alt="image" src="https://github.com/user-attachments/assets/8a210cfd-5264-4bb5-ad2b-51763cda75df" />

**Desktop (1280px)**

<img width="1190" height="912" alt="image" src="https://github.com/user-attachments/assets/35d53a64-edcb-4b57-89b6-49f596ad66aa" />
