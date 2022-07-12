# next-ecommerce

This ecommerce web app demonstrates my ability using technologies such as: React, Next.js, Strapi, Cloudinary, authO, Stripe.

**Here is where I will document my efforts in building this ecommerce app.**

I start by utilizing Strapi and creating a folder called backend.

**Strapi** is a quick solution for backend CMS to design APIs and manage content easily.

After installation, my browser opens up the Strapi dashboard. Here is where I create the Product Collection, where I require a Title and Description per Product object.

Once saved, Strapi exposes an API so I can access the data.

Then I add an Image and UID to the Product object. The UID will provide a slug that reflects the name of a given product in the address bar when user selects a product on the client side.

Lastly I add price to the Product object for obvious reasons.

(This is an ecommerce app)

I make a dummy product to make sure stuff is working—My roommate's dog is officially online and for sale!

By default, Strapi supports FEtch but not GraphQL. So I'm gonna install that via @strapi/plugin-graphql.

**GraphQL** is a query language that improves the ease of access for your APIs.

Back in the Strapi dashboard, I change permissions for public users.

I double-check if GraphQL plug-in is installed according to my dashboard. It isn't.

I cd into the backend folder and re-install the plug-in. It works now.

You want to use GraphQL over fetch because you can query and get the specific data you want, as opposed to getting all the data.

NOTE TO SELF: Use CTRL + Space in playground for dropdown of your data.

My goal is to replace the "data" in the Product object from Strapi to Cloudinary for optimization.

npm i @strapi/provider-upload-cloudinary

**Cloudinary** is a cloud-based media management service.

So I input data from my Cloudinary account into the env file within the backend folder.

I create the plugins.js file within the config folder to integrate Cloudinary.

Here are the docs I used for Cloudinary Integration: https://strapi.io/blog/add-cloudinary-support-to-your-strapi-application

On my Strapi dashboard I create a new Product—my custom made leather whip is now for sale! (theoretically).

However, the image shows as corrupted on Strapi. So I go on GraphQL Playground to view the data. Here I can see that the image data has been stored, and now retrieved, from Cloudinary.

(I fix this "corrupted" image bug on my Strapi dashboard with some instruction from the docs provided above)

Before I build out the frontend, I will install Next.js.

npx create-next-app@latest frontend

**Next.js** is a React framework that offers functionalities such as server-side rendering and generating static websites.

I create the frontend folder via installing Next.js.

(For some reason it doesn't want to show up on Github and I don't know why. I'll figure it out later probably.)

I clean up the files and folders. I add a product folder with a dynamic [id]. js file inside.
