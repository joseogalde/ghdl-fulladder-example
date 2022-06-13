GHDL=ghdl
MODULES=\
    hello.vhdl

ENTITY=hello_world
all: ${ENTITY}

${ENTITY}: ${MODULES}
	$(GHDL) -a ${MODULES}
	$(GHDL) -r ${ENTITY}

clean:
	rm -f *.o   hello work*.cf e*.lst *.ghw *.sav *.vcd
