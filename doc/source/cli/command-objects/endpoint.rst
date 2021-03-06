========
endpoint
========

Identity v2, v3

endpoint add project
--------------------

Associate a project to an endpoint for endpoint filtering

.. program:: endpoint add project
.. code:: bash

    openstack endpoint add project
        [--project-domain <project-domain>]
        <endpoint>
        <project>

.. option:: --project-domain <project-domain>

    Domain the project belongs to (name or ID).
    This can be used in case collisions between project names exist.

.. _endpoint_add_project-endpoint:
.. describe:: <endpoint>

    Endpoint to associate with specified project (name or ID)

.. _endpoint_add_project-project:
.. describe:: <project>

    Project to associate with specified endpoint (name or ID)

endpoint create
---------------

Create new endpoint

*Identity version 2 only*

.. program:: endpoint create (v2)
.. code:: bash

    openstack endpoint create
        --publicurl <url>
        [--adminurl <url>]
        [--internalurl <url>]
        [--region <region-id>]
        <service>

.. option:: --publicurl <url>

    New endpoint public URL (required)

.. option:: --adminurl <url>

    New endpoint admin URL

.. option:: --internalurl <url>

    New endpoint internal URL

.. option:: --region <region-id>

    New endpoint region ID

.. _endpoint_create-endpoint:
.. describe:: <service>

    Service to be associated with new endpoint (name or ID)

*Identity version 3 only*

.. program:: endpoint create (v3)
.. code:: bash

    openstack endpoint create
        [--region <region-id>]
        [--enable | --disable]
        <service>
        <interface>
        <url>

.. option:: --region <region-id>

    New endpoint region ID

.. option:: --enable

    Enable endpoint (default)

.. option:: --disable

    Disable endpoint

.. describe:: <service>

    Service to be associated with new endpoint(name or ID)

.. describe:: <interface>

    New endpoint interface type (admin, public or internal)

.. describe:: <url>

    New endpoint URL

endpoint delete
---------------

Delete endpoint(s)

.. program:: endpoint delete
.. code:: bash

    openstack endpoint delete
        <endpoint-id> [<endpoint-id> ...]

.. _endpoint_delete-endpoint:
.. describe:: <endpoint-id>

    Endpoint(s) to delete (ID only)

endpoint list
-------------

List endpoints

.. program:: endpoint list
.. code:: bash

    openstack endpoint list
        [--service <service>]
        [--interface <interface>]
        [--region <region-id>]
        [--long]
        [--endpoint <endpoint> |
        --project <project> [--project-domain <project-domain>]]

.. option:: --service <service>

    Filter by service (type, name or ID)

    *Identity version 3 only*

.. option:: --interface <interface>

    Filter by interface type (admin, public or internal)

    *Identity version 3 only*

.. option:: --region <region-id>

    Filter by region ID

    *Identity version 3 only*

.. option:: --long

    List additional fields in output

    *Identity version 2 only*

.. option:: --endpoint

    List projects that have access to that endpoint using
    endpoint filtering

    *Identity version 3 only*

.. option:: --project

    List endpoints available for the project using
    endpoint filtering

    *Identity version 3 only*

.. option:: --project-domain

    Domain the project belongs to (name or ID).
    This can be used in case collisions between project names exist.

    *Identity version 3 only*

endpoint remove project
-----------------------

Dissociate a project from an endpoint.

.. program:: endpoint remove project
.. code:: bash

    openstack endpoint remove project
        [--project-domain <project-domain>]
        <endpoint>
        <project>

.. option:: --project-domain <project-domain>

    Domain the project belongs to (name or ID).
    This can be used in case collisions between project names exist.

.. _endpoint_remove_project-endpoint:
.. describe:: <endpoint>

    Endpoint to dissociate with specified project (name or ID)

.. _endpoint_remove_project-project:
.. describe:: <project>

    Project to dissociate with specified endpoint (name or ID)

endpoint set
------------

Set endpoint properties

*Identity version 3 only*

.. program:: endpoint set
.. code:: bash

    openstack endpoint set
        [--region <region-id>]
        [--interface <interface>]
        [--url <url>]
        [--service <service>]
        [--enable | --disable]
        <endpoint-id>

.. option:: --region <region-id>

    New endpoint region ID

.. option:: --interface <interface>

    New endpoint interface type (admin, public or internal)

.. option:: --url <url>

    New endpoint URL

.. option:: --service <service>

    New endpoint service (name or ID)

.. option:: --enable

    Enable endpoint

.. option:: --disable

    Disable endpoint

.. _endpoint_set-endpoint:
.. describe:: <endpoint-id>

    Endpoint to modify (ID only)

endpoint show
-------------

Display endpoint details

.. program:: endpoint show
.. code:: bash

    openstack endpoint show
        <endpoint>

.. _endpoint_show-endpoint:
.. describe:: <endpoint>

    Endpoint to display (endpoint ID, service ID, service name, service type)
