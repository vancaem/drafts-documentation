---
title: Changelog
---

#### v0.1.1.82

- **Change:** Settings for visibility and display mode of tabs in both drafts and action lists are now in the "..." menus.
- **New:** People and Time action icon additions.
- **New:** Badge settings now take a tag filter expression, same as Workspaces, so you can set the app badge to only count "untagged", or "project-tag, !complete", etc.
- **Fix:** Clean up of some VoiceOver labelling.

#### v0.1.1.81

- **New:** Action group icons.  All your groups will have the default icon to start.
- **New:** <-> Display mode option for Workspace and Action Group tab views. Can toggle between display name name, icon and name, or icon only on tabs. Appears at end of scroll for those tab views.
- **New:** `editor.focusModeEnabled` property to access or set current focus mode status.
- **New:** `editor.linkModeEnabled` property to access or set current link mode status.
- **New:** First use explainer dialog for focus mode.
- **Fix:** Sync issue with conflicting idle timer.
- **Fix:** Clean up a couple of rare crashers.
- **Change:** A few theme tweaks.

#### v0.1.1.79

- **New:** Rewritten onboarding flow (only comes up if you reinstall). Still not finalized, just basics, but looks nicer and flows better now.
- **Change:** A few tweaks to Taskpaper language grammar.
- **Change:** A variety of changes to polish up Pro subscription permissions that you won't see yet.

#### v0.1.1.77

- **New:** OneDrive action step. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/onedrive)
- **New:** OneDrive scripting object to read and write files from OneDrive. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/OneDrive)
- **Change:** Dynamic tag suggestions. When you start to the type, the keyboard row tag suggessions become query based instead of a recent tag list.  Not exactly auto-complete, but helps.
- **Fix:** Detect and disable backup features if iCloud not available.
- **Fix:** If "edit on select" is disabled, do not enter edit mode on a cold start of app.
- **Change:** Updates to default actions groups setup on new installation. These will not update in existing installations, but can be re-installed from the directory if desired.  Groups are Basic, Keyboard-Basic, Keyboard-Markdown, Actions-Apps, and Processing.

#### v0.1.1.75

- **Fix:** Sync regression in last build prevented some updates from getting pushed to server properly.
- **Fix:** Avoid case-sensitive comparison of keyboard shortcuts.
- **Fix:** TJSProject object tags not exposed properly.
- **Fix:** Changes to current workspace not getting saved agressively enough, and could revert on a cold start.

#### v0.1.1.74

- **New:** `GoogleDrive` script object to read and write files on Google Drive. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/GoogleDrive)
- **New:** Additional commands in Workspaces widget.
- **New:** /replaceRange URL scheme, same functionality as D4 version. [Docs]()
- **Change:** Some refactoring in the Markdown syntax highlighting, including better handling of emphasis embedded in bold, and the reverse.
- **Change:** Revised `draft.languageGrammar` property to work based on displayed string names of syntaxes as shown when selecting them in the appearance menu. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Draft)
- **Fix:** Improve conflict handling in sync.
- **Fix:** Action and key migrations not updating last migrated date.
- **Fix:** Some work on cleaning up VoiceOver labelling.

#### v0.1.1.73

- **New:** "Simple List" syntax type. Supports list completion, tappable tasks and basic Markdown. Mostly intended to offer an alternative to allow selection of different fonts/styles for a check list type draft.
- **Change:** Tweaks to share extension layout.
- **Change:** Be less aggressive about reformatting javascript for better performance with longer scripts.
- **Fix:** Removing tags from a draft would not propagate properly through sync.
- **Fix:** call /open URL with action specified on the current draft did not work.
- **Fix:** Migration of mail and message steps did not properly migration recipients.
- **Fix:** Crash dragging workspace to invalid area.
- **Fix:** "Show all" in draft list should clear query field.
- **Fix:** New drafts were not getting the default language grammar assigned.
- **Fix:** VO labelling fixes in several areas

#### v0.1.1.72

- **Fix:** Changes to language grammar (syntax) of the current draft not immediately taking effect.
- **Fix:** Workspace sort index not synching properly across devices.
- **Fix:** Workspaces with duplicate names could get highlighted improperly in workspace tabs view.
- **Fix:** Keyboard shortcut conflicts identified incorrectly.

#### v0.1.1.71

- **Change:** Bottom shelf in draft list is now for workspace selection.
- **New:** Workspaces today widget.
- **New:** Recent drafts widget displays flags and tags.
- **Fix:** Recent drafts widget not always sized properly on initial display.
- **New:** /workspace?name=XXX URL scheme to load a workspace.
- **Change:** Action group bottom tab now just a list of groups in sort order, more like tabs at top in D4.
- **Fix:** "Save and Exit" option editing action step would not save properly in some circumstances.
- **Fix:** Applying Workspace settings with no tag filter could result in filtering for empty tag.
- **Fix?:** Hacky bits to force tint color on some system screens that want to inherit tint color from themes that don't work well for their non-dark theminess (like File Browser, Mail windows, etc.).

#### v0.1.1.70

- **Fix:** Workspaces not saving sort order properly.
- **Fix:** Show omitted tags in header of draft list.
- **New:** New vs. Save Current options creating Workspaces.

#### v0.1.1.69

