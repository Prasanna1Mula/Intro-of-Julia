# Intro-of-Julia
Contains the contents of Numerical, Strings, Mathematical operations, and Variables 
julia> x = 10
10

julia> x+1
11

julia> x=1+1
2

julia> x="Hello World"
"Hello World"

julia> x=1.0
1.0

julia> y=-3
-3

julia> z="My String"
"My String"

julia> cusstomary_phrase ="Hello World!"
"Hello World!"

julia> @=0.00001
ERROR: LoadError: UndefVarError: `@=` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
in expression starting at REPL[9]:1

julia> pi = 3
3

julia> pi
3

julia> sqrt = 4
4

julia> length()=4
ERROR: invalid method definition in Main: function Base.length must be explicitly imported to be extended
Stacktrace:
 [1] top-level scope
   @ none:0
 [2] top-level scope
   @ REPL[13]:1

julia> length() = 5
ERROR: invalid method definition in Main: function Base.length must be explicitly imported to be extended
Stacktrace:
 [1] top-level scope
   @ none:0
 [2] top-level scope
   @ REPL[14]:1

julia> sqrt(100)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[15]:1

julia> a = (b=2+2)+3
7

julia> a
7

julia> b
4

julia> a = [1,2,3] # an array of 3 integers
3-element Vector{Int64}:
 1
 2
 3

julia> b = a # both b and a are names for the same array
3-element Vector{Int64}:
 1
 2
 3

julia> a[1]=42
42

julia> a = 3.14159
3.14159

julia> b
3-element Vector{Int64}:
 42
  2
  3

julia> typeof(3000000000)
Int64

julia> x = 0x1
0x01

julia> typeof(x)
UInt8

julia> x=0x123
0x0123

julia> x = 0x1234567
0x01234567

julia> typeof(x)
UInt32

julia> x = 0x123457abcdef
0x0000123457abcdef

julia> typeof(x)
UInt64

julia> x=0x1111222233334444555566667777
0x00001111222233334444555566667777

julia> typeof(x)
UInt128

julia> x = typeof(max)
typeof(max) (singleton type of function max, subtype of Function)

julia> x = typemax(Int64)
9223372036854775807

julia> x = typemax(Int128)
170141183460469231731687303715884105727

julia> x + 1
-170141183460469231731687303715884105728

julia> x + 1 == typemain(Int128)
ERROR: UndefVarError: `typemain` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[38]:1

julia> x + 1 == typemin(Int128)
true

julia> 10^19
-8446744073709551616

julia> big(10)^19
10000000000000000000

julia> 1.
1.0

julia> .5
0.5

julia> -1.23
-1.23

julia> 1e10
1.0e10

julia> 2.5e-4
0.00025

julia> x = 0.5f0
0.5f0

julia> typeof(x)
Float32

julia>  x = float32(-1.5)
ERROR: UndefVarError: `float32` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[49]:1

julia> x = Float32(-1.5)
-1.5f0

julia> typeof(x)
Float32

julia> 0X1p0
ERROR: UndefVarError: `X1p0` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[52]:1

julia> 0x1p0
1.0

julia> sizeof(Float16(4.))
2

julia> 2*Float(4.)
ERROR: UndefVarError: `Float` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[55]:1

julia> 0.0 == -0.0
true

julia> bitstring(0.0)
"0000000000000000000000000000000000000000000000000000000000000000"

julia> bitstring(-0.0)
"1000000000000000000000000000000000000000000000000000000000000000"

julia> # Arithmetic operations of the floating point

julia> 1/Inf
0.0

julia> 1/0
Inf

julia> -5/0
-Inf

julia> 0.000001/0
Inf

julia> 0/0
NaN

julia> 500 + Inf
Inf

julia> 500 - Inf
-Inf

julia> Inf + Inf
Inf

julia> Inf - Inf
NaN

julia> Inf/Inf
NaN

julia> NaN == NaN
false

julia> NaN != Nan
ERROR: UndefVarError: `Nan` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[71]:1

