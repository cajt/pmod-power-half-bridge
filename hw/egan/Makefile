.PHONY: all clean

output/pdf/main-sch.pdf: main.kicad_sch
		kicad-cli sch export pdf --output "output/pdf/main-sch.pdf" main.kicad_sch

output/pdf/main-pcb.pdf: main.kicad_pcb
		kicad-cli pcb export pdf --output "output/pdf/main-pcb.pdf" -l B.Cu,Edge.Cuts,F.Cu main.kicad_pcb 

AP3602A.kicad_sym: AP3602A.csv 
		kipart -b AP3602A.csv -w -o AP3602A.kicad_sym

all: AP3602A.kicad_sym output/pdf/main-pcb.pdf output/pdf/main-sch.pdf

clean:
		rm -rf AP3602A.lib output/pdf/main-pcb.pdf output/pdf/main-sch.pdf
