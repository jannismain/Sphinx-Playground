.. This is a comment. Note how any initial comments are moved by
   transforms to after the document title, subtitle, and docinfo.

.. demo.rst from: http://docutils.sourceforge.net/docs/user/rst/demo.txt

.. |EXAMPLE| image:: _demo/lines.jpg
   :width: 1em

**********************
Paragraph Level Markup
**********************

.. contents:: Table of Contents

Inline Markup
=============

Paragraphs contain text and may contain inline markup: *emphasis*, **strong emphasis**, ``inline literals``,
standalone hyperlinks (http://www.python.org), external hyperlinks (Python_), internal cross-references (example_),
external hyperlinks with embedded URIs (`Python web site <http://www.python.org>`__), footnote references
(manually numbered [1]_, anonymous auto-numbered [1]_, labeled auto-numbered [1]_, or symbolic [1]_),
citation references ([12]_), substitution references (|example|), and _`inline hyperlink targets`
(see Targets_ below for a reference back to here). Character-level inline markup is also possible
(although exceedingly ugly!) in *re*\ ``Structured``\ *Text*.

Also with ``sphinx.ext.autodoc``, which I use in the demo, I can link to :class:`_test_module.test.Foo`.
It will link you right my code documentation for it.

The default role for interpreted text is `Title Reference`.  Here are some explicit interpreted text roles:
a PEP reference (:PEP:`287`); an RFC reference (:RFC:`2822`); a :sub:`subscript`; a :sup:`superscript`;
and explicit roles for :emphasis:`standard` :strong:`inline` :literal:`markup`.

GUI labels are a useful way to indicate that :guilabel:`Some action` is to be taken by the user.
The GUI label should not run over ``line-height`` so as not to :guilabel:`interfere` with text from adjacent lines.

Key-bindings indicate that the read is to press a button on the keyboard or mouse,
for example :kbd:`MMB` and :kbd:`Shift-MMB`. Another useful markup to indicate a user action
is to use ``menuselection`` this can be used to show short and long menus in software.
For example, and ``menuselection`` can be seen here that breaks is too long to fit on this line.
:menuselection:`My --> Software --> Some menu --> Some sub menu 1 --> sub menu 2`.

.. DO NOT RE-WRAP THE FOLLOWING PARAGRAPH!

Let's test wrapping and whitespace significance in inline literals:
``This is an example of --inline-literal --text, --including some--
strangely--hyphenated-words.  Adjust-the-width-of-your-browser-window
to see how the text is wrapped.  -- ---- --------  Now note    the
spacing    between the    words of    this sentence    (words
should    be grouped    in pairs).``

If the ``--pep-references`` option was supplied, there should be a live link to PEP 258 here.

Math
====

This is a test. Here is an equation:
:math:`X_{0:5} = (X_0, X_1, X_2, X_3, X_4)`.
Here is another:

.. math::
    :label: This is a label

    \nabla^2 f =
    \frac{1}{r^2} \frac{\partial}{\partial r}
    \left( r^2 \frac{\partial f}{\partial r} \right) +
    \frac{1}{r^2 \sin \theta} \frac{\partial f}{\partial \theta}
    \left( \sin \theta \, \frac{\partial f}{\partial \theta} \right) +
    \frac{1}{r^2 \sin^2\theta} \frac{\partial^2 f}{\partial \phi^2}

You can add a link to equations like the one above :eq:`This is a label` by using ``:eq:``.

Meta
====

.. meta::
   :keywords: reStructuredText, demonstration, demo, parser
   :description lang=en: A demonstration of the reStructuredText
       markup language, containing examples of all basic
       constructs and many advanced constructs.

Blocks
======

Literal Blocks
--------------

Literal blocks are indicated with a double-colon ("::") at the end of
the preceding paragraph (over there ``-->``).  They can be indented::

    if literal_block:
        text = 'is left as-is'
        spaces_and_linebreaks = 'are preserved'
        markup_processing = None

Or they can be quoted without indentation::

>> Great idea!
>
> Why didn't I think of that?

Line Blocks
-----------

| This is a line block.  It ends with a blank line.
|     Each new line begins with a vertical bar ("|").
|     Line breaks and initial indents are preserved.
| Continuation lines are wrapped portions of long lines;
  they begin with a space in place of the vertical bar.
|     The left edge of a continuation line need not be aligned with
  the left edge of the text above it.

| This is a second line block.
|
| Blank lines are permitted internally, but they must begin with a "|".

Take it away, Eric the Orchestra Leader!

    | A one, two, a one two three four
    |
    | Half a bee, philosophically,
    |     must, *ipso facto*, half not be.
    | But half the bee has got to be,
    |     *vis a vis* its entity.  D'you see?
    |
    | But can a bee be said to be
    |     or not to be an entire bee,
    |         when half the bee is not a bee,
    |             due to some ancient injury?
    |
    | Singing...

Block Quotes
------------

Block quotes consist of indented body elements:

    My theory by A. Elk.  Brackets Miss, brackets.  This theory goes
    as follows and begins now.  All brontosauruses are thin at one
    end, much much thicker in the middle and then thin again at the
    far end.  That is my theory, it is mine, and belongs to me and I
    own it, and what it is too.

    -- Anne Elk (Miss)

Doctest Blocks
--------------

>>> print 'Python-specific usage examples; begun with ">>>"'
Python-specific usage examples; begun with ">>>"
>>> print '(cut and pasted from interactive Python sessions)'
(cut and pasted from interactive Python sessions)

Code Blocks
-----------

.. parsed-literal::

    # parsed-literal test
    curl -O http://someurl/release-|version|.tar-gz


.. code-block:: json
    :caption: Code Blocks can have captions.

    {
    "windows": [
        {
        "panes": [
            {
            "shell_command": [
                "echo 'did you know'",
                "echo 'you can inline'"
            ]
            },
            {
            "shell_command": "echo 'single commands'"
            },
            "echo 'for panes'"
        ],
        "window_name": "long form"
        }
    ],
    "session_name": "shorthands"
    }

Emphasized lines with line numbers
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: python
   :linenos:
   :emphasize-lines: 3,5

   def some_function():
       interesting = False
       print 'This line is highlighted.'
       print 'This one is not...'
       print '...but this one is.'

Sidebar
=======

.. sidebar:: Ch'ien / The Creative

    .. image:: _demo/lines.jpg

    *Above* CH'IEN THE CREATIVE, HEAVEN

    *Below* CH'IEN THE CREATIVE, HEAVEN

The first hexagram is made up of six unbroken lines. These unbroken lines stand for the primal power,
which is light-giving, active, strong, and of the spirit. The hexagram is consistently strong in character,
and since it is without weakness, its essence is power or energy. Its image is heaven.
Its energy is represented as unrestricted by any fixed conditions in space and is therefore conceived of as motion.
Time is regarded as the basis of this motion.
Thus the hexagram includes also the power of time and the power of persisting in time, that is, duration.

The power represented by the hexagram is to be interpreted in a dual sense in terms of its action
on the universe and of its action on the world of men. In relation to the universe, the hexagram expresses the strong,
creative action of the Deity. In relation to the human world, it denotes the creative action of the holy man or sage,
of the ruler or leader of men, who through his power awakens and develops their higher nature. [11]_

Code with Sidebar
-----------------

.. sidebar:: A code example

    With a sidebar on the right.

.. literalinclude:: ../../src/_test_module/test.py
    :language: python
    :caption: Literal includes can also have captions.
    :linenos:
    :lines: 1-40

References
==========

Footnotes
---------

.. [1] A footnote contains body elements, consistently indented by at
   least 3 spaces.

   This is the footnote's second paragraph.

Citations
---------

.. [11] This is the citation I made, let's make this extremely long so that we can tell that it doesn't follow the normal responsive table stuff.

.. [12] This citation has some ``code blocks`` in it, maybe some **bold** and *italics* too. Heck, lets put a link to a meta citation [13]_ too.

.. [13] This citation will have two backlinks.


Here's a reference to the above, [12]_, and a [11]_ citation.

Here is another type of citation: `citation`

Glossary
--------

This is a glossary with definition terms for thing like :term:`Writing`:

.. glossary::

  Documentation
     Provides users with the knowledge they need to use something.

  Reading
     The process of taking information into ones mind through the use of eyes.

  Writing
     The process of putting thoughts into a medium for other people to :term:`read <Reading>`.

Targets
-------

.. _example:

This paragraph is pointed to by the explicit "example" target.
A reference can be found under `Inline Markup`_, above. `Inline
hyperlink targets`_ are also possible.

Section headers are implicit targets, referred to by name. See
Targets_.

Explicit external targets are interpolated into references such as "Python_".

.. _Python: http://www.python.org/

Targets may be indirect and anonymous.  Thus `this phrase`__ may also
refer to the Targets_ section.

__ Targets_


Directives
==========

Contents
--------

.. contents:: :local:

These are just a sample of the many reStructuredText Directives. For others, please see:
http://docutils.sourceforge.net/docs/ref/rst/directives.html.


Centered text
-------------

You can create a statement with centered text with ``.. centered::``

.. centered:: This is centered text!

Images & Figures
----------------

Images
^^^^^^

An image directive (also clickable -- a hyperlink reference):

.. image:: _demo/lines.jpg
   :target: directives_

Figures
^^^^^^^

.. figure:: _demo/lines.jpg
   :alt: reStructuredText, the markup syntax

   A figure is an image with a caption and/or a legend:

   +------------+-----------------------------------------------+
   | re         | Revised, revisited, based on 're' module.     |
   +------------+-----------------------------------------------+
   | Structured | Structure-enhanced text, structuredtext.      |
   +------------+-----------------------------------------------+
   | Text       | Well it is, isn't it?                         |
   +------------+-----------------------------------------------+

   This paragraph is also part of the legend.

A figure directive with center alignment

.. figure:: _demo/lines.jpg
   :align: center

   This caption should be centered.

Admonitions
-----------

.. Attention:: Directives at large.

.. Caution:: Don't take any wooden nickels.

.. DANGER:: Mad scientist at work!

.. Error:: Does not compute.

.. Hint:: It's bigger than a bread box.

.. Important::
   - Wash behind your ears.
   - Clean up your room.

     - Including the closet.
     - The bathroom too.

       - Take the trash out of the bathroom.
       - Clean the sink.
   - Call your mother.
   - Back up your data.

.. Note:: This is a note.
   Equations within a note:
   :math:`G_{\mu\nu} = 8 \pi G (T_{\mu\nu}  + \rho_\Lambda g_{\mu\nu})`.

.. Tip:: 15% if the service is good.

    +---------+
    | Example |
    +=========+
    | Thing1  |
    +---------+
    | Thing2  |
    +---------+
    | Thing3  |
    +---------+

.. WARNING:: Strong prose may provoke extreme mental exertion.
   Reader discretion is strongly advised.

.. admonition:: And, by the way...

   You can make up your own admonition too.

Topics, Sidebars, and Rubrics
-----------------------------

.. sidebar:: Sidebar Title
   :subtitle: Optional Subtitle

   This is a sidebar.  It is for text outside the flow of the main
   text.

   .. rubric:: This is a rubric inside a sidebar

   Sidebars often appears beside the main text with a border and
   background color.

.. topic:: Topic Title

   This is a topic.

.. rubric:: This is a rubric

Target Footnotes
----------------

.. target-notes::

Replacement Text
----------------

I recommend you try |Python|_.

.. |Python| replace:: Python, *the* best language around

Compound Paragraph
------------------

.. compound::

   This paragraph contains a literal block::

       Connecting... OK
       Transmitting data... OK
       Disconnecting... OK

   and thus consists of a simple paragraph, a literal block, and
   another simple paragraph.  Nonetheless it is semantically *one*
   paragraph.

This construct is called a *compound paragraph* and can be produced
with the "compound" directive.

Download Links
==============

:download:`This long long long long long long long long long long long long long long long download link should be blue, normal weight text with a leading icon, and should wrap white-spaces <_demo/lines.jpg>`
