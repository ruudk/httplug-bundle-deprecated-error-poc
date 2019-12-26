# httplug-bundle-deprecated-error-poc

Related to https://github.com/php-http/HttplugBundle/issues/371

```
composer install

$ bin/console lint:twig templates/base.html.twig -vvv
2019-12-26T11:42:26+00:00 [info] User Deprecated: The httplug.collector.twig.http_message service is deprecated since version 1.17 and will be removed in 2.0. Use "@Httplug/http_message.html.twig" template instead.
2019-12-26T11:42:26+00:00 [debug] Notified event "console.command" to listener "Symfony\Component\HttpKernel\EventListener\DebugHandlersListener::configure".
2019-12-26T11:42:26+00:00 [debug] Notified event "console.command" to listener "Http\HttplugBundle\Discovery\ConfiguredClientsStrategy::onEvent".
2019-12-26T11:42:26+00:00 [debug] Notified event "console.command" to listener "Http\HttplugBundle\Collector\PluginClientFactoryListener::onEvent".

 // OK in templates/base.html.twig


 [OK] All 1 Twig files contain valid syntax.


2019-12-26T11:42:26+00:00 [debug] Notified event "console.terminate" to listener "Symfony\Component\Console\EventListener\ErrorListener::onConsoleTerminate".
```
