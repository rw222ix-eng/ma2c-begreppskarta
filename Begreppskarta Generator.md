/*
# Begreppskarta Generator
Genererar en komplett begreppskarta for Ma 2c Kapitel 2.
```js*/

// Begreppskarta Ma 2c Kapitel 2 - v8
const X_GAP = 700;
const BASE_H = 90;
const LINE_H = 22;
const Y_SPACE = 160;
const BRANCH_GAP = 150;
const PH_GAP = 380;

const C = [
  { s: "#c92a2a", b: "#fff5f5" }, // 0 Ekvationer
  { s: "#1864ab", b: "#e7f5ff" }, // 1 Funktioner
  { s: "#2b8a3e", b: "#ebfbee" }, // 2 Logaritmer
  { s: "#862e9c", b: "#f8f0fc" }, // 3 Regression
];

// NODE REGISTRY (for cross-references)
const REG = {};

const T = {
  t: "Ma 2c \u2013 Kapitel 2\nAlgebra &\nicke-linj\u00e4ra modeller",
  c: [
    // ========================
    // EKVATIONER (H\u00d6GER UPP)
    // ========================
    { t: "EKVATIONER\n\nAtt l\u00f6sa ekvationer\n= hitta v\u00e4rdet p\u00e5 x\nsom g\u00f6r att b\u00e5da\nsidor blir lika.", side: "R", ci: 0, lbl: "att l\u00f6sa", c: [

      { t: "ANDRAGRADSEKVATIONER\n\nEkvationer d\u00e4r h\u00f6gsta\npotensen av x \u00e4r 2.\n\nFormen: ax\u00b2 + bx + c = 0\n\u2022 a = talet framf\u00f6r x\u00b2 (ej 0)\n\u2022 b = talet framf\u00f6r x\n\u2022 c = konstanten\n\nEx: 3x\u00b2 - 5x + 2 = 0\na=3, b=-5, c=2\n\nKan ha 0, 1 eller 2 l\u00f6sningar.", ref: "aeq", lbl: "högsta potens x²", c: [

        { t: "PQ-FORM\n\nSamma ekvation, omskriven\ns\u00e5 talet framf\u00f6r x\u00b2 = 1:\nx\u00b2 + px + q = 0\n\n\u2022 p = talet framf\u00f6r x (efter\n  division med a)\n\u2022 q = konstanten (efter\n  division med a)\n\nHUR: Dividera hela ekvationen\nmed talet framf\u00f6r x\u00b2.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\n2x\u00b2 + 6x - 8 = 0\nDividera med 2:\nx\u00b2 + 3x - 4 = 0\np = 3, q = -4", ref: "pqform", lbl: "skrivs om till" },

        { t: "KVADRATKOMPLETTERING\n\nMetod: G\u00f6r om x\u00b2+px\ntill en hel kvadrat.\n\n1. Se till att 1 st\u00e5r framf\u00f6r x\u00b2\n2. Flytta konstanten till h\u00f6gerledet\n3. Halvera talet framf\u00f6r x,\n   kvadrera, l\u00e4gg till b\u00e5da sidor\n4. V\u00e4nsterledet = perfekt kvadrat\n5. Dra roten\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nL\u00f6s: x\u00b2 + 6x + 5 = 0\nx\u00b2 + 6x = -5\nTalet framf\u00f6r x = 6.\n6/2 = 3, 3\u00b2 = 9\nx\u00b2 + 6x + 9 = -5 + 9\n(x + 3)\u00b2 = 4\nx + 3 = \u00b12\nx = -1 eller x = -5", ref: "kvkomp", lbl: "l\u00f6ses med" },

        { t: "PQ-FORMELN\n\nFormel som direkt ger svaret\np\u00e5 x\u00b2 + px + q = 0\n\n\u2022 p = talet framf\u00f6r x\n\u2022 q = konstanten\n\nFormeln:\nx = -p/2 \u00b1 \u221a((p/2)\u00b2 - q)\n\nKRAV: Talet framf\u00f6r x\u00b2\nm\u00e5ste vara 1 f\u00f6rst!\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nL\u00f6s: x\u00b2 - 2x - 3 = 0\np = -2, q = -3\n\nx = -(-2)/2 \u00b1 \u221a((-2/2)\u00b2-(-3))\nx = 1 \u00b1 \u221a(1 + 3)\nx = 1 \u00b1 2\nx = 3 eller x = -1\n\nNegativt under roten = inga svar\nNoll under roten = ett svar", ref: "pqformel", lbl: "l\u00f6ses med" },
      ]},

      { t: "ROTEKVATIONER\n\nEkvationer d\u00e4r x st\u00e5r\nunder ett rottecken.\nT.ex. \u221a(x+3) = 5\n\nVIKTIGT: Kvadrering\nkan skapa falska svar.\nKontrollera ALLTID!", ref: "roteq", lbl: "x under rottecken", c: [

        { t: "METOD\n\n1. Isolera roten\n   (f\u00e5 den ensam p\u00e5 en sida)\n2. Kvadrera b\u00e5da sidor\n   (tar bort rottecknet)\n3. L\u00f6s ekvationen som uppst\u00e5r\n   (ofta med pq-formeln)\n4. KONTROLLERA i original-\n   ekvationen!\n\n\u2500\u2500 EXEMPEL \u2500\u2500\n\u221a(2x+1) = x - 1\nKvadrera: 2x+1 = (x-1)\u00b2\n2x+1 = x\u00b2-2x+1\n0 = x\u00b2-4x = x(x-4)\nx = 0 eller x = 4\n\nKontroll:\nx=0: \u221a1=1 \u2260 -1 FALSK!\nx=4: \u221a9=3 = 3 OK!\nSvar: x = 4", ref: "rotmetod", lbl: "l\u00f6ses med" },

        { t: "FALSK ROT\n\nEtt svar som INTE st\u00e4mmer\nn\u00e4r man stoppar in det i\noriginalekvationen.\n\nVARF\u00d6R?\nKvadrering d\u00f6ljer minustecken:\nB\u00e5de 3\u00b2=9 och (-3)\u00b2=9.\nS\u00e5 kvadrering kan \"skapa\"\nl\u00f6sningar som inte fanns.\n\n\u2500\u2500 EGET EXEMPEL \u2500\u2500\nL\u00f6s: \u221a(x) = x - 6\nKvadrera: x = x\u00b2-12x+36\nx\u00b2-13x+36 = 0\np=-13, s\u00e5 p/2 = -6,5\nAllts\u00e5 -p/2 = 6,5\nx = 6,5 \u00b1 \u221a(42,25-36)\nx = 6,5 \u00b1 2,5\nx = 9 eller x = 4\n\nx=9: \u221a9=3, 9-6=3 OK!\nx=4: \u221a4=2, 4-6=-2\n  2\u2260-2 FALSK!\n\nSvar: Bara x = 9.", ref: "falskrot", lbl: "kan ge",
          ph: "[Bild: falsk rot\nexempel]" },

        { t: "KONTROLL\n\nS\u00e4tt ALLTID in svaret i\nden URSPRUNGLIGA ekvationen\n(inte den kvadrerade!).\n\n1. Ta ditt x-v\u00e4rde\n2. Ber\u00e4kna v\u00e4nsterledet\n3. Ber\u00e4kna h\u00f6gerledet\n4. Lika = r\u00e4tt, Olika = falsk rot\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nEkvation: \u221a(3x+4) = x\nVi fick x=4 och x=-1\n\nx=4: \u221a(16) = 4, h\u00f6gerled=4\n  4=4 St\u00e4mmer!\nx=-1: \u221a(1) = 1, h\u00f6gerled=-1\n  1\u2260-1 Falsk rot!\n\nSvar: Bara x = 4.\nHoppa ALDRIG \u00f6ver detta!", ref: "kontroll", lbl: "kr\u00e4ver alltid" },
      ]},

      { t: "EXPONENTIALEKVATION\nx sitter i EXPONENTEN\n\nT.ex. 5\u02e3 = 200\n\nMetod: Ta lg av b\u00e5da sidor.\nPotensregeln plockar ner x:\nlg(a\u02e3) = x \u00b7 lg(a)\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nL\u00f6s: 5\u02e3 = 200\nlg(5\u02e3) = lg(200)\nx \u00b7 lg(5) = lg(200)\nx = lg(200)/lg(5)\nx = 2,301/0,699 \u2248 3,29\n\nKontroll: 5^3,29 \u2248 200", ref: "expeq", lbl: "x i exponenten" },

      { t: "POTENSEKVATION\nx sitter i BASEN\n\nT.ex. x\u2075 = 200\n\nMetod: Upph\u00f6j till 1/n\n(dra n:te roten).\nH\u00c4R LOGARITMERAR MAN INTE!\n\n\u2500\u2500 EXEMPEL 1 \u2500\u2500\nL\u00f6s: x\u00b3 = 64\nx = 64^(1/3) = 4\nKontroll: 4\u00b3 = 64\n\n\u2500\u2500 EXEMPEL 2 \u2500\u2500\nL\u00f6s: x\u00b2 = 25\nx = \u00b1\u221a25 = \u00b15\nOBS: J\u00e4mn exponent\nger TV\u00c5 svar!", ref: "poteq", lbl: "x i basen" },
    ]},

    // ========================
    // REGRESSION (H\u00d6GER NER)
    // ========================
    { t: "REGRESSION\n\nHitta den matematiska\nformel som b\u00e4st passar\nen samling m\u00e4tpunkter.\n\nAnv\u00e4nds med grafr\u00e4knare\neller datorprogram.", side: "R", ci: 3, lbl: "att anpassa", c: [

      { t: "REGRESSIONSANALYS\n\n1. Samla m\u00e4tv\u00e4rden (x, y)\n2. Plotta punkterna\n3. V\u00e4lj modelltyp efter form:\n   Rak \u2192 linj\u00e4r\n   Kulle/dal \u2192 andragrad\n   Snabb \u00f6kning \u2192 exponentiell\n4. K\u00f6r regression p\u00e5 kalkylator\n   STAT \u2192 CALC \u2192 v\u00e4lj typ\n5. L\u00e4s av r\u00b2\n6. Prova andra modeller\n7. V\u00e4lj h\u00f6gst r\u00b2",
        ref: "regan", lbl: "hur man g\u00f6r",
        ph: "[Bild: datapunkter\n+ anpassad kurva]" },

      { t: "MODELLVAL & r\u00b2\n\nr\u00b2 = determinationskoefficient\nEtt tal 0\u20131 som visar hur\nbra modellen passar data.\n\nr\u00b2 = 1,00 \u2192 Perfekt\nr\u00b2 = 0,95 \u2192 Mycket bra\nr\u00b2 = 0,80 \u2192 Ganska bra\nr\u00b2 = 0,50 \u2192 D\u00e5lig\n\nOBS: H\u00f6gt r\u00b2 betyder bara\natt modellen PASSAR datan.\nDet betyder inte att modellen\n\u00e4r r\u00e4tt f\u00f6r att f\u00f6ruts\u00e4ga\nsaker utanf\u00f6r dataintervallet.\n\nTips: Prova alla modelltyper,\nv\u00e4lj h\u00f6gst r\u00b2.", ref: "modval", lbl: "utv\u00e4rderas med" },

      { t: "MODELLTYPER\n\n1. LINJ\u00c4R: y = kx + m\n   Rak linje, j\u00e4mn \u00e4ndring\n   Ex: l\u00f6n +1000 kr/\u00e5r\n\n2. ANDRAGRAD: y = ax\u00b2+bx+c\n   Parabel, kulle/dal\n   (a framf\u00f6r x\u00b2, b framf\u00f6r x,\n    c konstant)\n   Ex: bollkastning\n\n3. EXPONENTIELL: y = C\u00b7a\u02e3\n   (C startv\u00e4rde, a \u00e4ndringsfaktor)\n   Procentuell \u00e4ndring per steg\n   Ex: r\u00e4nta, befolkning\n\n4. POTENS: y = a\u00b7x^b\n   Naturlag, fysik\n   Ex: bromstr\u00e4cka", ref: "modtyp", lbl: "v\u00e4ljer bland" },
    ]},

    // ========================
    // FUNKTIONER (V\u00c4NSTER UPP)
    // ========================
    { t: "FUNKTIONER\n\nEn funktion beskriver\nhur y beror av x.\nVarje x-v\u00e4rde ger\nexakt ett y-v\u00e4rde.\n\nGrafen visar sambandet\nmellan x och y.", side: "L", ci: 1, lbl: "att beskriva", c: [

      { t: "ANDRAGRADSFUNKTIONER\n\nFunktioner d\u00e4r x\u00b2 \u00e4r h\u00f6gsta\npotens. Skrivs:\ny = ax\u00b2 + bx + c\n\n\u2022 a = framf\u00f6r x\u00b2 (riktning/bredd)\n\u2022 b = framf\u00f6r x\n\u2022 c = konstant = y-sk\u00e4rning\n\nGrafen kallas PARABEL.\n\nEx: y = x\u00b2 - 6x + 8\na=1, b=-6, c=8\nSk\u00e4r y-axeln i (0, 8).", ref: "agf", lbl: "y = ax\u00b2+bx+c", c: [

        { t: "KOEFFICIENTEN a\nI y = ax\u00b2+bx+c\n\n'a' = talet framf\u00f6r x\u00b2\n\nBest\u00e4mmer TV\u00c5 saker:\n1. Riktning (upp/ner)\n2. Bredd (smal/bred)", ref: "koeffa", lbl: "styrs av", c: [
          { t: "a > 0: GLAD MUN\n\nI y = ax\u00b2+bx+c \u00e4r 'a'\ntalet framf\u00f6r x\u00b2.\n\nN\u00e4r a \u00e4r positivt\n\u00f6ppnar parabeln UPP\u00c5T (U).\nHar en MINIMIPUNKT.\n\nVARF\u00d6R? N\u00e4r x \u00e4r stort\nblir a\u00b7x\u00b2 stort positivt\n\u2192 grafen g\u00e5r upp\u00e5t.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = 2x\u00b2-4x+1, a=2>0\nx=-1: y=7\nx= 1: y=-1 (botten)\nx= 3: y=7\nU-form!", ref: "apos", lbl: "om positivt",
            ph: "[Bild: glad\nparabel]" },
          { t: "a < 0: LEDSEN MUN\n\nI y = ax\u00b2+bx+c \u00e4r 'a'\ntalet framf\u00f6r x\u00b2.\n\nN\u00e4r a \u00e4r negativt\n\u00f6ppnar parabeln NED\u00c5T (n).\nHar en MAXIMIPUNKT.\n\nVARF\u00d6R? N\u00e4r x \u00e4r stort\nblir a\u00b7x\u00b2 stort NEGATIVT\n\u2192 grafen g\u00e5r ner\u00e5t.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = -x\u00b2+4x-1, a=-1<0\nx=0: y=-1\nx=2: y=3 (topp)\nx=4: y=-1\nn-form!", ref: "aneg", lbl: "om negativt",
            ph: "[Bild: ledsen\nparabel]" },
          { t: "BREDD\n\nI y = ax\u00b2+bx+c\nbest\u00e4mmer storleken\np\u00e5 |a| (a utan minus)\nhur BRED parabeln \u00e4r.\n\nStort |a| = SMAL\nLitet |a| = BRED\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny=5x\u00b2  (smal)\ny=x\u00b2   (normal)\ny=0,2x\u00b2 (bred)\n\nLogik: stort |a| g\u00f6r\natt y v\u00e4xer snabbt\n\u2192 brant, smal form.", ref: "bredd", lbl: "best\u00e4mmer" },
        ]},

        { t: "SYMMETRILINJE\n\nLodr\u00e4t linje som delar\nparabeln i tv\u00e5 lika halvor.\n\nI y = ax\u00b2+bx+c:\nFormel: x = -b/(2a)\n\u2022 b = talet framf\u00f6r x\n\u2022 a = talet framf\u00f6r x\u00b2\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = 2x\u00b2-8x+3\na=2, b=-8\nx = -(-8)/(2\u00b72) = 8/4 = 2\n\nSymmetrilinjen \u00e4r x = 2.\nExtrempunkten ligger d\u00e4r.", ref: "sym", lbl: "har en",
          ph: "[Bild: vertikal\nspegellinje]" },

        { t: "EXTREMPUNKT &\nEXTREMV\u00c4RDE\n\nPunkten d\u00e4r parabeln v\u00e4nder.\n\nExtremPUNKT = (x, y)\nExtremV\u00c4RDE = bara y\n\na>0 \u2192 minimipunkt\na<0 \u2192 maximipunkt\n\nI y = ax\u00b2+bx+c:\n1. x = -b/(2a)\n2. S\u00e4tt in x i funktionen\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = 2x\u00b2-8x+3\na=2, b=-8\nx = -(-8)/(2\u00b72) = 2\ny = 2\u00b74-8\u00b72+3 = -5\n\nExtrempunkt: (2, -5)\nExtremv\u00e4rde: -5 (minimum)", ref: "ext", lbl: "har en",
          ph: "[Bild: vertex\nmarkerad]" },

        { t: "NOLLST\u00c4LLEN\n\nDe x-v\u00e4rden d\u00e4r y = 0\n(d\u00e4r grafen korsar x-axeln).\n\nHitta dem: S\u00e4tt y = 0\ni y = ax\u00b2+bx+c\noch l\u00f6s med pq-formeln.\n\nAntal:\nPositivt under roten \u2192 2 st\nNoll under roten \u2192 1 st\nNegativt \u2192 inga\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = x\u00b2-5x+6\nx\u00b2-5x+6 = 0\np=-5, q=6\nx = 2,5 \u00b1 \u221a(6,25-6)\nx = 2,5 \u00b1 0,5\nx=2 och x=3\nGrafen korsar x-axeln\ni (2,0) och (3,0).", ref: "noll", lbl: "kan ha 0\u20132",
          ph: "[Bild: parabel\nsk\u00e4r x-axeln]" },

        { t: "FAKTORFORM\n\nAnnat s\u00e4tt att skriva\nfunktionen d\u00e4r nollst\u00e4llena\nsyns direkt.\n\nI y = ax\u00b2+bx+c d\u00e4r\na = talet framf\u00f6r x\u00b2 och\nx1,x2 = nollst\u00e4llena:\n\ny = a(x-x1)(x-x2)\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = x\u00b2-5x+6\nNollst\u00e4llen: x=2, x=3, a=1\ny = (x-2)(x-3)\n\nKontroll:\n(x-2)(x-3)\n= x\u00b2-3x-2x+6\n= x\u00b2-5x+6 St\u00e4mmer!", ref: "fakt", lbl: "kan skrivas i" },

        { t: "TILL\u00c4MPNINGAR\n\ny = ax\u00b2+bx+c beskriver\nverkliga situationer:\n\n\"Hur h\u00f6gt?\" \u2192 extremv\u00e4rde\n\"N\u00e4r landar?\" \u2192 nollst\u00e4lle\n\"H\u00f6jd efter 2s?\" \u2192 f(2)\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nBollens h\u00f6jd:\nh = -5t\u00b2+20t+1,5\n(a=-5, b=20, c=1,5)\n\nMaxh\u00f6jd?\nt = -20/(2\u00b7(-5)) = 2\nh(2) = -20+40+1,5 = 21,5 m\nBollen n\u00e5r 21,5 m efter 2 s.", ref: "tillamp", lbl: "anv\u00e4nds i" },
      ]},

      { t: "EXPONENTIALFUNKTIONER\ny = C \u00b7 a\u02e3\n\n\u2022 C = startv\u00e4rde (y vid x=0)\n\u2022 a = f\u00f6r\u00e4ndringsfaktor\n\u2022 x = antal steg\n\nAnv\u00e4nds n\u00e4r n\u00e5got \u00e4ndras\nmed fast PROCENT per steg.\nT.ex. r\u00e4nta, befolkning.", ref: "expf", lbl: "y = C\u00b7a\u02e3", c: [

        { t: "F\u00d6R\u00c4NDRINGSFAKTOR (a)\n\nI y = C\u00b7a\u02e3 \u00e4r 'a' det\ntal som y multipliceras\nmed f\u00f6r varje steg i x.\n\n\u00d6kning p%: a = 1 + p/100\nMinskning p%: a = 1 - p/100\n\na > 1 = tillv\u00e4xt\na = 1 = of\u00f6r\u00e4ndrat\n0 < a < 1 = avtagande\n\n\u2500\u2500 EXEMPEL \u2500\u2500\n+8%/\u00e5r: a = 1,08\n-15%/\u00e5r: a = 0,85\nF\u00f6rdubbling: a = 2\nHalvering: a = 0,50\n\nBil -15%/\u00e5r, 200 000 kr:\ny = 200000\u00b70,85\u02e3\n\u00c5r 1: 170 000\n\u00c5r 3: 122 825\n\u00c5r 5: 88 741", ref: "forand", lbl: "a anger" },

        { t: "STARTV\u00c4RDE (C)\n\nI y = C\u00b7a\u02e3 \u00e4r 'C'\ny-v\u00e4rdet n\u00e4r x = 0.\n\nVarf\u00f6r? N\u00e4r x = 0:\ny = C\u00b7a\u2070 = C\u00b71 = C\n(Allt upph\u00f6jt till 0 = 1)\n\nGrafiskt: d\u00e4r kurvan\nsk\u00e4r y-axeln.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\n50000 kr, 3% r\u00e4nta:\ny = 50000\u00b71,03\u02e3\nC = 50 000\n\n800 g radioaktivt:\ny = 800\u00b70,5\u02e3\nC = 800", ref: "start", lbl: "C anger" },

        { t: "GRUNDPOTENSFORM\n\nOmskrivning till bas 10:\ny = C \u00b7 10^(kx)\n\nD\u00e4r k = lg(a)\n\nDetta kopplar exponential-\nfunktioner till logaritmer:\nk = lg(a) anv\u00e4nder\nlogaritmens definition.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\ny = 500\u00b72\u02e3\nlg(2) = 0,301\ny = 500\u00b710^(0,301x)\n\nKontroll vid x=3:\n500\u00b72\u00b3 = 4000\n500\u00b710^0,903 \u2248 4000", ref: "grund", lbl: "kan skrivas som" },
      ]},

      { t: "POTENSFUNKTION\ny = a \u00b7 x^n\n\nSKILLNAD mot exponential:\nH\u00e4r sitter x i BASEN\n(inte i exponenten).\nn = fast exponent.\n\nAnv\u00e4nds f\u00f6r geometri\noch fysik.\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nBromstr\u00e4cka:\ns = 0,006\u00b7v\u00b2\n(a=0,006, n=2)\nv=80: 38,4 m\nv=120: 86,4 m\n\nJ\u00e4mf\u00f6relse vid x=10:\nPotens 3\u00b7x\u00b2 = 300\nExp 3\u00b72\u02e3 = 3072\nExp v\u00e4xer MYCKET snabbare!", ref: "potf", lbl: "y = a\u00b7x^n" },
    ]},

    // ========================
    // LOGARITMER (V\u00c4NSTER NER)
    // ========================
    { t: "LOGARITMER\n\nlg svarar p\u00e5 fr\u00e5gan:\n\"10 upph\u00f6jt till VAD\nger detta tal?\"\n\nlg(1000)=3 (10\u00b3=1000)\nlg(100)=2 (10\u00b2=100)\nlg(10)=1 (10\u00b9=10)\n\nT\u00e4nk: omv\u00e4nd upph\u00f6jning.", side: "L", ci: 2, lbl: "verktyg f\u00f6r", c: [

      { t: "DEFINITION\n\nlg(x) = y betyder:\n10 upph\u00f6jt till y ger x\n(10^y = x)\n\nEndast f\u00f6r x > 0!\n\n\u2500\u2500 EXEMPEL \u2500\u2500\nlg(1000) = 3 (10\u00b3=1000)\nlg(100) = 2\nlg(10) = 1\nlg(1) = 0 (10\u2070=1)\nlg(0,1) = -1\nlg(0,01) = -2\nlg(7) \u2248 0,845\n\nP\u00e5 kalkylatorn:\nKnappen LOG", ref: "lgdef", lbl: "vad \u00e4r lg?" },

      { t: "TIOLOGARITM (lg)\n\nlg = log med bas 10\nP\u00e5 kalkylatorn: LOG\n(inte ln, det \u00e4r annan bas)\n\nVIKTIGT SAMBAND:\nlg och 10-upph\u00f6jning \u00e4r\nMOTSATSER:\n\nlg(10\u02e3) = x\n10^(lg x) = x\n\nPrecis som + och -\ntar ut varandra!\n\nAnv\u00e4nds f\u00f6r att l\u00f6sa\nexponentialekvationer.", ref: "tiolog", lbl: "kallas" },

      { t: "LOGARITMLAGAR\n\nTre r\u00e4kneregler f\u00f6r lg.\n\n1. G\u00e5nger inuti lg\n   = plus utanf\u00f6r\n2. Delat inuti lg\n   = minus utanf\u00f6r\n3. Exponent inuti lg\n   = faktor framf\u00f6r\n   (VIKTIGAST!)\n\nAnv\u00e4nds f\u00f6r att:\n\u2022 F\u00f6renkla lg-uttryck\n\u2022 L\u00f6sa exponentialekvationer", ref: "lglagar", lbl: "har tre", c: [

        { t: "PRODUKTREGELN\n\nlg(A\u00b7B) = lg A + lg B\n\nG\u00c5NGER inuti lg\nblir PLUS utanf\u00f6r.\n\n\u2500\u2500 EXEMPEL 1 \u2500\u2500\nlg(20\u00b750)\n= lg(20) + lg(50)\n= 1,301 + 1,699 = 3\nKontroll: 20\u00b750=1000\nlg(1000)=3 St\u00e4mmer!\n\n\u2500\u2500 EXEMPEL 2 \u2500\u2500\nlg(2) + lg(5)\n= lg(2\u00b75) = lg(10) = 1", ref: "prodr", lbl: "regel 1" },

        { t: "KVOTREGELN\n\nlg(A/B) = lg A - lg B\n\nDELAT inuti lg\nblir MINUS utanf\u00f6r.\n\n\u2500\u2500 EXEMPEL 1 \u2500\u2500\nlg(1000/10)\n= lg(1000) - lg(10)\n= 3 - 1 = 2\nKontroll: 1000/10=100\nlg(100)=2 St\u00e4mmer!\n\n\u2500\u2500 EXEMPEL 2 \u2500\u2500\nlg(5) = lg(10/2)\n= lg(10) - lg(2)\n= 1 - 0,301 = 0,699", ref: "kvotr", lbl: "regel 2" },

        { t: "POTENSREGELN\n\nlg(A^n) = n \u00b7 lg A\n\nExponenten plockas NER\nfr\u00e5n inuti lg och blir\nen FAKTOR framf\u00f6r.\n\nDETTA \u00c4R VIKTIGASTE LAGEN!\nDen anv\u00e4nds f\u00f6r att l\u00f6sa\nexponentialekvationer\n(\"plocka ner x\").\n\n\u2500\u2500 EXEMPEL 1 \u2500\u2500\nlg(2\u00b3) = 3\u00b7lg(2)\n= 3\u00b70,301 = 0,903\n\n\u2500\u2500 EXEMPEL 2 \u2500\u2500\nL\u00f6s 3\u02e3 = 50:\nlg(3\u02e3) = lg(50)\nx\u00b7lg(3) = lg(50)\nx = 1,699/0,477 \u2248 3,56", ref: "potr", lbl: "regel 3\n(viktigast!)" },
      ]},
    ]},
  ]
};

