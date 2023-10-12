# DjangoProject
A record of studying Django and Python based on codeit site and book Jump to Django

In Django, each function of the web service is implemented on an app-by-app basis. It's a collection of apps that have different functions and make them into one project. In fact, one project consists of multiple apps and some setup files, and one app can be used for multiple projects.

### Django App Structure
- {app_name}/
-     __init__.py
-     admin.py
-     apps.py
-     migrations/
-         __init__.py
-     models.py
-     tests.py
-     views.py

### render( )
render( request, template_name, context=None, content_type=None, status=None, using=None )

Required arguments
- request
- template_name

Optional arguments
- context
- content_type
- status
- using

### Architecture Pattern
  ##### 1. Layered pattern
  ##### 2. Client-server pattern
  ##### 3. Master-slave pattern
  ##### 4. Pipe-filter pattern
  ##### 5. Broker pattern
  ##### 6. Peer-to-peer pattern
  ##### 7. Event-bus pattern
  ##### 8. Model-View-Controller pattern
         MVC               MVT  (Django)
         Model       ->    Model
         View        ->    Template
         Controller  ->    View
  ##### 9. Blackboard pattern
  ##### 10. Interpreter pattern

## Template Language
  ### Template Variable
         {{ variable }}
         user = {"name" : "sumi", "coffee" : True}
         
  ### Template Filter
         {{ variable|filter }}
         {{ variable|filter:args }}

  ##### default
        {{ variable|default:"coffee" }} 

  ##### capfirst
        {{ variable|capfirst }}

  ##### random
        {{ variable|random }}

  ##### upper & lower
        {{ variable | upper }} , {{ variable | lower }}

  ##### ljust & rjust
        {{ variable|ljust:"length" }}, {{ variable|rjust:"length" }}

## Template Tag
      {% tag %}
      {% tag %} ~ {% endtag %}

##### for
      {% for obj in values %} ~ {% endfor %}

      {% for food in foods %} 
         <li> {{ food.name }} </li>
      {% endfor %}

      {% for food in foods reversed %} 
         <li> {{ food.name }} </li>
      {% endfor %}

      {% for food in foods %} 
         <li> {{ food.name }} </li>
      {% empty %}
         <li> There is no food. </li>
      {% endfor %}



