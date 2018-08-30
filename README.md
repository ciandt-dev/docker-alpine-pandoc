# Docker image of pandoc on alpine

The smallest image available on August 2018 to compile pdf from markdown with pandoc.

## How to use it

```shell
export suffix_file=local
export pdf_args="-V geometry:margin=1cm -V urlcolor=blue"
docker run -v $(pwd):/code -w /code ciandt/pandoc-alpine:latest pandoc README.md -o README-${suffix_file}.pdf ${pdf_args}
```
