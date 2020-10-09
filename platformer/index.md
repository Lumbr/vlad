<!DOCTYPE html>
<html lang="{{ site.lang | default: "en-US" }}">
  <head>
    <meta charset='utf-8'>
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="{{ '/assets/css/style.css?v=' | append: site.github.build_revision | relative_url }}">

{% seo %}
  </head>

  <body>
    <header>
      <div class="container">
        <a id="a-title" href="{{ '/' | relative_url }}">
          <h1>{{ Vlad | default: site.github.vlad }}</h1>
        </a>
        <h2>{{ this site is very cool | default: site.github.project_tagline }}</h2>
        <section id="downloads">
          {% if site.show_downloads %}
            <a href="{{ site.github.zip_url }}" class="btn">Download as .zip</a>
            <a href="{{ site.github.tar_url }}" class="btn">Download as .tar.gz</a>
          {% endif %}
          <a href="{{ site.github.repository_url }}" class="btn btn-github"><span class="icon"></span>View on GitHub</a>
        </section>
      </div>
    </header>
    <link rel="shortcut icon" href="TemplateData/favicon.ico">
    <link rel="stylesheet" href="TemplateData/style.css">
    <script src="TemplateData/UnityProgress.js"></script>
    <script src="/Build/UnityLoader.js"></script>
    <script>
      var unityInstance = UnityLoader.instantiate("unityContainer", "Build/Webgl.json", {onProgress: UnityProgress});
    </script>
    <div class="container">
      <section id="main_content">
        <div class="webgl-content">
          <div id="unityContainer" style="width: 960px; height: 600px"></div>
          <div class="footer">
            <div class="webgl-logo"></div>
            <div class="fullscreen" onclick="unityInstance.SetFullscreen(1)"></div>
            <div class="title">MyFirstGame</div>
          </div>
        </div>
      </section>
    </div>
    {% if site.google_analytics %}
      <script>
        (function(i,s,o,g,r,a,m){i['GoogleAnalyticsObject']=r;i[r]=i[r]||function(){
        (i[r].q=i[r].q||[]).push(arguments)},i[r].l=1*new Date();a=s.createElement(o),
        m=s.getElementsByTagName(o)[0];a.async=1;a.src=g;m.parentNode.insertBefore(a,m)
        })(window,document,'script','//www.google-analytics.com/analytics.js','ga');
        ga('create', '{{ site.google_analytics }}', 'auto');
        ga('send', 'pageview');
      </script>
    {% endif %}
  </body>
</html>