// --- Layout ---
const nodeH = n => Math.max(BASE_H, n.t.split('\n').length * LINE_H + 20);
const subH = n => {
  if (!n.c || !n.c.length) return nodeH(n);
  let h = 0;
  n.c.forEach((c, i) => { h += subH(c); if (i < n.c.length - 1) h += Y_SPACE; });
  return h;
};

const doLayout = (n, x, yMid, dir, depth, ci) => {
  n.x = x; n.y = yMid; n.d = depth; n.dir = dir;
  n.ci = n.ci !== undefined ? n.ci : ci;
  if (n.ref) REG[n.ref] = n;
  if (!n.c || !n.c.length) return;
  const h = subH(n);
  let y0 = yMid - h / 2;
  const dx = dir === "R" ? X_GAP : -X_GAP;
  n.c.forEach(c => {
    const ch = subH(c);
    c.ci = n.ci;
    c.dir = dir;
    doLayout(c, x + dx, y0 + ch / 2, dir, depth + 1, n.ci);
    y0 += ch + Y_SPACE;
  });
};

["R", "L"].forEach(side => {
  const branches = T.c.filter(b => b.side === side);
  let total = branches.reduce((s, b, i) => s + subH(b) + (i ? BRANCH_GAP : 0), 0);
  let y0 = -total / 2;
  const baseX = side === "R" ? X_GAP : -X_GAP;
  branches.forEach(b => {
    const bh = subH(b);
    doLayout(b, baseX, y0 + bh / 2, side, 1, b.ci);
    y0 += bh + BRANCH_GAP;
  });
});
T.x = 0; T.y = 0; T.d = 0; T.dir = "R";

