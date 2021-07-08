# horse-requestlog
Middleware for inject Request Logge in HORSE

### For install in your project using [boss](https://github.com/HashLoad/boss):
``` sh
$ boss install github.com/eudisdeoliveira/HorseRequesLog
```

### Sample Horse Server with RequestLog middleware
```delphi
uses Horse, Horse.RequestLog;

begin  
  THorse.Use(Horse.Request);
  
  THorse.Post('/ping',
    procedure(Req: THorseRequest; Res: THorseResponse; Next: TProc)
    begin
      Res.Send('pong');
    end);

  THorse.Listen(9000);
end;
```
