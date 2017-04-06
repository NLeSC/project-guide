# Tutorial

In addition to good documentation having a good tutorial is very important.

To be clear on what is meant with a tutorial in this context:

> A self-paced interactive document or website, where the user follows on-screen instructions to learn how to use a piece of software.

Jupyter Notebooks appear to be the de facto standard for creating tutorials like this. There is also R Notebooks and Beaker Notebooks, use whichever is the most applicable for your software.

> GitHub automatically detects the programming languages used in your repository. If you have Jupyter Notebooks in your repository this will affect the linguistic analysis. You can mark the notebooks as being part of the documentation by using a `.gitattributes` file (see https://github.com/github/linguist).

The guidelines for creating tutorials for your software are:

 * Assume the user knows the purpose of the software. The user has already found your software and probably read the README before clicking on your tutorial. The tutorial is about how to learning how to use the software.

 * The tutorial should run ‘out-of-the-box’, required software and data should be readily available.

 * Use a concrete example use-case that relates to the intended audience. If you have multiple intended audiences, it's a good idea to create multiple tutorials. Also, it is better to have several tutorials instead of one extremely long one.

 * The user should be able to work through the tutorial in their own pace. It is fine to have short instruction videos as a supplement to the text.

 * Integrate the tutorial with the documentation website of the software and make sure this is easy to find. This way you increase the chances of users finding both your documentation and tutorial as well as gather all the usage documentation in one place.
  > If you are using sphinxdocs for building your documentation websites, you can use nbsphinx (https://nbsphinx.readthedocs.io) to embed your tutorial into your documentation pages.

