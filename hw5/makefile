#./LinkedList  (or whatever you call the TARGET)

CC = g++
CXXFLAGS = -g -std=c++11

ODIR=obj
SRC=src
TEST=test
TARGET=LinkedList

_OBJ = LinkedList.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

_MAIN = main.o
MAIN = $(patsubst %,$(ODIR)/%,$(_MAIN))

$(ODIR)/%.o: $(SRC)/%.cpp
	mkdir -p $(ODIR)
	$(CC) -c -o $@ $< $(CXXFLAGS)

$(TARGET): $(OBJ) $(MAIN)
	$(CC) -o $@ $^ $(CFLAGS)

.PHONY:  clean

clean:
	rm -rf $(ODIR) *~ core
	rm $(TARGET)
