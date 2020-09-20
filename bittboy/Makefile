# gpSP makefile
# Gilead Kutnick - Exophase
# pandora port - notaz
# respberry pi - DPR

# Global definitions

CC        = /opt/bittboy-toolchain/usr/bin/arm-linux-gcc

OBJS      = main.o cpu.o memory.o video.o input.o sound.o gui.o \
            cheats.o zip.o arm_stub.o  warm.o cpu_threaded.o video_blend.o sha1.o imageio.o

BIN       = gpsp

# Platform specific definitions 

VPATH      += .. ../arm
CFLAGS     += -DARM_ARCH -DPC_BUILD -DBITTBOY -Wall
CFLAGS     += -Ofast -fdata-sections -ffunction-sections -fsingle-precision-constant -fno-PIC -flto -march=armv5te -mtune=arm926ej-s -fprofile-generate=./profile
CFLAGS     += `/opt/bittboy-toolchain/arm-buildroot-linux-musleabi/sysroot/usr/bin/sdl-config --cflags`

# expecting to have PATH set up to get correct sdl-config first

LIBS       = -nodefaultlibs -lc -lgcc -lSDL -lpng -lasound -lz -Wl,--as-needed -Wl,--gc-sections -flto -s

# Compilation:

all: $(BIN)

%.o: %.S
	$(CC) $(CFLAGS) -c -o $@ $<


cpu.o cpu_threaded.o: CFLAGS += -Wno-unused-variable -Wno-unused-label

$(BIN): $(OBJS)
	$(CC) $(OBJS) $(LIBS) -o $(BIN)

clean:
	rm -f *.o $(BIN)
