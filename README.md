# Avada-Child-Theme

Template to build a WordPress Avada theme child theme.

## Overview

Essentially it's the out-of-the-box Avada-Child-Theme.zip content with a change to use a version number on the style.css file, to avoid caching issues, used as a baseline to create a more functional template for Avada Child Theme projects.

## Features

### Google Tag Manager support

Support for [Google Tag Manager](https://developers.google.com/tag-platform/tag-manager) code both in `<head>` and `<body>` is provided along with a [data layer](https://developers.google.com/tag-platform/devguides/datalayer) providing WordPress specific information about the current page.

Head code is added via the WordPress [`wp_head`](https://developer.wordpress.org/reference/hooks/wp_head/) hook and body code via the Avada [`avada_before_body_content`](https://avada.com/documentation/avada-hooks-actions-and-filters/#toc_How_To_Add_Code_After_The_Opening_Body) hook. There is no real harm in leaving the GTM code in place even if not using GTM, however, to disable, just deleted the relevant lines from the [`functions.php`](functions.php) file.

To configure, copy and paste the supplied GTM head code into the [`parts/gtm-head-code.html`](parts/gtm-head-code.html) file, and the body code into the [`parts/gtm-body-code.html`](parts/gtm-body-code.html) file.
