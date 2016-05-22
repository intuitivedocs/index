---
title: "Editing the sidebar"
---

## Purpose
- Testing markdown


The sidebar is a manually controlled HTML file. It is location in Jekyll/_includes/sidebar.html

We have to manually update it. The code looks something like this:

{% highlight bash %}

<div class="catbloc-collection">
     <div class="catbloc">          
            <ul class="sidebar-post">


                  <p class="icon-clipboard">
                    Misc
                  </p>
                  <li>
                        <a href="{{ site.contentsref }}Contents">
                         Contents
                        </a>
                  </li> 

                  <p class="icon-graph">
                  Test
                  </p>                             
                   <li>
                        <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/ReviewAndCoaching">
                         Review and Coaching
                        </a>

                        <ul>
                            <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/SpecificationWriting">
                             Specification Writing
                            </a>

                            <li>
                                  <a href="{{ site.contentsref }}SoftwareDevelopment-subtopics/TestDeploy">
                                   Test Deploy
                                  </a>
                            </li>
                        </ul> 
                  </li>



               </ul>
            </div>
</div>

{% endhighlight %}

The first and last three lines should be left well alone. This is to do with the larger overall page structure.

We curate the bits inbetween. To start a new section add in:

{% highlight bash %}
<p class="icon-clipboard">
	Misc
</p>
{% end highlight %}

Add a class of the form ``icon-xyz`` to specify the icon appearing on the left of the header. This needs to be updated in the intuitivedocs.github.io/DocumentationSiteTheme sidebar scss file, if the icon is not already in use.

Then add the articles you want. To specify a hierarchy nest the html. They should look like this:

{% highlight bash %}
<li>
	<a href="{{ site.contentsref }}Relative/Path/From/_content/Folder">
		Article Title
	</a>
</li>
{% end highlight %}
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