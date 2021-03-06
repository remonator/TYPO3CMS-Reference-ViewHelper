.. include:: ../../../../Includes.txt

=============
format.printf
=============


A view helper for formatting values with printf. Either supply an array for
the arguments or a single value.
See http://www.php.net/manual/en/function.sprintf.php

= Examples =

<code title="Scientific notation">
<f:format.printf arguments="{number: 362525200}">%.3e</f:format.printf>
</code>
<output>
3.625e+8
</output>

<code title="Argument swapping">
<f:format.printf arguments="{0: 3, 1: 'Kasper'}">%2$s is great, TYPO%1$d too. Yes, TYPO%1$d is great and so is %2$s!</f:format.printf>
</code>
<output>
Kasper is great, TYPO3 too. Yes, TYPO3 is great and so is Kasper!
</output>

<code title="Single argument">
<f:format.printf arguments="{1: 'TYPO3'}">We love %s</f:format.printf>
</code>
<output>
We love TYPO3
</output>

<code title="Inline notation">
{someText -> f:format.printf(arguments: {1: 'TYPO3'})}
</code>
<output>
We love TYPO3
</output>

Arguments
=========


value (string)
--------------


String to format

arguments (anySimpleType)
-------------------------


Default: array ()

The arguments for vsprintf