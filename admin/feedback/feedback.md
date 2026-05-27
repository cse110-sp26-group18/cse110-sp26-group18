# Team 18’s Review of Team 16’s Progress

[link to google doc](https://docs.google.com/document/d/1eqkIZbOflexJCwxneEtnjLm3iEQK1-CCAE982ng6lo0/edit?tab=t.0) 

## Process & Agile Method 

### This Worked Well 
1. The README.md in the Design/screens/ was really helpful in outlining the planning and vision process of the design of the webapp. I appreciated how it explained what the folder contained, what each file represented, and which issues they related to. It showed clear planning before the implementation of the app. -Aila 
2. The docs/meetings/ folder was easy to navigate, and each subfolder was named intuitively, which made it super clear to understand where everything was located. The templates for each meeting note were a nice addition and highlighted the overall organization of the group. - Aila
3. The repo looks really nice and well planned for how sprints, meetings, etc. should go. I really like the attendance policy and the attention to detail for what is expected from each member during the week. I also like how clear the action items are and what needs to be fixed regarding the project. -Daniel

### Nice To have/improvement
1. I noticed that the stand-up meetings all ended with a list of Follow-ups, which I is important to have. However, it seemed like people are not coming back to this file to actually check-off any of the To-Do’s. In order to keep the process for Agile and syncronizhed, I think it would be nice to either have people come back to these documents and update them, or making the list a simple bullet-point instead of check-boxes to avoid confusion that the list needs to get updated. -Aila 
2. The README.md at the repo root is essentially empty. For an outside reader landing on the repo, there's no description of what the project is, how to run it, who's on the team, or where to find the docs. Adding a short overview, link to the deployed GitHub Pages site, and pointers into docs/ and AGENTS.md would tie all their otherwise solid process artifacts together. - Tim
3. I think the repos meetings notes are kind of behind for me at least because I only see till 5/13. I think it should be more clear as to the problems that the overall team is facing. I think a lot of the standups I read mainly focused on the positives and not really as much the issues. - Daniel

## Version Control & Commits 

### This Worked Well 
1. Their team has a very clear structure for version control. They separate different types of work into clearly named branches so that it is easy to track what is being changed and where. The labelling they are using includes, devops, design, docs, feat, chore, backend, research. The separate branches are good in showing that they are using their GitHub repo for collaboration and not just for final work. -Ayat
2. Their AGENTS.md formalizes the branch naming convention as <type>/<short-description> and points to docs/COMMITFORMAT.md for conventional commits plus docs/SemVerInfo.md for SemVer. - Tim
3. The PR template (.github/PULL_REQUEST_TEMPLATE.md) asks for what, why, and sets a test plan as well as reviewer notes. Combined with docs/COMMITFORMAT.md as mentioned above, this gives the team a structure that makes PRs easy to review. - Ajay
4. Commits follow a conventional format with prefixes such as feat(home), docs(agents), etc. which makes it easy to scan the git log and understand the scope of the changes at a glance. - Ajay

### Nice To have/improvement
1. Some commits were simply “upload files via uploads” which is not a big deal since there were only a few, but it would be nice to have a short description of what files were being uploaded so future devs/reviewers do no have to manually click on each commit to figure out what those uploaded files were. - Aila
2. The commits into main were commented clearly and for the most part clear. However, the commits in individual branches had less comments. Specifically in the docs/ branches, I saw a lot of UPDATE (filename) which was hard to undesrarnd in the broader context. - Aila 
3. The github has a lot of branches that seem unnecessary in certain ways such maintaining a branch for documentation of a sprint that was already taken care of or a ta-meeting. It might be helpful for the set up of the github to delete these old branches as they are already merged to the main. The same goes for when other features are finished and merged. - Aaron


## CI/CD & Tooling 

### This Worked Well 
1. Their repo has GitHub Actions workflows for CI and deployment that runs when someone pushes to main which is great for automating checks and keeping their main branch reliable. -Ayat
2. I liked that the project already has a pretty complete set of quality tools in their package.json. They have scripts for JavaScript linting, CSS linting, HTML linting, md linting, json validation, and Prettier format checking. This shows that the team is thinking about code quality across the entire repo, not just the JavaScript files. - Brendan
### Nice To have/improvement
1. Their CI/CD workflow currently only runs dummy tests as a placeholder so it would be great if they can set up unit tests or build checks before PRs are merged. -Ayat
2. .github/workflows/deploy.yml uploads path: '.', which includes repo materials like research/, docs/, Design/.But narrowing the Pages artifact to only the files needed for the live site would make deployments cleaner. - Howard
3. Since the deploy workflow currently publishes the repo to GitHub Pages, it would be useful to make sure linting and formatting checks run before deployment. Thay way, the live site is less likely to deploy with avoidable style, HTML, md, or javascript issues. - Brendan


## Testing 

### This Worked Well 
1. Even though their test framework isn't in place yet, I appreciated that they planned testing as proper infrastructure. They have an umbrella issue (#11), with unit testing (#36) and E2E testing (#37) split into their own QA-labeled issues. I think that shows they're treating testing as something deliberate rather than an afterthought. - Solaiman
2. research/tests/edge-case-results.md  records AI safety cases. The AI guardrail testing is a good example of evidence-based validation. Even though it is still manual, the team recorded expected vs. observed behavior and was honest about remaining gaps, which makes the AI safety work more reviewable. - Howard

### Nice To have/improvement
1. Testing still seems to be in progress since the issues tab shows unit testing and E2E testing are open. Completing this will help them ensure that as team members add new features or make changes they can catch bugs early and make sure the functionality of the meme generator does not break. -Ayat
2. As previously mentioned testing should be done as soon as possible to catch errors before too much code is written. I also think it is imperative that human oversight/double checking over test cases generated by ai or created by other teammates would be good to do. -Daniel


## Code Quality & Documentation 

### This Worked Well 
1. Documenting the reasoning behind frontend choices, deployment targets, and backend stack is elaborate and is a testimony to a thorough thought process behind their decisions. -Olivia 
2. I thought that the JSDoc expectations in AGENTS.md were strong because they explain exactly what needs documentation, including exported functions, typedefs, custom elements, and more complex internal functions. This is extremely helpful for a vanilla js prohect because it gives the team clarity of typed code without adding typescript. - Brendan
3. I noticed they put all of their design values into one tokens.css file, and AGENTS.md has a rule that nobody is allowed to hardcode a value if a token already exists for it. With a team of 11, that kind of rule really helps everything stay consistent and also makes their light/dark mode much cleaner. - Solaiman
The PR template pushes contributors to explain both the reason for a 	change and how reviewers can verify it, instead of only describing what files changed. This should make future reviews more consistent and easier to grade. - Howard
4. interface-contract.md defines shared data shapes with full typedefs, specifies custom event names, and API model signatures, allowing subteams to code with the same data shapes and events. - Ajay
5. Documenting the consequences of what the decisions they are making in their ADRs is a great thing to have to also understand truly what their decisions are going to lead to. By having the consequences down now it shows that the team fully understands their decisions and are prepared for the challenges that will come with them. - Aaron

### Nice To have/improvement
1. For the design brief, the documentation gives users a general idea of what problem the team is trying to solve, but is a little vague in terms of a general overview of the actual design and features that it offers. I think adding some clarity for the specific abilities a user has or a quick walk through for the user flow could be helpful. -Olivia
2. For index.html, iIt would be cleaner to move the homepage’s repeated template/card data into JavaScript or a shared data source, so future changes do not require editing many hardcoded UI fragments by hand. - Howard
The <memebro-template-gallery> web component is defined in template-gallery.js but isn’t imported anywhere, index.html uses hand-coded placeholder cards instead. Wiring the component into the page would help the team validate the web component and interface end to end.  - Ajay
3. For the code both on your html and css have good naming structures, although it might be a good idea to comment different sections out to categorize which part of the css relates to which part of the html to have a bit more organization. - Aaron


## AI Usage 
### This Worked Well 
1. For the architecture.md, caching method, prompts, and token accounting are descriptive and clear in the method that is being used and how AI usage is occurring for MemeBro.  -Olivia
2. They documented their expectation for AI usage very clearly in AGENTS.md including that any AI output must be reviewed and disclosed in a PR body which is good practice for accountability and transparency. -Ayat
3. In their AI-prompt-testing.md, they give a great detail report about what their AI models are doing and the step by step system of how they are using their AI. They are giving the results of it the cost to make a meme and cons of it. By having that I think it sets up their project to keep running well by having a good idea of what they are using - Aaron

### Nice To have/improvement
1. For the architecture.md, it’s a bit confusing as to why the specific caching method is used. I think reasoning behind the method is important for understanding why caching is decidedly only triggered for prompts exceeding 1024 or why tokens are cached in 128 blocks. -Olivia
2. AGENTS.md has no guidance on error handling which could lead to inconsistent behavior across the code base. Some examples of what could be done is how failed API calls should be handled or what should be communicated to the user if something wrong - Anvay
3. In AGENTS.md, use all caps to highlight to the agent about what things are extremely important to follow so that the agent makes less errors. This is essentially like shouting at the agent (but not in a harmful way I guess) - Anvay
4. With dealing with your prompt stuffing of having too many templates it might be a good idea to categorize your templates to then have the AI select a certain category of memes to pull from based off the user’s input to not have hallucinations - Aaron


## Product & UX 
### This Worked Well 
1. For the design, I like the modern UI and black box is the first thing that grabs my attention and clearly gives the option of picking from templates or creating a new template. - Olivia
2. The design feels very modern and the colors feel balanced with a warm feel. Sort of reminds me of Claude’s light theme - Anvay
3. The wording used on the website feels modern and fast paced which gives it a more legitimate feel. It also communicates a fast meme generator - Anvay
4. The design pages are very clear, containing all the scenes needed in the app. It can instruct the frontend engineer with a concrete target. - Howard
5. I really liked that AGENTS.md makes their mobile-first design a CLEAR rule instead of treating it as an afterthought. It specifically says to build from a 375px width baseline and scale up, which matches the needs of a meme generator since the majority of users will be creating/sharing memes from their phones. - Brendan
6. I like the text on the boxes, especially the dark brown box. It makes it feel like I want to click on the box and see what the fastest way to ship a meme is all about. I like how there are multiple different text colors throughout the page as well. -Daniel
### Nice To have/improvement
1. On the landing page mockup, the sidebar shows big numbers next to each library and category link (like 10,482 next to "All templates"). I found those kind of distracting since they pull attention from the template names. It might feel cleaner if the counts only showed up on hover or were removed entirely. - Solaiman
2. I like the idea of the “recent” section but instead of solid color blocks I think it would be nice to have the block displaying the meme template (like a thumbnail) as it’s easier for the user to remember what the meme template looks like. One thing to watch out for is to make sure this doesn’t disrupt the color balance - Anvay
3. The overall product seems complex and capable, but it might make it inconvenient if users are looking for a meme to be quickly produced and used. The flow of the product seems to require a lot of effort/manual editing, which might take a long time - Tim
4. I think the italics are definitely a way to emphasize different words in the sentences, but I think there would be better ways in this case for the words “a meme” and “brand-new” on the front page. Maybe different colors or bigger fonts on those would work better. -Daniel


## Technical Constraints Compliance 
### This Worked Well 
1. I liked that they locked their stack to vanilla HTML, CSS, and JS in ADR-0001, and reinforced it in AGENTS.md at the top of their stack rules. They even called out that the .jsx design files are only meant as design intent, not code to copy, a nice safeguard against someone accidentally pulling React into the project. - Solaiman
2. Comprehensive .gitignore. Their .gitignore is 154 lines and covers Node tooling caches, OS junk (.DS_Store, Thumbs.db), editor files, build outputs from a dozen frameworks they don't even use. - Tim
3. I like that styles/tokens.css is a single source of truth, with all the palettes, spacing, and shadows tokenized. Home.css doesnt use any hardcoded values, this also helps the light/dark theme switch work cleanly. -Ajay

### Nice To have/improvement
1. ADR-0003 is still pending, and AGENTS.md says no one should write backend or serverless code until it's accepted. But there are already open backend issues waiting to be picked up. I think it would help to either finalize the ADR sooner or put those issues as blocked for now. - Solaiman
2. The CHANGELOG.md currently has exactly one entry. The project spec requires a changelog kept incrementally, and with 74 commits in main there should be many more user-visible changes documented. - Tim
3. AGENTS.md describes expected project areas like pages/, assets/, and test/ bt some of these areas seem less developed than the docs and design folders right now. I think it would really help to add short README/status notes for planned folders so reviewers can tell what is finished, still planned, or blocked. - Brendan