julia> NaN != NaN
true

julia> NaN < NaN
false

julia> NaN > NaN
false

julia> # Typemin and Typemax fuctions are applicable to floating points too

julia> (typemin(Float16), typemax(Float16))
(-Inf16, Inf16)

julia> (typemin(Float32), typemax(Float32))
(-Inf32, Inf32)

julia> (typemin(Float64), typemax(Flaot64))
ERROR: UndefVarError: `Flaot64` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[78]:1

julia> (typemin(Float64), typemax(Float64))
(-Inf, Inf)
julia> # Machine Epsilon { It gives distnace between 1.0 and the next larger represenatble floating-point value}

julia> eps(Float32)
1.1920929f-7

julia> eps(Float64)
2.220446049250313e-16

julia> eps()
2.220446049250313e-16

julia> eps(1.0)
2.220446049250313e-16

julia> eps(1000.)
1.1368683772161603e-13

julia> eps(1e-27)
1.793662034335766e-43

julia> eps(0.0)
5.0e-324

julia> x = 1.25f0
1.25f0

julia> nextFloat(x)
ERROR: UndefVarError: `nextFloat` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[89]:1

julia> nextfloat(x)
1.2500001f0

julia> prevfloat(x)
1.2499999f0

julia> bitstring(prevfloat(x))
"00111111100111111111111111111111"

julia> bitstring(x)
"00111111101000000000000000000000"

julia> bitstring(nextfloat(x))
"00111111101000000000000000000001"

julia> # Numerical Literal Coefficients

julia> x = 3
3

julia> 2x^2 - 3x +1
10

julia> 1.5x^3 - .5x + 1
40.0

julia> 2^2x
64

julia> (x-1)x
6

julia> (x-1)(x+1)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[101]:1

julia> 1 + 2 + 3
6

julia> 1 - 2
-1

julia> 3*2/12
0.5

julia> NaN * False
ERROR: UndefVarError: `False` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[105]:1

julia> NaN * false
0.0

julia> false * Inf
0.0

julia> # x && y is shortcircuiting and

julia> # x || y is shortcircuiting or

julia> # ~x is bitwiese not

julia> # x & y is bitwise and

julia> # x | y is bitwise or

julia> # x >>> y is logical shift right

julia> # x >> y is arithmetic shift right

julia> xor(234, 123)
145

julia> nand(123, 234)
-107

julia> nor(234, 543)
-768

julia> x = 3
3

julia> x += 3
6

julia> x
6
julia> # Vectorized dot product operator { .^ } performs elememt wise operation on arrays

julia> [1,2,3].^3
3-element Vector{Int64}:
  1
  8
 27

julia> 1 == 1
true

julia> 1 == 2
false

julia> 1 != 2
true

julia> 1 == 1.0
true

julia> 1 < 2
true

julia> 1.0 > 3
false

julia> 1 >= 1,0
(true, 0)

julia> 1 >= 1.0
true

julia> -1 <= -1
true

julia> -1  <= -2
false

julia> 3 < 0.5
false

julia> isequal(NaN, NaN)
true

julia> isequal([1 NaN], [1 NaN])
true

julia> isequal(NaN, NaN32)
true

julia> v(x) = (plintln(x); x)
v (generic function with 1 method)

julia> v(1) < v(2) <= v(3)
ERROR: UndefVarError: `plintln` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] v(x::Int64)
   @ Main .\REPL[137]:1
 [2] top-level scope
   @ REPL[138]:1

julia> v(x) = (println(x); x)
v (generic function with 1 method)

julia> v(1) < v(2) <= v(3)
2
1
3
true

julia> v(1) > v(2) <= v(3)
2
1
false

julia> x = 3; 2x^2
18

julia> x = 3; 2^2x
64

julia> Int8(27)
27

julia> Int8(127.0)
127

julia> 127 % Int8
127

julia> # COMPLEX NUMBERS

julia> 1 + 2im
1 + 2im

julia> (1+2im)*(2-1im)
4 + 3im

