LIB = libfast_trigo.a
OBJ = fast_trigo.o
TARGET = main

# Regole
all: $(TARGET)

$(LIB): $(OBJ)
    ar rcs $@ $^

$(OBJ): fast_trigo.c fast_trigo.h
    gcc -c fast_trigo.c -o $@

$(TARGET): main.c $(LIB)
    gcc main.c -L. -lfast_trigo -o $(TARGET)

clean:
    rm -f $(OBJ) $(LIB) $(TARGET)