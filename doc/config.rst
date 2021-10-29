NRM Configuration/Manifest Guide
================================

Daemon Configuration
--------------------

``nrmd``'s configuration can be defined
in ``json``, ``yaml``, or `Dhall`_ formats. Admissible values are defined
via the following ``dhall`` file:

.. literalinclude:: ./configfiles/types_nrmd.dhall

Optional values are filled using defaults that can
be found in either Dhall or ``json`` format:

.. literalinclude:: ./configfiles/defaults_nrmd.dhall

.. literalinclude:: ./configfiles/defaults_nrmd.json

Attribute merging is always performed with those defaults. Example configurations
are located in the `examples`_ folder.

.. literalinclude:: ./configfiles/nrmd_control.yaml

Manifest Configuration
----------------------

Manifest files can also be defined either using Dhall, YAML, or JSON,
and are in similar formats or locations:

.. literalinclude:: ./configfiles/types_manifest.dhall

Under-specified manifests like the one in our ```workloads`` above (with missing
optional fields from the schema) fill missing values with defaults, which are located
here:

.. literalinclude:: ./configfiles/defaults_manifest.dhall

The ``dhall`` and ``dhall-to-json`` utilities are available as convenience in
this environment should you need them. Dhall is useful as a configuration language in itself:

.. literalinclude:: ./configfiles/defaults_manifest.json

.. literalinclude:: ./configfiles/manifests_perfwrap.yaml

.. _`Dhall`: https://dhall-lang.org/
.. _`examples`: https://github.com/anlsys/nrm-core/tree/master/examples
