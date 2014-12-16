LINKER = gcc

#LIB = -L ./lib -lpower

OBJ_DIR = ../build
OBJS = $(OBJ_DIR)/*.o

SERVICE = service
SOFTBUS = softbus
EVS     = evs

EVS_OBJS = $(EVS)/*.o

EXECUTABLE = evsbin

.PHONY: all

all: $(OBJS) $(EVS_OBJS) $(EXECUTABLE)


$(OBJS):
	@echo "== making service ==" && cd $(SERVICE) && $(MAKE) all
	@echo "== making softbus ==" && cd $(SOFTBUS) && $(MAKE) all
	
$(EVS_OBJS):
	@echo "== making evs ==" && cd $(EVS) && $(MAKE) all

$(EXECUTABLE): $(OBJS) $(EVS_OBJS)
	@echo "== You are linking to generate final executable =="
	$(LINKER) -o $@ $^ 
	@echo "== Building completed, executable generated =="
	
clean:
	rm $(OBJS) $(EVS_OBJS) $(EXECUTABLE)


