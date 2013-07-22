all: paper

# Really clean should clean here and in subdirectories
# Most notably it should at least clean .blg and .bbl files
clean:
	-rm -f *.aux *.log *.dvi *.blg *.bbl *.inx *.aut *.toc *.out 
#	-rm -f */*.aux */*.log */*.dvi */*.blg */*.bbl */*.inx */*.aut */*.toc */*.out 
	-rm -f */*.aux */*.log */*.dvi */*.blg */*.inx */*.aut */*.toc */*.out 
	-rm -f */*/*.aux */*/*.log */*/*.dvi */*/*.blg */*/*.bbl */*/*.inx */*/*.aut */*/*.toc */*/*.out 

cleanall: clean
	-rm -f */chapter.pdf */chapter.ps *~ */*~

TEXFILES = *.tex */*.tex */*/*.tex
BIBFILES = */*/*.bib

paper: pdf

pdf: subaru_ngao_SR_en.pdf

subaru_ngao_SR_en.dvi: clean subaru_ngao_SR_en.tex $(BIBFILES) $(TEXFILES)
	platex subaru_ngao_SR_en.tex
	bibtex science/veryhighz/nbf
#	bibtex science/koyama/ykoyama
#	bibtex science/saito/saito
#	bibtex science/shibuya/shibuya
#	bibtex science/imanishi/ImanishiSJ
#	bibtex science/yasui/yasui
#	bibtex science/nishiyama/nishi
#	bibtex science/iwata/ngao_spec_simulation
#	bibtex science/iwata/legacy_survey
#	bibtex science/iwata/nbf
#	bibtex science/pyo/pyo
#	bibtex science/fukagawa/fukagawa
#	bibtex science/chiba/chiba
#	bibtex simulation/glao/oya
#	bibtex simulation/moao/akiyama
#	bibtex project/hayano/system_design
	platex subaru_ngao_SR_en.tex
	platex subaru_ngao_SR_en.tex
	platex subaru_ngao_SR_en.tex

subaru_ngao_SR_en.pdf: subaru_ngao_SR_en.dvi
#	dvipdfmx -s 1-11 subaru_ngao.dvi
	dvipdfmx subaru_ngao_SR_en.dvi

