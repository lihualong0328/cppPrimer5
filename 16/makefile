# executable files for this directory
OBJECTS = Array.exe array-parms4.exe \
		  compare.exe compareDef.exe compareSpec.exe \
		  debug.exe multiset.exe overloaded.exe overSpec.exe qm.exe \
		  SP.exe special.exe specialized.exe \
		  useBlob.exe useChcking.exe Vecmain.exe

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I../14

SP.o: DebugDelete.h

Vecmain.o: Vec.h

compareDef.exe: compareDef.o ../14/Sales_data.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) compareDef.o ../14/Sales_data.o 

qm.exe: qm.o build.o 
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) qm.o build.o 

specialized.exe: debug.cpp
	#$(CPP) /Fespecialized -D SPECIALIZED $(CPPFLAGS) $(LOCFLAGS) debug.cpp 
	$(CPP) -D SPECIALIZED $(CPPFLAGS) $(LOCFLAGS) debug.cpp 

overloaded.exe: debug.cpp
	#$(CPP) /Feoverloaded -D OVERCHAR $(CPPFLAGS) $(LOCFLAGS) debug.cpp 
	$(CPP) -D OVERCHAR $(CPPFLAGS) $(LOCFLAGS) debug.cpp 

debug.exe: debug.cpp
	$(CPP) -D DEBUG $(CPPFLAGS) $(LOCFLAGS) debug.cpp 

multiset.exe: multiset.o Sales_data.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) multiset.o Sales_data.o 
 

