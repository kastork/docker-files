FROM ruby:2.3.1-alpine

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
  


RUN gem install --no-ri --no-rdoc awestruct \
  && gem install --no-ri --no-rdoc nokogiri -- --use-system-libraries \
  && gem install --no-ri --no-rdoc hitimes \
  && gem install --no-ri --no-rdoc activesupport \
  && gem install --no-ri --no-rdoc addressable \
  && gem install --no-ri --no-rdoc colorator \
  && gem install --no-ri --no-rdoc colored \
  && gem install --no-ri --no-rdoc ethon \
  && gem install --no-ri --no-rdoc gemoji \
  && gem install --no-ri --no-rdoc html-pipeline \
  && gem install --no-ri --no-rdoc html-proofer \
  && gem install --no-ri --no-rdoc i18n \
  && gem install --no-ri --no-rdoc jekyll \
  && gem install --no-ri --no-rdoc jekyll-compose \
  && gem install --no-ri --no-rdoc jekyll-feed \
  && gem install --no-ri --no-rdoc jekyll-mentions \
  && gem install --no-ri --no-rdoc jekyll-paginate \
  && gem install --no-ri --no-rdoc jekyll-redirect-from \
  && gem install --no-ri --no-rdoc jekyll-sass-converter \
  && gem install --no-ri --no-rdoc jekyll-sitemap \
  && gem install --no-ri --no-rdoc jekyll-watch \
  && gem install --no-ri --no-rdoc jemoji \
  && gem install --no-ri --no-rdoc listen \
  && gem install --no-ri --no-rdoc liquid \
  && gem install --no-ri --no-rdoc maruku \
  && gem install --no-ri --no-rdoc mercenary \
  && gem install --no-ri --no-rdoc mini_portile2 \
  && gem install --no-ri --no-rdoc posix-spawn \
  && gem install --no-ri --no-rdoc pygments.rb \
  && gem install --no-ri --no-rdoc rouge \
  && gem install --no-ri --no-rdoc safe_yaml \
  && gem install --no-ri --no-rdoc thread_safe \
  && gem install --no-ri --no-rdoc typhoeus \
  && gem install --no-ri --no-rdoc tzinfo \
  && gem install --no-ri --no-rdoc yajl-ruby \
  && gem install --no-ri --no-rdoc yell \
  && gem install --no-ri --no-rdoc webrick \
  && gem install --no-ri --no-rdoc compass \
  && gem install --no-ri --no-rdoc opal \
  && gem install --no-ri --no-rdoc asciidoctor \
  && gem install --no-ri --no-rdoc slim \
  && gem install --no-ri --no-rdoc kramdown \
  && gem install --no-ri --no-rdoc htmlcompressor \
  && gem install --no-ri --no-rdoc uglifier \
  && gem install --no-ri --no-rdoc bootstrap-sass \
  && gem install --no-ri --no-rdoc zurb-foundation \
  && gem install --no-ri --no-rdoc semantic-ui-sass


# RUN apk del make\
#   && g++ \
#   && gcc

RUN rm -rf /var/cache/apk/*

EXPOSE 4242
EXPOSE 63342

WORKDIR /documents
VOLUME /documents

CMD ["/bin/bash"]
