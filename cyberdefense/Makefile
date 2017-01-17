WINCFLAGS= \
	-ffast-math \
	-O3 \
	-std=gnu11 \
	-mmmx -msse -msse2 -msse3 -msse4a -mssse3 -mfpmath=sse \
	-falign-functions -falign-jumps -falign-labels -falign-loops \
	-fbranch-probabilities -fbranch-target-load-optimize2 \
	-fcprop-registers \
	-fcrossjumping \
	-finline-functions -finline-small-functions \
	-fipa-matrix-reorg \
	-fmodulo-sched \
	-fpeephole2 -fpeephole \
	-fpeel-loops \
	-foptimize-sibling-calls \
	-foptimize-register-move \
	-frounding-math \
	-fsel-sched-pipelining \
	-funsafe-math-optimizations \
	-funsafe-loop-optimizations \
	-funroll-all-loops \
	-masm=intel -m3dnow -mtune=core2 \
	-Ibass 	

MACCFLAGS= \
	-ffast-math \
	-O3 \
	-std=gnu11 \
	-mmmx -msse -msse2 -msse3 -msse4a -mssse3 -mfpmath=sse \
	-foptimize-sibling-calls \
	-funsafe-math-optimizations \
	-masm=intel -m3dnow -mtune=core2 \
	-Ibass
	
OBJECTS=cityscape2.o \
	cityscape3.o \
	tower.o \
	livingroom.o \
	rasterize.o \
	fixedmath.o \
	enemy.o \
	ringworld.o \
	core.o \
	main.o
	
all: $(OBJECTS)
	gcc $(OBJECTS) $(WINCFLAGS) -Lbass -lbass -lm -lGL -lglut -lGLU -o cyberdefense
	
mac: $(OBJECTS)
	gcc $(OBJECTS) $(MACCFLAGS) -Lbass -lbass -lm -framework GLUT -framework OpenGL -o cyberdefense

clean:
	rm -r *.o
	rm cyberdefense
