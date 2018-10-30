FROM golang

RUN mkdir -p /go/src/github.com/lengocgiang/todos

ADD . /go/src/github.com/lengocgiang/todos

#RUN curl https://glide.sh/get | sh
RUN go get  github.com/canthefason/go-watcher
RUN go install github.com/canthefason/go-watcher/cmd/watcher

#RUN cd $GOPATH/src/github.com/lengocgiang/todos && glide install

ENTRYPOINT  watcher -run github.com/lengocgiang/todos/todo/cmd -watch github.com/lengocgiang/todos/todo