- **New:** Keyboard shortcut assignment conflict feedback in UI. Shows conflicting assignments when editing.
- **New:** Drag and drop reordering of Workspaces.  If you have existing Workspaces you may have to move them around a couple of times to get them to start sorting properly....or delete and re-create them. They did not get sort indexes assigned prior to this build.
- **New:** Updates to tag filters and Workspaces to support omitting tags.
- **Fix:** Prevent possibility of empty tag getting added to draft.
- **Change:** Blacklist certain characters from tag names (!=&|) to reserve them for use in query strings.
- **New:** Migration of script action steps from Drafts 4 should work now with conversion of function signatures where needed. Please let me know if any fail after migration.
- **Fix:** Arrow keys only when through keyboard assigned action groups.
- **Fix:** Crash moving last action out of a group in Manage view.
- **Fix:** Changes to keyboard shortcuts were not being picked up right away in some cases.
- **Fix:** Share extension was not loading file content properly due to variable scoping issue.
- **Fix:** Changes to "Count only flagged" switch in Notification settings not sticking.
- **Change:** Performance improvements to lookup of actions when triggered via external keyboard shortcut.
- **Fix:** Limit keyboard shortcut text to one character.

#### v0.1.1.68

- **New:** Left-right arrows on external keyboard now navigate between tabs in draft list.
- **New:** Left-right arrows on external keyboard now navigate between action groups in action list.
- **Fix:** Bad locale values passed to `editor.dictate(locale)` could prevent dictation from working.
- **Fix:** Installations of the watch that had never set the default tag option in the watch app on iPhone could get default tags of "0".
- **New:** Added more third party app URLs to app plist so they will work in link mode.
- **New:** A few more action icons based on built-in UI elements.

#### v0.1.1.67

- **Fix:** Append/prepend from share extension might not always get picked up if the main app had the draft loaded.  Now should immediately refresh, even in split view.
- **Change:** Refactor drawer animations (again) to fix a few glitches and streamline the code.
- **Fix:** If tag editor was visible, flagged status for current draft would not update if changed in script.
- **Fix:** Dragging and dropping a draft from draft list on an action in the action list could result in the action running twice.
- **Fix:** Incorrect rounding of longitude and latitude output in templates.
- **Change:** Adjustments to key text.
- **Fix:** Glitchy animation reordering actions in the action list.
- **Change:** Performance improvements on the Watch app.
- **Change:** Re-enabled extended keyboard resizing on iPhone X because it's weird if I don't even if it causes a few glitches.
- **Fix:** Request notification access if the "flagged only" switch is enabled in settings.
- **Fix:** Changing from split view to  full screen might not enable pinning again on action list view.

#### v0.1.1.66

- **New:** Workspaces. The list options screen now has more advanced options for controlling sorting of each draft list tab, etc.  These filtering settings can also be saved as workspaces that can be re-applied.
- **Fix:** TJSProject should support "tags" property.
- **Change:** Some changes to display of current filtering in draft list.
- **Fix:** Trash cleanup should work off accessed date, not modified date.
- **Change:** Disable smart quotes and dashes in URL template editing fields.
- **Fix:** With actions list pinned on iPad, actions which had after success effects could hide action drawer when they shouldn't.

#### v0.1.1.65

- **New:** Pin mode replaced with "Focus" mode. Still disables the creation of new drafts after a timeout, and now also changes the behavior of "after success" settings to open next draft instead of a new draft if the action archives or trashes current draft.
- **New:** "After success" now has an additional "Ask" option, which will prompt after running the action and ask if you want to archive, trash or skip.
- **New:** Add visual indicator of key action presses. Probably needs a spinner but fades the key while the action is running for now.
- **New:** Along with latest Drafts 4 beta, support for "Drafts 5: Add as Callback" migration, accessed from Action edit screen in Drafts 4. This is for actions that cannot be directly migrated to Drafts 5, and creates an action in Drafts 5 which calls the Drafts 4 action as a callback URL.
- **Change:** Rename `editor.focus()` to `editor.activate()` to avoid confusion with focus mode.  Old method still works for now, but will be phased out.
- **New:** `app.themeMode` property. Allows getting or setting of 'light', 'dark' or 'automatic' theme mode from script.
- **New:** D4 key migrator will migrate "Toggle dark theme" command now.
- **Change:** Better handling of network reachability for actions which require network.
- **Fix:** Migrating URL actions should attempt to change occurrences of "drafts4:" with "drafts5:".
- **Fix:** Recent tags should not allow duplicates.
- **Fix:** Importing action groups would fail with "Invalid" message.
- **Fix:** Hiding keyboard hides keys again.
- **Fix:** Crasher deleting last action from a group in the group edit screen.
- **Fix:** TJSTodo object was not setting tags properly.

#### v0.1.1.64

- **IMPORTANT:** Due to data level changes, if you have a previous beta installed, you will need to delete it before installing this build! Data will re-sync from iCloud, but take appropriate backup steps as you see fit.
- **New:** Reworked the draft list filtering sidebar and quick access shelf at bottom. Filtering can now be done based on more than one tag, and also on "untagged" drafts.
- **New:** Manual sort of Action Groups. Either via drag and drop, or traditional table reordering in Manage groups view.
- **New:** Action search.
- **Change:** More aggressive capture of version histories and some more work on sync conflict resolution.
- **Fix:** Dimming view regression cancelling action drawer animation.
- **Fix:** Label clipping in migration window.
- **Change:** Round output of location coordinate tags in template processor.
- **Change:** Some work on performance...mostly low-hanging fruit.
- **New:** Watch should broadcast Handoff information for current draft.
- **New:** "minuteInterval" option for date pickers in prompts to specify how many minutes for each step in time selection.

#### v0.1.1.62

- **New:** Prompt additions... [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Prompt)
    - `addTextView` support for larger text input area.
    - `addSwitch` support for on/off toggle switch.
    - `addDatePicker` for date and or time pickers
    - `addSelect` for single or multi-option selection controls.
