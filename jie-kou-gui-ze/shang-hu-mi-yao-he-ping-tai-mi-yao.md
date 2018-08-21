###在商户与平台的交互中需要两对密钥 — 商户密钥对和平台密钥对

商户密钥对： 由商户生成，商户保留私钥，公钥提供给平台，商户用该私钥对商户发送给平台的信息进行签名；
平台密钥对： 由平台生成，平台保留私钥，公钥提供给用户，商户用该公钥对平台发送给商户的信息进行验签；

##RSA公私钥生成
生成方式：使用OpenSSL命令生成。
首先进入OpenSSL工具，再输入以下命令：

    OpenSSL> genrsa -out rsa_private_key.pem   1024  #生成私钥
    OpenSSL> pkcs8 -topk8 -inform PEM -in rsa_private_key.pem -outform PEM -nocrypt -out         rsa_private_key_pkcs8.pem #Java开发者需要将私钥转换成PKCS8格式
    OpenSSL> rsa -in rsa_private_key.pem -pubout -out rsa_public_key.pem #生成公钥
    OpenSSL> exit #退出OpenSSL程序
    
经过以上步骤，开发者可以在当前文件夹中（OpenSSL运行文件夹），看到rsa_private_key.pem（RSA私钥）、rsa_private_key_pkcs8.pem（pkcs8格式RSA私钥）和rsa_public_key.pem（对应RSA公钥）3个文件。开发者将私钥保留，将公钥提交平台，用于验证签名。

注意：对于使用Java的开发者，将pkcs8在console中输出的私钥去除头尾、换行和空格，作为开发者私钥，对于.NET和PHP的开发者来说，无需进行pkcs8命令行操作。
