FROM lambci/lambda:build-ruby2.5
RUN gem install ramsey_cop solargraph
ENV PATH="/var/runtime/bin:$PATH"
RUN yard gems
ENV SHELL /bin/bash
