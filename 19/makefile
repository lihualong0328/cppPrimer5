# executable files for this directory
OBJECTS = bitfields.exe calc.exe dyn_cast.exe enum.exe enum-match.exe \
		  memFN-bind.exe typeid.exe useScreen.exe

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I ../14

Screen.o useScreen.o: Screen.h

useScreen.exe: useScreen.o Screen.o 
	$(CPP) $(CPPFLAGS) useScreen.o Screen.o 


