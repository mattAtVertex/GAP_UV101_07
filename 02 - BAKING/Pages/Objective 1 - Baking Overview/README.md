# Objective 1 - Baking Overview

<p><iframe src="https://player.vimeo.com/video/452915604" width="960" height="540" allowfullscreen="allowfullscreen" allow="autoplay; fullscreen"></iframe></p>
<hr>
<h2>Objective</h2>
<p>In this handout, we’re going to explore the baking process a little more to understand how it is going to help us later in the texturing phase.</p>
<p><img src="https://vertexschool.instructure.com/courses/8/files/535/preview?verifier=C6ijJiYRJuxscIRsNERCvOjl9HbGkMB2N8hmQ9hM" alt="image1.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/535" data-api-returntype="File"></p>
<hr>
<h2>Baked Maps in 3D Art</h2>
<h3>What is Baking?</h3>
<p>Baking is the process of extracting information from the high poly mesh and mapping it to the UV space of the low poly mesh. Through the baking process, we transfer the details from the high poly to the low poly.</p>
<p>The core map resulting from this process is the Normal Map. This very important map is what fakes lighting information to give the illusion that the low poly has more geometry than it actually does.</p>
<p>But the Normal Map is only one of the many maps that gets baked. There are several other maps generated in the process that contribute to the texturing phase.</p>
<p>&nbsp;</p>
<p><img src="https://vertexschool.instructure.com/courses/8/files/542/preview?verifier=bpoRrfkUZdppdW4zwuYtZXKaFBEsnzrmlc0BQoIX" alt="image8.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/542" data-api-returntype="File"></p>
<p>&nbsp;</p>
<h3>The Baked Maps</h3>
<p><span style="font-weight: 400;">During the baking process, several maps are generated. Each one contributes to the texturing process in a different way, but they are all important for successful texturing.</span></p>
<p>&nbsp;</p>
<p><strong>Normal</strong><span style="font-weight: 400;"> - Map that fakes lighting to show high poly details on the low poly. Responsible for making the low poly look like it has more geometry than it does.&nbsp;</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/540/preview?verifier=fWAHZbS6vjsh3HAQo1yqMdaVQxeVjyFNCe00vS2L" alt="image6.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/540" data-api-returntype="File"></span></p>
<p><span style="font-weight: 400;">&nbsp;</span></p>
<p><strong>Curvature</strong><span style="font-weight: 400;"> - Map that defines the edges and cavities of the mesh. This is useful for generating edge highlights and controlling areas for dirt and dust.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/541/preview?verifier=gpMDSS8rgFVcWYpiJZQq7AFPeA9KBpRwSKMUOL6l" alt="image7.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/541" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Ambient Occlusion</strong><span style="font-weight: 400;"> - Map that defines the shadowy areas of the mesh. This map is responsible for the shadows you see in the cracks and crevices, as well as contributing to the control of dust and dirt.</span></p>
<p><strong>Position</strong><span style="font-weight: 400;"> - Map that stores the position in 3D space as a gradient. This map is important for procedurally generating gradients in your texture work.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/537/preview?verifier=k6x9OhZfwIozx0EjfjpbTtu5ObPq9iY0SX5ZMjqd" alt="image3.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/537" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Thickness Map</strong><span style="font-weight: 400;"> - Simulates the thickness of the model. This map is useful for things like SubSurface Scattering.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/536/preview?verifier=5Vj3lzfkjp4vEPG6reqXzhZo1JUtCBWDP2sfG9QI" alt="image2.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/536" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<p><strong>Material ID</strong><span style="font-weight: 400;"> - Color map that masks different areas meant for different materials. Another very important map that helps organize the physical materials into groups.</span></p>
<p><span style="font-weight: 400;"><img src="https://vertexschool.instructure.com/courses/8/files/538/preview?verifier=FA7pww6JLMZ3hOSNBp2FLdn6KIdkb6QuSlhkTfKp" alt="image4.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/538" data-api-returntype="File"></span></p>
<p>&nbsp;</p>
<h3>THEY ALL WORK TOGETHER</h3>
<p>&nbsp;</p>
<p><img src="https://vertexschool.instructure.com/courses/8/files/539/preview?verifier=4glqrnuzP762dmhlcZo8NBupKGly445Ec803xVO1" alt="image5.png" width="650" height="366" data-api-endpoint="https://vertexschool.instructure.com/api/v1/courses/8/files/539" data-api-returntype="File"></p>