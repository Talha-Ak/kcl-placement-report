FROM qmcgaw/latexdevcontainer

# For svg importing
RUN apt-get install -y inkscape

RUN tlmgr install datetime2 datetime2-english
RUN tlmgr install svg koma-script trimspaces xcolor transparent pgf catchfile
RUN texhash
