# Msgpack for Delphi
    Topic in [offical website](http://www.qdac.cc) is in chinese language available,[Visit it](http://www.qdac.cc/?cat=44).
    QMsgPack is a simple and powerful Delphi & C++ Builder implementation,It can pack and unpack messagepack data in Pascal or C++ code quickly.
    QMsgPack support full protocol feathers,include extension type。For some reason,I don't want to support low version delphi and c++ builder.If you want use QMsgPack , please upgrade you ide first.
    Current version of QMsgPack support follow Delphi and C++ Builder versions:
    Delphi/C++ Builder 2006~2009
    Delphi/C++ Builder XE~XE7
    Some feathers,like RTTI only support after Delphi/C++ Builder 2009。
    As a part of [QDAC](http://www.qdac.cc) [3.0](http://sourceforge.net/p/qdac3),you can checkout it by SVN from http://svn.code.sf.net/p/qdac3/code/ or svn://svn.code.sf.net/p/qdac3/code/.The github only the placehole,and the newest version maybe not update in here.
    If you has any question,please contact QDAC 3.0 team with follow information:
    1、[Project Host at Sourceforge](http://sourceforge.net/p/qdac3)
    2、[Email to author](mailto://chinawsb@sina.com)
    3、[Project Websit at qdac.cc](http://www.qdac.cc)
    4、QQ group:250530692
    5、[Forum at baidu](http://tieba.baidu.com/f?kw=qdac)
    The lasted code please use svn from:
    1、[HTTP Protocol http://svn.code.sf.net/p/qdac3/code/](http://svn.code.sf.net/p/qdac3/code/)
    2、[SVN Protocol svn://svn.code.sf.net/p/qdac3/code/](svn://svn.code.sf.net/p/qdac3/code/) 
    
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
