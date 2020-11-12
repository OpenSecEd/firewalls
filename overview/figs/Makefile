%-crop.pdf: %.pdf
	pdfcrop $<

network.pdf: network.svg
network-rotated.pdf: network.pdf
	pdftk $< cat 1-endeast output $@

network-layers.pdf: network-layers.svg


.PHONY: clean
clean:
	${RM} *-crop.pdf
	${RM} network.pdf network.pdf_tex network-rotated.pdf
	${RM} network-layers.pdf network-layers.pdf_tex


INCLUDE_MAKEFILES?=../../makefiles
include ${INCLUDE_MAKEFILES}/doc.mk
