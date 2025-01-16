import time
import random
def poprawnaOdpowiedz(tekst):              #funkcja ktora sprawdza czy input jest poprawny i zgodny z trescia
    while True:
        user_input = input(tekst).strip().lower()
        if user_input in ["tak", "nie"]:
            return user_input
        else:
            print ("Podaj poprawną odpowiedź!")
wyniki = ['orzeł', 'reszka']
wylosowany_wynik = random.choice(wyniki)
print("************ Witamy w grze ************")
pytanie1 = poprawnaOdpowiedz("O godzinie 3:00 w nocy budzi Cię głośny dźwięk. Czy chcesz iść do kuchni sprawdzić co się stało? (tak/nie): ")
if pytanie1 == "tak":
    pytanie2 = poprawnaOdpowiedz("W kuchni włączone jest światło. Na krześle siedzi Twój kolega ze studiów. Czy podejmujesz z nim rozmowę? (tak/nie): ")
    if pytanie2 == "tak":
        pytanie3 = poprawnaOdpowiedz("Twój kolega wytłumaczył Ci, że włamał Ci się do mieszkania z tęsknoty za Tobą. Czy wybaczasz mu ten wybryk? (tak/nie): ")
        if pytanie3 == "tak":
            pytanie4 = poprawnaOdpowiedz("Rozmawiacie długie godziny, aż nadchodzi ranek. Jest jednak czwartek. Czy postanawiasz iść do pracy?: ")
            if pytanie4 == "tak":
                print ("W pracy przez wlane w siebie hektolitry kawy szef postanawia Cię zwolnić.")
            elif pytanie4 == "nie":
                print ("Twój szef Cię zwalnia, kolega okazał się być wysłannikiem szefa. To był test, którego nie zdałeś.")
        elif pytanie3 == "nie":
            pytanie5 = poprawnaOdpowiedz("Miedzy Tobą a twoim kolegą dochodzi do bojki, w wyniku której oboje lądujecie w szpitalu. Czy chcesz mieć łóżko obok niego? (tak/nie): ")
            if pytanie5 == "tak":
                print("Dochodzi między Wami do pojednania. Umawiacie się na spotkanie. Historia kończy się szczęśliwie.")
            elif pytanie5 == "nie":
                print("Dobra decyzja. Twój kolega to szaleniec, a od takich lepiej trzymać się z daleka.")
    elif pytanie2 == "nie":
        print ("Przez Twój brak kultury intruz postanawia, że o Twoim losie zadecyduje rzut monetą.")
        time.sleep (3)
        print (f"Wylosowany wynik: {wylosowany_wynik}")
        if wylosowany_wynik == "orzeł":
            pytanie6 = poprawnaOdpowiedz("Wypadł orzeł. Masz szczęście. Twój kolega zrezygnowany wychodzi z mieszkania. Czy idziesz za nim? (tak/nie): ")
            if pytanie6 == "tak":
                print("Znajomy znika za rogiem sąsiedniego budynku i już nigdy więcej go nie spotkasz.")
            elif pytanie6 == "nie":
                print("Wracasz spać, zastanawiając się czy to nie był po prostu wytwór twojej wyobraźni...")
        elif wylosowany_wynik == "reszka":
            pytanie7 = poprawnaOdpowiedz("Wypadła reszka. Masz pecha. Twój kolega otwiera lodówkę, po czym zabiera z niej Twój jutrzejszy obiad. Czy pozwalasz znajomemu na to? (tak/nie): ")
            if pytanie7 == "tak":
                print("Twój znajomy wychodzi z mieszkania, a historia kończy się wizją jutrzejszego obiadu na mieście.")
            elif pytanie7 == "nie":
                print("Intruz, w obawie przed Tobą, oddaje Ci jedzenie i ucieka z mieszkania. Zostałeś bohaterem własnego domu.")
elif pytanie1 == "nie":
        print("Zastanawiasz się czy iść spać dalej, czy iść do łazienki. Postanawiasz rzucić monetą.")
        time.sleep (3)
        print(f"Wylosowany wynik: {wylosowany_wynik}")
        if wylosowany_wynik == "orzeł":
            pytanie8 = poprawnaOdpowiedz("Wypadł orzeł. Idziesz spać dalej, jednak tym razem dzwoni Twój telefon. Czy odbierasz połączenie? (tak/nie): ")
            if pytanie8 == "tak":
                pytanie9 = poprawnaOdpowiedz("To twoja mama, przypominająca Ci o tym, że nie wziąłeś klopsików z domu. Czy obiecujesz jej przyjazd? (tak/nie): ")
                if pytanie9 == "tak":
                    print("Twoja mama jest ucieszona, a Ciebie czeka jeszcze kilka godzin snu. Dobranoc.")
                elif pytanie9 == "nie":
                    print("Twoja mama jest zdenerwowana na Ciebie i zamienia się w potwora, którego wrzasków musisz słuchać. Ostatecznie jednak budzisz się, a to wszystko okazało się być tylko złym snem.")
            elif pytanie8 == "nie":
                pytanie10 = poprawnaOdpowiedz("Po odrzuconym połączeniu zasypiasz. Rano do Twojego mieszkania puka sąsiadka. Czy otwierasz jej drzwi? (tak/nie): ")
                if pytanie10 == "tak":
                    print("Okazuje się, że to ona do Ciebie dzwoniła w nocy. Potrzebowała twojej pomocy w szukaniu jej zaginionego chomika.")
                elif pytanie10 == "nie":
                    print("Dopadają cię wyrzuty sumienia, po których dzwonisz do niej. Okazało się, że Twoja sąsiadka jest już martwa.")
        elif wylosowany_wynik == "reszka":
            pytanie11 = poprawnaOdpowiedz("Wypadła reszka. W łazience znajdujesz swojego kota. Poprosił Cię on o wyjście na spacer (jest Wigilia, dlatego przemówił ludzkim głosem). Czy wychodzisz z nim na zewnątrz? (tak/nie): ")
            if pytanie11 == "tak":
                pytanie12 = poprawnaOdpowiedz("Na nocnym spacerze z kotem spotykasz swojego dawnego nauczyciela od matematyki. Kradnie on twojego czworonożnego przyjaciela. Czy gonisz złodzieja? (tak/nie): ")
                if pytanie12 == "tak":
                    print ("Udaje Ci się go dopaść, a Twój kot już na zawsze jest tobie oddany.")
                elif pytanie12 == "nie":
                    print("Nagle budzisz się z tego koszmaru i nie dowierzasz, jak ktoś mógłby nie biec za swoim własnym kotem.")
            elif pytanie11 == "nie":
                pytanie13 = poprawnaOdpowiedz("Twój kot jest obrażony na Ciebie. Sam bierze klucze i wychodzi. Czy idziesz za nim? (tak/nie): ")
                if pytanie13 == "tak":
                    print("Przepraszasz swojego kota, po czym godzicie się ze sobą i wracacie do mieszkania. Historia kończy się szczęśliwie.")
                elif pytanie13 == "nie":
                    print("Twój kot ucieka w nieznane, a Ty już nigdy go nie zobaczysz. Postanawiasz wziąć psa, żebyś nie czuł się samotnie.")