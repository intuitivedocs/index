---
title: "Editing the sidebar"
---

## Example HTML

The sidebar is a manually controlled HTML file. It is location in Jekyll/_includes/sidebar.html

We have to manually update it. The code looks something like this:


{% highlight bash %}

<div class="catbloc-collection">
     <div class="catbloc">          
            <ul class="sidebar-post">

                  <!-- This is the first header -->
                  <p class="icon-clipboard">
                    Misc
                  </p>

                  <!-- This is the first list of articles -->
                  <li>
                        <a href="{{ site.contentsref }}Contents">
                         Contents
                        </a>
                  </li> 

                  <!-- This is the second header -->
                  <p class="icon-graph">
                  Test
                  </p>   

                  <!-- This is the second list of articles -->                          
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

#### Adding sections


We curate the bits inbetween. To start a new section add in:


{% highlight bash %}

<p class="icon-clipboard">
	Misc
</p>

{% endhighlight %}


Add a class of the form "icon-xyz" to specify the icon appearing on the left of the header. The icons we have available are:

- calender
- contract
- document
- flag
- flight
- folder
- graph
- hotel
- info
- misc

New icons can be added in sidebar.scss in intuitivedocs/DocumentationThemeSite

#### Adding articles

Then add the articles you want. To specify a hierarchy nest the html. They should look like this:

{% highlight bash %}

<li>
	<a href="{{ site.contentsref }}Relative/Path/From/_content/Folder">
		Article Title
	</a>
</li>

{% endhighlight %}

Boom! You should now see your results.