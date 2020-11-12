%-crop.pdf: %.pdf
	pdfcrop $<

%-rotated.pdf: %.pdf
	pdftk $< cat 1-endeast output $@

network.pdf: network.svg
network-dmz.pdf: network-dmz.svg
network-layers.pdf: network-layers.svg
network-layers-packet.pdf: network-layers-packet.svg
network-layers-fw.pdf: network-layers-fw.svg
network-layers-dpi.pdf: network-layers-dpi.svg


.PHONY: clean
clean:
	${RM} *-crop.pdf
	${RM} network.pdf network.pdf_tex network-rotated.pdf
	${RM} network-dmz.pdf network-dmz.pdf_tex network-dmz-rotated.pdf
	${RM} network-layers.pdf network-layers.pdf_tex
	${RM} network-layers-packet.pdf network-layers-packet.pdf_tex
	${RM} network-layers-fw.pdf network-layers-fw.pdf_tex
	${RM} network-layers-dpi.pdf network-layers-dpi.pdf_tex


INCLUDE_MAKEFILES?=../../makefiles
include ${INCLUDE_MAKEFILES}/doc.mk
