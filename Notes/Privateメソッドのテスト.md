```php
/**

* privateメソッドを呼び出す

* @param object $object

* @param string $methodName

* @param array<mixed> $parameters

*

* @return mixed

*/

private function invokePrivateMethod(

	object $object,
	
	string $methodName,
	
	array $parameters = []

): mixed {

	$reflection = new ReflectionClass($object);
	
	$method = $reflection->getMethod($methodName);
	
	$method->setAccessible(true);

	return $method->invoke($object, ...$parameters);
}

```