// Nudge: flytta POTENSEKVATION lite \u00e5t v\u00e4nster s\u00e5 pilen inte \u00f6verlappar EXPONENTIALEKVATION
if (REG.poteq) REG.poteq.x -= 120;

// --- Clear canvas from previous runs, then render ---
ea.deleteViewElements(ea.getViewElements());
ea.reset();
const phNodes = [];

const mkNode = n => {
  const col = C[n.ci !== undefined ? n.ci : 0];
  ea.style.fontFamily = 1;
  ea.style.fillStyle = "solid";
  ea.style.roughness = 1;
  ea.style.roundness = {type: 3};
  ea.style.strokeStyle = "solid";
  ea.style.opacity = 100;

  if (n.d === 0) {
    ea.style.strokeColor = "#343a40";
    ea.style.backgroundColor = "#dee2e6";
    ea.style.fontSize = 20;
    ea.style.strokeWidth = 3;
  } else if (n.d === 1) {
    ea.style.strokeColor = col.s;
    ea.style.backgroundColor = col.b;
    ea.style.fontSize = 15;
    ea.style.strokeWidth = 2;
  } else {
    ea.style.strokeColor = col.s;
    ea.style.backgroundColor = "#ffffff";
    ea.style.fontSize = 13;
    ea.style.strokeWidth = 1;
  }

  n.id = ea.addText(n.x, n.y, n.t, {
    box: n.d === 0 ? "ellipse" : "rectangle",
    textAlign: n.d >= 2 ? "left" : "center",
    textVerticalAlign: "middle",
  });

  if (n.ph) phNodes.push(n);
  if (n.c) n.c.forEach(mkNode);
};
mkNode(T);

