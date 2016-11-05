FROM mysql:5.7.16

RUN apt-get update && apt-get install -yq mecab libmecab-dev unzip curl g++ make autotools-dev perl

RUN curl -sSL -o /tmp/mecab-ko.tar.gz https://bitbucket.org/eunjeon/mecab-ko-dic/downloads/mecab-ko-dic-2.0.1-20150920.tar.gz

RUN cd /tmp/ && tar xvzf mecab-ko.tar.gz && cd mecab-ko-dic-2.0.1-20150920 && ./configure && make && make install

RUN echo "dicdir=/usr/lib/mecab/dic/mecab-ko-dic" > /etc/mecabrc

RUN echo "loose-mecab-rc-file=/etc/mecabrc" >> /etc/mysql/my.cnf

RUN echo "innodb_ft_min_token_size=1" >> /etc/mysql/my.cnf
