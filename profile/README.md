# Matter

RBC Innovation Challenge - Team Luigiz

## Solution Details

### General Description

Matter is an online platform that allows small and medium enterprises (SMEs) and business owners to more easily find sustainable raw materials for their products.
The primary purpose of the site is to provide a convenient and easily-navigable marketplace for these materials to reduce the difficulty of finding high-quality, sustainable materials for products. Through our research of the current landscape for finding sustainable materials, we found that the multitude of available sustainability certifications and marketplaces makes it difficult for business-owners to search for and compare products among a variety of sources, so we built Matter to help alleviate this difficulty.

[Watch our pitch video here](https://www.youtube.com/watch?v=62tKXf8JTj4)

<img width="1440" alt="image" src="https://user-images.githubusercontent.com/17555595/216184500-18c34f6a-2487-4469-ab9c-3937e4a1bfa4.png">
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/17555595/216184539-81879b7e-434c-4844-8a25-054daac61a55.png">
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/17555595/216184601-524ee7e1-2295-438a-a296-0921cddf95ae.png">
<img width="1440" alt="image" src="https://user-images.githubusercontent.com/17555595/216184621-d3640f9e-2023-4af7-8f97-293dc48b7f54.png">


### Features

As mentioned, the core page of the Matter site is our product marketplace, where users can search for materials that fit their needs. As part of our goal to allow users to search among a variety of sources, we implemented tools to aggregate product listings from a number of existing sustainable marketplaces and certification bodies; this makes Matter a more comprehensive tool, as there is no longer a need to perform many separate searches in order to find the best materials.

Matter also includes a page for suppliers to apply to be listed in our product registry. At the moment, all of our product listings were pulled from other sites and contain links to those original listings, but our intention for the site is to eventually form connections with sustainable materials suppliers and host their product listings fully on Matter to further reduce the time needed to find sustainable materials.

Finally, because one of the biggest issues we found in the field of sustainable materials is a general lack of understanding of what issues are important when searching for materials and what each of the many available sustainability certifications actually means, Matter includes a 'Learn' page to educate users about this topic. However, due to time constraints, we were unable to fully implement this page, though it is at the top of our priorities for future work on the site.

### Built With

Matter exists on a relatively simple tech stack.

Our frontend is programmed using React Typescript (starting from Create-React-App) and is hosted on a DigitalOcean droplet. We used NGINX for reverse-proxy to serve the site, and our domain, [luigiz-matter.tech](https://luigiz-matter.tech), was purchased from [get.tech](https://get.tech/). This frontend contains the Home, Search, Learn, and Supply pages, and connects with our backend for search requests and results.

Our backend is an Express server, programmed with JavaScript. It is hosted on Heroku. It has routes to get available product categories and perform searches among our product listings.

This product list is an aggregate of multiple sustainable product manufacturer websites, which were webscraped. The webscraping tool used was selenium, as it allowed for navigation of dynamic webpages. The general process for webscraping these sites was to find their navigation menu, iteratively click each category, and find the list of the products on each of those pages. While each website varied slightly on what metadata was offered, generally with each product listed, an image, a link to its unique product page, the cost, and a list of certifications were easily accessed by searching through the encompassing html. This data was then sorted into dictionaries and stored. At the moment, we store product listings in a JSON format; in the future, however, we would want to migrate this to a relational database to improve query efficiency. In addition, we plan on forming more direct relationships with materials manufacturers, so that listings could be more directly integrated into the site.

## Technical Details

### Architecture Diagram

![Matter Architecture](https://user-images.githubusercontent.com/17555595/212224736-debdfc74-a279-42de-a990-3b723ec7e961.jpg)

## Closing Notes

### Authors

Gabe Guralnick

Ian Lavine

Megan Horsthuis

Jayden Jung

Karrie Chou

Jueun Kang

### Acknowledgements

We'd like to thank the following sites who we used for our product listings:

- Cradle to Cradle - https://www.c2ccertified.org/products/registry
- Cirplus - https://www.cirplus.com/app
- Inesscents - https://inesscents.com/shop-all/

We'd also like to thank [Storyset](https://storyset.com/) for providing various graphics that we used on the site.

Finally, we'd like to thank UofT Entrepreneurship and RBC for hosting this hackathon.
