---
title: Action Step – Print
---
# Action Step: Print

Print to an AirPrint printer.

## Examples

- [Print: Text](drafts5://action?data=%7B%22uuid%22:%2201767171-37DE-453F-BC1E-8C6D120D5541%22,%22steps%22:%5B%7B%22type%22:%22print%22,%22data%22:%7B%22template%22:%22%5B%5Bdraft%5D%5D%22,%22format%22:%22text%22%7D,%22uuid%22:%226C1437F8-E081-4D52-B783-21AF3E5BCE4F%22%7D%5D,%22shortName%22:%22%22,%22shouldConfirm%22:false,%22disposition%22:3,%22keyCommand%22:%7B%22optionKey%22:false,%22input%22:%22%22,%22controlKey%22:false,%22commandKey%22:false,%22type%22:%22action%22,%22discoverabilityTitle%22:%22Print:%20Text%22,%22shiftKey%22:false%7D,%22logLevel%22:2,%22notificationType%22:2,%22tintColor%22:%22none%22,%22actionDescription%22:%22Print%20as%20plain%20text%20to%20AirPrint%20printer.%22,%22keyUseIcon%22:false,%22icon%22:%22action_print%22,%22visibility%22:2,%22supportedPlatform%22:%22any%22,%22groupDisposition%22:0,%22name%22:%22Print:%20Text%22%7D)
  - Print draft as plain text.
- [Print: HTML](drafts5://action?data=%7B%22uuid%22:%2205E8F8EB-4FCB-4B2E-9379-D5A9410297EB%22,%22steps%22:%5B%7B%22type%22:%22print%22,%22data%22:%7B%22template%22:%22%3Chtml%3E%5Cn%3Cstyle%3E%5Cnbody%20%7B%5Cn%20%20font-family:%20Helvetica,%20sans-serif;%5Cn%20%20font-size:%20100%25;%5Cn%7D%5Cn%3C%5C/style%3E%5Cn%3Cbody%3E%5Cn%25%25%5B%5Bdraft%5D%5D%25%25%5Cn%3C%5C/body%3E%5Cn%3C%5C/html%3E%22,%22format%22:%22html%22%7D,%22uuid%22:%22AA38F49B-84B8-45CD-866B-C0DB2FADC433%22%7D%5D,%22shortName%22:%22%22,%22shouldConfirm%22:false,%22disposition%22:3,%22keyCommand%22:%7B%22optionKey%22:false,%22input%22:%22%22,%22controlKey%22:false,%22commandKey%22:false,%22type%22:%22action%22,%22discoverabilityTitle%22:%22Print:%20HTML%22,%22shiftKey%22:false%7D,%22logLevel%22:2,%22notificationType%22:2,%22tintColor%22:%22none%22,%22actionDescription%22:%22Convert%20Markdown%20to%20HTML%20and%20print%20with%20basic%20sans-serif%20style.%22,%22keyUseIcon%22:false,%22icon%22:%22action_print%22,%22visibility%22:2,%22supportedPlatform%22:%22any%22,%22groupDisposition%22:0,%22name%22:%22Print:%20HTML%22%7D)
  - Convert Markdown in draft to HTML and print with basic san-serif css applied.

## Options

- **Template**: Template for content of the printout.
- **Format**: Text or HTML.  Text will print as plain text document. HTML expects the template to output fully formed HTML, which allows Markdown conversion and application of styles and formatting.
