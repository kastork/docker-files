FROM ruby:2.3-alpine

ENV ASCIIDOCTOR_VERSION "1.5.5"

RUN apk add --update make \
 && apk add --update gcc \
 && apk add --update g++ \
 && apk add --update musl-dev \
 && apk add --update libxml2 \
 && apk add --update libxml2-dev \
 && apk add --update libxslt \
 && apk add --update libxslt-dev \
 && apk add --update git \
 && apk add --update nodejs \
 && apk add --update bash
  
  
RUN gem install --no-ri --no-rdoc nokogiri -- --use-system-libraries \
 && gem install --no-ri --no-rdoc asciidoctor --version $ASCIIDOCTOR_VERSION \
 && gem install --no-ri --no-rdoc asciidoctor-diagram \
 && gem install --no-ri --no-rdoc asciidoctor-pdf --version 1.5.0.alpha.13 \
# && gem install --no-ri --no-rdoc asciidoctor-epub3 --version 1.5.0.alpha.6 \
# && gem install --no-ri --no-rdoc asciidoctor-confluence \
 && gem install --no-ri --no-rdoc asciidoctor-latex --pre\
 && gem install --no-ri --no-rdoc pygments.rb \
 && gem install --no-ri --no-rdoc thread_safe \
# && gem install --no-ri --no-rdoc epubcheck \
# && gem install --no-ri --no-rdoc kindlegen \
 && gem install --no-ri --no-rdoc coderay \
 && gem install --no-ri --no-rdoc rouge \
 && gem install --no-ri --no-rdoc slim \
 && gem install --no-ri --no-rdoc haml \
 && gem install --no-ri --no-rdoc tilt 
# \
# && gem install --no-ri --no-rdoc compass --version 0.12.7 \
# && gem install --no-ri --no-rdoc zurb-foundation --version 4.3.2


# RUN apk del make\
#   && g++ \
#   && gcc

RUN rm -rf /var/cache/apk/*

EXPOSE 4242

WORKDIR /documents
VOLUME /documents

CMD ["/bin/bash"]