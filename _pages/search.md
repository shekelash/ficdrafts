---
layout: page
title: Search
---

<style>
	#search-container {
	    max-width: 100%;
	}

	input[type=text] {
		font-size: normal;
	    outline: none;
	    padding: 1rem;
		background: rgb(236, 237, 238);
	    width: 100%;
		-webkit-appearance: none;
		font-family: inherit;
		font-size: 100%;
		border: none;
	}
	#results-container {
		margin: .5rem 0;
	}
</style>

<!-- Html Elements for Search -->
<div id="search-container">
<input type="search" id="search-input" placeholder="Search...">
<ol id="results-container"></ol>
</div>

<!-- Script pointing to search-script.js -->
<script src="{{ site.baseurl }}/js/simple-jekyll-search.min.js" type="text/javascript"></script>

<!-- Configuration -->
<script type="text/javascript">
      window.simpleJekyllSearch = new SimpleJekyllSearch({
        searchInput: document.getElementById('search-input'),
        resultsContainer: document.getElementById('results-container'),
        json: '{{ site.baseurl }}/search.json',
        searchResultTemplate: '<li><a href="{url}?query={query}" title="{desc}">{title}</a></li>',
        noResultsText: 'No results found',
        limit: 10,
        fuzzy: false,
        exclude: ['Welcome']
      })
</script>
