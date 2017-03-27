# em2a - Emoji to ASCII art

[![license: MIT](https://img.shields.io/badge/license-MIT-blue.svg?maxAge=31536000)](COPYING)

For macOS 10.12 or later.

## Dependencies

- Bundler (`gem install bundler`);
- ImageMagick (`brew install imagemagick`);
- jp2a (`brew install jp2a`).

Tested with Ruby 2.4.1p111, gemoji 3.0.0, ImageMagick 7.0.5-4 and jp2a 1.0.6 on
macOS 10.12.3.

## Installation

Clone this repository, then

```
bundle install
```

Now you can invoke em2a via Bundler:

```
bundle exec em2a
```

You can also install a shell wrapper to any location of your choice, e.g.,

```
./install-wrapper ~/bin
```

Then you can invoke em2a as

```
~/bin/em2a
```

or `em2a` alone if `$HOME/bin` is in your `$PATH`.

## Usage

`em2a` supports both raw UTF-8 emojis
and [`:alias:`-styled emoji escape sequences][1] used on GitHub and
friends. You can pass in one or more strings as arguments, each containing zero
or more emojis in either form. Whitespace characters are automatically ignored.

[1]: https://www.webpagefx.com/tools/emoji-cheat-sheet/

## Examples

```
$ em2a :+1: 🎠 🦄 🚀 :ship:
                                    .........                                   
                                  ..............                                
                                  ''............'.                              
                                  .,.............''                             
                                   .'.............,.                            
                                   .'.............,'                            
                                    .............';'                            
                                    ............',;                             
                                   .............,;.                             
                                 ...............';.                             
                               .'................,.                             
                            ..'...................''....                        
                          .'......................''''''''................      
         .........     ........................'''........................'.    
       ..............''.......................,............................,'   
      .......................................,:'''''''..................'';;.   
     .......................................';clc:;;;;,,,''''''''',,;;:c:,.     
    .......................................'',:cllc:;;;;;;,,,,,;;;;;;;;,,,..    
    .......................................'',;:;'''......................','   
    .......................................''';:,'''''''..................',;   
    .......................................''',:c:;;;;;;,,'''''''''''''',,,'.   
    ........................................''',cllccccccc::::::::::::::;.      
    .........................................'';:,'''''''...............''.     
    ................'',''.....................';;''''''''...............','     
     .......'''''',,,;;:c:,,''''''............';c::;;;;,,'''.''...''''',,'.     
       .',,,;;;;:::cclloodoc:;,,'''''''''''''',;:lolllccccccccccccclc,..        
         .';:ccc::;,,'..... .';:::;;,,,,,,,,,,,;::;,,,,'''''''',,,,,;,.         
                                ..,;cllccccc::::cc;,,,,''.........'',;.         
                                      ...'',,;;;;;,,,;;;;,,,,,;;;:;;'.          
                                                      ...',,,,,'..              


                                       ...                                      
        .',,.  .       .....          .;;;.                                     
        ..,cc,;ll.    ..ldd;,'       .;::;;.                                    
        'llc:c:loc;,.  ..:d:,:c..     .c;;.                                     
        .c;,lo:;l:.'lc'..'c:,col:'.   .c;;.                                     
        .:;coo:;l:. .od;..'::;;:lc,.  .c:;.                                     
         ,''...;o:..'okl''',:,.:cl;c. .c;;.                                     
         ',...'lolc;.lkl,,,clooolc:c, .c;;.                                     
         ';,,,:ll.   oxc,,cc:,;::;;;c,.l:;.                                     
         .ldddloc   cxo;''',',,,,;;::,'o:;.                                     
           ';:;,. .col;'''',,;;;;:ccc:ldll.        ..':l,           ..          
                 .,:;,,,,':;;;,'..',,lodddoc::::cclodoc;,'.....','''''.'''.     
               .::;;;;;;;,...     .'lodddddl;:cc:c:cccc;..   ..';:ccc:;,...,.   
              .llc:dxc,.         .;;;loolc::oooc:lloooo,.       .'ldxkxoc:'.,.  
              .ooccdc..         .',,:::::clllol;ool::lo,.        .'. :kxlcc;;.  
        .';:;'.cdldo;...        ':,;ccccccclll;cooolclc'.        .':cxxo;;:c,   
       .;:loclodxkxl:'.....  ..';:ccoddoooolllllooolc:;,'.     .';:dxl:;;cc,    
        .:dd. .;ldoc,...'''....,:clc:ccccccclccccc:,,,,,'......,:cccclllc'      
         .';,. .........'''',,:lddl:;;;;;;;;;:lodxo:;,''''''',;:cccodl,.        
       ...',;;,''',,,;;;;;,,,;okOkxdolccclloxkO0000x:;'''''...'..;lo;.          
       .;,';';lll:'.,:c,.        ....cxdooxl...ckKKKOo;''''......',,,;;,;,      
        .:;,. .coddoddxko'           .clcll.     .;:cc'.';;::cccccl;;lcc:       
         .;;,.     .....              .lcc.           .':ooc,,clll:,;cc'        
          .;;,.                       .c::.          ;ccol.    'coc:lo:.        
           .:;;,.  ...                .c::.         .lolo'      .',l:..         
            .::clccdkx;               .:::.          cdddc     ';,;;            
                .',::::.              .:,;.          .cc'      .c;;;,           
                                      .:;;.                     ;clx:           
                                      .;,;.                      .,.            
                                      .;';.                                     


                                                                                
                                                                                
                                .;.        .,.                                  
       ';'..                    coo'       :ll;                                 
         .:;...                .lodd'     .cloo:.                               
           .,:.......          ,loddo'....,:clod: .,,''''....                   
              .c:...;.....     ,clc:;,:lod:;clodd. ;ool:,'',;;,'.               
                .;ol'. ',',,'';llc;;lxxd:;c;:clod; .;:clol:;;,;:c;.             
                   ,odd;.  ';'ldl::xkodd:';c;:cod,..:c;;:clllllllll:.           
                     ,ldlcc'  ,dolo,.,ccllcc:..,;..'lxoc;,;;::clllllo:.         
                       .cdl:,..:odo.               .;ddxxkkkkkkxdooolllc'       
                       .,'..     .....,;,..          ;oollloddddoolcllcccc,.    
                     .,'.          ,ONNl:00:.         .:olc:;,,,;;:clooocccc,   
                   .',..           :NMMMMMWl            .':lddxxkkkOkdllolllo:. 
                  .,'..             .cddol'                 .cxxooxkxoc::coood: 
                .''..                                        ,c::oxdllc;;;:lddl.
               .,..                                      ...';:ldxdlcclc::;:ldo.
             .,'..                                     .....''''cdolccllcc::cox;
            ,:,.                                    ...'''.......;odlccodllllodc
          .ccc;.       .............................',::;'.........:oocclooooooc
         'loolc:,.    ...........................',:lll:,............;oxdlllloo;
        .loONXxccc;'.........''',,,,,''''',,,;;:cldddo:;'.............:kxdxxxxl.
        .codkkdlllllc;,''',;::ccc:;;;;;,,,,,,,:dxxdol:;,'.............:::coooo, 
         .cooooooooooodddoloc;'.               ,ddolc:;,'............',:cc;:dl, 
           .;cloooddxxkxo:..                   .lxdolc:;,,'......'''''..    .,;.
               ...',,'.                         .dxdolcc:;,,''..               .
                                                 .cloolc:,'..                   
                                                                                
                                                                                
                                                                                


                                                                                
                                                                    .........   
                                                          ....''',,;:::;;,',:dl 
                                                     ....'''',,;::ccc:;,'.';lxO;
                                                 .':lodkkkxlc::;;,,,,,.....;oxO;
                                             ..:oodxxkOKXNWXxol,'......   .cdOk.
                                         ...,ckxodk0KXNWWMMWkll,..      .,cdk0: 
                                      .....,ok0k0KNNWWMMMMWKoc;.      ..':ok0d  
                                   .',.',,;ldx0XNWWMMMMMWKOxd;.   ....,:coxko.  
                                .;'..';cc;coxkxkOKXXKK0Okdc,.  ....',:cldkk:    
                             'ckOc.',;:lololllooodddoc:,.. .....',;:cldxOx.     
              '''......',;cdk0KOc,:cllooooool:;,''....  .....',;;:codxOk;       
           .:dxxkkkkkkkkOO000X0ollooddoooolccc:'''.......'',;;:clodxOOc         
         'cxxxkkkkkkkOOO000KNXOddddddoollc:;,,''''...'',,;::clodxkOk:.          
       ,odxxxxxxxkkkkOO000KNX0xddddoolc:;;,'''',;:::;;::cllodxkO0x;             
     .cllooloooodddxxkOO0KNX0xdooolc:;;,,',:lddolooddxxdodxkkOOo'               
   .;:;;:::::ccclllcclodkKX0dlcc::;;;;:codxkkkxdxxxkkOO0000Oo;.                 
  ',''',,,,,;;;;:,.  .;,lkkl:;;;;;:ldk0kllxOkkkOOOO000KKkl.                     
.................  .xKKO0NKdc:coxO0XX0xldO0000000KKK0o;.                        
                  ..;x00O00XXKKXNNNXOxOKXXKKKKKKK00o.                           
             .....   .,coooxXNNXK0xlxKXXXKKK00OOOk:                             
           .'..         .oKNNXKkxd,.o00OOOOOOOOOOd.                             
      .. .,'..        'd0KKOdc;,. .;dkOOOOOOOOOOOo                              
      ..,,'....     .l0K0o;..  'cdkOOOOOOOOOOOOOOx.                             
      .,'....      ,kkl,..     ;odxkkOOOOOOOOOkd:'                              
    .:c;'....    'cc'....      'codxkkOOOOOOd:.                                 
     ;'.,'...',','....         .:loxkkOkxl;.                                    
    ,;.';,,,,''....            .:codoc,.                                        
   .,.......                   ','..                                            
                                                                                


                                                                                
                                                                                
                                                  ;ldddddddooc.       ,ldddddxxd
                                                 .oO00OOOO00KK.       o0000000KK
                                                 .oO00OOOOO0K0,      .oO000000KK
                                                 .okOOOOOOOO0O.       lO00OO0000
                                                 .oO0OOOOOO00O.       lO00000000
                                                 .okOOOOOOOOOk.       lkOOO00000
                                          ........:,cllc,lll;c........coc:ood:cd
                                         .','','.,:;cllc;lll:c,';,',;,lolcdddlld
                                         ...lc....cc....lc...'lc...,oc...,dl...c
                                           .,,.  .,,.  .,,.. .,,....;,...':;...,
                                        ........................................
    .. ..   .    .   .                     .,,.  .,,.  .,,.  .;,.  .;,.  .:;...,
   .c,'cc'';c,'',c,',:;'                   .c:.  .cc.  .c:.  .c:.. 'l:...,oc...:
    ,;;;;,,,''''''''..;oxl'           .................................'''''''''
    .............  ......;ldl;;:::::;,'',,,,,,,,,,,,,,,,,,,,,,,,,,,,,,;;;;;;;;;;
     ............     ......''''''''',,,,,,,,,,,,,,,,,,,,,,,,,,,,;;;;;;;;;;:::::
      ..............  ..........................................................
      .................................... cKK; .oK0,..xKO'..dX0,..xX0,..xXK;.;0
        ....................................''....,'....,.....,'....,'...';,...,
         .......................................................................
          'cllooddddddddddddddddddddddddddddddddddddddddddddddddddxxxxxxxxxxxxxx
           .cdxxkOOO000000000000000000000000000000000000000000000KKKKKKKKKKKKKKK
             ,ldxxkkOO00000000000000000000000000000000000000000K0KKKKKKKKKKKKKKK
               ,lddxkkOOO00000000000000000000000000000000000000KKKKKKKKKKKKKKKKK
                 'coddxkkOOOO00000000000000000000000000000000000000000000KKKKKKK
                   .,cooddxxxkkkkkkkkkkkOkkkkkkkkkkOOOOOOOOOOOOOOOOOOOOOO0000000
                       ..',;:ccllooodddddxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
                                                                                
```