// --- Labeled arrows ---
// Label placement algorithm:
// 1. Find arrow midpoint
// 2. Compute perpendicular direction pointing "above" the line
// 3. Estimate text pixel dimensions from char count & font size
// 4. Offset label center so its bottom edge sits just above the arrow
// 5. Subtract half-dimensions because addText uses top-left corner
const LBL_FS = 22;

const mkArrows = n => {
  if (!n.c) return;
  n.c.forEach(child => {
    const col = C[child.ci !== undefined ? child.ci : 0];
    ea.style.strokeColor = col.s;
    ea.style.strokeWidth = n.d === 0 ? 3 : (n.d === 1 ? 2 : 1);
    ea.style.roughness = 1;
    ea.style.roundness = {type: 2};
    ea.style.strokeStyle = "solid";

    // Straight edge-to-edge arrow
    const arrowId = ea.connectObjects(
      n.id, null, child.id, null,
      { numberOfPoints: 0, startArrowHead: null, endArrowHead: "arrow" }
    );

    // Label centered on arrow, shifted above the line
    if (child.lbl && arrowId) {
      ea.style.fontSize = LBL_FS;
      ea.style.strokeColor = col.s;
      ea.style.fontFamily = 1;
      const lblId = ea.addLabelToLine(arrowId, child.lbl);
      if (lblId && ea.elementsDict) {
        const txt = ea.elementsDict[lblId];
        const arr = ea.elementsDict[arrowId];
        if (txt && arr && arr.points && arr.points.length >= 2) {
          const p = arr.points[1];
          const len = Math.sqrt(p[0]*p[0] + p[1]*p[1]) || 1;
          let px = -p[1]/len, py = p[0]/len;
          if (py > 0) { px = -px; py = -py; }
          txt.x += px * 20;
          txt.y += py * 20;
          txt.containerId = null;
          if (arr.boundElements) {
            arr.boundElements = arr.boundElements.filter(b => b.id !== lblId);
          }
        }
      }
    }

    mkArrows(child);
  });
};
mkArrows(T);

