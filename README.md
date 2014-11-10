### QMsgPack-Messagepack for Delphi/C++ Builder
QMsgPack is a simple and powerful Delphi & C++ Builder implementation for messagepack protocol.
QMsgPack is a part of QDAC 3.0,Source code hosted in Sourceforge(http://sourceforge.net/p/qdac3).

### Feathers
· Full types support,include messagepack extension type

· Full open source,free for used in ANY PURPOSE

· Quick and simple interface

· RTTI support include

### Install
QMsgPack is not a desgin time package.So just place QMsgPack files into search path and add to your project.

### Support
· Topic in Website (http://www.qdac.cc/?cat=44)

· Mail to author (chinawsb@sina.com)

· Post in forum (http://tieba.baidu.com/f?kw=qdac)

· QQ Group (250530692)

### Source check out
· HTTP (http://svn.code.sf.net/p/qdac3/code/)

· SVN (svn://svn.code.sf.net/p/qdac3/code/)

### Example
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

