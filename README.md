```
### ruby-2.3.8.tar.gz:

sudo apt-get install zlib1g-dev libssl-dev

#### zlib:   
        cd ext/zlib
        ruby extconf.rb
        make


#### openssl:
        cd ext/openssl
        ruby extconf.rb
        make

        这时出错，make: *** No rule to make target `/include/ruby.h', needed by `ossl.o'

        其实是ext/openssl/Makefile中忘了给路径变量top_srcdir赋值,调用的时候当然就报错了，修改 Makefile 增加 top_srcdir = ../..


### ubuntu_ruby_gems_2.3.0.tar || centos_ruby_gems_2.3.0.tar

sudo cp -r usr/local/lib/ruby/gems/2.3.0/* /usr/local/lib/ruby/gems/2.3.0/


### ubuntu_local_bin.tar

sudo cp bundler bundle compass jekyll /usr/local/bin/
sudo cp bayes.rb  kramdown  listen  rackup  safe_yaml  summarize.rb  tilt  /usr/local/bin/

rake renerate

```
