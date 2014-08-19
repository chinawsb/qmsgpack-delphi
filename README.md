# Msgpack for Delphi

    QMsgPack is a MessagePack protocol implementation for Delphi and C++ Builder.
The lowest version is Delphi/C++ Builder 2006,and tested with Delphi/C++ Builder 
2007/XE/XE6,Other version should support,but not tested.
    QMsgPack is a part of QDAC 3.0,so if you has any question,please contact 
QDAC 3.0 team with follow information:
    
    E-Mail:chinawsb@sina.com
    QQ Group:250530692
    Forum:http://tieba.baidu.com/f?kw=qdac
    Blog:http://hi.baidu.com/chineseswish
    SVN:http://svn.code.sf.net/p/qdac3/code/ or svn://svn.code.sf.net/p/qdac3/code/
    Author:swish

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
