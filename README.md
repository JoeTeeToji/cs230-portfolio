# cs230-portfolio

## Module Eight Journal: The Gaming Room Software Design

### Client and requirements
The Gaming Room is the client for this project. They had a game called Draw It or Lose It that only ran on Android and wanted it expanded so it could run on multiple platforms through a browser instead. The main requirements were that the game had to support multiple teams and multiple players per team, keep game and team names unique, and only allow one game to exist in memory at any time. That last requirement is what drove the need for the singleton pattern in the design.

### What I did well
I think the strongest part of this project was matching design patterns to actual requirements instead of just including patterns because they're expected. The singleton pattern fit naturally because only one game could run in memory at a time, and the iterator pattern fit because the app needed to check for duplicate names before adding a new game, team, or player. Both patterns came directly out of what the client needed rather than being added on top of the design.

### What helped when writing the code
Having the UML diagram finished before writing any code made the actual implementation a lot smoother. Once the class relationships were mapped out, like Game holding a list of Teams and Team holding a list of Players, writing the code became mostly a matter of filling in logic that was already planned. It saved me from having to restructure things partway through, which would have slowed everything down.

### What I'd revise
If I revised one part, it would be the System Architecture View section. It wasn't required in depth for this project so I left it pretty minimal, but going back and building it out more would give a clearer picture of how the pieces connect physically, not just through the class relationships in the domain model.

### Interpreting user needs
The client's core need was getting off Android and onto something accessible from any browser, so the whole design had to avoid anything Android-specific from the start. Considering user needs matters because the software only has value if it actually solves the problem the client has. A design can be technically sound and still fail if it doesn't account for how the client actually plans to use it.

### Approach to designing software
My approach was to start with the requirements and constraints first, then figure out which patterns and class structures would actually satisfy them. For a similar project going forward, I'd use the same order of operations: lock down what the software needs to do before deciding how to build it and get the UML diagram done early so the class relationships are clear before any code gets written.
