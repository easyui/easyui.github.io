---
layout: products
title: Products
permalink: /products/
gambar: /img/products.png
---
<!-- <section>
	<div class="container">
		<div class="row">
			<div class=" col-xs-10 col-xs-offset-1 col-lg-8 col-lg-offset-2  post-list">
				{% for post in site.posts %}
							<a class="post-link" href="{{ post.url | prepend: site.baseurl }}"><h2>{{ post.title }}</h2></a>
								<p>
									{{post.description}}
								</p>
								<span class="post-meta">{{ post.date | date: "%b %-d, %Y" }}</span>
						<hr>
				{% endfor %}

			</div>
		</div>
	</div>
</section> -->

<section id="portfolio" class="bg-light-gray">
		<div class="container">

		{% for post in site.categories['products'] %}
						<div class="col-md-4 col-sm-6 portfolio-item">

								<a href="{{ post.url | prepend: site.baseurl }}" class="portfolio-link" data-toggle="modal">
										<div class="portfolio-hover">
												<div class="portfolio-hover-content">
														<i class="fa fa-plus fa-3x"></i>
												</div>
										</div>
										<img src="{{ post.thumbnail }}" class="img-responsive img-centered" alt="">
								</a>
								<div class="portfolio-caption">
										<h4>{{ post.title }}</h4>
										<p class="text-muted">{{ post.subtitle }}</p>
								</div>
						</div>
				{% endfor %}
		</div>
</section>