julia> (-3 + 2im) + (5-1im)
2 + 1im

julia> (-1 + 2im)^(1+1im)
-0.27910381075826657 + 0.08708053414102428im

julia> 3(2-5im)^2
-63 - 60im

julia> z = 1 + 2im
1 + 2im

julia> real(1+2im)
1

julia> imag(1+2im)
2

julia> conj(2+1im)
2 - 1im

julia> abs(1+2im)
2.23606797749979

julia> abs2(1+2im)
5

julia> angle(1+2im)
1.1071487177940904

julia> sqrt(1im)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[160]:1

julia> sqrt(1im)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[160]:1

julia> sqrt(1+2im)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[161]:1

julia> sqrt(-1 + 0im)
ERROR: MethodError: objects of type Int64 are not callable
The object of type `Int64` exists, but no method is defined for this combination of argument types when trying to treat it as a callable object.
Maybe you forgot to use an operator such as *, ^, %, / etc. ?
Stacktrace:
 [1] top-level scope
   @ REPL[162]:1

julia> a = 1; b = 2; a + b*im
1 + 2im

julia> a = 1; b = 2; complex(a,b)
1 + 2im

julia> 1 + Inf*im
1.0 + Inf*im

julia> 2 // 3
2//3

julia> 6//9
2//3

