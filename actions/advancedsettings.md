---
title: Advanced Action Settings
---

The action edit screen contains a number of advanced configuration options which affect how the action is run.  

<div class="doc-image">
<img src="{{ site.baseurl }}/images/docs/actions/after-success.png" alt="Advanced Settings"/>
</div>

### Confirm before running

While Drafts is geared around making it quick and frictionless to act on drafts, there are sometimes actions which publish text, or update or overwrite files, etc., which you might not want to accidentally trigger with an errant tap.

If "Confirm before running" is enabled, whenever the action is run, a prompt will open to confirm you wish to run the action, with the option to cancel.

### After success

After the successful completion of an action, drafts can be filed away automatically using the "After success" setting.

After Success can be set on individual actions in their action edit view, or use a default set on the Action Group the action reside in. The default value on an action is "Default", which will inherit the setting from the Action Group. The options are as follows:

- **Default**: Use the "After success" setting configured for the Action Group.
- **Nothing**: After success, do not do anything with the draft. This is common for actions used as keyboard keys, or which modify some text in the current draft.
- **Archive**: After the action is successful, file the draft in the archive.
- **Trash**: After success, move the draft to the trash can.

If the after success is set to archive or trash the draft, and that draft is currently loaded in the editor, Drafts will also end editing of that draft.  If [focus mode]({{ site.baseurl }}/editor/focusmode) is current enabled, the next draft in the draft list will be loaded.  If focus mode is off, you will be returned to a new draft, ready to edit.

### Notification

The notification setting determines whether Drafts will show a banner and confirmation sounds after running the action.  The options are:

- **None**: Do not show a banner or play notification sounds after the action. Typically used for actions (like keys which insert text) that require no confirmation.
- **Errors**: Only show notifications if an error occurs running the action.
- **All**: Always show completion confirmation, regardless of success or failure.

#### Log Level

Actions generate logs of the actions execution which provide useful records of what actions have been performed on a draft, and what (if any) error occurred. These logs are available in the draft detail (i) view. Depending on the type of action, it may make sense not to log the execution of the action. For example, you might not need to know a history of each time you copied the draft to clipboard, or inserted a bold text markup with an action key.  

- **None**: Do not save logs of this action's execution.
- **Errors**: Only log if an error occurs running the action.
- **All**: Always log completion confirmation, regardless of success or failure.
