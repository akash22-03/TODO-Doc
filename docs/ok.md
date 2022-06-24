<div id="swagger-ui" data-url="swagger.yaml">

</div>

<link rel="stylesheet" type="text/css" href="https://unpkg.com/swagger-ui-dist@3/swagger-ui.css" />

<script src="https://unpkg.com/swagger-ui-dist@3/swagger-ui-bundle.js"> 

</script>

<script> 
    window.onload = function() {
        window.ui = SwaggerUIBundle({
        url: "./TODO.yaml",
        dom_id: '#swagger-ui',
        });
    };
</script>