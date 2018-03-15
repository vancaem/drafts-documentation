---
title: Notifications and App Badge
---

Drafts can display a badge on the app home screen icon to indicate the number of unprocessed drafts in the inbox. This count can additionally be filter based on criteria described below.

{% include doc-image.html src="/settings/notifications.png" %}

To enable the app badge, visit Settings > Notifications. Available options:

- *Show inbox count*: Toggle this on to enable the app badge. If you have not enabled the badge before, you will be prompted to allow notification permissions. These permissions are required to display the badge.
- *Count only flagged inbox drafts*: If enabled, only flagged drafts will be included in the count.
- *Tag filter* The tag filter allows filtering of the counted drafts by tags. This can be a single tag, a comma-delimited list of tags. The special value "untagged" is also support to filter by only drafts which are not assigned a tag - and ! can be used to omit a tag. Example expressions:
  - `blue, green`: Only drafts with both blue and green tags.
  - `blue, !green`: Only drafts with the blue tag, but NOT the green tag.
