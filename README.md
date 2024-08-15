# Filemerger
Developed a Python script to automate file merging, efficiently combining multiple files into a single, cohesive document. This tool supports various file formats, reduces manual effort, and eliminates errors in data consolidation. Ideal for streamlining workflows and saving time, especially when handling large volumes of data. #Python 


from PyPDF2 import PdfMerger
import os

#enter your file include path
pdfs=[ "C:\mywork\python\experiment_dl\salman_cv_new.pdf","c:\mywork\python\experiment_dl\Salmancv_old.pdf", "c:\mywork\python\experiment_dl\zakcv_old.pdf"]

merger=PdfMerger()

for pdf in pdfs:
    merger.append(pdf)

merger.write("C:\mywork\python\experiment_dl/new.pdf")
merger.close()
