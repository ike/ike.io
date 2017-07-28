# Hire Isaac

If you tell me about your project, there's a good chance that I'll think it's the best thing since HTTP. I work on a large variety of projects in a large variety of roles, and I'd love to see if there's a way I can help you make your dreams a reality.

Some of the things I'm great at:

- front-end web development
- project management and making hard problems simpler
- business planning, development
- event design/coordination
- market research
- music production/promotion
- general dreaming and "omg we could totally do that"

### Folks I've worked with:

<a href="http://wild.land" target="_blank"><img src="img/wildland.svg" class="logos"/></a>
<a href="http://andyet.com" target="_blank"><img src="img/andyet.svg" class="logos"/></a>
<a href="http://www.dougwaltman.com/" target="_blank"><img src="img/dw2.svg" class="logos"/></a>
<a href="http://cgcc.edu" target="_blank"><img src="img/cgcc.png" class="logos"/></a>
<a href="http://hireelectric.com" target="_blank"><img src="img/hire-electric.svg" class="logos"/></a>

* * *

<form id="hire-form" action="http://formspree.io/isaac@ike.io" method="POST">
	<h2>Let's talk!</h2>
	<div class="row">
		<input type="text" name="name" class="col c4 hire-form-input" id="hire-name" placeholder="Full name*" required />
		<input type="email" name="email" class="col c4 hire-form-input" id="hire-email" placeholder="Email address*" required />
	</div>
	<div class="row">
		<div id="hire-timeline" class="col c4">
			<label for="timeline" id="hire-timeline-label">Estimated Timeline\*:</label><br>
			<select name="timeline" class="hire-form-input" id="hire-timeline" required>
				<option>1 week</option>
				<option>1 Month</option>
				<option>6 Months</option>
				<option>1 Year</option>
				<option>Ongoing or not sure</option>
			</select>
		</div>
		<div id="hire-budget" class="col c4">
			<label for="budget" id="hire-budget-label">Budget\*:</label><br>
			<select name="budget" class="hire-form-input" id="hire-budget" required>
				<option>$1,000-$5,000</option>
				<option>$5,000-$10,000</option>
				<option>$10,000-$25,000</option>
				<option>$25,000+</option>
				<option>Not sure</option>
			</select>
		</div>
	</div>
	<div class="row">
		<textarea placeholder="Tell me about your project*" class="col c8 hire-form-input" name="project-description" rows="5" id="hire-comment"></textarea>
	</div>
	<input type="text" name="_gotcha" style="display:none" />
	<input type="hidden" name="_next" value="//ike.io/thanks.html" />
	<button class="btn btn-b btn-sm form-button" type="submit">submit</button>
</form>