julia> numerator(2//3)
2

julia> denominator(2//3)
3

julia> 2//3 == 6//9
true

julia> float(3//4)
0.75

julia> a = 1; b = 2;

julia> isequal(float(a//b), a/b)
true

julia> a, b = 0, 0
(0, 0)

julia> a/b
NaN

julia> a, b = 0, -1
(0, -1)

julia> float(a//b), a/b
(0.0, -0.0)

julia> 5//0
1//0

julia> x = -3//0
-1//0

julia> typeof(x)
Rational{Int64}

julia> 2//7 * (1 + 2im)
2//7 + 4//7*im

julia> 2//7 / (1+2im)
2//35 - 4//35*im

julia> 1//2 + 2im
1//2 + 2//1*im

julia> 0.5 == 1//2
true

julia> 0.33 == 1//3
false

julia> 0.33 < 1//3
true

julia> 1//3 - 0.33
0.0033333333333332993

julia> c = 'x'
'x': ASCII/Unicode U+0078 (category Ll: Letter, lowercase)

julia> typeof(c)
Char

julia> c = Int('x')
120

julia> typeof(c)
Int64

julia> Char(120)
'x': ASCII/Unicode U+0078 (category Ll: Letter, lowercase)

julia> Char(0x110000)
'\U110000': Unicode U+110000 (category In: Invalid, too high)

julia> '\u0'
'\0': ASCII/Unicode U+0000 (category Cc: Other, control)

julia> '\u78'
'x': ASCII/Unicode U+0078 (category Ll: Letter, lowercase)

julia> '\u2200'
'∀': Unicode U+2200 (category Sm: Symbol, math)

julia> Int('\0')
0

julia> Int('\t')
9

julia> Int('\n')
10

julia> Int('\e')
27

julia> 'A' < 'a'
true

julia> 'A' <= 'a' <= 'Z'
false

julia> 'A' <= 'X' <= 'Z'
true

julia> str = "Hello,World!"
"Hello,World!"

julia> """Contains "quote" characters"""
"Contains \"quote\" characters"

julia> "This is a long \
ERROR: ParseError:
# Error @ REPL[206]:1:17
"This is a long \
#               ╙ ── invalid escape sequence
Stacktrace:
 [1] top-level scope
   @ none:1

julia> str[end-1]
'd': ASCII/Unicode U+0064 (category Ll: Letter, lowercase)

julia> str[end/2]
ERROR: MethodError: no method matching getindex(::String, ::Float64)
The function `getindex` exists, but no method is defined for this combination of argument types.

Closest candidates are:
  getindex(::String, ::UnitRange{Int64})
   @ Base strings\string.jl:496
  getindex(::String, ::Int64)
   @ Base strings\string.jl:460
  getindex(::String, ::AbstractUnitRange{<:Integer})
   @ Base strings\string.jl:494
  ...

Stacktrace:
 [1] top-level scope
   @ REPL[208]:1

julia> str[4:9]
"lo,Wor"

julia> str = "long string"
"long string"

julia> substr = SubString(str, 1, 4)
"long"

julia> typeof(substr)
SubString{String}

julia> s = "\u2200 x \u2203 y"
"∀ x ∃ y"

julia> s[1]
'∀': Unicode U+2200 (category Sm: Symbol, math)

julia> s[2]
ERROR: StringIndexError: invalid index [2], valid nearby indices [1]=>'∀', [4]=>' 'Stacktrace:
 [1] string_index_err(s::String, i::Int64)
   @ Base .\strings\string.jl:12
 [2] getindex_continued(s::String, i::Int64, u::UInt32)
   @ Base .\strings\string.jl:472
 [3] getindex(s::String, i::Int64)
   @ Base .\strings\string.jl:464
 [4] top-level scope
   @ REPL[215]:1

julia> s[3]
ERROR: StringIndexError: invalid index [3], valid nearby indices [1]=>'∀', [4]=>' 'Stacktrace:
 [1] string_index_err(s::String, i::Int64)
   @ Base .\strings\string.jl:12
 [2] getindex_continued(s::String, i::Int64, u::UInt32)
   @ Base .\strings\string.jl:472
 [3] getindex(s::String, i::Int64)
   @ Base .\strings\string.jl:464
 [4] top-level scope
   @ REPL[216]:1

julia> s[4]
' ': ASCII/Unicode U+0020 (category Zs: Separator, space)

julia> s[end-1]
' ': ASCII/Unicode U+0020 (category Zs: Separator, space)

julia> s[end-2]
ERROR: StringIndexError: invalid index [9], valid nearby indices [7]=>'∃', [10]=>' '
Stacktrace:
 [1] string_index_err(s::String, i::Int64)
   @ Base .\strings\string.jl:12
 [2] getindex_continued(s::String, i::Int64, u::UInt32)
   @ Base .\strings\string.jl:472
 [3] getindex(s::String, i::Int64)
   @ Base .\strings\string.jl:464
 [4] top-level scope
   @ REPL[219]:1

julia> s[1:1]
"∀"

julia> s[1:2]
ERROR: StringIndexError: invalid index [2], valid nearby indices [1]=>'∀', [4]=>' 'Stacktrace:
 [1] string_index_err(s::String, i::Int64)
   @ Base .\strings\string.jl:12
 [2] getindex(s::String, r::UnitRange{Int64})
   @ Base .\strings\string.jl:502
 [3] top-level scope
   @ REPL[221]:1

julia> s[1:4]
"∀ "

julia> for c in s
       println(c)
       end
∀

x

∃

y

julia> #Obtain the valid indicies

julia> collect(eachindex(s))
7-element Vector{Int64}:
  1
  4
  5
  6
  7
 10
 11

julia> "\xc0\xa0\xe2\x88\xe2|"
"\xc0\xa0\xe2\x88\xe2|"

julia> foreach(display, s)
'∀': Unicode U+2200 (category Sm: Symbol, math)
' ': ASCII/Unicode U+0020 (category Zs: Separator, space)
'x': ASCII/Unicode U+0078 (category Ll: Letter, lowercase)
' ': ASCII/Unicode U+0020 (category Zs: Separator, space)
'∃': Unicode U+2203 (category Sm: Symbol, math)
' ': ASCII/Unicode U+0020 (category Zs: Separator, space)
'y': ASCII/Unicode U+0079 (category Ll: Letter, lowercase)

julia> greet = "Hello"
"Hello"

julia> whom = "World"
"World"

julia> string(greet, ", ", whom, ".\n")
"Hello, World.\n"

julia> a, b = "xe2\x88", "\x80"
("xe2\x88", "\x80")

julia> c = string(a,b)
"xe2\x88\x80"

julia> collect.([a,b,c])
3-element Vector{Vector{Char}}:
 ['x', 'e', '2', '\x88']
 ['\x80']
 ['x', 'e', '2', '\x88', '\x80']

julia> length.([a,b,c])
3-element Vector{Int64}:
 4
 1
 5

julia> # Interpolation

julia> greet = "Hello"; whom = "world";

julia> "$greet, $whom.\n"
"Hello, world.\n"

julia> "1 + 2 = $(1+2)"
"1 + 2 = 3"

julia> v = [1,2,3]
ERROR: invalid redefinition of constant Main.v
Stacktrace:
 [1] top-level scope
   @ REPL[239]:1

julia> V = [1,2,3]
3-element Vector{Int64}:
 1
 2
 3

julia> "V: $V"
"V: [1, 2, 3]"

julia> "hi, $c"
"hi, xe2\x88\x80"

julia> print("I have \$100 in my account.\n")
I have $100 in my account.

julia> str = """
              Hello,
              World.
              """
"Hello,\nWorld.\n"

julia> "abracadabra" < "xylophone"
true

julia> "Hello, World" != "Goodbye, World."
true

julia> "1+2 = 3" == "1 + 2 = $(1+2)"
false

julia> findfirst('o', "xylophone")
4

julia> findlast('o', "xylophone")
7

julia> occursin("world", "Hello, world.")
true

julia> occursin("o", "Xylophone")
true

julia> occursin('o', "Xylophon")
true

julia> repeat(".:Z:.", 10)
".:Z:..:Z:..:Z:..:Z:..:Z:..:Z:..:Z:..:Z:..:Z:..:Z:."

julia> join(["apples', "bananas" "pineapples"], ",", " and ")
ERROR: ParseError:
# Error @ REPL[254]:1:18
join(["apples', "bananas" "pineapples"], ",", " and ")
#                └ ── cannot juxtapose string literal
Stacktrace:
 [1] top-level scope
   @ none:1

julia> m = match(r"(a|b)(c)?(d)", "acd")
RegexMatch("acd", 1="a", 2="c", 3="d")

julia> m.match
"acd"

julia> m.captures
3-element Vector{Union{Nothing, SubString{String}}}:
 "a"
 "c"
 "d"

julia> m.offset
1

julia> m.offsets
3-element Vector{Int64}:
 1
 2
 3

julia> m = match(r"(a|b)(c)?(d)", "ad")
RegexMatch("ad", 1="a", 2=nothing, 3="d")

julia> m.captures
3-element Vector{Union{Nothing, SubString{String}}}:
 "a"
 nothing
 "d"

julia> m.offset
1

julia> x = 10
10

julia> r"$x"
r"$x"

julia> "$x"
"10"

julia> r"\x"
r"\x"

julia> "\x"
ERROR: ParseError:
# Error @ REPL[267]:1:2
"\x"
#└┘ ── invalid hex escape sequence
Stacktrace:
 [1] top-level scope
   @ none:1

julia> x = b"123"
3-element Base.CodeUnits{UInt8, String}:
 0x31
 0x32
 0x33

julia> x[1]
0x31

julia> x[1] = 0x32
ERROR: CanonicalIndexError: setindex! not defined for Base.CodeUnits{UInt8, String}Stacktrace:
 [1] error_if_canonical_setindex(::IndexLinear, A::Base.CodeUnits{UInt8, String}, ::Int64)
   @ Base .\abstractarray.jl:1421
 [2] setindex!(A::Base.CodeUnits{UInt8, String}, v::UInt8, I::Int64)
   @ Base .\abstractarray.jl:1412
 [3] top-level scope
   @ REPL[270]:1

julia> Vectore{UInt8}(x)
ERROR: UndefVarError: `Vectore` not defined in `Main`
Suggestion: check for spelling errors or missing imports.
Stacktrace:
 [1] top-level scope
   @ REPL[271]:1

julia> Vector{UInt8}(x)
3-element Vector{UInt8}:
 0x31
 0x32
 0x33

julia>

