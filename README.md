MyBlueBlazor

link to the actual working static page https://imaginarydevelopment.github.io/MyBlueBlazor/

File structure I setup to not have to manually or script moving files around to be able to build and publish without switching branches:

- projects/MyBlueBlazor
  - MyBlueBlazor.Code (master branch)
    - .git
    - FiringMyBlazor
  - MyBlueBlazor.Pages (publish target)
    - FiringMyBlazor
      - dist (gh-pages branch)
        - .git
        - _framework
        - css
        - index.html
        - .nojekyll
        
Remaining unsolved problem, VS doesn't know how to push to github with credentials, and for each change I make, I have to publish to github for each change to check it because of the problems https://github.com/aspnet/Blazor/issues/261 causes

However publishing to the .Pages directory above, and then commit+pushing is nice and streamlined.
