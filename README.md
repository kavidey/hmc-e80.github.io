# Installing Quarto
- Go to [https://quarto.org/](https://quarto.org/) and install the latest version of the Quarto command line interface (CLI) tool.
- You can use whatever GUI you are most comfortable with, but I recommend following the instructions for VS Code.


# How to update the site

- All the files for the website are in this directory.
- Make any edits and then commit to the respository (see [Git Best Practices](#git-best-practices){target="_self"}).
- A GitHub Action will automatically republish the site to deploy your changes (click into the Actions tab on GitHub to view the status - it will take a minute or two). To manually update the site (you typically shouldn't have to do this), navigate to the `/.github/workflows/` subdirectory in the command line and then run `quarto publish`. (Note: You should be on the branch `main` when you do this.) This will render the site locally and then automatically push to the `gh-pages` branch and update the GitHub Pages website. The GitHub repository has already been configured to publish from the root of the `gh-pages` branch.

For more detailed information, check out the instructions [here](https://quarto.org/docs/publishing/github-pages.html#publish-command).


# Git Best Practices

We use these practices to simplify tracking live changes, keep an uncluttered workspace, and ensure changes are all deployed together.

1. Always develop on your own branch instead of directly on main.  This lets multiple users edit at once more easily. You can make your own branch by clicking on the "Current Branch" tab in Github Desktop and selecting "new branch"
2. Branch names should beging with the branch owner's name.  e.g.: "matt_lab1_edits"
3. Try to minimize merge conflicts by keeping the scope of your branches small, merging them quickly, and communicating with the team. e.g.: "matt_lab1_edits" probably has a much more reasonable scope than "matt_lab_edits".
4. Squash commits when you merge to main instead of leaving them separate.  Do this by changing to the main branch, selecting the "Branch" menu and the "Squash and merge into current branch" option.
5. Delete your branch after it is merged. Making new branches is cheap, and having old ones lying around can be confusing.
6. We have a GitHub Action to republish the site.

Note [MS]: We may be able to set up Github to automatically squash commits and delete branches.  Not figuring it out right now.
