---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<div class="row align-items-center my-5">
	<div class="col-md-7">
		<h1 class="display-4">Welcome to {{ site.title }}</h1>
		<p class="lead">Your new Jekyll blog is now responsive and powered by Bootstrap. Edit this page to customize your home page content.</p>
		<a href="/about.html" class="btn btn-primary btn-lg mt-3">Learn More</a>
	</div>
	<div class="col-md-5 text-center">
		<img src="https://getbootstrap.com/docs/5.3/assets/brand/bootstrap-logo-shadow.png" alt="Bootstrap Logo" class="img-fluid" style="max-height:200px;">
	</div>
</div>

<div class="row">
	<div class="col-12">
		<h2>Latest Posts</h2>
		<ul class="list-group list-group-flush">
			{% for post in site.posts limit:5 %}
				<li class="list-group-item">
					<a href="{{ post.url }}">{{ post.title }}</a>
					<small class="text-muted">{{ post.date | date: "%B %d, %Y" }}</small>
				</li>
			{% endfor %}
		</ul>
	</div>
</div>
