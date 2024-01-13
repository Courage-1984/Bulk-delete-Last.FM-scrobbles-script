# Bulk Delete Last.FM Scrobbles Script

**Bulk delete Last.FM scrobbles using your browser console and some Javacript.**

## Steps:

- On Last.FM go to the page which lists the tracks that you have scrobbled. 

usually:
   ```sh
   https://www.last.fm/user/your_username/library
   ```
- Open your browser DevTools, "F12" usually works for this
- Look for a "Console" tab in the DevTools window that just opened and click on it
- You should see your cursor in the console, there you paste the following code:
   ``` js
   jQuery('button.dropdown-menu-clickable-item[data-ajax-form-sets-state=deleted]').each(function(_, b) {
  b.click();
  });
  location.reload();
   ```
- Press enter to run the code.
- You should see a bunch of scrobbles was deleted.
- This basically clicks on all the delete buttons on the page and reloads the page.
- Repeat as necessary.

Credit goes to [Nick Mathew](https://gist.github.com/teknikqa) on [this page](https://gist.github.com/teknikqa/f14fa07cf28228cb2dfe49a0caab8e70).
