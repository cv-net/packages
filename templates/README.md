# datadesk/packages

All of our open-source software packages. Also available as [a CSV file](packages.csv).

| slug | distributor | ci | maintained |
|:--|:--|:--|:--|{% for obj in object_list %}
|  [{{ obj.slug }}](https://www.github.com/{{ obj.repo }}) | {% if obj.pypi %}[![PyPI version](https://img.shields.io/pypi/v/{{ obj.pypi }}.svg)](https://pypi.org/project/{{ obj.pypi }}){% endif %} | {% if obj.travisci %}[![Build Status](https://travis-ci.org/{{ obj.travisci }}.png?branch=master)](https://travis-ci.org/{{ obj.travisci }}){% endif %} | {% if obj.is_maintained == 'TRUE' %}👍{% else %}👎{% endif %} |{% endfor %}
