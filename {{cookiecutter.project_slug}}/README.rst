{% set is_open_source = cookiecutter.open_source_license != 'Not open source' -%}
{% for _ in cookiecutter.project_name %}={% endfor %}
{{ cookiecutter.project_name }}
{% for _ in cookiecutter.project_name %}={% endfor %}

{% if is_open_source %}
.. image:: https://img.shields.io/pypi/v/{{ cookiecutter.github_repo }}.svg
        :target: https://pypi.python.org/pypi/{{ cookiecutter.github_repo }}

.. image:: https://img.shields.io/travis/{{ cookiecutter.github_username }}/{{ cookiecutter.github_repo }}.svg
        :target: https://travis-ci.com/{{ cookiecutter.github_username }}/{{ cookiecutter.github_repo }}

.. image:: https://readthedocs.org/projects/{{ cookiecutter.github_repo }}/badge/?version=latest
        :target: https://{{ cookiecutter.github_repo }}.readthedocs.io/en/latest/?version=latest
        :alt: Documentation Status
{%- endif %}

{% if cookiecutter.add_pyup_badge == 'y' %}
.. image:: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.github_repo }}/shield.svg
     :target: https://pyup.io/repos/github/{{ cookiecutter.github_username }}/{{ cookiecutter.github_repo }}/
     :alt: Updates
{% endif %}


{{ cookiecutter.project_short_description }}

{% if is_open_source %}
* Free software: {{ cookiecutter.open_source_license }}
* Documentation: https://{{ cookiecutter.github_repo }}.readthedocs.io.
{% endif %}

Features
--------

* TODO

Credits
-------

This package was created with Cookiecutter_ and the `unixnut/cookiecutter-pypackage`_ project template.

.. _Cookiecutter: https://github.com/audreyr/cookiecutter
.. _`unixnut/cookiecutter-pypackage`: https://github.com/unixnut/cookiecutter-pypackage