- **New:** TextExpander fill-in support.
- **Fix:** Sync should not try to run when network is unreachable.
- **Fix:** Capture from the watch with no tags should not get "0" assigned.
- **Fix:** "Invalid callback URL" warning should not appear for callback URL steps/scripts not set to wait for a response.
- **New:** Allow renaming of export file when exporting a script from script step.
- **Fix:** setting isTrashed and isArchived properties on draft script object did not work.
- **Fix:** editor.setSelectedRange should include consideration of content offsets.
- **Change:** Some more adjustments to line number positioning.
- **Fix:** Script step import/export button text clipping on smaller devices.
- **Fix:** Dimming view not always dismissed if action disposed of draft after success.
- **Fix:** Few improvements for SE size phones.
- **Fix:** List auto-completion should recognize a completed task line beginning ("- [x] ")

#### v0.1.1.61

- **New:** Watch app can flag, unflag, tag, untag drafts - still needs some design work.
- **New:** Watch app has setting for default tag to assign to drafts captured on the watch (set in iPhone Watch app)
- **New:** "Hide toolbar when editing" setting. Now in "Aa" appearrance view.
- **Fix:** Un-hide keyboard row if an action group is selected and it's hidden.
- **Fix:** Adjustments for content and scrolling insets on iPhone X.
- **Fix:** Merge operation should merge tags to new draft.
- **Change:** Work on prompt presentation animations.
- **Change:** Updates to default action groups (only applies to new installations).

#### v0.1.1.60

- **New:** Migrate Actions and Keys from Drafts 4 available in Settings. Requires latest Drafts 4 beta.  Still quite a few things that will not migrate, but many of the basic ones will.
- **Fix:** Work on a few issues with updates to the currently loaded draft in the editor, when changes occur outside the editor. Fixes some issues (like with archived drafts re-appear in inbox), and with sync.
- **Fix:** More reliable capture of version history in cases where sync conflicts occur.
- **New:** Drafts migration can now optionally assign a tag to migrated drafts.
- **Change:** Performance profiling of text editing. Handled some low hanging fruit to improve rendering performance of text, especially longer texts.
- **Fix:** Print step not saving "HTML" option selection.
- **Fix:** Merge operation not adding line feeds for non-blank separator.
- **Fix:** VO labelling for recent tags quick entry incorrect.
- **New:** Some improvements in Find & Replace view.  Restores last search.  Clear buttons.

#### v0.1.1.59

- **BREAKING Change:** Credential script object has been changed to support arbitrary fields. If you are using this object, see docs for modifications needed. There are convenience methods to create ones pre-configured for user/pass, etc. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Credential)
- **New:** Things scripting integration. This consists of convenience wrappers for their new URL scheme support.  Requires Things 3.4 (still in beta). [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Things)
- **New:** Support for migration of more action step types, including URL and Print.
- **New:** "Merge" operation in draft list.

#### v0.1.1.58

- **New:** Print action step. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/print)
- **New:** Initial work on migration of Actions and Keys from Drafts 4.  Available as migration of individual actions and keys only from Drafts 4 beta version. Not all will migrate successfully, either because they are not supported or I just haven't done migration code for the step.  Please test and look for conversion issues...especially with scripts since a number of changes needed to made to scripts to account for API changes.
- **New:** Migration of Drafts 4 drafts available in settings. I would love some detailed testing of this, if anyone is up for it, but would not necessarily recommend everyone dive in until we have some confirmation of the functionality.
- **Fix:** Flagged tab should not show flagged drafts in trash.
- **Fix/Change:** Various Prompt fixes/improvements.  Better keyboard handling, etc.
- **Fix:** Draft list empty state would not get hidden when new draft create, making new draft invisible until tab tapped to reload.

#### v0.1.1.57

- **New:** Tagging interface now has button to toggle flagged status.
- **New:**: Prompt object expanded to allow configuration of text field options, like placeholder text, auto-correct, keyboard type. Details in [docs](https://github.com/agiletortoise/drafts-documentation/wiki/Prompt).
- **New:** /dictate URL now supporte `locale` param to pass preferred language, in the format "en-US", "es-MX", "it-IT", etc.
- **New:** Editor object changes [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Editor)
    - `editor.arrange(text)` method accepts initial text to arrange, opens arrange mode, and returns the arranged text.
    - `editor.dictate(locale)` method opens dictation interface, returns dictated text.
    - `editor.showArrange()` : non-blocking call that just opens arrange mode as if you tapped the button.
    - `editor.showDictate()` : non-blocking call that just opens the mode as if you tapped the button.
    - `editor.showFind()` : non-blocking call that just opens the mode as if you tapped the button.
- **Change:** Limit size of drafts pushed to Watch, with indicator that complete draft is available on phone.
- **Change:** Bounce the action icon when changing tint color, because why not.
- **Change:** Increase scheduling priority of sync operations from .background to .userInitiated. The later is what D4 uses and seems to keep things updating faster.
- **Change:** Rewrite some of the lower level TextKit classes in Obj-C to avoid bridging penalty with Swift. Noticeable performance boost rendering longer texts.

#### v0.1.1.56

- **New:** Toggle to show/hide extended keyboard row in "..." keyboard options.
- **New:** WebDAV action step to create and modify files on a WebDAV server. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/webdav)
- **New:** `Credential` script object. Used to prevent the need to hard code login credentials in action scripts which utilize web services. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Credential)
- **Fix:** Tapping task marks should not reset scroll position.
- **New:** "Visit Directory" option when created action.
- **Change:** Reworked navigation in action editing a bit to auto-save, better support swipe-back navigation, and allow exit from action step level.
- **Fix:** Cancelling an action with "Confirm before running" active did not cleanup activity indicator.
- **Change:** Re-label "Delete" to "Remove" in Arrange swipe actions.
- **Change:** Improvements to prompt text fields.
- **Fix:** Button to remove tint color from action should have X indicator.
- **Fix:** "Cut" should not make text scroll to end.
- **Change:** Minor changes to Appearance view.

