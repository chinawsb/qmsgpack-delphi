# Msgpack for Delphi

It's like JSON but small and fast.

author: swish

this project belong qdac3

qdac3 url:
  http://sourceforge.net/p/qdac3
  
### Code Example
```Pascal

var
  lvMsg, lvMsg2:TQMsgPack;
  lvBytes:TBytes;
  s:string;
begin
  lvMsg := TQMsgPack.Create;
  lvMsg.ForcePath('key.obj').AsString := '汉字,ascii';
    
  //
  lvBytes := lvMsg.Encode;

  lvMsg2 := TQMsgPack.Create;
  lvMsg2.Parse(lvBytes);
  //
  showMessage(lvMsg.ForcePath('key.obj').AsString);
  ....
  
  ```
