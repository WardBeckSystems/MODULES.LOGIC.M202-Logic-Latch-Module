# M202 Logic Latch Module · Logic

Ward-Beck Systems M202, 1979|12. Wiki page: [M202 on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/PAGES/M202.html)

| Folder | What is in it | Files |
|---|---|---|
| [SCHEMATICS/](SCHEMATICS/) | electrical drawings: schematics, functional diagrams, component layouts, wiring | 19 |
| [MECHANICAL/](MECHANICAL/) | front panels, cover plates, metalwork, assemblies; the front panel as vectors | 11 |
| [PINOUTS/](PINOUTS/) | the RTO-144 connector: connection sheets, connector layouts, rear views | 4 |
| [MANUALS/](MANUALS/) | manuals, manual pages, price lists, brochures, documents | 87 |
| [PHOTOS/](PHOTOS/) | photographs of the module | 12 |
| [KICAD/](KICAD/) | KiCad schematics traced from the drawings, the symbol, PCB projects | 5 |
| [OCR/](OCR/) | the note of every file: date, origin, title block, OCR text | 39 |

<!-- module data: tools/module_specs.py, tools/forum_quotes.py -->

**On the WBSps forum (2006|39 - 2014|47):** [1 topic](FORUM.md): what owners and technicians said about it.

## Circuit description

From [1979 - M202 - Logic Latch Module (2).pdf](MANUALS/1979%20-%20M202%20-%20Logic%20Latch%20Module%20(2).pdf) pages 2-6 (read by OCR; check against the pages). As data: [`CircuitDescription.json`](CircuitDescription.json).

<details><summary>Read it</summary>

The M202 Logic Latch mod.... re accepts three momentary push b u 1ton inputs and stores o r latches the stat.... soft hep.... a h button depressed. Only one of the t hrae stat.... s outp.... t swill bela tched a t any onetime.

Additional l y, ana lte rna te action typ ala tch Isp rov ided fora fourth pushbu tt on Input.

Inputs

The Input etrevn configuration Is Identical fora ll four pus hb....1ton I n p.... t a, With the control inputs floating, the open -e ir&lt;;u;t voltage at the control pins I s app ro&quot;, lmate l y +9 volts. The inputs are protected against Ina dv e r tenth ighv o ltage a p pl ica t ion and maybe safely operated a t potentials up to +30 volts. A n R/C network guards the inputs against the eHect s of switch bounce. Each Input c l r&lt;;u it is followed by a n Inverting Schm ill trigger.

I n order to affect a change o f status, a logic &quot;0&quot; I s app lied to any oft he inputs, ranging from 0 to +2 volts, and having a minim.... m d u ration of 100 milliseconds.

Interlocking Three P u shbutton Cont..o l Logic

The function o f the t h r.... control inputs atp ins 2, Band 13 can be compared to that of a bank oft h r ee Inter locking p u shb.... tto n switches, wh e..e l h e operation o f anyone switch causes the other two tore lease.

This opera tl on I sac hie v ed in the following way.

U2 i s a BCD tod ec i ma l decoder, used asap rio r i t y decoder. Of the four available binary inputs, only the first three are being used, namely A (pint 5), a (pin 14) and C (pin 13). A s these Inputs ere Individual l y addressed with a logic &quot;1 &quot; level 0&quot;;9 ln ating from the outputs of UI, the decoderw ill p..oduce a logic &quot;0 &quot; decimal outputs i gnal at output I (pin 2 }, output 2 (pin 3) or output ' (pin S). If more than one Input I sad dressed simultaneously, nod ecode.. output will result.

The t h r-ee decimal outputs a&quot;e combined via an OR gate consist ing o f

CR9, CR to and CR1 1, the output of which tr lgge.. s a oneshot multi v lb r-ato.. configured from two of the f o u.. gates contained I n U J.

A. nega t ive-going pulse o f about 20 milliseconds d u ration I s generated