#### v0.1.1.55

- **New:** First stab at Siri support on the Watch. Likely somewhat buggy...but feel free to try "Create a note using Drafts".
- **Change:** More playing with the blue icons.
- **New:** Improvements to Taskpaper syntax. Notes are italic and recognized for indentation.
- **Change:** Swap Flagged and Archive tabs in draft list.
- **Fix:** Improvements to accuracy of enabled state for next/previous draft buttons.
- **New:** "Empty Trash" operation when Operations used with no drafts selected.
- **Fix:** Tapping "Replace All" in find screen could clear draft content if no find text was available.
- **Fix:** Action Directory posting should save description information used.
- **Fix:** Avoid crash rendering text for very large drafts (still slow, but shouldn't crash)
- **Fix:** "Unlisted" switch in directory posting screens should reflect the last value sent to the directory.
- **Change:** Update custom action icon files to better match Symbolicon set icons.
- **Fix:** Assets for a few missing action icons.
- **Change:** Tighten up key icon sizing.
- **Fix:** Paragraph numbers should now be baseline aligned to text of the line.
- **Fix:** Overlapping lines in code blocks in "basic" preview stylesheet.
- **Change:** Swipes for moving between keyboards were logically reversed.
- **Change:** Improve visibility of empty states.
- **Change:** Add empty state to find & replace.

#### v0.1.1.54

- **Change:** Reworked recent tags at bottom of drafts list as collection view.
- **Change:** Reworked recent groups at bottom of drafts list as collection view.
- **New:** Tap and hold "Select" in draft list to Select All.
- **New:** Tap and hold "Select" in actions list to Select All.
- **Fix:** Added way to dismiss keyboard on iPhone in a few places.
- **Fix:** Twitter steps should fail if template generates empty string.
- **Change:** Visible state for margin size in Appearance settings.
- **New:** Added [[tags]] template tag which returns comma separated list of tags.

#### v0.1.1.53

- **New:** Action Directory support. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/actiondirectory)
    - It's not pretty or complete, but it works (I hope...you are suppose to confirm that)
    - It now supports sharing of Action Groups as well as individual actions.
    - It now supports updating and/or removing items you have shared. No account needed, each share is tracked with individual secrets synced in your iCloud account. This allows quick fixes for typos, or bug fix updates to shared actions without loosing the unique URL.
    - *No, I don't need to hear about the lack of search, or discoverability, etc.* Just test that sharing, modifying, removing and install of actions and groups works, please.
    - *It is entirely possible I will need to wipe data from the beta directory* due to issues if they come up, or format changes. Don't rely on it as a backup.
- **Fix:** Status bar and keyboard appearrance should respect style preference, regardless of whether the style is used as "light" or "dark" mode.
- **Fix:** Drafts created by Siri should capture location.
- **Fix:** Display glitch showing part of sidebars on iPad coming out of split view.
- **Fix:** Improvements to output of [[safe_title]] template tag.
- **Fix:** When exporting actions or groups to file, make sure the file name is "safe" for the file system.

#### v0.1.1.51

- **New:** Tag and Action Group panels in sidebars can now be swiped away, in addition to tap dismissal, for consistency.
- **Fix:** Arrange button at bottom not working.
- **Fix:** Selecting draft with draft list anchored should not dismiss list.
- **Fix:** Display glitches with text in search fields.
- **Change:** Don't disable new draft timeout setting in pin mode.
- **New:** Feedback and help entries in Settings.

#### v0.1.1.50

- **Fix:** Callback URL steps now work properly with calls to Drafts own URL schemes. Although if you are doing that, there's probably a better way now - but it works now.
- **Fix:** If a /runAction URL was used to call an action with an "After success" disposition of Archive or Trash, the text would get saved as a draft, not forgotten as intended.
- **New:** `app.selectDraft();` method. Opens UI to select a draft - same UI as Share extension selection for appending - and returns the draft object selected (or nil if cancelled). [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/App)
- **Change:** Tone down notification banner colors in dark themes.
- **Fix:** Added way to dismiss keyboard in dictation interface on iPhone.
- **Fix:** Avoid flash of error text when loading dictation screen.
- **Fix:** Exit link mode when changing drafts.
- **Fix:** Editing in Arrange mode did not pick up dark mode keyboard appearance.
- **Change:** Improvements to positioning of drawer anchoring buttons on iPad.
- **Change:** Put arrange button back in the bottom row.
- **New:** Arrange mode remembers the last used mode (block-line).
- **New:** Explainer dialogs on first use of link and arrange mode.
- **Fix:** Select checkboxes would sometimes not appear when tapping "Select" in action list.
- **Fix:** Changing theme with action drawer visible did not update appearance on all rows.

#### v0.1.1.49

- **New:** CallbackURL scripting object.  Allows scripting of x-callback-url calls, similar to Callback URL step, but better suited to sequencing calls or working with results. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/CallbackURL)
- **New:** Support for "allowEmpty" parameter in URL schemes where appropriate.
- **Fix:** Some dialogs with longer messages could result in clipping of buttons.
- **New:** Add `lastError` property to event object to track errors that might occur when updating.
- **Fix:** `Calendar.findOrCreate(...)` was not finding calendars properly, resulting in duplicate calendar creation.

#### v0.1.1.48

- **Change:** Improve watch complication assets.
- **Change:** If background email generates blank body, add a space to prevent Mailgun error.

#### v0.1.1.47

