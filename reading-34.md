# Dynamic Routes and Deplyment


## [Dynamic Routes](https://nextjs.org/learn/basics/dynamic-routes/page-path-external-data)

### Page Path Depends on External Data
- This make me think about getting to a specific cookie store from our list of stores to create a path to go to that page and then render that page

- Steps:
  - folder `posts` inside of `pages`
  - any page with `[].js` is considered a dynamic routes
  - then create you JSX inside `[].js`
  - export an async functioni called `getStaticPaths`
    - needs to return a list of possible values for whatever is inside `[].js`
  - Then export an async function `getStaticProps` and pass it the arguement `{params}`. This will contain the inside of the brackets
  
### [Depoyment with Vercel](https://nextjs.org/learn/basics/deploying-nextjs-app/deploy)
- Connect with Github
- organize the enviroment variables
- and build
- Tada!

- [Return to Home](README.md)