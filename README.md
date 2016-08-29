# window-opener-vuln

An example of how to exploit window.opener.

## Problem

When setting the `target` attribute on links (or other HTML elements that
allow the `target` attribute) with a `_blank` value, users can get
access to the `Window` object of the tab that opened the link. In case
of applications where users can post content, this functionality can be 
abused for Phishing.

## Solution

Always use the `rel="noopener"` attribute on links that contain a 
`target="_blank"` attribute. As a rule of thumb do this unless you
have a very good reason not to.

## References

* https://developer.mozilla.org/en/docs/Web/API/Window/opener
* https://bugs.chromium.org/p/chromium/issues/detail?can=2&start=0&num=100&q=&colspec=ID%20Pri%20M%20Week%20ReleaseBlock%20Cr%20Status%20Owner%20Summary%20OS%20Modified&groupby=&sort=&id=168988
* https://www.reddit.com/r/programming/comments/4zikpx/the_target_blank_vulnerability_by_example/
