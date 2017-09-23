.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

matchAll()
==========

This function is used to apply a regular expression to a piece of text,
and return a list of matching groups (elements found inside parentheses)
as a two-dimensional String array. If there are no matches, a null value
will be returned. If no groups are specified in the regular expression,
but the sequence matches, a two dimensional array is still returned, but
the second dimension is only of length one.

To use the function, first check to see if the result is null. If the
result is null, then the sequence did not match at all. If the sequence
did match, a 2D array is returned.

If there are groups (specified by sets of parentheses) in the regular
expression, then the contents of each will be returned in the array.
Assuming a loop with counter variable i, element [i][0] of a regular
expression match returns the entire matching string, and the match groups
start at element [i][1] (the first group is [i][1], the second [i][2],
and so on).

**รูปแบบการใช้งาน**

matchAll ( str, regexp )

**พารามิเตอร์**

- ``str``  : the String to be searched

- ``regexp``  : the regexp to be used for matching


.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var string = "Hello p5js*! Hello world!"
	var regexp = "Hello"
	matchAll(string, regexp);
	</script>

	<br><br>

.. toctree::

