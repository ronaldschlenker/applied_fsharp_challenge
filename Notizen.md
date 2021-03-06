
Aufbau nach Einleitung:

* Anhang von Blockschaltbildern zeigen, was die Problematik ist.
    * Pure
    * Eigener State
    * Arbeiten auf Werten und Vergangenheitswerten ("fold")
    * Rückkopplungen (Feedback) - "Oh, this has nothing to do with FP
    * Closures: Der Ausgang eines Blocks soll im folgenden Netzwern beliebig verwendet werden können

Sonstiges
* "Inline" Rechnen mit F-Monaden (Plus, Minus, Multiplikation)
* Konzept in Abgrenzung zu FRP
* Control Rate and Audio Rate
* State (Block mit „X“) pop -> state as local feedback 
    * Oop Beispiel: vorher im FP Beispiel zeigen, dass ein Effekt eine Factory ist. Bei oop ist das mit State dann doof, weil wir immer erst Parameter setzen müssen.


Begriffe
---
circuit, network -> computation





Sonstiges
---
mix: params sollen nicht original und processed heien, sondern a und b
* Mehr zu Typinferenz sagen (Seite 2 oder so)

Soll ich wirklich so viel dazu sagen, dass float->float so wichtig ist? Ist ja gar nicht soooo wichtig.

* Generell viel mehr Zwischenüberschriften einfügen

* Kurze EInführung in F#
    * Function evaluation
    * Precedence: myList |> rest a
    * Infix operators
    * |> und >>
    * A word on sequences and List and Array

* TLDR: Instead of writing ... we can write ... (Keine Instanziierung; keine Evaluierung)


Counter: In OOP, there is a disadvantage: We couldn't modulate the desiredSampleLength parameter. Now, we can!

* Anhang:
    * Alternative: Man hätte auch einen Dictionary passing Ansatz wählen können - Performance
    * FETT: "Instead of identifying "things" by a name or by a reference pointer, we identify them by their position inside of a structure."

Öfter mal "Key Points" am Ende von Sektionen machen bzw. am Anfang.

Exkurs: What is state? State is made up of a bunch of things:
    A location in a global space
    A value that resides in that location
    The location can be accessed (read or written) from several other points
    Mutation is necessary (beause if not; copy would be suficcient)

Nochmal rausarbeiten, warum Currying hilfreich ist (Currying as factory methods)
    Ein Block mit 2 Inputs zeichnen; das ist eine curried function (von unten nach oben)

Einleitung: We are interested in a comprehensive way of expressing signal flows.

Vorwissen: Woher bekommt man das?
    Oder kurz in den Anhang nehmen, was interessant ist.
    Writing functions
    Types
    Applying functions
    Currying
    FSI / VS Code / Ionide
    >> |> and custom operators
    kein return -> dafür let..in expressions


Nesting patches

* i -> input
* Alle Codebeispiele auf Korrektheit prüfen
* patch -> coputation

* Identify a stateful thing not by reference, but by a given datastructure + a relative position.
* Zuerst nochmal Blockdiagram anschauen
* Rückkopplung kann gesehen werden als Value+State -> Value+State
* Strategie ist: "Pick up and Delivery"
* Das Ziel nochmal in Code beschreiben:
    * Nochmal das Beispiel mit einer puren Funktion anschauen
    * Das geht aber so nicht; State fehlt.

Am Ende:
* Wir haben hier float als Value; könnten wir aber generalisieren.

Type signatures:
    We make things inline to leave out signatures:

Signature in den Codebeispielen reinnehmen

Vorwort: Etwas über FluX erzählen

last -> previous (state)

Reader State (env)

Result -> Output

TODOs

BlendedDistortion - das existiert in so vielen Versionen - welches gilt denn nun?

chapter -> ?

---

IO - irgendwann muss es den Übergang geben auf die Soundkarte.
Abgrenzung zu Observables
Sequence of values is equal to a stream. It is continuous and doesn't have to be persisted into memory.
Anforderung: Easily composable
Zum Schluss: Reduce benutzen als Runtime



* Why Time is not enough
* Generators (sinus)
    * Example-Links an die jeweiligen Stellen einbauen
* Alternative Composition / Modulation
* Fazit
* Die Codes im Artikel sind teilweise noch veraltet?
* About the author
* Erklären: Diese Technik kann man für vieles einsetzen und sie ist nicht gebunden an Audio, da ein Signal nur ein sich über die Zeit ändernder Wert ist
* <em> tag anders formatieren
* 