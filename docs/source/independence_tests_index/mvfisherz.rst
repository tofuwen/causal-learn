.. _Missing-value Fisher-z test:

Missing-value Fisher-z test
====================================

Perform a testwise-deletion Fisher-z independence test to data sets with missing values.
With testwise-deletion, the test makes use of all data points that do not have missing values for the variables involved in the test.

(We have updated the independence test class and the usage example hasn't been updated yet. For new class, please refer to `TestCIT.py <https://github.com/cmu-phil/causal-learn/blob/main/tests/TestCIT.py>`_ or `TestCIT_KCI.py <https://github.com/cmu-phil/causal-learn/blob/main/tests/TestCIT_KCI.py>`_.)


Usage
--------
.. code-block:: python

    from causallearn.utils.cit import mv_fisherz
    p = mv_fisherz(mvdata, X, Y, condition_set)


Parameters
---------------
**mvdata**: numpy.ndarray, shape (n_samples, n_features). Data with missing value, where n_samples is the number of samples
and n_features is the number of features.

**X, Y and condition_set**: column indices of data.

Returns
----------------
**p**: the p-value of the test.
