
Sunshine Smarthome document
============================

This is repository of Smarthome's document

To build document, following instruction below

#. Install **poetry**

    .. code-block:: bash

      pip install --user poetry
    
    .. note:: 
    
      Other installation mehtod at `Poetry doc <https://python-poetry.org/docs/>`_
    
#. Install requirement packages

    .. code-block:: bash

      poetry install

#. Build document to HTML

    .. code-block:: bash

      make html

    Result of the command will in ``_build`` folder