test-domain-py-type-lookup
===========================

This tests the fix for issue #8551 where :type: and :rtype: fields 
gave false ambiguous class lookup warnings.

.. py:class:: mod.A
.. py:class:: mod.submod.A

.. py:currentmodule:: mod.submod

.. py:function:: f()

    This function should resolve type references correctly.

    :param A a: Should link to mod.submod.A (not generate ambiguous warning)
    :rtype: A