- **New:** Watch app. I have some other plans for it, but it is currently a port of the updated D4 watch app. Not super well tested, but I think it mostly works. Going to run it through the paces myself this weekend.  Will circle back on it and add Siri and some other planned features soon.  I made a couple UI flips just to make it distinguishable from the D4 watch app.
- **Change:** Darken blue icon sets slightly.
- **Fix:** Do not ask for Siri access if Siri is disabled.
- **Fix:** Do not start displaying drawers when scrolling a long tag list.
- **Change:** If focus is dismissed from tag entry field without assigning tag, clear the field.
- **Fix:** Do not warn about invalid callback url if the source action step did not have "Wait for response" enabled.
- **Fix:** VO labels for pin button not updated for status.
- **Fix:** A few layout issues on the little phones.

#### v0.1.1.46

- **New:** "Insert Text" action step. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/inserttext)
- **Fix:** Fixes for a few odd configuration bits in the default action set.  These will not re-install automatically.
- **Change:** Capture and warn about invalid links in HTML preview.
- **Change:** Open valid links in HTML Previews using Safari View Controller instead of the preview window itself.

#### v0.1.1.45

- **Change:** Action groups and action export files are now in compressed binary format. This works better for sharing, downloading, etc. - in addition to being a space-saver for backups, etc. - and users don't get confronted with a wall of JSON which scares them. At least that's what I'm hoping.  Still need to test more.
- **Change:** Port D4's RTL language support.
- **New:** Template tag helper keyboard row. Probably not done yet, but it's something.
- **New:** Include Action step type. Works like the D4 version.
- **New:** Draft script object "languageGrammar" property to read/write the preferred syntax for the draft.
- **New:** `editor.focus()` method to return focus to the editor. Useful if an action takes focus to display other UI (like a prompt) and you would like to return to editing mode.
- **Change:** A few tweaks in the default action groups.
- **Fix:** Action group backup was being a bit too agressive about ensuring the safety of your Action Groups.
- **Change:** More tweaks to javascript editing and syntax highlighting.
- **New:** Google Drive action step.  May still be a bit buggy, but should mostly work. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/googledrive)
- **New:** "Edit on draft selection" setting (default: true) in Appearance settings. Controls whether tapping a draft in the draft list immediately focuses the draft for editing.
- **New:** Prompt script object now has `addPasswordField(name, label, initialText)` method.
- **Fix:** Crash calling reminder.addAlarm() without any parameters.
- **New:** Improvements to Javascript grammar, especially handling comments.
- **New:** Some basic indentation support in Javascript editing.
- **Change:** Default light theme was underlining tasks.
- **Change:** Begin edit on cold start of app.
- **Change:** Script editor should respect javascript editing attributes configured in editor.
- **New:** `Drafts.recentTags()` scripting object. Useful for building prompts to select a tag.
- **Fix:** Scrolling jumping around after scripting call that updated text (like setSelectedText()).
- **Fix:** Automatic list completion could cause jumping around in longer drafts.
- **Change:** General improvements to display of prompts and dialogs, but style and animation.
- **Fix:** "Auto-correct" selection was not being saved in Editor settings properly.
- **Fix:** Smart quote and smart dash toggle where not working if you enabled them. They do now. If you like that kind of thing.
- **New:** Launch screen revisions.
- **Fix:** Optional not getting unwrapped flipped to a new dictation session when one expires leaving extraneous characters.
- **New:** Lots of works on IAPs, subs, pitch screens, etc., that you won't actually see yet.
- **New:** Some work on fleshing out Siri vocabularies. "Capture a note using Drafts", "Dictate a note with Drafts" should trigger correct intent now.

#### v0.1.1.42

- **New:** Work on the on-boarding process.  If you delete and reinstall you will get the first launch experience. Design is not done, but it will on-board an initial set of actions and keys now.  The on-boarding sets up a "Basic" actions group with some common actions, and also loops over a set of actions for popular apps (like OmniFocus, Fantastical, Things, Tweetbot, Ulysses, etc.) and sets up actions in the Basic list for those apps *IF* the user has that app installed on the device.  This process updates status in iCloud, so the groups will not be re-created on a new install if the user already has been through it on another device, or in a previous install.
- **New:** Arrange mode is now available from a text selection popover menu to arrange only the current selected lines, instead of the full text of the draft.
- **New:** Scripting changes:
    - app.version: Return current version number of Drafts.
    - `device` object for access to model, os version, battery level. Useful for scripting actions which behave differently on iPad/iPhone, etc. 1[Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Device)
- **Fix:** Dialogs and prompts could clip longer message texts.
- **Fix:** Enabling Reminder import should request Reminder permissions if they have not already been granted.
- **Change:** Add syntax coloring for ES6 Template literals to javascript language grammar.
- **Change:** Updated to blue app icons.
- **Change:** Change default app icon to gradient blue variant.
- **Fix:** "List in Reminders" action could fail to finish properly.

#### v0.1.1.41

- **New:** Dialogs and prompts support keyboard interaction now.  Tab or down arrow, or Shift-tab or up arrow move been selections.  Enter to select the current button.
- **Fix:** Keyboard shortcut (CMD-0) to show actions would hide draft list, but not move main view back if drawer was pinned.
- **Fix:** You should not be able to delete the "no steps" placeholder row in the action editing.
- **New:** Callback URL steps now create template tags for each parameter returned in an x-success callback from the target app, in the format `[[callback_parameter]]`. These values are still available via script as well.
- **New:** Run Workflow steps now create a template tag for the result returned in an x-success callback from the Workflow, with the name `[[workflow_result]]`. These values are still available via script as well.

#### v0.1.1.40

