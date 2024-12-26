<div class="container">
    <div id = "{{alum.name | replace: ' ', '-'}}" class="row" style="padding-top: 60px; margin-top: -60px;">
      <img style="float: left; height: 15%; width: 15%; border-radius: 50%;" src="{{ alum.image | prepend: '/assets/img/' | prepend: site.baseurl | prepend: site.url }}" alt="photo of {{alum.name}}">
    <div class="col-sm-10" >
        <b>{{alum.name}}{% if alum.degrees %}, {{alum.degrees}} {% endif %}</b>
        {{alum.position}}<br>
        {% if alum.website %}
          <i class="fa fa-globe"></i> <a href= "{{alum.website}}" target="_blank">{{alum.website}}<br></a>
        {% endif %}
        <i>previously:</i> {{alum.previously}} <br>
        <i>now:</i> {{alum.now}}
        <p class="text-justify">{{alum.description | markdownify}}</p>

</div>
</div>
</div>
<hr>