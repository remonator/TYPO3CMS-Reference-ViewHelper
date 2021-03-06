.. include:: ../../../../Includes.txt

============
format.cdata
============


Outputs an argument/value without any escaping and wraps it with CDATA tags.

PAY SPECIAL ATTENTION TO SECURITY HERE (especially Cross Site Scripting),
as the output is NOT SANITIZED!

= Examples =

<code title="Child nodes">
<f:format.cdata>{string}</f:format.cdata>
</code>
<output>
<![CDATA[(Content of {string} without any conversion/escaping)]]>
</output>

<code title="Value attribute">
<f:format.cdata value="{string}" />
</code>
<output>
<![CDATA[(Content of {string} without any conversion/escaping)]]>
</output>

<code title="Inline notation">
{string -> f:format.cdata()}
</code>
<output>
<![CDATA[(Content of {string} without any conversion/escaping)]]>
</output>

Arguments
=========


value (anySimpleType)
---------------------


The value to output