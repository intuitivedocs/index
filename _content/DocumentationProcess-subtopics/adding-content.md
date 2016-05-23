---
title: "Adding content"
author: Reuben Evans
---

In order to add content, first set up a github account and download [GitHubDesktop]. You will then need to be added as a collaborator for the repository.

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

You can add other content in the header - it will not be displayed on the website. This could include author, editor, date edited and so on, but all of this can be tracked through github so is unnecessary.

See the "Exemplar markdown" post as a guide on how to write the markdown.

[GitHubDesktop]: https://desktop.github.com/