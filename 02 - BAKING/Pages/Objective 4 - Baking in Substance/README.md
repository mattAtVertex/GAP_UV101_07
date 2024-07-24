# Objective 4 - Baking in Substance

<p><iframe src="https://www.youtube.com/embed/nBbiAcbT_YQ?rel=0" width="960" height="540" allowfullscreen="allowfullscreen" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"></iframe></p>
<hr>
<h2>Objective</h2>
<p>In this worksheet, we’re going to explore how to bake our high poly meshes to their low poly versions. The generated maps will then be used by Painters’ effects and utilities to aid in the texturing process of your model. In this worksheet, we will be covering.</p>
<ul>
<li>Baking setup</li>
<li>Baking "By Mesh Name"</li>
<li>Common Issues</li>
</ul>
<hr>
<h2>The Interface</h2>
<p>When you open Substance Painter you will be greeted with a blank canvas. Let’s define some of the areas.</p>
<p><img src="https://vertexschool.instructure.com/courses/8/files/543/preview?verifier=TfPsw46VC6WbKhjt13f9uGyJdgufscbT7bskhzZH" alt="interface.jpg" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/543" data-api-returntype="File"></p>
<p>&nbsp;</p>
<h3>Interface Areas</h3>
<ul>
<li style="font-weight: 400;">
<strong>Viewports</strong><span style="font-weight: 400;"> are where you will see the model upon import. You can manipulate the viewports with the familiar “Maya” style navigation. ALT+LMB rotate : ALT+RMB zoom (or scroll wheel) : ALT+MMB pan</span>
</li>
<li style="font-weight: 400;">
<strong>Viewport Tools</strong><span style="font-weight: 400;"> manipulate the viewports as well as the imported model.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Brush and Selection Tools</strong><span style="font-weight: 400;"> operate within the viewports on your model.</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Active Tab Panel </strong><span style="font-weight: 400;">displays information related to the tabs across the top of the window.&nbsp;</span>
</li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">The </span><strong>Properties Panel </strong><span style="font-weight: 400;">displays the properties and options available based on what is selected in the Active Tab. </span>
</li>
<li style="font-weight: 400;">
<strong style="font-family: inherit; font-size: 1rem;">The Library</strong><span style="font-weight: 400;"> is a collection of tools, materials, and utilities that alter your model or viewport.</span>
</li>
</ul>
<hr>
<h3>Creating Your Project</h3>
<p>To start, let’s create a New File.</p>
<p><img src="https://vertexschool.instructure.com/courses/8/files/545/preview?verifier=3vGobh1Rbf8HuqHkRmGKG8xv5cuP0rb4uXWYm5Ee" alt="fileNew.png" width="189" height="44" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/545" data-api-returntype="File"></p>
<ol>
<li><span style="font-weight: 400;">In the New Project window: Select the Unreal Engine 4 (Allegorithmic) template from the drop-down box as we will be importing these into Unreal later.</span></li>
<li><span style="font-weight: 400;">Click the “Select…” box. Here you will navigate to your low poly models .FBX file. This will be the imported mesh.</span></li>
<li><span style="font-weight: 400;">Leave the Document Resolution at the default setting. This setting can be changed at any time, as Painter is non-destructive and only encodes the resolution on export.</span></li>
<li><span style="font-weight: 400;">Normal Map: Set to DirectX </span></li>
<li><span style="font-weight: 400;">Leave all other settings at default.&nbsp; AutoUVUnwrap is checked.&nbsp; Compute tangent… is checked.</span></li>
<li><span style="font-weight: 400;">Click OK. Your mesh will now import and you will have something resembling the first image, where your model is in the viewport. Now we are ready to start baking the maps!</span></li>
</ol>
<p>&nbsp;</p>
<h3>Baking Mesh Maps Using Match By Name (The Preferred Approach)</h3>
<p><span style="font-weight: 400;">Initializing the baker window. Edit &gt; Bake Mesh Maps.&nbsp;</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/544/preview?verifier=SqouNK70zbTq4DY7EsveVE6XThjgw5K2zHci8Zj3" alt="BakerWindow.jpg" width="625" height="996" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/544" data-api-returntype="File"></span></p>
<ol>
<li><span style="font-weight: 400;">Set the Output Size to 2048.</span></li>
<li><span style="font-weight: 400;">Select your High Definition Mesh and click the little paper icon.&nbsp; This will allow you to select your high-resolution mesh.</span></li>
<li><span style="font-weight: 400;">Set Max Frontal and Max Rear Distance to 0.07</span></li>
<li><span style="font-weight: 400;">Set Anialiasing to Subsampling 4x4.</span></li>
<li><span style="font-weight: 400;">Set Match to By Mesh Name.</span></li>
<li><span style="font-weight: 400;">Check the ID box (The ID parameters will show up)</span></li>
<li><span style="font-weight: 400;">Set Color Source to Mesh ID/Polygroup.</span></li>
<li><span style="font-weight: 400;">Set Color Generator to Random.</span></li>
<li><span style="font-weight: 400;">Click Bake 1001 Mesh Maps.</span></li>
</ol>
<p>When the Baker is done it's time to check the maps for issues.</p>
<p>&nbsp;</p>
<h3><span style="font-weight: 400;">Common Problems</span></h3>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">Missing parts of the map: check your Max frontal/Rear Distance settings.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Maps are not showing: check to see if the missing map is ticked in the baker window.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Maps still not showing:</span>
<ul>
<li style="font-weight: 400;" dir="ltr"><span style="font-weight: 400;">Confirm your mesh names are set: _high and _low.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">And Match: By Mesh Name.</span></li>
</ul>
</li>
<li style="font-weight: 400;"><span style="font-weight: 400;">ID is not showing: check to see if Color Source is set to Mesh ID/Polygroup.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Stretching: check your UVs.</span></li>
<li style="font-weight: 400;">
<span style="font-weight: 400;">Artifacting:</span>
<ul>
<li style="font-weight: 400;"><span style="font-weight: 400;">check your Max frontal/Rear Distance settings.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">check your hard/soft edges in Maya.</span></li>
</ul>
</li>
</ul>
<p><span style="font-weight: 400;">&nbsp;</span></p>
<p><span style="font-weight: 400;">This Quick Start Guide is the general workflow for successful baking in Substance Painter.</span></p>