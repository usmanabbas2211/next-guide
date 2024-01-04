# next guide

## environment variables

    .env.local has higher priority than all other env files.

## static vs dynamic pages

    when page consists of getServerSideProps it is considered dynamic and when there is not then it is considered static.
    So when someone visits static pages next js immediately returns the html file but for dynamic pages it will first run intermediate login and then returns the page

## getStaticProps

    If you export a function called getStaticProps (Static Site Generation) from a page, Next.js will pre-render this page at build time using the props returned by getStaticProps
    export function getStaticProps(context: GetStaticProps) {
    return {
    props: { count: Math.floor(Math.random() \* (1000 - 500) + 500) },
    revalidate: 7,
    };
    }

## getStaticPaths

    If a page has Dynamic Routes and uses getStaticProps, it needs to define a list of paths to be statically generated.

    When you export a function called getStaticPaths (Static Site Generation) from a page that uses dynamic routes, Next.js will statically pre-render all the paths specified by getStaticPaths
