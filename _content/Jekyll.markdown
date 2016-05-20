---
title:  "Jekyll"
---
Jekyll is the software we use to convert markdown files into our documentation websites.

Each documentation website has its own github repository. The github username of the repository owner forms the first part of the url - “intuitivedocs”, and the repository name forms the third part of the url - “DevelopmentTeamDocumentation”.

In order to add content, first set up a github account and download [GitHubDesktop]

Clone the exisiting repository for the website you wish to add content to and it will appear on the left hand side of the GUI. All website content exists within the "gh-pages" branch of the repository, so content can be added through either of the following processes:

- the normal git process of committing directly into the gh-pages branch
- branching off the "gh-pages" branch and then making a pull request

Every markdown file added requires a title which is added at the very top of every file as follows:

{% highlight bash %}
---
title:  "Jekyll"
---
{% endhighlight %}

Jekyll does not require the title and filenames to match but for the sake of site maintenance this will be enforced.

See the subposts in this category for more information.

[GitHubDesktop]: https://desktop.github.com/
