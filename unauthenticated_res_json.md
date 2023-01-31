
# sanctum API authentication redirects to login page

> ## Excerpt
> Hi, Im trying to access an API from postman that has a middleware
middleware('auth:sanctum')

well it means that I need to send a bearer token in API request header. And it works when I do send the token.
But the problem is if I don't send token it s

---
you can also override the shouldReturnJson function in your app exception Handler.php and make it return true:



```php
/**
 * Determine if the exception handler response should be JSON.
 *
 * @param  \Illuminate\Http\Request  $request
 * @param  \Throwable  $e
 * @return bool
 */
protected function shouldReturnJson($request, Throwable $e)
{
    return true;
}
```
