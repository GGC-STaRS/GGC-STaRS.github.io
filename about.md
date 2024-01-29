---
layout: about
title: About
permalink: /about/
photos:
- 12915108384_1a98518cfa_o.jpg
- 16625184114_f70749312b_b.jpg
- 16627102103_1d05c23e64_b.jpg
- 17061099369_a1e34de66b_b.jpg
- 17247305655_b9ae4e3dbf_b.jpg
- 18378901762_6b8003daf3_o.jpg
- 23833278995_e661c76950_o.jpg
- Biology Food Burn Calorie Lab Biology Food Burn Calorie Ct_GGC2158.jpg
- Biology Food Burn Calorie Lab Biology Food Burn Calorie Ct_GGC2167.jpg
- Candid Chemistry Images for H12841578704_458defb39e_o.jpg
- Candid Chemistry Images for H16776090625_f4ab55cca2_o.jpg
- Candid Chemistry Images for H44621689285_a108f29202_o.jpg
- Game of Drones Fall 2019_GGC9879.jpg
- GGC5524.JPG
- GGC5579.JPG
- GGC5750.JPG
- GGC5804.JPG
- GGC9281.JPG
- Jesse Merida 3D Face masks_GGC5642.JPG
- Mai Yin Tsoi Teaching Chem _GGC7491.JPG
- Screenshot (48).png
- Service learning Interns SST_GGC4759.JPG
- SST Students and Faculty _GGC6848.jpg
- Strickland Lab 1.jpg
- Strickland Lab 2.jpg
- Strickland Lab 3.jpg
- Strickland Lab 4.jpg
- TAP Event Fall 2019_GGC2975.jpg
- TAP Event Fall 2019_GGC3446.jpg
- TAP Event Fall 2019Tech Ambassador Program TAP_GGC1558.jpg
- TAP Event Fall 2019Tech Ambassador Program TAP_GGC1644.jpg
- Tech Ambassador Program TAP_GGC1439.JPG
---

## ✨ Science, Technology, and Reseach Symposium (STaRS) ✨

The STaRS event is organized by the [School of Science and Technology](https://www.facebook.com/ggc.sst) at [Georgia Gwinnett College](https://www.ggc.edu/) every spring. The purpose of this event is to promote science, math, and technology for our STEM students, and to provide opportunities to showcase the scientific research and other STEM activities that take place at GGC.

<div class="project_pictures">
    <div id="slideshow">
      {% for photo in page.photos %}
      <div class="pictures">
        <a  id="lightgallery" href="{{ site.baseurl }}/assets/images/slideshow/{{ photo }}">
          <img src="{{ site.baseurl }}/assets/images/slideshow/{{ photo }}">
        </a>
      </div>

      {% endfor %}
    </div>
  </div>


### 🐻 Location of Events 🐻
Building H2, 1st, 2nd, & 3rd floors



### 🐻 School of Science and Technology (SST) 🐻

The School of Science and Technology (SST) at GGC is creating a diverse community of STEM graduates. SST offers programs in Biology, Chemistry, Information Technology, Mathematics, Exercise Science, and Environmental Science and has a unique and diverse student population (32% Black or African-American, 19% Hispanic, and 14% Asian), with 54% males and 46% females.  About 30% of SST students are the first in their families to go to college.  Nearly all STEM students participate in STaRS and the event is open to other GGC students as well, with an estimated 3,000 GGC students in attendance.

Read the SST dean's message for STaRS 2023 <a href= "https://ggc-stars.github.io/stars2023/update/2023/02/22/deans-message.html">here! </a>

![SST collage]({{ '/assets/images/sst-image-fb.jpg' | relative_url }} "A collage of SST faculty and students")

<!-- lightgallery -->
  <script src="https://cdn.jsdelivr.net/lightgallery/1.3.7/js/lightgallery.min.js"></script>
  <script src="https://cdn.jsdelivr.net/g/lg-zoom"></script>

  <script type="text/javascript">
    $(document).ready(function() {
      // Slideshow setup
      $("#slideshow > div:gt(0)").hide();

      setInterval(function() {
        $('#slideshow > div:first')
          .fadeOut(1000, function() {
	  	$(this).appendTo('#slideshow');
		$('#slideshow > div:first').fadeIn(1000); } );
      }, 3000);

      // LightGallery
      $("body").lightGallery({
	zoom: true,
	selector: 'a#lightgallery',
	selectWithin: 'body'
      });
    });
  </script>
