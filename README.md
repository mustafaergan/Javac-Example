Tek bir claas derleyip çalistirilmasi göstereceksek

C:\Users\mustafa.ergan\Desktop\javac\JavacExample\single>javac Deneme1.java

C:\Users\mustafa.ergan\Desktop\javac\JavacExample\single>java Deneme1


Paket içersinde ki kodlarin derlenmesi ve çalistirilmasi

C:\Users\mustafa.ergan\Desktop\javac\JavacExample>javac paket\*.java

C:\Users\mustafa.ergan\Desktop\javac\JavacExample>java paket.Deneme1

javac \
-sourcepath src \
-your_jar_path/your.jar:. \
your_class_path/your.java \
-d classes


Javap Bize derlenmis class ilgili bilgileri verir.

javap -c Deneme1
