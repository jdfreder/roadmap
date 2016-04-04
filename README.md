# Project Jupyter Roadmap

The following is a very rough outline of the roadmap for Project Jupyter and IPython.
Historically, we have published major releases every 6-9 months. With our project now
split across many subprojects, we expect to release subprojects separately and more
often.

This roadmap only includes mainline subprojects under the Jupyter
(https://github.com/jupyter) and IPython (https://github.com/ipython) GitHub orgs. We
also have a number of newer, experimental subprojects in the Jupyter Incubator
(https://github.com/jupyter-incubator) organization.

In this roadmap, we refer to the future major releases as follows:

* Next (the next major release)
* Next+1 (the major release after that)
* Future (any release beyond the Next+1)

This reflects the inherent uncertainty in releases that are more than about 1 year away. In
some cases, if progress is made more quickly, features may be moved to earlier releases.

## Documentation

We list documentation as a top-level section in our roadmap to acknowledge the importance
of it for developer communication, scaling and maintenance of deployments, and early user
adoption of new releases. The state of the existing documentation has not kept pace with
the rapid development in our projects, and effort will be focused on improving it. Because
our documentation spans all subprojects, each of which have their own release cycles and
versioning, the documentation roadmap doesn't have concrete version numbers associated with
each milestone.

### Next

* Hire full time and part time staff who will focus on improving our documentation.
* Research existing tools for writing documentation (Readthedocs, Sphinx, Notebooks, etc.)
  and evaluate which tools we use to write documentation.
* Develop a project wide outline of our existing and proposed documentation.
* Perform observational and survey based user studies of our documentation to guide its
  design and development.
* Explore and research the questions around how to maintain documentation across multiple
  subprojects. Do we centralize all or some of our documentation? Do we keep it in separate
  subproject repos?
* Build publicly accessible API documentation on all commits for all JavaScript and
  TypeScript repositories.
* Encode documentation in our project principles and community process as a core activity
  that is part of the everyday process of development, and adopt this in an integral
  fashion throughout the project for all project members.

### Next+1

* Integrate Jupyter Notebooks more closely into our documentation tools.
* Develop a formal documentation process and standard that includes technical review,
  organizational review, design, usability testing and copy-editing.* Where needed, develop
  additional tools for writing our documentation.
* Work with each subproject to integrate our documentation tools and process into their
  workflow and roadmap.

### Future

* Begin to block releases of subprojects until documentation meets our standards.
* Using our new JavaScript packages and live kernels hosted in the cloud, enable
  documentation to be runnable in place.
* Build documentation indexing and search into the Jupyter Workbench.
* Build tools that make it easier for downstream projects to distribute notebook based
  documentation to users.

## Notebook

### Next (4.1)

* Multi-cell selection and actions.
* Notebook wide find and replace.
* Command palette.
* Restart kernel and run all.

### Next+1 (5.0)

* Prototype of the *Jupyter Workbench*:
  - Initially, a new page in the existing notebook web-app that allows multiple
    plugins in the same browser tab.
  - Flexible, customizable tabbed and paneled layout system.
  - Initial plugins:
    - Menu bar.
    - Overall page layout.
    - File browser.
    - Text editor.
    - Terminal.
* All new frontend work is being done as small, loosely coupled npm packages.
* The entire Jupyter Workbench will be a set of plugins (again just npm packages)
  that exchange runtime APIs.
* Application infrastucture (keyboard shortcuts, commands, menus, layout), view
  layer, and other utilities (signals, properties, messages) provided by phosphorjs
  (http://phosphorjs.github.io/).
* Here is a list of all the repositories in which we are developing the Jupyter Workbench:
  - https://github.com/jupyter?utf8=%E2%9C%93&query=jupyter-js
* Movement towards having stable, documented JavaScript APIs.
* Usability and UX User survey to help us guide the design process of the Jupyter Workbench.
* Ability to hide/show code and entire cells based on query syntax.

### Next+2

* New plugins for the Jupyter Workbench:
  - Standalone output area.
  - Ability to hook kernels up to text editors and output areas.
  - Themes.

### Future

* New plugins for the Jupyter Workbench:
  - Notebook.
  - Variable inspector.
  - UI for managing plugins.
* Dashboarding of output areas and interactive widgets.
* If, and only if, the Jupyter Workbench becomes a full replacement, deprecate existing pages in the notebook
  web-application.
* Real-time collaboration on the notebook, text editor, and other plugins.
* Perform and publish accesibility audit by running an automated tool.
* Bring our core plugins up to the level of the Web Accessibility Standards
  (http://www.w3.org/standards/webdesign/accessibility)

## ipywidgets

### Next (5.0)

* Improved and consistent visual style of built-in widgets.
* Better abstractions for styling widgets using CSS and doing layout with flexbox.
* Ability to run ipywidgets outside of the notebook.
* Use npm for packaging the JavaScript code as `jupyter-js-widgets`.
* Use the new notebook nbextension mechanism, introduced in Jupyter notebook 4.2
  for the widgetsnbextension package, which will contain all of the notebook
  specific widget Javascript.
* Include two mechanisms for exporting widgets to static formats, rasterized
  screencaptures of the widgets and an embed widget manager which is capable of
  rendering widgets outside of the notebook.
* Add examples for using the widgets outside of the notebook.
* Add narrative docs describing the widgets basic usage and low level widget
  spec information.

### Future

* Treat widgets as regular output, and not have to have a separate widget area
  in the DOM.
* Transition to ES6/TypeScript.
* Remove dependency on jQuery, jQuery UI, and bootstrap.
* Integrate existing widgets with JupyterLab.
* Explore mechanisms to allow Phosphor views to be used directly with
  jupyter-js-widget models.
* Integrate framework/foundation classes of the Declaritive Widget incubator
  directly into jupyter-js-widgets and ipywidgets.
* Evaluate and possibly transition the codebase to use modern Javascript
  standards.  Linting tools (i.e. eslint) should be used to assist developers
  into complying to said standard.
* Shrink the jupyter-js-widgets codebase using well adopted Javascript libraries
  installed via npm.
* Give the widgets a facelift.  Maybe material-ui?  Home spun design?
* Add more synchronized events.  In the process, investigate slicker ways to do
  cross context event synchronization.

## traitlets

### Next (4.1)

* Much nicer, decorator based APIs for observing (`@observe`), validating
  (`@validate) and providing defaults (`@default) for traits.
* Looking forward to its usage in Matplotlib.

## nbconvert

### Next

* Bring examples of nbconvert functionality that exists in locations like @takluyver's
  demos from last summer's Southampton workshop into the official docs.

### Future

* Explore implementing nbconvert using Pandoc extensions.
* Explore implementing the html output of nbconvert using node.js and the various npm packages we are creating to avoid reimplementing all of the HTML logic.
* Implement an exporter for EPUB.

## JupyterHub

## Deployment

## IPython

## nbgrader

## nbviewer

## Notebook document

## Message specification
