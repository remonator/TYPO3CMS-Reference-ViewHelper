.. include:: ../../../../Includes.txt

===========
format.html
===========


Renders a string by passing it to a TYPO3 parseFunc.
You can either specify a path to the TypoScript setting or set the parseFunc options directly.
By default lib.parseFunc_RTE is used to parse the string.

== Examples ==

<code title="Default parameters">
<f:format.html>foo <b>bar</b>. Some <LINK 1>link</LINK>.</f:format.html>
</code>
<output>
<p class="bodytext">foo <b>bar</b>. Some <a href="index.php?id=1" >link</a>.</p>
(depending on your TYPO3 setup)
</output>

<code title="Custom parseFunc">
<f:format.html parseFuncTSPath="lib.parseFunc">foo <b>bar</b>. Some <LINK 1>link</LINK>.</f:format.html>
</code>
<output>
foo <b>bar</b>. Some <a href="index.php?id=1" >link</a>.
</output>

<code title="Inline notation">
{someText -> f:format.html(parseFuncTSPath: 'lib.parseFunc')}
</code>
<output>
foo <b>bar</b>. Some <a href="index.php?id=1" >link</a>.
</output>

Arguments
=========


parseFuncTSPath (string)
------------------------


Default: &#039;lib.parseFunc_RTE&#039;

path to TypoScript parseFunc setup.