#Tim Dufala
#CS434

EXE:=as2
REPORT:= Assignment2.pdf
#########################
#TARBALL VARIABLES
#########################

TARBALL:=${EXE}.tar.gz

#List of files to put in the tarball
FILES:=${EXE}.m iteration.png learn_rate.png regularization.png test.m train.m learn.m Makefile ${REPORT}

#########################
#PHONY TARGETS
#########################

.PHONY: all clean submit unpack cleantest

all: ${EXE}

clean:
	rm -rf ${wildcard regPlot.pdf ${TARBALL}}

#Used to submit source tree
submit:
	tar -cjvf ${TARBALL} ${FILES}

#Used to open submission
unpack:
	tar -xjf ${TARBALL}

#########################
#EXPLICIT TARGETS
#########################

${EXE}: ${EXE}.m
	matlab -r ${EXE}

#########################
#TEST TARGETS/VARIABLES
#########################
#Has all test information
#All files should be in ${TESTDIR}
#${TESTOUTPUT} should be made
include ${TESTMAKE}

#########################
#INCLUDE DEPENDENCY INFO
#########################

-include ${SOURCE:%.c=%.d}
