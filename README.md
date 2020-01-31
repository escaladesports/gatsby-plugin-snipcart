# gatsby-plugin-snipcart

A plugin for using [Snipcart](https://snipcart.com/) with [Gatsby](https://www.gatsbyjs.org/).

## Usage

In your `gatsby-config.js` file, add:

```javascript
module.exports = {
	plugins: [
		{
			resolve: 'gatsby-plugin-snipcart',
			options: {
				apiKey: 'YOUR_SNIPCART_KEY'
			}
		}
	]
}
```

## Options

`apiKey` (required): Your Snipcart API key. If not set, it will try to find it in `process.env.GATSBY_SNIPCART_APIKEY`.

`autopop`: Whether or not the cart will open once a product is added. (Defaults to `false`)

`js`: A Snipcart JavaScript file. (Defaults to `https://cdn.snipcart.com/scripts/2.0/snipcart.js`)

`jquery`: A jQuery file to link to. Set to `false` for none. (Defaults to `https://ajax.googleapis.com/ajax/libs/jquery/2.2.2/jquery.min.js`)

`styles`: A stylesheet file to link to. Set to `false` for none. (Defaults to `https://cdn.snipcart.com/themes/2.0/base/snipcart.min.css`)

## Using Snipcart v3

To add the use of Snipcart v3 to your Gatsby site you will require the `'gatsby-plugin-react-helmet'`.

In order to add v3 to your site, you will need to add a `Helmet` section to your main `Layout.js` file, inside the `Layout` section:

```    <Helmet htmlAttributes={{ lang: 'en' }}>
         <title>"Simply-Vids"</title>
         <link rel="stylesheet" href="https://cdn.snipcart.com/themes/v3.0.6/default/snipcart.css" />
         <div data-api-key="<YOUR API KEY HERE>"></div>
         <script src="https://cdn.snipcart.com/themes/v3.0.6/default/snipcart.js"></script>
       </Helmet>
```
![SnipCart v3](.SnipCartv3.png)
