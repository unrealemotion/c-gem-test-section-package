# Shopify Section: C GEM Test Section

**Version:** 1.0.0
**Date:** 2025-04-15

## Overview

This package contains a custom Shopify section named "C GEM Test Section" (`c-gem-test.liquid`). It's designed for Online Store 2.0 themes (like Dawn) and provides a flexible way to build homepage or landing page content using pre-defined block types based on the provided HTML/CSS structure.

The section allows merchants to add and arrange different content blocks via the Shopify Theme Customizer, offering control over text, images, videos, colors, buttons, and more.

## Files Included

The zip package contains the following files in their respective theme directories:

*   `sections/c-gem-test.liquid`: The main Liquid file containing the section's HTML structure, Liquid logic, and schema definition.
*   `assets/section-c-gem-test.css`: The CSS file containing all the necessary styles for the section.

## Installation

1.  **Unzip the Package:** Extract the contents of this `.zip` file. You should see `sections` and `assets` folders.
2.  **Access Theme Code:** Log in to your Shopify admin, go to **Online Store > Themes**. Find the theme you want to edit, click **Actions > Edit code**.
3.  **Upload CSS:** In the theme code editor, find the `assets` directory. Click **Add a new asset** and upload the `section-c-gem-test.css` file from the unzipped package's `assets` folder.
4.  **Upload Liquid Section:** In the theme code editor, find the `sections` directory. Click **Add a new section**, name it exactly `c-gem-test` (the `.liquid` extension will be added automatically), and click **Done**. Delete the default code within the newly created file and **paste the entire content** of the `c-gem-test.liquid` file (from the unzipped package's `sections` folder) into it.
5.  **Save:** Click **Save** in the code editor.

## How to Use

1.  **Navigate to Theme Editor:** Go to **Online Store > Themes** and click **Customize** on the theme where you installed the section.
2.  **Add the Section:** Navigate to the page template where you want to add the section (e.g., Homepage). In the left-hand sidebar, click **Add section** and search for or scroll to find **"C GEM Test Section"**. Click on it to add it to the page.
3.  **Configure Blocks:**
    *   Once the section is added, you will see options to **Add block**.
    *   Choose from the available block types: "Features Showcase", "Content with Stats", or "Alternating Media Rows".
    *   Add as many blocks as needed (up to the section's `max_blocks` limit, currently 10).
    *   Click on each added block in the sidebar to expand its settings.
    *   Customize the text, images, colors, links, and other options provided for each block.
4.  **Reorder Blocks:** You can drag and drop the blocks in the sidebar to change their vertical order on the page.
5.  **Save Changes:** Click **Save** in the Theme Editor.

## Section Architecture

This section (`c-gem-test.liquid`) utilizes Shopify's block-based architecture. Instead of being multiple separate sections, it acts as a container where different types of content layouts ("blocks") can be added.

*   **Single Section File:** All layout variations are managed within this single section file and its associated CSS.
*   **Block-Based Design:** The section defines multiple `block` types in its schema. Merchants can add instances of these blocks in the Theme Customizer.


### Block Types

1.  **`features_with_image` ("Features Showcase")**
    *   **Purpose:** Displays a central heading, two columns of feature items flanking a central image, followed by a call-to-action button, guarantee text/icon, and payment icons.
    *   **Layout:** Three columns on desktop (Features L, Image, Features R), stacked vertically on mobile.
    *   **Key Settings:** Main Heading, Center Image, Feature Items (Icon, Title, Description - up to 4), Button (Label, Link, Colors), Guarantee (Icon, Text), Payment Icons (up to 5).

2.  **`content_with_stats` ("Content with Stats")**
    *   **Purpose:** Displays a block of text content (heading, description) alongside key statistics/points, paired with a large image and a call-to-action button.
    *   **Layout:** Two columns on desktop (Text/Stats, Image), stacked vertically on mobile.
    *   **Key Settings:** Background Color, Heading, Description (Rich Text), Main Image, Key Points Title, Key Points (Statistic, Text - up to 3), Statistic Color, Button (Label, Link, Colors).

3.  **`alternating_media_rows` ("Alternating Media Rows")**
    *   **Purpose:** Creates two distinct content rows, each featuring a media element (image or video) and a text block (heading, description). The layout alternates the position of the media and text between the two rows on desktop.
    *   **Layout:** Two full-width rows. Each row is two columns on desktop (Media/Text, then Text/Media), stacked vertically on mobile.
    *   **Key Settings (per row):** Heading, Description (Rich Text), Media Type (Image, Video URL, Shopify Video), Image Picker, Video URL input, Shopify Video Picker.

## Key Features & Settings

*   **Highly Customizable:** Most text content, images, icons, and button links/labels are editable via the Theme Customizer.
*   **Color Control:** Background colors and button colors are configurable for relevant blocks.
*   **Media Flexibility:** Supports images, YouTube/Vimeo video URLs, and Shopify-hosted videos in the "Alternating Media Rows" block.
*   **Responsive Design:** Styles include basic responsive adjustments for common breakpoints, adapting layouts for mobile, tablet, and desktop views.
*   **Placeholders:** Uses Shopify's placeholder system for images and icons when no content is selected, aiding in setup.
*   **Defaults:** Schema settings include default text and colors based on the original static design, making initial setup quicker.

## Dependencies

*   **CSS:** This section requires the `section-c-gem-test.css` file to be present in the theme's `assets` folder and correctly linked within the `c-gem-test.liquid` file. This CSS file is included in the package.
*   **Fonts:** The CSS uses the 'Inter Tight' font via Google Fonts, assuming it's loaded globally by the theme or relies on browser defaults if not available. Ensure your theme loads this font if strict adherence to the original typography is required.

## Compatibility

*   Designed for Shopify Online Store 2.0 themes.
*   Requires themes that utilize JSON templates for section inclusion via the Theme Editor.

---

*This README provides guidance for installing and using the "C GEM Test Section". Please refer to the Shopify documentation for more advanced theme development concepts.*