// --- Cross-references (colored arrows between related concepts) ---
const xrefs = [
  { from: "fakt", to: "noll", lbl: "avl\u00e4ses \u2194 byggs", bidir: true },
];

ea.style.strokeStyle = "solid";
ea.style.strokeWidth = 2;
ea.style.strokeColor = "#d9480f";
ea.style.roughness = 0;
ea.style.roundness = {type: 2};
ea.style.opacity = 70;

for (const xr of xrefs) {
  const from = REG[xr.from];
  const to = REG[xr.to];
  if (!from || !to) continue;

  const xArrowId = ea.connectObjects(
    from.id, null, to.id, null,
    { numberOfPoints: 0,
      startArrowHead: xr.bidir ? "arrow" : null,
      endArrowHead: "arrow" }
  );

  // Label centered on arrow, shifted above
  ea.style.fontSize = 18;
  ea.style.strokeColor = "#d9480f";
  ea.style.fontFamily = 1;
  if (xArrowId) {
    const xLblId = ea.addLabelToLine(xArrowId, xr.lbl);
    if (xLblId && ea.elementsDict) {
      const xt = ea.elementsDict[xLblId];
      const xa = ea.elementsDict[xArrowId];
      if (xt && xa && xa.points && xa.points.length >= 2) {
        const xp = xa.points[1];
        const xlen = Math.sqrt(xp[0]*xp[0] + xp[1]*xp[1]) || 1;
        let xpx = -xp[1]/xlen, xpy = xp[0]/xlen;
        if (xpy > 0) { xpx = -xpx; xpy = -xpy; }
        xt.x += xpx * 20;
        xt.y += xpy * 20;
        xt.containerId = null;
        if (xa.boundElements) {
          xa.boundElements = xa.boundElements.filter(b => b.id !== xLblId);
        }
      }
    }
  }
}

