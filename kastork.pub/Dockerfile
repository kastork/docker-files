FROM ruby:2.3-alpine

ENV ASCIIDOCTOR_VERSION "1.5.4"

# RUN apk add --update ruby-nokogiri \

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
  
  
# RUN gem install --no-ri --no-rdoc nokogiri -- --use-system-libraries \
#   && gem install --no-ri --no-rdoc asciidoctor --version $ASCIIDOCTOR_VERSION \
#   && gem install --no-ri --no-rdoc asciidoctor-diagram \
#   && gem install --no-ri --no-rdoc asciidoctor-pdf --version 1.5.0.alpha.11 \
#   && gem install --no-ri --no-rdoc asciidoctor-epub3 --version 1.5.0.alpha.6 \
#   && gem install --no-ri --no-rdoc asciidoctor-confluence \
#   && gem install --no-ri --no-rdoc coderay pygments.rb thread_safe epubcheck kindlegen rouge \
#   && gem install --no-ri --no-rdoc slim \
#   && gem install --no-ri --no-rdoc haml tilt \
#   && gem install --no-ri --no-rdoc compass --version 0.12.7 \
#   && gem install --no-ri --no-rdoc zurb-foundation --version 4.3.2 \


RUN gem install --no-ri --no-rdoc awestruct \
  && gem install --no-ri --no-rdoc webrick \
  && gem install --no-ri --no-rdoc compass \
  && gem install --no-ri --no-rdoc opal \
  && gem install --no-ri --no-rdoc asciidoctor \
  && gem install --no-ri --no-rdoc kramdown \
  && gem install --no-ri --no-rdoc htmlcompressor \
  && gem install --no-ri --no-rdoc uglifier \
  && gem install --no-ri --no-rdoc bootstrap-sass \
  && gem install --no-ri --no-rdoc zurb-foundation


# RUN apk del make\
#   && g++ \
#   && gcc

RUN rm -rf /var/cache/apk/*

EXPOSE 4242

WORKDIR /documents
VOLUME /documents

CMD ["/bin/bash"]