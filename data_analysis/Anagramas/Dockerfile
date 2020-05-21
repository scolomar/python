#########################################################################
#      Copyright (C) 2020        Sebastian Francisco Colomar Bauza      #
#      SPDX-License-Identifier:  GPL-2.0-only                           #
#########################################################################
FROM alpine/git AS clone
WORKDIR /app
RUN git clone https://github.com/secobau/python
#########################################################################
FROM python:alpine AS production
WORKDIR /app
COPY --from=clone /app/python/data_analysis/Anagramas/anagramas.py script
ENTRYPOINT ["python"]
CMD ["script"]
#########################################################################