ea.style.strokeStyle = "solid";
ea.style.opacity = 100;

// --- Embedded Desmos images (replacing placeholders) ---
const imgMap = {
  apos: "Excalidraw/Scripts/Downloaded/images/desmos-graph 1.png",
  aneg: "Excalidraw/Scripts/Downloaded/images/desmos-graph 2.png",
  sym:  "Excalidraw/Scripts/Downloaded/images/desmos-graph 3.png",
  ext:  "Excalidraw/Scripts/Downloaded/images/desmos-graph 4.png",
  noll: "Excalidraw/Scripts/Downloaded/images/desmos-graph 5.png",
  falskrot: "Excalidraw/Scripts/Downloaded/images/desmos-graph 6.png",
  regan: "Excalidraw/Scripts/Downloaded/images/desmos-graph 7.png",
};

for (const n of phNodes) {
  const col = C[n.ci !== undefined ? n.ci : 0];
  const dir = n.dir || "R";
  const phX = dir === "R" ? n.x + PH_GAP : n.x - PH_GAP;
  const imgPath = imgMap[n.ref];
  if (!imgPath) continue;

  const imgId = await ea.addImage(phX, n.y, imgPath, true);
  // Skala ner bilden till max 250px bred
  if (imgId && ea.elementsDict && ea.elementsDict[imgId]) {
    const el = ea.elementsDict[imgId];
    const ratio = el.height / el.width;
    el.width = 250;
    el.height = 250 * ratio;
  }

  // Connection arrow from node to image
  ea.style.strokeColor = col.s;
  ea.style.strokeWidth = 1;
  ea.style.strokeStyle = "dashed";
  ea.style.roughness = 0;
  ea.style.roundness = {type: 2};
  ea.style.opacity = 40;
  ea.addArrow(
    [[n.x, n.y], [phX, n.y]],
    { startObjectId: n.id, endObjectId: imgId,
      startArrowHead: null, endArrowHead: null }
  );
  ea.style.opacity = 100;
  ea.style.strokeStyle = "solid";
}

ea.style.strokeStyle = "solid";
ea.style.opacity = 100;
await ea.addElementsToView(true, true);
