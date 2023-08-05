# Evangelium
Evangelium is a file format designed specifically for transcribing Bible manuscripts. It
aims to provide a simple and accessible way for researchers to read transcribed Bible
texts without requiring any additional tools or software.

## Syntax
Evangelium follows a straightforward syntax that allows for easy
transcription of Bible manuscripts.

### Metadata
```less
@METADATA_KEY: METADATA_VALUE
```

Replace `METADATA_NAME` with the specific metadata field (e.g., "Manuscript Name," "Author" etc.), and `METADATA_VALUE` with the corresponding value.

```less
@Manuscript Name: P1
@Author: Unknown
@Date: 1st century AD
```

### Pages
```plaintext
-PAGE_NUMBER-
```

Place the page number between the hyphens, and all the texts written after this line will belong to the specified page.

### Columns

```plaintext
$COLUMN_NUMBER$
```

### Damaged Texts

To indicate damaged texts, use the pound symbol (#) at the beginning and end of the
damaged section. This will highlight that the following text is damaged and may be
unreadable.

```ruby
#This section of text is damaged#
```

### Unreadable Texts

To mark unreadable texts, use angle brackets (< >) at the beginning and end of the
unreadable section. This will indicate that the following text is illegible or
indecipherable.

```plaintext
<This section of text is unreadable>
```

### Books

```plaintext
%BOOK_NAME%
```

### Verses

```plaintext
[Chapter:Verse]
```

### Nomina Sacra
```plaintext
~NOMEN_SACRUM~
```

Replace `NOMEN_SACRUM` with the sacred name or title you want to abbreviate. This notation will indicate that the following text represents a sacred name or title.

## Example

![P1 - Page 1](https://www.penn.museum/collections/assets/1600/29398.jpg)
![P1 - Page 2](https://www.penn.museum/collections/assets/1600/102397.jpg)

```less
@Manuscript: P1
@Language: g
@Content: Mt 1,1-9.12; 1,14-20.23
@Origin Year Early: 200
@Origin Year Late: 299
@Origin Year: III
@Leaves: 1
@Columns: 1
@Lines: 37
@Lines Max: 38
@Script: Majuscule
@Material: Papyrus

%Mt%

-1-
$1$

[1:1]βιβλος γενεσεως ~ιυ~ ~χυ~ ~υυ~ δαυιδ #υιου#
αβρααμ [1:2]αβρααμ <εγ>εννησεν το<ν> #ισαακ#
ισαακ <δε> εγε<νν>ησεν τ#ον# ιακ<ωβ> #ιακωβ#
δε εγ#ε#<νν>ησε<ν> το<ν> ιο<υ>δαν <κ>#α#<ι> <τ>#ους#
<α>#δ#ελφ<ου>ς αυτου [1:3]ιουδ<ας> <δ>ε εγε<ννη>
<σεν> τον φαρες και τον ζαρε εκ της θ<α>
<μ>α<ρ> φαρες δε εγεννησεν τον <ε>σ<ρ>ωμ
εσ#ρω#<μ> δε ε<γ>ενν<η>σεν τ<ον> #α#<ρ>#α#μ [1:4]#αραμ#
δε #ε#<γε>ννησεν τ<ον> αμ<μιν>αδα<β> <αμ>
<μ>#ι#<να>#δα#β δε εγεννησε<ν> τον ναασσων
<ν>αασσων δε εγεννη<σ>εν τον σα<λ>#μω#ν
[1:5]σαλμων δε εγεν<ν>#η#<σ>εν τον βοε<ς> #εκ#
της ραχαβ βο<ε>ς δε <εγε>ννησεν τον ι
ωβηδ εκ της ρ#ο#υθ ι<ω>#βη#<δ> <δ>ε εγενν<η>
σεν τον ιε<σσ>αι [1:6]ιεσ<σ>#αι# <δ>ε εγε<νν>ησεν
το<ν> δ<αυιδ> <τ>ον βασι<λε>#α δαυ#<ιδ> <δ>ε <εγ>εν
<ν>ησεν τον σ<ο>λ<ο>μων<α> <εκ> της ουρειου [1:7]σ<ο>
λο<μ>ων <δ>ε εγεν<ν>η#σ#ε<ν> <τον> #ρ#οβ<ο>αμ ροβο
<α>μ δε εγεν<ν>η<σ>εν #το#<ν> <αβ>#ει#α αβεια δε
εγε<νν>ησεν #τ#<ο>ν ασ<α>#φ# [1:8]#ασα#<φ> δε εγ<ε>ν
ν<η>σ<εν> τον ιωσαφα<τ> #ιωσα#φατ δ<ε> εγεν
ν#η#<σε>#ν# τ<ον> ιωραμ ιω<ρα>μ δε εγεν<ν>#ησεν#
τον <ο>ζει<α>ν [1:9]οζε<ι>α<ς> <δ>ε ε<γ>ε<ν>νησεν
#---#
#---#
#---#
#---#
#---#
#---#
#---#
[1:12]#μετα δε την# <μ>ε
#τοικεσιαν βαβυλωνος ιεχονι#ας εγεν
#νησεν τον σαλαθιηλ σαλαθιηλ δε εγε#<ν>
#νεσεν τον ζοροβαβελ# [1:13]#ζοροβαβελ δ#ε
#---#
#---#
#---#

-2-
$1$

[1:14]#τον σ#<α>δω#κ σ#αδω<κ> δ<ε> <ε>γεννησεν το#ν#
#αχειμ# α<χ>ειμ δε εγε#ν#νησεν τον ελιου#δ#
[1:15]#ελιου#<δ> <δε> εγ#εν#ν<η>#σ#<ε>#ν# τον ελ<εα>ζαρ ελε
#αζ#<α>ρ #δε εγ#εν<ν>ησεν #το#ν <μαθ>θ<αν> μαθθ<α>#ν#
<δ>ε εγ<εν>ν<ησε>ν το<ν> ιακωβ [1:16]ι<ακ>ωβ δε
#εγ#εννη<σ>ε<ν> <τ>ον ιω<ση>φ τον <α>νδρα <μ>#α#
<ρι>ας #ε#ξ ης εγενν#ηθ#<η> ις ο λεγομενο#ς# #~χς~#
[1:17]<π>ασ<αι> <ουν> <γε>#νε#<αι> <α>πο αβρααμ ε<ως>
δαυιδ γενεαι ι<δ> κα<ι> απ<ο> #δαυιδ εως της#
μετοικε<σ>ι<α>ς βαβυλων<ο>#ς# <γ>ε#νεαι# ~ι<δ>~ <κα>#ι#
<απ>ο της με<τ>#οι#κεσια<ς> β<α>β#υ#λω<ν>#ο#ς εως
του ~χ<υ>~ <γ>εν<ε>αι ~ιδ~ [1:18]του δε ~ι<υ>~ ~χυ~ η γενε
σις ουτως ην <μν>ησ<τευ>θεισης της μη
τρος αυτου <μ>#αρι#<α>#ς# τ<ω> #ιω#σηφ πριν η συν
ε<λ>θ<ε>ιν αυτο<υ>ς <ευ>ρ<ε>θη <ε>ν <γ>αστρι εχου
σ<α> <ε>#κ πνς αγιου# [1:19]#ιωσηφ δε ο# αν<ηρ> <αυ>
<της> #δικα#ι#ος ων και μη θελων αυτην#
<δ>ειγμ<α>#τ#<ε>#ισαι εβουλη#<θη> #λαθρα#
#α#<πο>λυ#σαι αυ#<τ>#η#<ν> [1:20]#τ#α<υτα> #δε αυτου εν#
#θ#<υ>μη#θεντος ι#<δου> <α>#γγελος ~κυ~ κατ#
#ο#<ν>αρ #εφανη αυ#τ<ω> #λεγων# <ιωσ>#ηφ#
#υιος δαυιδ# <μ>#η# φ<ο>#βηθη#<ς> <παρ>#αλαβ#<ει>ν
#μ#<α>ρι<α>#ν την γυ#ν<αι>#κα σου# <το> #γαρ εν αυ#
#τη γεν#νη<θεν> <ε>#κ# <πν>ς #εστιν αγιου#
#---#
#---#
#---#
#---#
#---#
#---#
#---#
#---#
[1:23]μ<ε>#θερμηνευομενον μεθ ημων ο ~θς~#
```
