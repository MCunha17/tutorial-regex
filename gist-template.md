# Regex Tutorial: Matching an HTML Tag

In the realm of Search Advertising, understanding and applying regular expressions (regex) can become an indispensable skill. They allow you to manipulate text and find specific patterns in a string, enabling you to handle and make sense of large sets of data, like the ones you might encounter in a search advertising campaign.

One frequent application in search advertising could be ensuring that all your HTML tags, crucial for SEO and tracking purposes, are correctly formatted. This tutorial will focus on understanding a specific regex used to match HTML tags.

## Summary

This tutorial dives into the regex /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/, designed to match HTML tags in a string. Properly formatted HTML tags are crucial for search advertising as they influence how your webpage is indexed and how tracking scripts are triggered.

## Table of Contents

- [Anchors](#anchors)
- [Grouping and Capturing](#grouping-and-capturing)
- [Character Classes](#character-classes)
- [Quantifiers](#quantifiers)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Back-References](#back-references)
- [Non-Capturing Groups](#non-capturing-groups)

## Regex Components

### Anchors

Anchors correspond to positions before, after, or between characters. The ^ and $ symbols are start and end of line anchors, ensuring that the string fully matches the pattern from the beginning to the end. This is vital in search advertising where HTML tags need to be exact.

### Grouping and Capturing

([a-z]+) forms a capturing group and matches one or more (+ is a quantifier) lowercase letters (a-z). Grouping is crucial for distinguishing different parts of an HTML tag, like the tag name and attributes.

### Character Classes

[^<]+ is a character set that matches any character that is NOT a <. This is important in matching HTML tags as we want to ignore any character that isn't part of the tag name or attributes.

### Quantifiers

Quantifiers like * in our regex determine how many instances of a character, group, or character class must be present for a match. It's important in parsing HTML tags where some parts of the tag may repeat.

### Greedy and Lazy Match

Our regex uses a greedy quantifier * to match as many characters as possible. This helps in extracting the entire content within an HTML tag.

### Back-References

\/\1 is a back-reference that matches the same text as the first capturing group. This ensures the closing HTML tag matches the opening tag.

### Non-Capturing Groups

(?:> and |\s+\/>) forms a non-capturing group, useful in scenarios where we want to group parts of the regex but don't need to capture the information for later use.

## Author

This tutorial was crafted by Maria Cunha, a dedicated Product Marketing professional. Currently, I am expanding my horizons by learning how to code, aiming to bridge the gap between the technical and marketing worlds. My mission is to enhance my understanding of the technical dimensions of products and foster more effective communication with engineering teams. I believe that this skillset will enable me to bring our products closer to the market and our customers. Check out my [GitHub profile MCunha17](https://github.com/MCunha17) to see more of my projects.