at UJ, pin J. Routed via CRI 2, this pulse feeds the CLEAR Inputs o f

the R/ S type latches U4A, U4 Sand USA..

• 0,. - _...

o p

c:;, &quot; -i, &gt; =nllO ~ 00 - ' 1£1)

a..., i.. g., '&quot; &quot;,,1»::r

O-..l::J:T ~ !. '0.. It

... _.

.1:. ~ - ', e ~ o,

0 0

Vl;;

&quot; c roll

a III

..., n

o ~~ [;r m

o_ I -e 0c'

·,•..-,.-K &quot;,- - • g:..... •--.. ••,.• • r -',.,- -_. III ll;;

**II '&lt; I.,;;;-.. 3**

(II l;I

o • •Q. c_.

**• 0 &lt;0 _::I**

Cl c.

0 &quot;'_.

'&quot; Ill.:J

**-0' III**

...,- ca. III. &quot; H •'' c o ~

•o 0, 0' ••n 60 111 •n.:

• Ion

&lt;&gt; l '&lt;;; (l - I -.s=.,0 It:T s:

c::r,,'&lt;

•c s e cr &lt;:1 =..'

• z..~g:!.:1~

•::r&quot;-ll O ~ &quot; l;I'. &quot;.

**II C 0 C**

00.';; '- '':Tell

1M - - •., n

n Q:t

110(00

:JlO ll

= I !! s:

• &quot; g;.::;&quot;.;.. n.i III

' on r &quot; • -.i s,

o - C_ n0 () 2'!l....

o 0

· •-, '0 ~,;l.; c o •:&gt; -.. 3

n • 0 ~, c_ i0 • • ss ~&lt;;'! o

• c.. 0 _.

cr;;&quot; '0

:J:T c _ Sl,:T&quot;

'&lt; -. I &lt;Q '~ o

**'., I 0 ·**

•• •&gt;, 1) 0

. o• n o &quot; o ' I &quot; • o. ~ ~

;'&lt; iii&quot; es &quot; ·: 0

':!. (l j 0:, '0::,

.an.,-.- • ··..:r-.

• &gt;1,::.:&gt; _.

! '0 l oil

• 0 ' • c C - 'Ill

• •, &quot;. &quot;&gt;.&quot; \ _ 3.&gt; lJ' ~ III 0

o' -. &quot;0 '&quot;.. 0 III lII B · c;:; g',, N ~ g..... ill !o a, c

, 0

**:T**

• H... I It....

**BCD to DECIMAL DECODER**

The 74C42: one often decoder I s a ~on o l ithf c CMOS c irc uft. This decoder produces a logic ' 0 ' at the output corresponding t oaf our b ft binary f nput frolll zero to nine, and a log f c ' I' at the other out puts. For bfnary inputs from tent o f 1f teen all outputs are logic ' 1 '.

**, OUTPUTS**

• c o • • I&quot; &quot; &quot; ta &quot; &quot; &quot; •

**TOP VIEW**

s3 7

**TABLE**

0 c8 A 0 1 2 J 4 5,, 7 8

0 DOD 0 1 1 1 1 1 1 1 1 1 0 o 0 1 1 0 1 1 1 1 1 1 1 1 0 DID 1 1 0 1 1 1 1 1 1 1 0 0 1 1 1 1 1 0 1 1 1 1 1 1 0 100 1 1 1 1 0 1 1 1 1 1 0 1 0 1 1 1 1 1 1 0 1 1 1 1 0 1 1 0 1 1 1 1 1 1 0 1 1 1

0 III 1 1 1 1 1 1 1 0 1 1

1 000 1 1 1 1 1 1 I 1 0 1

1 o 0 1

1 1 1 1 1 1 1 1 1 0

**74C4 2:**

INTEGRATE a CIRCUIT DATA

**74C76**

DUAL J -K FLIP - FLOP WITH CLEAR AND PRESET

The 74C76 J - K f11 pf lop is • monolithic CMOS circuit. Each flip flop has 1ndepe nde nt J, K, clock, clear and preset inputs as well as Q and &quot;lT outputs. The flip -flops are edge se ns H1ve tot he clock 1np ut and changes tate on the negative g01ng transition oft he clock pulses. Clear or preset is independent o f the clock and is ac compl t s bed by a low level on the r-espec e t ve input.

**PRESET A**

jJ J CLEAR

**CLEAR A**

KpRESET~...J

KPRESETa

**TOP VIEW**

Hate 1: A 10g1 c ~ D &quot; on clear sets Q t o a logic &quot;0&quot;. Hate Z: A 10g1c &quot; D ~ on preset sets Q t o a 10g1c ·1 &quot;.

tn+l

TRUnt

**TABLE**

Preset

Clear

0 1 0 1 0 0 1

1 0 1 1 1. Q&quot;

1 1 0,

t n· b1t t 1me before clock pulse. · NO change 1n output

tn+l • b1t t 1me after clock pulse. from previous state

</details>

<!-- /module data -->

## Photos

_Photographs of the module itself: front, back, inside, racked._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKRVlhWkk4OE1NXzg/view?resourcekey=0-xZeVi9p1XoOVvJj1zZdCDg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKRVlhWkk4OE1NXzg&resourcekey=0-xZeVi9p1XoOVvJj1zZdCDg" width="240" alt="1979 - M202 - IMG_3518.jpg"></a><br><sub>1979|12 · IMG_3518</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcm9SVUNRck1QZG8/view?resourcekey=0-7JehoZr6In8-klnfrwYSQw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcm9SVUNRck1QZG8&resourcekey=0-7JehoZr6In8-klnfrwYSQw" width="240" alt="1979 - M202 - IMG_3519.jpg"></a><br><sub>1979|12 · IMG_3519</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKQUVCdlo0UlozWjQ/view?resourcekey=0-O8GBBmgrAe-gd63KmUYqxQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKQUVCdlo0UlozWjQ&resourcekey=0-O8GBBmgrAe-gd63KmUYqxQ" width="240" alt="1979 - M202 - IMG_3521.jpg"></a><br><sub>1979|12 · IMG_3521</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcTRNV2hrMDBrTDg/view?resourcekey=0-28YkBnNWCVZgNreyruW2aw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcTRNV2hrMDBrTDg&resourcekey=0-28YkBnNWCVZgNreyruW2aw" width="240" alt="1979 - M202 - IMG_3523.jpg"></a><br><sub>1979|12 · IMG_3523</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKWUh6SF9oYVNwUUU/view?resourcekey=0-aAAioMc_F11DT0QOUCJRoA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKWUh6SF9oYVNwUUU&resourcekey=0-aAAioMc_F11DT0QOUCJRoA" width="240" alt="1979 - M202 - IMG_3525.jpg"></a><br><sub>1979|12 · IMG_3525</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKQzg5SGVhUy0zMms/view?resourcekey=0-88nvslx6cqSZor-efcKhEQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKQzg5SGVhUy0zMms&resourcekey=0-88nvslx6cqSZor-efcKhEQ" width="240" alt="1979 - M202 - IMG_3526.jpg"></a><br><sub>1979|12 · IMG_3526</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKQmpla2RQeFZRN2c/view?resourcekey=0-AEH0oEPmxdvnvTj8bnNUZg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKQmpla2RQeFZRN2c&resourcekey=0-AEH0oEPmxdvnvTj8bnNUZg" width="240" alt="1979 - M202 - IMG_3528.jpg"></a><br><sub>1979|12 · IMG_3528</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKN3VoZWNjczVmZm8/view?resourcekey=0-1W3qZo1-A0lejGmZucZJvA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKN3VoZWNjczVmZm8&resourcekey=0-1W3qZo1-A0lejGmZucZJvA" width="240" alt="1979 - M202 - IMG_3529.jpg"></a><br><sub>1979|12 · IMG_3529</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKd2k4bm45RGJXRkk/view?resourcekey=0-_vpUVbiHB48icPIScwsOQQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKd2k4bm45RGJXRkk&resourcekey=0-_vpUVbiHB48icPIScwsOQQ" width="240" alt="1979 - M202 - IMG_3531.jpg"></a><br><sub>1979|12 · IMG_3531</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKclF4azd0S01uZWs/view?resourcekey=0-UYFi05S3g6c-4k02EfzZ4Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKclF4azd0S01uZWs&resourcekey=0-UYFi05S3g6c-4k02EfzZ4Q" width="240" alt="1979 - M202 - IMG_3533.jpg"></a><br><sub>1979|12 · IMG_3533</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUDgxX2FFNmxkZVU/view?resourcekey=0-Puhoy-KsdC19y0RmCzmxIw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUDgxX2FFNmxkZVU&resourcekey=0-Puhoy-KsdC19y0RmCzmxIw" width="240" alt="1979 - M202 - IMG_3534.jpg"></a><br><sub>1979|12 · IMG_3534</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNWdsaFlYbUtCdjA/view?resourcekey=0-ywyPgCRcTqcU_oafAt2uTw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNWdsaFlYbUtCdjA&resourcekey=0-ywyPgCRcTqcU_oafAt2uTw" width="240" alt="1979 - M202 - IMG_3537.jpg"></a><br><sub>1979|12 · IMG_3537</sub></td></tr>
</table>

## Mechanical

_Mechanical drawings: front panels, cover plates, metalwork and hardware (-03- drawings), AutoCAD files, each with its `(EXTRACTED).svg` vectors; `<module> - front panel.svg` is the front panel as vectors._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKcWU3NXgyeHNlVHc/view?resourcekey=0-nEUsqSo6oLtvya3M_AuQuQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKcWU3NXgyeHNlVHc&resourcekey=0-nEUsqSo6oLtvya3M_AuQuQ" width="240" alt="1979 - M202 - 202-04-001 - LOGIC LATCH MODULE.jpg"></a><br><sub>1979|12 · 202-04-001 - LOGIC LATCH MODULE · <a href="MECHANICAL/1979%20-%20M202%20-%20202-04-001%20-%20LOGIC%20LATCH%20MODULE%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## 3-D model

[`MECHANICAL/M202.stl`](MECHANICAL/M202.stl) (GitHub turns it in 3-D) · [view, change and generate it on WBSps.ca](https://wardbecksystems.github.io/WBSps.ca/2026/stl.html?m=M202)

- **Size:** 41 × 178 mm panel, 165 mm deep, 3.2 mm plate (assumed: 1.6" x 7" x 6.5", the common module)
- **From the drawing:** 0 holes and cut-outs, 0 knobs (front panel: `MECHANICAL/M202 - front panel.svg`)
- no drawing of the front panel: the panel is blank
- Made by `tools/module_models.py` (→ `MECHANICAL/M202.model.json`) and `tools/stl/make_stl.mjs` in [WBSps.ca](https://github.com/WardBeckSystems/WBSps.ca); the site makes the same STL from the same JSON.

## Schematics

_Electrical drawings: schematics (-02-), functional diagrams (-01-), component layouts (-06-), wiring (-09-), PCB files (.pcb .dsn), and beside each scan its `(EXTRACTED).svg`: the vectors traced from it._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUVg5RFpLc21fSHc/view?resourcekey=0-WN2s_-Bj4HJSyQNJrDLpkg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUVg5RFpLc21fSHc&resourcekey=0-WN2s_-Bj4HJSyQNJrDLpkg" width="240" alt="1979 - M202 - 202-02-001 - FTTVLA LOGIC LATCH MODULE SCHEMATIC.jpg"></a><br><sub>1979|12 · 202-02-001 - FTTVLA LOGIC LATCH MODULE SCHEMATIC · <a href="SCHEMATICS/1979%20-%20M202%20-%20202-02-001%20-%20FTTVLA%20LOGIC%20LATCH%20MODULE%20SCHEMATIC%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKVVNFNWxZQzNNRU0/view?resourcekey=0--1X3PdhXggpmjxAEZ7nzWQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKVVNFNWxZQzNNRU0&resourcekey=0--1X3PdhXggpmjxAEZ7nzWQ" width="240" alt="1979 - M202 - 202-02-001.jpg"></a><br><sub>1979|12 · 202-02-001 · <a href="SCHEMATICS/1979%20-%20M202%20-%20202-02-001%20(EXTRACTED).svg">vectors</a></sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKR0pka0ZJRUxuYlE/view?resourcekey=0-z2bi0PmK-AnoHgiVdUQiig" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKR0pka0ZJRUxuYlE&resourcekey=0-z2bi0PmK-AnoHgiVdUQiig" width="240" alt="1979 - M202 - 202-06-001 - ARW LOGIC LATCH MOOULE.jpg"></a><br><sub>1979|12 · 202-06-001 - ARW LOGIC LATCH MOOULE · <a href="SCHEMATICS/1979%20-%20M202%20-%20202-06-001%20-%20ARW%20LOGIC%20LATCH%20MOOULE%20(EXTRACTED).svg">vectors</a></sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKUjlObDJQS1FQQlE/view?resourcekey=0-6vuUeBcFdPogSmW1VEphgQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKUjlObDJQS1FQQlE&resourcekey=0-6vuUeBcFdPogSmW1VEphgQ" width="240" alt="1979 - M202 - 202-06-001 - LOGIC LATCH MODULE CKO RUUL COMPONENT LAYOUT.jpg"></a><br><sub>1979|12 · 202-06-001 - LOGIC LATCH MODULE CKO RUUL COMPONENT LAYOUT · <a href="SCHEMATICS/1979%20-%20M202%20-%20202-06-001%20-%20LOGIC%20LATCH%20MODULE%20CKO%20RUUL%20COMPONENT%20LAYOUT%20(EXTRACTED).svg">vectors</a></sub></td></tr>
</table>

## Pinouts

_Pinouts: the RTO-144 edge connector (connection sheets, connector layouts and rear views, strapping), and the pinout / connections drawings made from them. The module root `RTO.json` lists every contact._

## RTO-144 pinout

RTO-144 edge connector. Every contact, with where it was read: [`RTO.json`](RTO.json).

| Pin | Signal | Kind | Pair | Confidence |
|---|---|---|---|---|

## Manuals and documents

_Manuals and manual pages, price lists, RTO-144 connection sheets, brochures, ads and other document scans._

<table>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKc19WX1Q1UGNZeUE/view?resourcekey=0-KquvapQFjbS4YEYoVNtFeQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKc19WX1Q1UGNZeUE&resourcekey=0-KquvapQFjbS4YEYoVNtFeQ" width="240" alt="1979 - M202 - Logic Latch Module (2).pdf"></a><br><sub>1979|12 · Logic Latch Module (2)</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKdk5vX0VQTnY0S1U/view?resourcekey=0-3Vls0Cwwve-H3G0vK-G0cw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKdk5vX0VQTnY0S1U&resourcekey=0-3Vls0Cwwve-H3G0vK-G0cw" width="240" alt="1979 - M202 - Logic Latch Module.pdf"></a><br><sub>1979|12 · Logic Latch Module</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKTmlQcDJlaDliWHM/view?resourcekey=0-JpZRZmAdPhRH9FIPK86xQw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKTmlQcDJlaDliWHM&resourcekey=0-JpZRZmAdPhRH9FIPK86xQw" width="240" alt="1979 - M202 - P001 - Title Page.jpg"></a><br><sub>1979|12 · P001 - Title Page</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKLUdMY2ZSUkM2dG8/view?resourcekey=0-7VvI8A5vIMYe94XonNT0zA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKLUdMY2ZSUkM2dG8&resourcekey=0-7VvI8A5vIMYe94XonNT0zA" width="240" alt="1979 - M202 - P002 - 1-1.jpg"></a><br><sub>1979|12 · P002 - 1-1</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKN2x6dnJ2Y1E1R3c/view?resourcekey=0-GvISZfyU2flk0n69jlYE6A" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKN2x6dnJ2Y1E1R3c&resourcekey=0-GvISZfyU2flk0n69jlYE6A" width="240" alt="1979 - M202 - P003 - 1-2.jpg"></a><br><sub>1979|12 · P003 - 1-2</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKaHIwVkw5WWZLTlE/view?resourcekey=0-FC5Sq343sH62L4uN2KJdEA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKaHIwVkw5WWZLTlE&resourcekey=0-FC5Sq343sH62L4uN2KJdEA" width="240" alt="1979 - M202 - P004 - 74C42.jpg"></a><br><sub>1979|12 · P004 - 74C42</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKQkpuRXdvZnRBeE0/view?resourcekey=0-soqY_U6LlxPB1uOElk_W_g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKQkpuRXdvZnRBeE0&resourcekey=0-soqY_U6LlxPB1uOElk_W_g" width="240" alt="1979 - M202 - P005 - 74C75.jpg"></a><br><sub>1979|12 · P005 - 74C75</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKWUhWUm54ZzUzY0U/view?resourcekey=0-vPBb6wNSGju_EtlDMsQ_qA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKWUhWUm54ZzUzY0U&resourcekey=0-vPBb6wNSGju_EtlDMsQ_qA" width="240" alt="1979 - M202 - P006 - 3-1.jpg"></a><br><sub>1979|12 · P006 - 3-1</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKS3c1aDZZOGw0ams/view?resourcekey=0-2N73wZoyX1SAY4GjKuQvxw" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKS3c1aDZZOGw0ams&resourcekey=0-2N73wZoyX1SAY4GjKuQvxw" width="240" alt="1979 - M202 - P007 - 3-2.jpg"></a><br><sub>1979|12 · P007 - 3-2</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKYy0tbG81cVBsdHc/view?resourcekey=0-vZtLgTwWZEM1_4WeZwObUg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKYy0tbG81cVBsdHc&resourcekey=0-vZtLgTwWZEM1_4WeZwObUg" width="240" alt="1979 - M202 - P008 - 3-3.jpg"></a><br><sub>1979|12 · P008 - 3-3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNTJxeFlsUVp2LXM/view?resourcekey=0-TH7XCdL9m65dqxferXwVkA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNTJxeFlsUVp2LXM&resourcekey=0-TH7XCdL9m65dqxferXwVkA" width="240" alt="1979 - M202 - p1.jpg"></a><br><sub>1979|12 · p1</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKYTRhdXMxSVJXbmc/view?resourcekey=0-gm7tyhhu7JbP9m3h5RMJjQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKYTRhdXMxSVJXbmc&resourcekey=0-gm7tyhhu7JbP9m3h5RMJjQ" width="240" alt="1979 - M202 - p10.jpg"></a><br><sub>1979|12 · p10</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKWnAzbUFqa0R5bFU/view?resourcekey=0-Pm3pMGG8TnQ3enqJNRAo7g" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKWnAzbUFqa0R5bFU&resourcekey=0-Pm3pMGG8TnQ3enqJNRAo7g" width="240" alt="1979 - M202 - p2.jpg"></a><br><sub>1979|12 · p2</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKT3lpQWJsLWNNaFU/view?resourcekey=0-T7jmR4nXEg6eEOMxw1lyfg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKT3lpQWJsLWNNaFU&resourcekey=0-T7jmR4nXEg6eEOMxw1lyfg" width="240" alt="1979 - M202 - p3.jpg"></a><br><sub>1979|12 · p3</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKNThuM0RpSTg3TG8/view?resourcekey=0-vDxZVoyJ-QUS98fP7veq6w" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKNThuM0RpSTg3TG8&resourcekey=0-vDxZVoyJ-QUS98fP7veq6w" width="240" alt="1979 - M202 - p4.jpg"></a><br><sub>1979|12 · p4</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKZk1Ra2NhcnZnNlE/view?resourcekey=0-XvpuS1zftRwFIieaiVfD0Q" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKZk1Ra2NhcnZnNlE&resourcekey=0-XvpuS1zftRwFIieaiVfD0Q" width="240" alt="1979 - M202 - p5.jpg"></a><br><sub>1979|12 · p5</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKR2lEVHhzbnAzTUE/view?resourcekey=0-78XN72WVqv3qCHIwuDrfGg" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKR2lEVHhzbnAzTUE&resourcekey=0-78XN72WVqv3qCHIwuDrfGg" width="240" alt="1979 - M202 - p6.jpg"></a><br><sub>1979|12 · p6</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKc3lOOHh2dEF1eDA/view?resourcekey=0-eVTQQTlKCOhF_m7TXEe3VQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKc3lOOHh2dEF1eDA&resourcekey=0-eVTQQTlKCOhF_m7TXEe3VQ" width="240" alt="1979 - M202 - p7.jpg"></a><br><sub>1979|12 · p7</sub></td></tr>
<tr><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKclhYMVV5Ri1nQTA/view?resourcekey=0-Nhgs0mA504IkdIWlSv37iA" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKclhYMVV5Ri1nQTA&resourcekey=0-Nhgs0mA504IkdIWlSv37iA" width="240" alt="1979 - M202 - p8.jpg"></a><br><sub>1979|12 · p8</sub></td><td align="center" valign="top" width="33%"><a href="https://drive.google.com/file/d/0B0yR0b5T78SKbENjVkJidjBSOGM/view?resourcekey=0-v5jVcql0m6gDCzhTAHJzkQ" title="Open on Google Drive"><img src="https://drive.google.com/thumbnail?sz=w480&id=0B0yR0b5T78SKbENjVkJidjBSOGM&resourcekey=0-v5jVcql0m6gDCzhTAHJzkQ" width="240" alt="1979 - M202 - p9.jpg"></a><br><sub>1979|12 · p9</sub></td></tr>
</table>

## KiCad

_KiCad: a schematic (`.kicad_sch`) traced from each electrical drawing, the module symbol (`.kicad_sym`) and its PCB projects. Traced schematics are the line work only: redraw with symbols over them._

- [1979 - M202 - 202-02-001 - FTTVLA LOGIC LATCH MODULE SCHEMATIC.kicad_sch](KICAD/1979%20-%20M202%20-%20202-02-001%20-%20FTTVLA%20LOGIC%20LATCH%20MODULE%20SCHEMATIC.kicad_sch)
- [1979 - M202 - 202-02-001.kicad_sch](KICAD/1979%20-%20M202%20-%20202-02-001.kicad_sch)
- [1979 - M202 - Logic Latch Module p9.kicad_sch](KICAD/1979%20-%20M202%20-%20Logic%20Latch%20Module%20p9.kicad_sch)
- [19xx - M202 - Integrated Circuit Data 74C76 Dual J-K Flip-Flop.kicad_sch](KICAD/19xx%20-%20M202%20-%20Integrated%20Circuit%20Data%2074C76%20Dual%20J-K%20Flip-Flop.kicad_sch)
- [M202.kicad_sym](KICAD/M202.kicad_sym)

---
Archive: Anthony Peter Kuzub · [WBSps.ca](https://WBSps.ca) · [WBSps.Kuzub.com](https://WBSps.Kuzub.com)
