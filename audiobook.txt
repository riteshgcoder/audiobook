import pyttsx3
import pyPDF2
book=open('python.pdf','rb')
pdfReader=pyPDF2.pdfFileReader(book)
pages=pdfReader.numpages
print(pages)
speaker=pyttsx3.init()
for num in range(1,pages):
    page=pdfReader.getpage(7)
    text=page.extractText()
    speaker.say(text)
    speaker.runAndWait()
