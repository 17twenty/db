# Temporary Makefile just to handle early testing
C_FILES = nums.c
C_FLAGS = -I../../../include
CLEAN_FILES = ${O_FILES} cidr_nums *core .depend

L_FLAGS = -g -pipe -L../.. -lcidr

.include "../../Makefile.inc"

# This need to be after the include
all build: cidr_nums

LCIDR = ../../libcidr.so

cidr_nums: ${O_FILES} ${LCIDR}
	${CC} ${L_FLAGS} -o ${@} ${O_FILES}

${LCIDR}:
	(cd ../.. && make)
