# CSS Variable in :before content with unescaped special characters

This repository demonstrates a subtle bug related to using CSS variables within the `content` property of the `::before` pseudo-element.  Specifically, the issue arises when the CSS variable contains special characters that aren't properly escaped.

The `bug.css` file contains the buggy code.  The `bugSolution.css` file provides a corrected version.

## Problem

When a CSS variable containing unescaped special characters (like single quotes or backslashes) is used within the `content` property of `::before`, the CSS parser might misinterpret the content, leading to errors or unexpected output.

## Solution

Properly escape special characters within the CSS variable to prevent these issues.  This typically involves using backslashes to escape quotes and other special characters. Alternatively, consider using different methods of managing dynamic content.