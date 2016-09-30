Tests
=====

We use Alice Fixtures for tests.

A little bit of :poop: code is allowed in tests and is not a sin. (Don't forget, when you write :poop: code in non-test code base, you shall get punished! :rage:)

Avoid using IDs when referencing to entities. Rather use email address, note or any other entity field and find it through EntityRepository. It is 1) human readable 2) it doesn't broke when you add a new entity (if you add an entity somewhere between old entities, it shifts up all consequent IDs)


Composer
========

Use only `composer install` to sync your composer dependencies. We use `composer update` only when we really want to update something.

This Composer plugin makes installing dependencies faster by installing them in parallel https://github.com/hirak/prestissimo. Recommended.