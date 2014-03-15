Preface to Stanford Notes
=========================

To confirm theming works, use the repository and version mechanisms as outlined in
[build-version.yml gist](https://gist.github.com/yarko/8818633).
Replace the GIT_ACCT and THEME_ACCT with your github account names,
using with the `edx_platform_version` of your `edx_platform_repo`.
Be sure you or the baseline you've started from has merged pull request #2387 from `edx/edx-platform`.

Once you have confirmed basic theming using the canonical Stanford theme,
it's recommended you make a branch and affect your theme changes there.
Update the `edxapp_theme_version` variable in your `build-version.yml` as appropriate,
and re-provision.

To effect the same on a deployment, you can follow the general instructions
[configuring-themes-in-devstack](https://github.com/edx/edx-platform/wiki/Developing-on-the-edX-Developer-Stack#configuring-themes-in-devstack),
modified by guidance from
[compile-assets-manually](https://github.com/edx/configuration/wiki/edX-Managing-the-Production-Stack#compile-assets-manually).

To affect homepage video, see `edx-platform/lms/templates/index.html`
(search for section id `video_modal`).
Note: to change this, copy the modified `index.html` to the same relative file space in your theme.

Overview
========
This directory stores Stanford's theming files for its edX instance.
We're storing the stuff here and then pulling it in to our instance
when we deploy.

We've organized the tree to mimic the directory structure of the edX
codebase so that it's easy to tell where the files will end up upon
deploy. We'll use a special settings file to set the template and
staticfiles paths properly to point to these files.

Theme Authoring
===============
The proposed theming solution for edX (see [this pull](https://github.com/edx/edx-platform/pull/1907)
for more details) provides a number of hooks for themes to adjust
both HTML and CSS to their liking.


License
=======

The code in this repo is licensed under the Apache 2.0 License.
See [LICENSE.txt](LICENSE.txt) for more info.  The copyright for the Stanford
brands and assets (e.g. logo and images) are held by Stanford
University.

