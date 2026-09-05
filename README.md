# Sprint Board

A shared sprint-planning board for the team. It tracks incoming work, who
it's assigned to, hours available vs. assigned per person, and current
client context.

## Live site
https://sprint.solutionsinsightslab.org

## How it works
- The board's data (tickets, capacities, client notes) lives in a
  Google Sheet, not in this code. The link to the Google Sheet is here: https://docs.google.com/spreadsheets/d/1fXcuKuEDdns2xqJAbgsYw3FgOtzVPIJQgy2MrZjuUUI/edit?gid=0#gid=0
- A Google Apps Script web app sits in front of that Sheet and reads/
  writes it whenever the page loads or you make a change.
- The password is checked by that Apps Script, not by this file.

## Making changes
This is a single self-contained `index.html` — no build step. Edit it
directly, then:

    git add index.html
    git commit -m "describe your change"
    git push

GitHub Pages picks up the change automatically within a minute or two.

## Changing the password
Edit the `PASSWORD` constant in the Apps Script project (Extensions >
Apps Script, from the Google Sheet). After editing, you must create a
new deployment version for the change to take effect: Deploy > Manage
deployments > edit (pencil icon) > Version: New version > Deploy.

## Don't rename or move
- The Sheet tab called `SprintBoardData`
- Cell A1 on that tab (this is where all the board's data is stored,
  as one block of JSON — not meant to be edited by hand)