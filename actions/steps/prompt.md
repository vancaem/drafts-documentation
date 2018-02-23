---
title: Action Step – Prompt
---

Display a prompt with buttons and optional a text input field.  The results of the prompt are placed in a template tags for use in subsequent action steps.  More advanced prompts are possible with [the prompt script object](https://github.com/agiletortoise/drafts-documentation/wiki/Prompt) as well.

## Options

- **Key** *(default: prompt)*: The key is used to create Drafts tags based on the text input and/or buttons pressed when the prompt is displayed to the user. See discussion below.
- **Title** *(default: Prompt)*: A short title of the prompt window.
- **Message** *(default: blank)*: A longer text to appear in the prompt and explain the input desired, if necessary.
- **Include text field** *(default: OFF)*: If ON, the prompt will include a single line text input field which can be used to take information from the user.
Text field default (default: blank): The default text to place in the text field, if included. This field can contain Drafts tags, like [[title]] to set a default value. After the prompt is displayed, the value in the text field will be accessible via the a `[[prompt_text]]` tag in scripts and templates used in steps after the prompt step.
- **Include cancel button** *(default: ON)*: If ON, a "Cancel" button will automatically be included in the prompt. The cancel button will cancel execution of the action and no further steps after the prompt will be run.
- **Buttons** *(default: OK)*: A string listing buttons to include in the prompt. Multiple buttons can be listed by using the | character as a separator, for example "Red|Green|Blue" would result in three buttons appearing in the prompt. After the prompt is displayed, the name of the button tapped by the user will be available in the `[[prompt_button]]` tag in scripts and templates used in steps after the prompt step.

#### Keys, Tags and Multiple Prompts

Prompts use Drafts tagging system to expose values from the prompt for use in action steps which occur after the prompt in the same action. The tags used are constructed using the "Key" value for the prompt.  If using a single prompt in an action, the default "prompt" key is fine and will result in two new tags being available:

- **[[prompt_button]]**: will contain the name of the button pressed in the prompt.
- **[[prompt_text]]**: will contain the text in the optional text field.
If using multiple prompts in the same action, you can distinguish results by the changing the "Key" on the prompt steps.  A key of "myselection" will result in tags `[[myselection_button]]` and `[[myselection_text]]`, etc.

These tags can then be used in subsequent steps.  A common application would be to prompt for a filename to use, then use the `[[prompt_text]]` tag as the filename value in a Dropbox step. The Save to Dropbox as... action in the directory demonstrates this example.

If you wish to use the results of prompt in an script action step, you can retrieve the values using the "draft.getTag('tagName');' function.  
