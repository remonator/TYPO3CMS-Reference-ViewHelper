.. include:: ../../../../Includes.txt

================
format.urlencode
================


Encodes the given string according to http://www.faqs.org/rfcs/rfc3986.html (applying PHPs rawurlencode() function)
Note: The output is not escaped. You may have to ensure proper escaping on your own.

= Examples =

<code title="default notation">
</code>
<output>
foo%20%40%2B%25%2F (rawurlencode() applied)
</output>

<code title="inline notation">
{text -> f:format.urlencode()}
</code>
<output>
Url encoded text (rawurlencode() applied)
</output>

Arguments
=========


value (string)
--------------


string to format