- **New:** Mail action step supports "Send in background".  The "Use Markdown" option has been removed in favor of the more generic "Send as HTML". [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/mail)
- **New:** Mail script object has "sendInBackground" property, and, well, can send in background. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Mail)
- **New:** /create, /append and /prepend URLs can now take "tag=..." parameters to attach tags to the draft. [Docs](https://agiletortoise.github.io/drafts-documentation/urls/)
- **Change:** Shrink size of icons on keys a little.
- **Change:** Make tag and action group slide-overs a little wider.
- **New:** A few more action icons in the Editor category.
- **Fix:** Notification settings should copy with an action if it's copied/moved.

#### v0.1.1.39

- **Change:** More reworking of keyboard selection.  It's back at the start of the keyboard row, but will scroll with the keys.
- **Fix:** Inability to select a keyboard if one had not already been selected in the installation.
- **Change:** Rewrote url query parameter coding based on AlamoFire implementation, instead of old C one. Hopefully doesn't break anything.
- **Change:** Move arrange mode access to keyboard selection view (with find-replace).
- **Fix:** Clean up more funky behaviors after cancelling a drawer show animation.
- **Fix:** Crash using URL step set to use Safari with non-http(s) URL.
- **Fix:** Drawers should not dismiss when editing started if pinned.
- **Fix:** JavaScript language grammar handles multiline comments properly now.
- **Fix:** JavaScript language grammar handles regex literals.
- **Fix:** Changes to share extension template would only be saved the first time they were edited.
- **Fix:** Navigating action list by using up-down arrows would not properly highlight the selected row.
- **New:** Add "show" option to reveal tag selection if the recent tags list is empty at the bottom of draft list.
- **Fix:** Some fields which show keyboard in Settings were not picking up the dark keyboard for dark themes.

#### v0.1.1.38

- **Change:** Try "Manage keyboards" ... button at the end of the scrolling key row.  Can't promise it will stay there, but worth a try.
- **Fix:** A proper fix (workaround, really) for the double drawer animation weirdness.
- **Change:** Refactored task identifiers and enabling to language grammar definitions. Task marks are now only enabled in Markdown grammar.
- **Fix:** Tags on current draft would not update in editor if changed in script.
- **Change:** Display improvements to recent drafts widget.  Implement pro only mode.

#### v0.1.1.37

- **New:** "Callback URL" action step. Similar to Open URL, but appends x-callback-url parameters and can wait for a response from the target app - with result parameters being available subsequent script steps. [Details in the docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/callbackurl)
- **Change:** "Run Workflow" action steps supports same callback system as new Callback URL step - allowing Drafts to wait for the result of a workflow, to be used in subsequent script steps. [Docs](https://agiletortoise.github.io/drafts-documentation/actions/steps/runworkflow)
- **New:** context script object adds "callbackResponses" object to access parameters returned by x-callback-url call using Callback URL or Run Workflow steps which "Wait for response". [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Context)
- **Fix:** Probably with animations getting confused by poor gesture timing making both side drawers visible.

#### v0.1.1.36

- **New:** TextExpander support. Basically the same as in D4, with a few notes:
    - TE Settings/refresh are now under a separate screen in Settings.
    - Fill-in snippets are not supported.
    - TE snippets work in the Share extension.
    - Expansion in action templates is supported for shortcuts wrapped in << >> as in D4.
- **New:** Additional and updated App icon options (in Aa view).
- **New:** A couple more categories of action icons from the Symbolicon set.
- **Fix:** "Restore" button in version history works now.
- **Fix:** Drawer interactions will now cancel if directly of swipe is reversed.
- **Fix:** Updated drawer interactions for tags in draft list and groups in action list to match fixes in the other drawer interactions.
- **Fix:** Maybe(?) a fix for case where swiping to left on action in action list could show "Delete" option instead of triggering groups drawer.

#### v0.1.1.35

- **Fix:** Main glitches in Backup features introduced yesterday. Most of the failures were due to file naming conflicts.
- **Change:** Support `application/x-www-form-urlencoded` params in HTTP request with new setting option for encoding - defaults to `application/json`.  [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/HTTP)

#### v0.1.1.34

- **New:** On-demand and automated periodic backups of Drafts and Action Groups to iCloud Drive - configured in Settings > Backup. Currently the periodic interval is set to 7 days when enabled. [Docs](https://agiletortoise.github.io/drafts-documentation/settings/backups)
- **New:** Mostly finished up Share extension. Append/Prepend available now.
- **Fix:** Performance issue with external keyboard.
- **Fix:** Disable iPhone X input accessory resizing with external keyboard, because of text drop issue.
- **Change:** Update Dropbox action icon to their new logo shape.
- **Fix:** URL encode Workflow name in Run Workflow action.
- **Fix:** Crash after using date formatted template tags in a prompt action step.
- **Fix:** When drawer is visible and pinned, do not grab up-down arrow key from editor.
- **Fix:** Share extension template not saving in settings.

#### v0.1.1.32

- **New:** Run Workflow action step.
- **New:** Swipe up or down on extended keyboard row to swap between available keyboards.
- **New:** Sharing action or action group now offers the option to share as URL or File.
- **Change:** Refactored drawer animations and gestures.
- **Fix:** Theme problem on share extension settings page.
- **Fix:** Custom implementations of cut and copy commands to force plain text.
- **Fix:** Case where quick select buttons for action groups could point to invalid groups and not do anything.
- **Fix:** Make sure action group buttons are updated when switching groups.
- **New:** Scripting:
    - Reminder object now has priority property [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/Reminder)
    - app.openURL(url) now can take optional boolean param to open in Safari View Controller. [Docs](https://github.com/agiletortoise/drafts-documentation/wiki/App)
- **Fix:** Allow a little more padding for key if icon and label are shown to avoid clipping.
- **Fix:** /append URL was, actually, prepending.
- **New:** "Play sounds" setting to disable/enable UI and notification sounds.

#### v0.1.1.30

- **Fix:** Workaround for glitching display when pasting text into editor.

#### v0.1.1.29

- **New:** Share extension (no append-prepend yet) and related settings.
- **Fix:** Importing action group should not add "(copy)" in action names.
- **Change:** Better activity indication on tapped actions.
- **New:** Misc. UI tweaks, added haptics, etc.

#### v0.1.1.27

!!! IMPORTANT: Before installing this build, you will have to delete and previous builds on the device, or it will crash on launch due to underlying data changes. Sync should restore your data, if it was enabled prior to the deletion, but not a bad idea to back up.

- **Fix:** Problem in persisting drafts which could generate a duplicate of the draft in the database when certain timing scenarios were hit.
- **New:** Conflict recognition for incoming sync changes when occuring to the same draft loaded in the editor.
- **Fix:** Action groups now refresh (in list and keyboard) when changes are made to the group, either via manage screens or sync.  This means you should not have to reload keyboards and or the action list to pick up changes.
- **Change:** On new installs, if iCloud is available, enable sync by default.

#### v0.1.1.26

- **New:** Actions in the action list are now drop targets for anything that can provide text.  Drag one or more text snippets, text files, drafts to an action and it will be queued and run for each item.
- **Fix:** A variety of storage issues with the new editor settings changes.
- **Fix:** Do not add "(copy)" to action names when importing.
- **New:** Add selectionStart and selectionLength properties to draft script object.
- **New:** Improved editing of action in a group when accessed in Manage screen - including options to duplicate, move actions and drag and drop reordering.
- **Change:** Adjust sidebar pane sizes.

#### v0.1.1.25

- **New:** Refactored editor settings by syntax.  All the text related settings (font, size, autocorrect, etc.) are stored separately by syntax and automatically changed when you change syntax - so you can have different fonts and behaviors for Markdown and Javascript, for example.  These are synced to iCloud, but by device - so they will restore from iCloud if reinstalled, but can be different on iPhone and iPad.
- **Fix:** Misc. fixes/improvements to syntax highlighting, especially in Markdown.
- **Fix:** Crasher passing invalid text ranges to some editor script methods.
- **New:** Mail and Message script steps now have contact selection option to insert recipients.
- **New:** /arrange URL scheme to use arrange mode with external apps/services.
- **New:** `editor.find()` and `editor.arrange()` methods to display arrange and find modes.

#### v0.1.1.24

- **Fix:** [[selection]] tag did not default to full contents if there was no selection.
- **Fix:** Possible threading gap that could allow a duplicate draft to be created if the timing was just right running an action.

#### v0.1.1.23

- **New:** Recent tag quick access list at bottom of draft list.
- **New:** Recent action group quick access list at the bottom action list.
- **New:** Groups now all appear in the action list sidebar.  Individual groups can be configured with "Available as keyboard" option to also make them visible in the keyboard selector.  A variety of related changes around this also.
- **New:** Add sync activity indicator at top of draft list.
- **Change:** A variety of visual fixes and improvements around the app.
- **New:** Actions now have "use icon" option to display the action's icon on keyboard keys.

#### v0.1.1.21

- **New:** "Recent Drafts" today widget.
- **New:** Dropbox scripting object allows read/write of files in Dropbox via script. (see: https://github.com/agiletortoise/drafts-documentation/wiki/Dropbox)
- **New:** Enhancements to Draft scripting object, including... (details: https://github.com/agiletortoise/drafts-documentation/wiki/Draft)
    - isArchived, isFlagged, isTrashed properties.
    - `find(uuid)` to retrieve existing draft by UUID.
    - `query(query, filter, tags)` method to query and return a list of matching drafts.
- **New:** `alert(msg);` script method to show a simple alert dialog.
- **Fix:** Re-enable some of the Script Editor settings which got disabled by accident in last build.
- **Change:** Styling improvement in action step editing.
- **New:** Start to include summarys in action step list for some types of steps.
- **Fix:** Layout glitch editing clipboard action step.
- **Fix:** Recent drafts available via 3D Touch should not include drafts in trash.
- **Fix:** HTML Preview display issue on iOS 11.2 (same issue Script Editor had).
- **Fix:** Tag keyboard helper suggestions getting clipped.

#### v0.1.1.20

- **Fix:** Script editor now displays properly on 11.2 devices.
- **Fix:** undo/redo were not working due to extra call to registerUndo points.
- **Change:** Build with iOS 11.2 b2 SDK on Xcode 9.2b2

#### v0.1.1.19

- Scripting changes (details on Wiki: https://github.com/agiletortoise/drafts-documentation/wiki):
    - **New:** Calendar and Event scripting objects to create calendar events.
    - **New:** "context" object in scripts with cancel and fail calls to stop execution of additional steps.
    - **New:** "action" object in scripts to query current action information and find actions by name.
    - **New:** `app.queueAction(action, draft)` method to queue and action to run after the current action.
    - **Change:** Moved "getClipboard" and "setClipboard" methods from editor to app object. They make more sense there.
    - **New:** `app.htmlToClipboard(html)` method. Takes HTML and converts it to rich-text in the clipboard - compatible with pasting into most rich-text apps (Mail, Pages, etc.).
- **Fix:** Clean up of a few styling issues in settings screens.
- **Change:** Contrast tweaks in dark theme.

#### v0.1.1.18

- **New:** Prompt action step type. Works just like in D4.
- **New:** Clipboard action step now supports append/prepend.
- **New:** Export operation in drafts list to export selected drafts.
- **New:** Export feature in Settings to export json or csv dumps of drafts.
- **Change:** "Operations" in draft list should error if no drafts are selected.
- **Fix:** Fix URL encoding of line feeds.
- **Fix:** Better handling of clearing tags from the list when no remaining drafts are assigned to a tag.
- **Change:** Hide tag shelf if draft list is hidden.
- **Change:** Hide action group shelf if action list hidden.
- **New:** FileManager.createLocal() and FileManager.createCloud() convenience methods.

#### v0.1.1.17

- **Fix:** Sync issues preventing edits of existing drafts from syncing properly.
- **Fix:** A couple of crashing issues in template evaluation, particularly url encoding.  Most recursive URLs should work now, but "AllowEmpty" doesn't do anything as of now, so they might end back in the target app.
- **Fix:** Issue with duplicate insert which could hang sync.
- **Fix:** Dropbox append/prepend would fail if file did not already exist.
- **Fix:** ||clipboard|| tag in incoming URLs should become blank string if nothing is in clipboard.
- **Fix:** Running action from keyboard would not properly save changes to the draft before running.
- **New:** Trash is now swept leaving only the last 7 days of drafts when the app is sent to the background.

#### v0.1.1.16

- **New:** "File" action step type to create/append/prepend to files in either the Local app storage or iCloud Drive.
- **New:** FileManager script object. This allows reading from and writing to files in both the Drafts' local documents directory (visible in Files.app) or iCloud Drive (in "Drafts5" folder).
    - [FileManager docs](https://github.com/agiletortoise/drafts-documentation/wiki/FileManager)
- **Change:** Improve visibility of sidebar pinning buttons when available (mainly on iPad)
- **Fix:** Custom template tags defined in scripts were not being evaluated properly.
- **Fix:** Attempt to create Reminder objects in script should request Reminders access permissions if not already granted.

#### v0.1.1.15

- **New:** Prompt scripting object for creation and display of prompt dialogs with custom text input and buttons (see docs: https://github.com/agiletortoise/drafts-documentation/wiki/Prompt)
- **Fix:** Tapping on the draft in Siri after using "Create note using Drafts..." properly opens the new draft now.
- **Fix:** Crash deleting action step if it was the only action step in the action.
- **Fix:** If draft loaded in editor is moved to the trash, start a new draft.
- **Fix:** Search button from widget now works.
- **Fix:** /search URL scheme now works. Supports query and new "tag" arguments.
- **Fix:** Set the app badge to 0 using the old API because Apple's new API doesn't work for 0 because ??
- **New:** Custom template tags defined by "draft.setTemplateTag(name, value)" javascript calls are not evaluated in templates properly.
- Laying some groundwork for the watchOS app in the underlying frameworks.

#### v0.1.1.14

- **New:** Work on URL schemes.  Most of the same URLs supported by D4 should work now, just with the drafts5: scheme.
- **Change:** Tweaks to Find and Replace view.
- **Change:** Theme preview improvements.
- **New:** "Copy to Drafts" file imports work now.
- **Change:** Switch to sharing and import of Action Groups and Actions using URL (in leiu of files) for better compatibility.
- **New:** Fill in a few more missing action icons.

#### v0.1.1.13

- **New:** List auto-completion for Markdown and TaskPaper language grammars.
- **New:** Alternate app icons available in Appearance settings.  Preliminary set, options may change.
- **New:** Reminders import functionality. Can be configured in Settings.
- **Fix:** Actions with "use default" dispositions did not always properly inherit the disposition setting of their action group.
- **Change:** Some Script Editor changes for better flow.  Syntax checker warning symbol added.

#### v0.1.1.12

- **New:** Reminder action step.
- **New:** List in Reminders action step.
- **New:** Reminder and Reminder list scripting interfaces, including alarms. Details in wiki...
    - [Reminder](https://github.com/agiletortoise/drafts-documentation/wiki/Reminder)
    - [ReminderList](https://github.com/agiletortoise/drafts-documentation/wiki/ReminderList)
    - [Alarm](https://github.com/agiletortoise/drafts-documentation/wiki/Alarm)
- **Change:** Disable landscape support on iPhone, at least for now.
- **Change:** Fix up some visual inconsistencies across views.
- **Change:** Insert custom popover view background class for better styling.
- **New:** Expand theming to buttons and action tint colors.
- **Fix:** Modifications to the draft currently in editor from the draft list (archiving, etc.) could get lost when editor re-saved draft.

#### v0.1.1.11

- **Fix:** Deleting action steps did not work properly.
- **New:** Added template tag and processTemplate methods to draft object in scripting (Details: https://github.com/agiletortoise/drafts-documentation/wiki/Draft)
- **Fix:** Script methods on editor object which change text should register undo points so the change can be reverted with undo.
- **Fix:** Change to draft content in action script might not be loaded in the editor.
- **Fix:** Extended keyboard should reload action group after changes are made in the "Manage" screen.
- **Fix:** List indentations for ordered lists in Markdown language grammar did not indent wrapped lines properly.
- **Fix:** Deleting actions in manage groups views did not work properly.
- **Fix:** Some encoding issues for certain characters posting to twitter.

#### v0.1.1.10

- **Change:** Sync can now be enabled in Settings - can't promise I won't clear data, however.
- **Change:** Tweak momentum for drawer gestures a little.
- **Change:** Make "Get info" keyboard shortcut opt-cmd-I to avoid conflict with italics.
- **Change:** Default draft list sort order to "modified" on new install.
- **New:** HTML Preview action step type.
- **Fix:** Add title to step editing views.
- **New:** Tweaks to recent tag suggestions, including way to clear recent list.
- **Fix:** Prevent keyboard shortcuts from interferring with other views (like Script Editor)
- **Change:** Keyboard shortcut for "Enter" in draft list should hide draft list.
- **New:** Incorporate Date.js library into Scripting context for easy date parsing/manipulation (http://www.datejs.com)
- **Change:** Improve display of table view separators.
- **New:** "Remove tag" operation in draft list.
- **Change:** Build with Xcode 9.1 against 11.1 SDK.
