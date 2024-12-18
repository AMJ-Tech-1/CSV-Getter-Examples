# CSV Getter WordPress Components

Welcome to the **CSV Getter WordPress Components** repository! This collection of free, open-source WordPress widgets allows you to seamlessly integrate dynamic data from your CSV Getter endpoints into your WordPress sites. Use it to display and interact with data from Airtable, Notion, static CSV files, and more!

## About CSV Getter

[CSV Getter](https://csvgetter.com) is a powerful tool that lets users create API endpoints directly from various data sources like Airtable, Notion, or static CSV files. With CSV Getter, you can make your data accessible and dynamically updateable via simple JSON endpoints, allowing for a flexible way to work with data on websites and applications without needing to manually update each piece of content.

## Available WordPress Components

This repository includes four dynamic components that you can use to display data from CSV Getter endpoints on your WordPress site:

### 1. AccordionDropDown

A customisable accordion dropdown component that fetches data from your CSV Getter endpoint and displays it in an expandable/collapsible format. Ideal for FAQs, lists, or any data that you’d like to display in an organised, easily navigable structure.

- **Features**: Dynamic item generation, expandable sections, customisable styling.
- **Use case**: FAQs, product specifications, detailed information lists.

### 2. ImageCarousel

A stylish image carousel that allows users to navigate through images pulled from their CSV Getter endpoint. This component is perfect for showcasing products, portfolios, or image galleries with additional details available on hover.

- **Features**: Slide transitions, customisable navigation buttons, dynamic data fetching.
- **Use case**: Product galleries, portfolios, travel images, and any image collection.

### 3. ImageGallery

An image gallery that pulls images and related information from your CSV Getter endpoint, displaying them in a grid format. Hovering over each image reveals more details, making it a great choice for visual collections that benefit from additional context.

- **Features**: Hover effects for additional information, responsive grid layout, dynamic image fetching.
- **Use case**: Art collections, product displays, real estate listings, photo galleries.

### 4. InfoCards

This component renders individual cards with images and relevant details, dynamically generated from the data in your CSV Getter endpoint. Each card displays a title, image, and essential details, making it a flexible solution for displaying summaries or previews.

- **Features**: Responsive card layout, image integration, auto-generated content based on endpoint data.
- **Use case**: Team bios, product summaries, service highlights, event previews.

### 4. SearchItems

This component allows you to search the data returned from your endpoint and renders individual cards with the json objects that match the search query. Each card displays the full object and searches keys and values, making it a flexible solution for querying.

- **Features**: Responsive card layout, single image integration, returns all content from the object that matches.
- **Use case**: Searching large datasets, displaying data, displaying single images.

### 4. Table

This component renders a dynamic table, populated by the data in your CSV Getter endpoint. The table can be queried with a search bar, while also filtered by count. The result is a powerfull tool for querying and displaying all data. Not suitable for use with image data.

- **Features**: Displays all data, offers search and limit functionality, ability to order individual columns.
- **Use case**: When all data is required, when basic ordering and filtering can be useful, searching and comparing data.

## Installation and Usage

1. **Add Your CSV Getter Endpoint**: Each component includes an API URL variable where you should input your CSV Getter endpoint URL. Replace the sample URLs with your specific endpoint.
2. **Embed Components on Your Site**: Copy the HTML and JavaScript code for each component and paste it into the WordPress post, page, or widget where you'd like to display the data.
3. **Customise Styling**: Each component comes with a base style, but you can adjust the CSS as needed to match your site’s branding.

## Example Usage

Here’s a sample of how you might set up the `InfoCards` component with your CSV Getter endpoint:

```html
<div id="card-container" class="card-container"></div>

<script>
	const apiUrl = "https://api.csvgetter.com/YOUR_ENDPOINT_HERE?type=json_records";

	fetch(apiUrl)
	  .then(response => response.json())
	  .then(data => {
		renderCards(data);
	  })
	  .catch(error => console.error('Error fetching data:', error));
  
	// Render function for InfoCards goes here...
</script>
```

Each component's code is designed to be plug-and-play, so you can quickly display data from your endpoint by adjusting the apiUrl variable.

## License
This project is open-source and available under the MIT License. Feel free to use, modify, and share the components, and let us know if you make any improvements!

## Contributions
We welcome contributions! Feel free to open issues, submit pull requests, or suggest new features. We aim to keep these components versatile and easy to use for all CSV Getter users.

## Support
For questions about integrating CSV Getter with WordPress or using these components, reach out to our support team or check the CSV Getter documentation for more information.

Happy building with CSV Getter! 🎉