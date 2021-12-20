# CALIFORNIA ELECTION DAY DATA GATHERING

## Background

### Beginnings
This project began as a proposed collaboration between Stanford University, Big Local News, and The California Newsroom (local radio stations, NPR and CalMatters). The central question: Can we provide a free resource for newsrooms across the state to report election results on election night, especially down ballot and using as little human resources as possible.

### Known challenges
* California reports elections results at the county level. 58 counties distribute their results in 58 different ways. Some highly technical and organized, others much less so.
* Automating the entire process will likely be impossible, especially in 10 weeks.
* Some counties have overlapping governing/oversight positions and therefore overlapping election results.
* Existing solutions stop roughly at the state legislature level and are costly.
* Building sustainable tools. Counties will change how they report results after this project is done, then what?

### Proposed solution
A mobile-first data entry web application that auto-populates where automation is possible and predictable, and otherwise provides a simple user experience such that remaining results can be manually entered by newsroom volunteers, stringers, or staff with minimal risk for error. The web application would be accompanied by a flat-file or API results portal and basic prebuilt iframe-capable results widgets.

## Imagined interfaces
* Fuzzy search list of counties. Click through to >
  * Fuzzy search list of offices/positions within county. Click through to >
    * Information text of county result reporting method and instructions for entering/verifying results.
    * Fuzzy search list of candidates for office/position ordered by # of Google News search hits
      * Next to/below each candidate name:
        * Numerical data entry field:
          * Auto-populated with scraped/APIed data where available
            * Color coded for entry type (manual, scraped, API, verified)
          * Clicking entry field pops up numpad
        * Status dropdown
          * No data, Unknown, <25% precincts, 25-50% precincts, 50-75% precincts, >75% precincts, 100% precincts, Preliminary, Verified, Certified/Winner!
* County-level results hosted as JSON flat file (or maybe all-state Datasette SQLite database?!)
* Basic prebuilt widget(s) for story/results page placement.

## Timeline

### Week 1
* Background research
  * Survey counties to develop spreadsheet of reporting methods.
    * Possible columns: 
      * County | Distribution method (Dropdown: Paper | API | Structured PDF | Unstructured PDF | Other Structured | Other Unstructured) | Manual required? | Manual explanation | Population count | URL | Notes
  * Tech stack frameworks/possibilities, out-of-the-box solutions, ???

### Week 2
* Frontend wireframing
* Extract, Transform, Load pipeline diagramming
* Front and backend design, tech stack decisions made

### Week 3
* Project management
  * Write requirements
  * Establish reverse timeline
    * Example: Wk 10 - Publish final product, Wk 9 - Final product finished, debugging and testing only, Wk 8 - Mock election day using historical data, Wk 7 - CSS/UI minor tweaks & accessibility testing, Wk 6 - ETL finalized & frontend UIs talking to backend data structure, Wk 5 - Holy shit major ETL curveball, everything is broken, Wk 4 - Working mock data entry UI/UX w/ fake data & working widget UI/UX, ETL pipeline working besides edge cases, Wk 3 - Project management, begin ETL and frontend design work.

### Week 4
* Wireframes > working prototypes (data entry interface and widgets), begin HTML, CSS, and JS
* ETL Diagrams > successfully munging easiest machine readable data, beginning manual entry and edge case automation approaches
* Front and backend begin communicating about data connections

### Week 5
* Built-in time for major ETL hurdles and revisions
* Finalizing HTML, CSS and JS
* Code reviews

### Week 6
* ETL backend revisions, finalizing
* ETL/backend successfully talking to frontend data entry UI and widgets
* Code reviews

### Week 7
* Accessibility testing, minor CSS/UI tweaks
* ETL bulletproofing, data entry testing
* Code reviews

### Week 8
* More testing and editing before ... 
* Mock election day, using historical data sources
* Establish final punch list

### Week 9
* Execute punch list
* Further testing and debugging

### Week 10
* Publish and present project!

## Post
* Who will maintain this project?
* Who will fund the maintainers?
* How can this model be applied to other states?