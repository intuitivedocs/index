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

Test