# executable files for this directory
OBJECTS = Animal.exe book.exe class.exe \
		  ex-over.exe inherit.exe mi-scope.exe\
		  over.exe over2.exe \
		  usingDirective.exe virt-inherit.exe

# tells make to use the file "..\MS_makefile_template", which
# defines general rules for making .obj and .exe files
include ../MS_makefile_template

LOCFLAGS = -I ../14

Animal.o: Animal.h
book.o: ../14/Sales_data.h bookexcept.h
virt-inherit.o: Animal_virtual_baseVers.h

book.exe: book.o bookexcept.h ../14/Sales_data.o
	$(CPP) $(CPPFLAGS) $(LOCFLAGS) book.o ../14/Sales_data.o 
