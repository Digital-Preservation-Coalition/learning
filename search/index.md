---
title: Search
---


<div id="search"></div>


<script src="{{ '/_pagefind/pagefind-ui.js' | relative_url }}" type="text/javascript"></script>
<script>
    window.addEventListener('DOMContentLoaded', (event) => {
        new PagefindUI({ 
            element: "#search",
            openFilters: ['Kind','Skill']
         });
    });
</script>
