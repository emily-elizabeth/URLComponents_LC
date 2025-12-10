# URLComponents_LC

Takes a URL and separates it in to the individual components. Insert the stack into use (this is a library stack) and call the function **NewURLComponents(_url_)** to get a pointer to the instance. This allows you to pass an instance to multiple commands/functions without having to run the RegEx code multiple times. To delete an instance call the command **DeleteURLComponents _instance_**

```
on mouseUp
   local urlComponentsInstance
   put NewURLComponents("https://github.com/emily-elizabeth/URLComponents_LC/tree/main") into urlComponentsInstance
   DisplayURLComponents urlComponentsInstance
   DeleteURLComponents urlComponentsInstance
end mouseUp


private command DisplayURLComponents urlComponentsInstance
   put the Schema of urlComponentsInstance & LF & \
         the UserName of urlComponentsInstance & LF & \
         the UserPassword of urlComponentsInstance & LF & \
         the ServerHost of urlComponentsInstance & LF & \
         the ServerPort of urlComponentsInstance & LF & \
         the URLPath of urlComponentsInstance & LF & \
         the URLQuery of urlComponentsInstance & LF & \
         the URLFragment of urlComponentsInstance
end DisplayURLComponents
```
