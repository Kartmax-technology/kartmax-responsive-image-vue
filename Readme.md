# KartMax Responsive Image Component

This Vue Component helps embed responsive images in your HTML and completely eliminates the practise of loading different images based on media queries
breakpoints.

# First Time Setup
- If this is the first time that you are setting up your project to install private repositories as npm package, please make sure to set up your project first.
- For setting up the project, please read the steps from [here](https://postscripts.medium.com/npm-install-packages-from-github-9ec5c6fd0058)

# Package installation

- [CRITICAL] Make sure you have access to this Github Repo in the first place.
- Open a terminal in your root folder of your project.
- Run
    ```
    npm install @Kartmax-technology/kartmax-responsive-image-vue@1.0.0
    ```
- Once the installation is complete, you shall have the package in your node modules folder.

# Usage

- Simply import the component in any of your Vue File.
    ```
    import ResponsiveImages from "node_modules/Kartmax-technology"
    ```
- This shall import the package in your Vue file.
- For rendering a responsive image, use the below snippet
```
    <ResponsiveImage
        v-bind:desktop="image_url_c+'cover/700x450/filters:quality(70)/images/men-collection.jpg'"
        v-bind:tab="image_url_c+'cover/650x480/filters:quality(70)/images/men-collection.jpg'"
        v-bind:mobile="image_url_c+'cover/650x480/filters:quality(70)/images/men-collection.jpg'"
        v-bind:default_image="image_url_c+'cover/800x750/images/men-collection.jpg'"
        v-bind:custom_width="'100%'"
        custom_class="img-fluid"
        :custom_style="'height:auto;border-radius:10px'"
    />
```

# Attributes

The component also offer certain attributes which you find helpful but is not mandatory.

- `custom_class`: This attribute can be used to pass a custom class for styling purposes.
- `custom_style`: This attribute can be used to pass a custom style to override class rules.
- `custom_width`: This attribute can be used to pass a custom width to override class based width.
- `data-src`: This attribute can be used to when using this component with image zoom plugin or slick slider in our projects.
# Author

[KartMax](https://kartmax.in/chauhansahab005) is developed by GreenHonchos, one of India’s largest 360-degree eCommerce Service Providers & Consultants. From startup brands who need a one-stop-shop cart to large enterprises of international repute looking for scale – GreenHonchos provides a one-stop solution by advising across services, such as Technology, Marketing, Operations & Marketplace Management.