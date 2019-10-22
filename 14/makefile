# executable files for this directory
OBJECTS = absInt.exe add.exe calc.exe directcall.exe \
		  fcnobj.exe newcount-size.exe readStr.exe

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I../1 -I../6

add.o directcall.o Sales_data.o: Sales_data.h

add.exe: add.o Sales_data.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) add.o Sales_data.o

directcall.exe: directcall.o Sales_data.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) directcall.o Sales_data.o

