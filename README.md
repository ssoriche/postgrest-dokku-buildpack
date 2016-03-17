# postgrest-dokku-buildpack
A build pack for deploying postgrest applications onto dokku

Dokku App Configuration:
========================

dokku apps:create myapp
dokku postgres:link workjournal-database myapp
dokku config:set myapp BUILDPACK_URL=https://github.com/ssoriche/postgrest-dokku-buildpack
dokku config:set myapp ANONYMOUS_ROLE=anon
dokku config:set myapp DB_POOL=10
dokku config:set myapp AUTH_ROLE=auth
dokku config:set myapp JWT_SECRET=<your secret here>

git remote add dokku dokku@example.com:myapp
