# Matter

RBC Innovation Challenge - Team Luigiz

## Solution Details

### General Description

Matter is an online platform that allows small and medium enterprises (SMEs) and business owners to more easily find sustainable raw materials for their products.
The primary purpose of the site is to provide a convenient and easily-navigable marketplace for these materials to reduce the difficulty of finding high-quality, sustainable materials for products. Through our research of the current landscape for finding sustainable materials, we found that the multitude of available sustainability certifications and marketplaces makes it difficult for business-owners to search for and compare products among a variety of sources, so we built Matter to help alleviate this difficulty.

### Features

As mentioned, the core page of the Matter site is our product marketplace, where users can search for materials that fit their needs. As part of our goal to allow users to search among a variety of sources, we implemented tools to aggregate product listings from a number of existing sustainable marketplaces and certification bodies; this makes Matter a more comprehensive tool, as there is no longer a need to perform many separate searches in order to find the best materials.

Matter also includes a page for suppliers to apply to be listed in our product registry. At the moment, all of our product listings were pulled from other sites and contain links to those original listings, but our intention for the site is to eventually form connections with sustainable materials suppliers and host their product listings fully on Matter to further reduce the time needed to find sustainable materials.

Finally, because one of the biggest issues we found in the field of sustainable materials is a general lack of understanding of what issues are important when searching for materials and what each of the many available sustainability certifications actually means, Matter includes a 'Learn' page to educate users about this topic.

### Built With

Matter exists on a relatively simple tech stack.

Our frontend is programmed using React Typescript (starting from Create-React-App) and is hosted on a DigitalOcean droplet. We used NGINX for reverse-proxy to serve the site, and our domain, [luigiz-matter.tech](https://luigiz-matter.tech), was purchased from [get.tech](https://get.tech/). This frontend contains the Home, Search, Learn, and Supply pages, and connects with our backend for search requests and results.

Our backend is an Express server, programmed with JavaScript. It is hosted on Heroku. It has routes to get available product categories and perform searches among our product listings.
INSERT WEB SCRAPING EXPLANATION
At the moment, we store product listings in a JSON format; in the future, however, we would want to migrate this to a relational database to improve query efficiency.

## Technical Details

### Architecture Diagram

## Closing Notes

### Authors

### Acknowledgements
