CC ?= riscv64-nerves-linux-musl-gcc

source  = cvi_pinmux.c devmem.c
object  = $(source:%.cc=%.o)

CFLAGS += -march=rv64imafdc_zicsr_zifencei -mcmodel=medany -mabi=lp64d -static

all: $(object)
	$(CC) $(CFLAGS) $(object) -o cvi_pinmux

%.o: %.c
	$(CC) $(CFLAGS) -c $<

clean:
	$(RM) *.o cvi_pinmux
