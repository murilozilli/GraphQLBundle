OverblogGraphQLBundle
=======================

Description
-----------

This Bundle provide integration [GraphQL](https://facebook.github.io/graphql/) using [webonyx/graphql-php](https://github.com/webonyx/graphql-php) 
and [GraphQL Relay](https://facebook.github.io/relay/docs/graphql-relay-specification.html).

Requirements
------------
PHP >= 5.6

Installation
------------

**a)** Download the bundle

In the project directory:

```
composer require overblog/graphql-bundle
```

**b)** Enabled the bundle

```php
// in app/AppKernel.php
class AppKernel extends Kernel
{
    public function registerBundles()
    {
        $bundles = [
            // ...
            new Overblog\GraphQLBundle\OverblogGraphQLBundle(),
        ];

        // ...
    }
}
```

**c)** Enable GraphQL endpoint

```yaml
# in app/config/routing.yml
overblog_graphql_endpoint:
    resource: "@OverblogGraphQLBundle/Resources/config/routing/graphql.yml"
```

**c)** Enable GraphiQL in dev mode (required twig)

```yaml
# in app/config/routing_dev.yml
overblog_graphql_graphiql:
    resource: "@OverblogGraphQLBundle/Resources/config/routing/graphiql.yml"
```

Usage
-----

TODO