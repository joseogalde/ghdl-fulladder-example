GHDL=ghdl
GTKWAVE=gtkwave
MODULES=\
    full_adder.vhd\
    full_adder_testbench.vhd

STD=synopsys
VSTD=93c
ENTITY=full_adder_testbench
GENERAL_OPTIONS=-g --mb-comments
RUN_OPTIONS=  --wave=${ENTITY}.ghw
all: ${ENTITY} test
test: $(ENTITY)
	$(GTKWAVE) ${ENTITY}.ghw ${ENTITY}.sav

${ENTITY}: ${MODULES}
	$(GHDL) -a ${GENERAL_OPTIONS} --std=${VSTD} --ieee=${STD} ${MODULES}
	$(GHDL) -r ${GENERAL_OPTIONS} --std=${VSTD} --ieee=${STD} -fexplicit ${ENTITY} ${RUN_OPTIONS}

clean:
	rm -f *.o *_testbench *_testbench.vcd full_adder carry_ripple_adder work*.cf e*.lst *.ghw *.sav
