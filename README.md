# test-setup

setup to test different features with sphinx-markdown-parser.

## usage

Installing the python dependecies needs `pandoc` installed locally.  To skip over this you can execute the pipenv install inside the container as well.

```
alias pdr='podman run  -ti --rm --security-opt label=disable --userns=keep-id  -v /home:/home  -e HOME=$HOME -w $(pwd)'
cd docs
pdr greyrook/cde-texlive:cbfa6f05455445fbdc86acc3c7d7945c42c61829 pipenv install --dev
pdr greyrook/cde-texlive:cbfa6f05455445fbdc86acc3c7d7945c42c61829 pipenv run make html singlehtml latexpdf
```