ROOTLIBS  = `root-config --libs`
ROOTFLAGS = `root-config --cflags --glibs`
#SPECIALFLAGS= --exceptions
CFLAGS = -I.
RCXX =$(DELPLIBS) $(EXTLIBS) $(CFLAGS) $(ROOTFLAGS) $(ROOTLIBS)


DBG = -g -O2
CC = g++ $(DBG) $(RCXX)
SRC = src
UTILS= utils
INCLUDE = include
LIBS= lib
BIN= bin


all: SigBkgNtupleMaker main


SigBkgNtupleMaker: $(SRC)/SigBkgNtupleMaker.cxx
	$(CC) -o $(LIBS)/SigBkgNtupleMaker.o -c $(SRC)/SigBkgNtupleMaker.cxx

main: $(SRC)/main.cxx
	$(CC) -o $(BIN)/NtupleMaker $(SRC)/main.cxx $(LIBS)/SigBkgNtupleMaker.o

clean:
	@rm $(EXEC)
