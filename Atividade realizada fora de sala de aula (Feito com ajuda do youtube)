import speech_recognition as sr
import pyttsx3 
import datetime
import wikipedia
import pywhatkit

audio = sr.Recognizer()
maquina = pyttsx3.init()

def executa_comando():
    try:
        with sr.Microphone() as source:
            print ('ouvindo..')
            voz = audio.listen(source)
            comando = audio.recognize_google( voz, language='pt-BR')
            comando = comando.lower()
            if 'moana' in comando:
                comando = comando.replace('moana', '')
                maquina.say(comando)
                maquina.runAndWait()

    except:
        print('Microfone não está ok')

    return comando
    
def comando_voz_usuario():
        comando = executa_comando()
        if 'horas' in comando:
            hora = datetime.datetime.now().strftime('%H:%M')
            maquina.say('Agora são' + hora)
            maquina.runAndWait()
        elif 'o que é' in comando:
             procurar = comando.replace('o que é', '')
             wikipedia.set_lang('pt')
             resultado = wikipedia.summary(procurar,3)
             print(resultado)
             maquina.say(resultado)
             maquina.runAndWait()

        elif 'quem é' in comando:
             procurar = comando.replace('quem é', '')
             wikipedia.set_lang('pt')
             resultado = wikipedia.summary(procurar,3)
             print(resultado)
             maquina.say(resultado)
             maquina.runAndWait()

        elif 'quem foi' in comando:
             procurar = comando.replace('quem foi', '')
             wikipedia.set_lang('pt')
             resultado = wikipedia.summary(procurar,3)
             print(resultado)
             maquina.say(resultado)
             maquina.runAndWait()
        elif 'toque no youtube' in comando:
             musica = comando.replace('toque', '')
             resultado = pywhatkit.playonyt(musica)
             maquina.say('abrindo a' + musica + 'no youtube')
             maquina.runAndWait()
            
comando_voz_usuario()

