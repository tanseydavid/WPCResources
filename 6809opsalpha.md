List of 6809 instructions (in alphabetical order)
=================================================

Compiled by Pugsy of http://www.mamecheat.co.uk
V1 released on 27 Mar 2011

Note there may well be some (very few) omissions/errors in this list.

This list will be handy when you are looking to quickly patch an emulator image without having to dig out
an assembler..but this is only meant for the simplest of jobs not for major changes.

Note: To use this list you should have a understanding of 6809 assembler. All the possible branch
instructions are not shown as it over complicates things.

-----------------------------------------------------------------------------------------------------------

abx                                          3A
adca  #$ff                                   89 FF
adca  $0,s                                   A9 60
adca  $0,u                                   A9 40
adca  $0,x                                   A9 00
adca  $0,y                                   A9 20
adca  $01,pc                                 A9 8C 01
adca  $01,pc                                 A9 AC 01
adca  $01,pc                                 A9 CC 01
adca  $01,pc                                 A9 EC 01
adca  $01,s                                  A9 E8 01
adca  $01,u                                  A9 C8 01
adca  $01,x                                  A9 88 01
adca  $01,y                                  A9 A8 01
adca  $1,s                                   A9 61
adca  $1,u                                   A9 41
adca  $1,x                                   A9 01
adca  $1,y                                   A9 21
adca  $2,s                                   A9 62
adca  $2,u                                   A9 42
adca  $2,x                                   A9 02
adca  $2,y                                   A9 22
adca  $3,s                                   A9 63
adca  $3,u                                   A9 43
adca  $3,x                                   A9 03
adca  $3,y                                   A9 23
adca  $4,s                                   A9 64
adca  $4,u                                   A9 44
adca  $4,x                                   A9 04
adca  $4,y                                   A9 24
adca  $5,s                                   A9 65
adca  $5,u                                   A9 45
adca  $5,x                                   A9 05
adca  $5,y                                   A9 25
adca  $6,s                                   A9 66
adca  $6,u                                   A9 46
adca  $6,x                                   A9 06
adca  $6,y                                   A9 26
adca  $7,s                                   A9 67
adca  $7,u                                   A9 47
adca  $7,x                                   A9 07
adca  $7,y                                   A9 27
adca  $8,s                                   A9 68
adca  $8,u                                   A9 48
adca  $8,x                                   A9 08
adca  $8,y                                   A9 28
adca  $9,s                                   A9 69
adca  $9,u                                   A9 49
adca  $9,x                                   A9 09
adca  $9,y                                   A9 29
adca  $a,s                                   A9 6A
adca  $a,u                                   A9 4A
adca  $a,x                                   A9 0A
adca  $a,y                                   A9 2A
adca  $b,s                                   A9 6B
adca  $b,u                                   A9 4B
adca  $b,x                                   A9 0B
adca  $b,y                                   A9 2B
adca  $beef                                  A9 8F BE EF
adca  $beef                                  A9 AF BE EF
adca  $beef                                  A9 CF BE EF
adca  $beef                                  A9 EF BE EF
adca  $beef                                  B9 BE EF
adca  $beef,pc                               A9 8D BE EF
adca  $beef,pc                               A9 AD BE EF
adca  $beef,pc                               A9 CD BE EF
adca  $beef,pc                               A9 ED BE EF
adca  $beef,s                                A9 E9 BE EF
adca  $beef,u                                A9 C9 BE EF
adca  $beef,x                                A9 89 BE EF
adca  $beef,y                                A9 A9 BE EF
adca  $c,s                                   A9 6C
adca  $c,u                                   A9 4C
adca  $c,x                                   A9 0C
adca  $c,y                                   A9 2C
adca  $d,s                                   A9 6D
adca  $d,u                                   A9 4D
adca  $d,x                                   A9 0D
adca  $d,y                                   A9 2D
adca  $e,s                                   A9 6E
adca  $e,u                                   A9 4E
adca  $e,x                                   A9 0E
adca  $e,y                                   A9 2E
adca  $f,s                                   A9 6F
adca  $f,u                                   A9 4F
adca  $f,x                                   A9 0F
adca  $f,y                                   A9 2F
adca  $ff                                    99 FF
adca  ,--s                                   A9 E3
adca  ,--u                                   A9 C3
adca  ,--x                                   A9 83
adca  ,--y                                   A9 A3
adca  ,-s                                    A9 E2
adca  ,-u                                    A9 C2
adca  ,-x                                    A9 82
adca  ,-y                                    A9 A2
adca  ,s                                     A9 E4
adca  ,s+                                    A9 E0
adca  ,s++                                   A9 E1
adca  ,u                                     A9 C4
adca  ,u+                                    A9 C0
adca  ,u++                                   A9 C1
adca  ,x                                     A9 84
adca  ,x+                                    A9 80
adca  ,x++                                   A9 81
adca  ,y                                     A9 A4
adca  ,y+                                    A9 A0
adca  ,y++                                   A9 A1
adca  -$1,s                                  A9 7F
adca  -$1,u                                  A9 5F
adca  -$1,x                                  A9 1F
adca  -$1,y                                  A9 3F
adca  -$10,s                                 A9 70
adca  -$10,u                                 A9 50
adca  -$10,x                                 A9 10
adca  -$10,y                                 A9 30
adca  -$2,s                                  A9 7E
adca  -$2,u                                  A9 5E
adca  -$2,x                                  A9 1E
adca  -$2,y                                  A9 3E
adca  -$3,s                                  A9 7D
adca  -$3,u                                  A9 5D
adca  -$3,x                                  A9 1D
adca  -$3,y                                  A9 3D
adca  -$4,s                                  A9 7C
adca  -$4,u                                  A9 5C
adca  -$4,x                                  A9 1C
adca  -$4,y                                  A9 3C
adca  -$5,s                                  A9 7B
adca  -$5,u                                  A9 5B
adca  -$5,x                                  A9 1B
adca  -$5,y                                  A9 3B
adca  -$6,s                                  A9 7A
adca  -$6,u                                  A9 5A
adca  -$6,x                                  A9 1A
adca  -$6,y                                  A9 3A
adca  -$7,s                                  A9 79
adca  -$7,u                                  A9 59
adca  -$7,x                                  A9 19
adca  -$7,y                                  A9 39
adca  -$8,s                                  A9 78
adca  -$8,u                                  A9 58
adca  -$8,x                                  A9 18
adca  -$8,y                                  A9 38
adca  -$9,s                                  A9 77
adca  -$9,u                                  A9 57
adca  -$9,x                                  A9 17
adca  -$9,y                                  A9 37
adca  -$a,s                                  A9 76
adca  -$a,u                                  A9 56
adca  -$a,x                                  A9 16
adca  -$a,y                                  A9 36
adca  -$b,s                                  A9 75
adca  -$b,u                                  A9 55
adca  -$b,x                                  A9 15
adca  -$b,y                                  A9 35
adca  -$c,s                                  A9 74
adca  -$c,u                                  A9 54
adca  -$c,x                                  A9 14
adca  -$c,y                                  A9 34
adca  -$d,s                                  A9 73
adca  -$d,u                                  A9 53
adca  -$d,x                                  A9 13
adca  -$d,y                                  A9 33
adca  -$e,s                                  A9 72
adca  -$e,u                                  A9 52
adca  -$e,x                                  A9 12
adca  -$e,y                                  A9 32
adca  -$f,s                                  A9 71
adca  -$f,u                                  A9 51
adca  -$f,x                                  A9 11
adca  -$f,y                                  A9 31
adca  a,s                                    A9 E6
adca  a,u                                    A9 C6
adca  a,x                                    A9 86
adca  a,y                                    A9 A6
adca  b,s                                    A9 E5
adca  b,u                                    A9 C5
adca  b,x                                    A9 85
adca  b,y                                    A9 A5
adca  d,s                                    A9 EB
adca  d,u                                    A9 CB
adca  d,x                                    A9 8B
adca  d,y                                    A9 AB
adca  [$01,pc]                               A9 9C 01
adca  [$01,pc]                               A9 BC 01
adca  [$01,pc]                               A9 DC 01
adca  [$01,pc]                               A9 FC 01
adca  [$01,s]                                A9 F8 01
adca  [$01,u]                                A9 D8 01
adca  [$01,x]                                A9 98 01
adca  [$01,y]                                A9 B8 01
adca  [$beef,pc]                             A9 9D BE EF
adca  [$beef,pc]                             A9 BD BE EF
adca  [$beef,pc]                             A9 DD BE EF
adca  [$beef,pc]                             A9 FD BE EF
adca  [$beef,s]                              A9 F9 BE EF
adca  [$beef,u]                              A9 D9 BE EF
adca  [$beef,x]                              A9 99 BE EF
adca  [$beef,y]                              A9 B9 BE EF
adca  [$beef]                                A9 9F BE EF
adca  [$beef]                                A9 BF BE EF
adca  [$beef]                                A9 DF BE EF
adca  [$beef]                                A9 FF BE EF
adca  [,--s]                                 A9 F3
adca  [,--u]                                 A9 D3
adca  [,--x]                                 A9 93
adca  [,--y]                                 A9 B3
adca  [,s++]                                 A9 F1
adca  [,s]                                   A9 F4
adca  [,u++]                                 A9 D1
adca  [,u]                                   A9 D4
adca  [,x++]                                 A9 91
adca  [,x]                                   A9 94
adca  [,y++]                                 A9 B1
adca  [,y]                                   A9 B4
adca  [a,s]                                  A9 F6
adca  [a,u]                                  A9 D6
adca  [a,x]                                  A9 96
adca  [a,y]                                  A9 B6
adca  [b,s]                                  A9 F5
adca  [b,u]                                  A9 D5
adca  [b,x]                                  A9 95
adca  [b,y]                                  A9 B5
adca  [d,s]                                  A9 FB
adca  [d,u]                                  A9 DB
adca  [d,x]                                  A9 9B
adca  [d,y]                                  A9 BB
adca  []                                     A9 97
adca  []                                     A9 9A
adca  []                                     A9 9E
adca  []                                     A9 B7
adca  []                                     A9 BA
adca  []                                     A9 BE
adca  []                                     A9 D7
adca  []                                     A9 DA
adca  []                                     A9 DE
adca  []                                     A9 F7
adca  []                                     A9 FA
adca  []                                     A9 FE
adcb  #$ff                                   C9 FF
adcb  $0,s                                   E9 60
adcb  $0,u                                   E9 40
adcb  $0,x                                   E9 00
adcb  $0,y                                   E9 20
adcb  $01,pc                                 E9 8C 01
adcb  $01,pc                                 E9 AC 01
adcb  $01,pc                                 E9 CC 01
adcb  $01,pc                                 E9 EC 01
adcb  $01,s                                  E9 E8 01
adcb  $01,u                                  E9 C8 01
adcb  $01,x                                  E9 88 01
adcb  $01,y                                  E9 A8 01
adcb  $1,s                                   E9 61
adcb  $1,u                                   E9 41
adcb  $1,x                                   E9 01
adcb  $1,y                                   E9 21
adcb  $2,s                                   E9 62
adcb  $2,u                                   E9 42
adcb  $2,x                                   E9 02
adcb  $2,y                                   E9 22
adcb  $3,s                                   E9 63
adcb  $3,u                                   E9 43
adcb  $3,x                                   E9 03
adcb  $3,y                                   E9 23
adcb  $4,s                                   E9 64
adcb  $4,u                                   E9 44
adcb  $4,x                                   E9 04
adcb  $4,y                                   E9 24
adcb  $5,s                                   E9 65
adcb  $5,u                                   E9 45
adcb  $5,x                                   E9 05
adcb  $5,y                                   E9 25
adcb  $6,s                                   E9 66
adcb  $6,u                                   E9 46
adcb  $6,x                                   E9 06
adcb  $6,y                                   E9 26
adcb  $7,s                                   E9 67
adcb  $7,u                                   E9 47
adcb  $7,x                                   E9 07
adcb  $7,y                                   E9 27
adcb  $8,s                                   E9 68
adcb  $8,u                                   E9 48
adcb  $8,x                                   E9 08
adcb  $8,y                                   E9 28
adcb  $9,s                                   E9 69
adcb  $9,u                                   E9 49
adcb  $9,x                                   E9 09
adcb  $9,y                                   E9 29
adcb  $a,s                                   E9 6A
adcb  $a,u                                   E9 4A
adcb  $a,x                                   E9 0A
adcb  $a,y                                   E9 2A
adcb  $b,s                                   E9 6B
adcb  $b,u                                   E9 4B
adcb  $b,x                                   E9 0B
adcb  $b,y                                   E9 2B
adcb  $beef                                  E9 8F BE EF
adcb  $beef                                  E9 AF BE EF
adcb  $beef                                  E9 CF BE EF
adcb  $beef                                  E9 EF BE EF
adcb  $beef                                  F9 BE EF
adcb  $beef,pc                               E9 8D BE EF
adcb  $beef,pc                               E9 AD BE EF
adcb  $beef,pc                               E9 CD BE EF
adcb  $beef,pc                               E9 ED BE EF
adcb  $beef,s                                E9 E9 BE EF
adcb  $beef,u                                E9 C9 BE EF
adcb  $beef,x                                E9 89 BE EF
adcb  $beef,y                                E9 A9 BE EF
adcb  $c,s                                   E9 6C
adcb  $c,u                                   E9 4C
adcb  $c,x                                   E9 0C
adcb  $c,y                                   E9 2C
adcb  $d,s                                   E9 6D
adcb  $d,u                                   E9 4D
adcb  $d,x                                   E9 0D
adcb  $d,y                                   E9 2D
adcb  $e,s                                   E9 6E
adcb  $e,u                                   E9 4E
adcb  $e,x                                   E9 0E
adcb  $e,y                                   E9 2E
adcb  $f,s                                   E9 6F
adcb  $f,u                                   E9 4F
adcb  $f,x                                   E9 0F
adcb  $f,y                                   E9 2F
adcb  $ff                                    D9 FF
adcb  ,--s                                   E9 E3
adcb  ,--u                                   E9 C3
adcb  ,--x                                   E9 83
adcb  ,--y                                   E9 A3
adcb  ,-s                                    E9 E2
adcb  ,-u                                    E9 C2
adcb  ,-x                                    E9 82
adcb  ,-y                                    E9 A2
adcb  ,s                                     E9 E4
adcb  ,s+                                    E9 E0
adcb  ,s++                                   E9 E1
adcb  ,u                                     E9 C4
adcb  ,u+                                    E9 C0
adcb  ,u++                                   E9 C1
adcb  ,x                                     E9 84
adcb  ,x+                                    E9 80
adcb  ,x++                                   E9 81
adcb  ,y                                     E9 A4
adcb  ,y+                                    E9 A0
adcb  ,y++                                   E9 A1
adcb  -$1,s                                  E9 7F
adcb  -$1,u                                  E9 5F
adcb  -$1,x                                  E9 1F
adcb  -$1,y                                  E9 3F
adcb  -$10,s                                 E9 70
adcb  -$10,u                                 E9 50
adcb  -$10,x                                 E9 10
adcb  -$10,y                                 E9 30
adcb  -$2,s                                  E9 7E
adcb  -$2,u                                  E9 5E
adcb  -$2,x                                  E9 1E
adcb  -$2,y                                  E9 3E
adcb  -$3,s                                  E9 7D
adcb  -$3,u                                  E9 5D
adcb  -$3,x                                  E9 1D
adcb  -$3,y                                  E9 3D
adcb  -$4,s                                  E9 7C
adcb  -$4,u                                  E9 5C
adcb  -$4,x                                  E9 1C
adcb  -$4,y                                  E9 3C
adcb  -$5,s                                  E9 7B
adcb  -$5,u                                  E9 5B
adcb  -$5,x                                  E9 1B
adcb  -$5,y                                  E9 3B
adcb  -$6,s                                  E9 7A
adcb  -$6,u                                  E9 5A
adcb  -$6,x                                  E9 1A
adcb  -$6,y                                  E9 3A
adcb  -$7,s                                  E9 79
adcb  -$7,u                                  E9 59
adcb  -$7,x                                  E9 19
adcb  -$7,y                                  E9 39
adcb  -$8,s                                  E9 78
adcb  -$8,u                                  E9 58
adcb  -$8,x                                  E9 18
adcb  -$8,y                                  E9 38
adcb  -$9,s                                  E9 77
adcb  -$9,u                                  E9 57
adcb  -$9,x                                  E9 17
adcb  -$9,y                                  E9 37
adcb  -$a,s                                  E9 76
adcb  -$a,u                                  E9 56
adcb  -$a,x                                  E9 16
adcb  -$a,y                                  E9 36
adcb  -$b,s                                  E9 75
adcb  -$b,u                                  E9 55
adcb  -$b,x                                  E9 15
adcb  -$b,y                                  E9 35
adcb  -$c,s                                  E9 74
adcb  -$c,u                                  E9 54
adcb  -$c,x                                  E9 14
adcb  -$c,y                                  E9 34
adcb  -$d,s                                  E9 73
adcb  -$d,u                                  E9 53
adcb  -$d,x                                  E9 13
adcb  -$d,y                                  E9 33
adcb  -$e,s                                  E9 72
adcb  -$e,u                                  E9 52
adcb  -$e,x                                  E9 12
adcb  -$e,y                                  E9 32
adcb  -$f,s                                  E9 71
adcb  -$f,u                                  E9 51
adcb  -$f,x                                  E9 11
adcb  -$f,y                                  E9 31
adcb  a,s                                    E9 E6
adcb  a,u                                    E9 C6
adcb  a,x                                    E9 86
adcb  a,y                                    E9 A6
adcb  b,s                                    E9 E5
adcb  b,u                                    E9 C5
adcb  b,x                                    E9 85
adcb  b,y                                    E9 A5
adcb  d,s                                    E9 EB
adcb  d,u                                    E9 CB
adcb  d,x                                    E9 8B
adcb  d,y                                    E9 AB
adcb  [$01,pc]                               E9 9C 01
adcb  [$01,pc]                               E9 BC 01
adcb  [$01,pc]                               E9 DC 01
adcb  [$01,pc]                               E9 FC 01
adcb  [$01,s]                                E9 F8 01
adcb  [$01,u]                                E9 D8 01
adcb  [$01,x]                                E9 98 01
adcb  [$01,y]                                E9 B8 01
adcb  [$beef,pc]                             E9 9D BE EF
adcb  [$beef,pc]                             E9 BD BE EF
adcb  [$beef,pc]                             E9 DD BE EF
adcb  [$beef,pc]                             E9 FD BE EF
adcb  [$beef,s]                              E9 F9 BE EF
adcb  [$beef,u]                              E9 D9 BE EF
adcb  [$beef,x]                              E9 99 BE EF
adcb  [$beef,y]                              E9 B9 BE EF
adcb  [$beef]                                E9 9F BE EF
adcb  [$beef]                                E9 BF BE EF
adcb  [$beef]                                E9 DF BE EF
adcb  [$beef]                                E9 FF BE EF
adcb  [,--s]                                 E9 F3
adcb  [,--u]                                 E9 D3
adcb  [,--x]                                 E9 93
adcb  [,--y]                                 E9 B3
adcb  [,s++]                                 E9 F1
adcb  [,s]                                   E9 F4
adcb  [,u++]                                 E9 D1
adcb  [,u]                                   E9 D4
adcb  [,x++]                                 E9 91
adcb  [,x]                                   E9 94
adcb  [,y++]                                 E9 B1
adcb  [,y]                                   E9 B4
adcb  [a,s]                                  E9 F6
adcb  [a,u]                                  E9 D6
adcb  [a,x]                                  E9 96
adcb  [a,y]                                  E9 B6
adcb  [b,s]                                  E9 F5
adcb  [b,u]                                  E9 D5
adcb  [b,x]                                  E9 95
adcb  [b,y]                                  E9 B5
adcb  [d,s]                                  E9 FB
adcb  [d,u]                                  E9 DB
adcb  [d,x]                                  E9 9B
adcb  [d,y]                                  E9 BB
adcb  []                                     E9 97
adcb  []                                     E9 9A
adcb  []                                     E9 9E
adcb  []                                     E9 B7
adcb  []                                     E9 BA
adcb  []                                     E9 BE
adcb  []                                     E9 D7
adcb  []                                     E9 DA
adcb  []                                     E9 DE
adcb  []                                     E9 F7
adcb  []                                     E9 FA
adcb  []                                     E9 FE
adda  #$ff                                   8B FF
adda  $0,s                                   AB 60
adda  $0,u                                   AB 40
adda  $0,x                                   AB 00
adda  $0,y                                   AB 20
adda  $01,pc                                 AB 8C 01
adda  $01,pc                                 AB AC 01
adda  $01,pc                                 AB CC 01
adda  $01,pc                                 AB EC 01
adda  $01,s                                  AB E8 01
adda  $01,u                                  AB C8 01
adda  $01,x                                  AB 88 01
adda  $01,y                                  AB A8 01
adda  $1,s                                   AB 61
adda  $1,u                                   AB 41
adda  $1,x                                   AB 01
adda  $1,y                                   AB 21
adda  $2,s                                   AB 62
adda  $2,u                                   AB 42
adda  $2,x                                   AB 02
adda  $2,y                                   AB 22
adda  $3,s                                   AB 63
adda  $3,u                                   AB 43
adda  $3,x                                   AB 03
adda  $3,y                                   AB 23
adda  $4,s                                   AB 64
adda  $4,u                                   AB 44
adda  $4,x                                   AB 04
adda  $4,y                                   AB 24
adda  $5,s                                   AB 65
adda  $5,u                                   AB 45
adda  $5,x                                   AB 05
adda  $5,y                                   AB 25
adda  $6,s                                   AB 66
adda  $6,u                                   AB 46
adda  $6,x                                   AB 06
adda  $6,y                                   AB 26
adda  $7,s                                   AB 67
adda  $7,u                                   AB 47
adda  $7,x                                   AB 07
adda  $7,y                                   AB 27
adda  $8,s                                   AB 68
adda  $8,u                                   AB 48
adda  $8,x                                   AB 08
adda  $8,y                                   AB 28
adda  $9,s                                   AB 69
adda  $9,u                                   AB 49
adda  $9,x                                   AB 09
adda  $9,y                                   AB 29
adda  $a,s                                   AB 6A
adda  $a,u                                   AB 4A
adda  $a,x                                   AB 0A
adda  $a,y                                   AB 2A
adda  $b,s                                   AB 6B
adda  $b,u                                   AB 4B
adda  $b,x                                   AB 0B
adda  $b,y                                   AB 2B
adda  $beef                                  AB 8F BE EF
adda  $beef                                  AB AF BE EF
adda  $beef                                  AB CF BE EF
adda  $beef                                  AB EF BE EF
adda  $beef                                  BB BE EF
adda  $beef,pc                               AB 8D BE EF
adda  $beef,pc                               AB AD BE EF
adda  $beef,pc                               AB CD BE EF
adda  $beef,pc                               AB ED BE EF
adda  $beef,s                                AB E9 BE EF
adda  $beef,u                                AB C9 BE EF
adda  $beef,x                                AB 89 BE EF
adda  $beef,y                                AB A9 BE EF
adda  $c,s                                   AB 6C
adda  $c,u                                   AB 4C
adda  $c,x                                   AB 0C
adda  $c,y                                   AB 2C
adda  $d,s                                   AB 6D
adda  $d,u                                   AB 4D
adda  $d,x                                   AB 0D
adda  $d,y                                   AB 2D
adda  $e,s                                   AB 6E
adda  $e,u                                   AB 4E
adda  $e,x                                   AB 0E
adda  $e,y                                   AB 2E
adda  $f,s                                   AB 6F
adda  $f,u                                   AB 4F
adda  $f,x                                   AB 0F
adda  $f,y                                   AB 2F
adda  $ff                                    9B FF
adda  ,--s                                   AB E3
adda  ,--u                                   AB C3
adda  ,--x                                   AB 83
adda  ,--y                                   AB A3
adda  ,-s                                    AB E2
adda  ,-u                                    AB C2
adda  ,-x                                    AB 82
adda  ,-y                                    AB A2
adda  ,s                                     AB E4
adda  ,s+                                    AB E0
adda  ,s++                                   AB E1
adda  ,u                                     AB C4
adda  ,u+                                    AB C0
adda  ,u++                                   AB C1
adda  ,x                                     AB 84
adda  ,x+                                    AB 80
adda  ,x++                                   AB 81
adda  ,y                                     AB A4
adda  ,y+                                    AB A0
adda  ,y++                                   AB A1
adda  -$1,s                                  AB 7F
adda  -$1,u                                  AB 5F
adda  -$1,x                                  AB 1F
adda  -$1,y                                  AB 3F
adda  -$10,s                                 AB 70
adda  -$10,u                                 AB 50
adda  -$10,x                                 AB 10
adda  -$10,y                                 AB 30
adda  -$2,s                                  AB 7E
adda  -$2,u                                  AB 5E
adda  -$2,x                                  AB 1E
adda  -$2,y                                  AB 3E
adda  -$3,s                                  AB 7D
adda  -$3,u                                  AB 5D
adda  -$3,x                                  AB 1D
adda  -$3,y                                  AB 3D
adda  -$4,s                                  AB 7C
adda  -$4,u                                  AB 5C
adda  -$4,x                                  AB 1C
adda  -$4,y                                  AB 3C
adda  -$5,s                                  AB 7B
adda  -$5,u                                  AB 5B
adda  -$5,x                                  AB 1B
adda  -$5,y                                  AB 3B
adda  -$6,s                                  AB 7A
adda  -$6,u                                  AB 5A
adda  -$6,x                                  AB 1A
adda  -$6,y                                  AB 3A
adda  -$7,s                                  AB 79
adda  -$7,u                                  AB 59
adda  -$7,x                                  AB 19
adda  -$7,y                                  AB 39
adda  -$8,s                                  AB 78
adda  -$8,u                                  AB 58
adda  -$8,x                                  AB 18
adda  -$8,y                                  AB 38
adda  -$9,s                                  AB 77
adda  -$9,u                                  AB 57
adda  -$9,x                                  AB 17
adda  -$9,y                                  AB 37
adda  -$a,s                                  AB 76
adda  -$a,u                                  AB 56
adda  -$a,x                                  AB 16
adda  -$a,y                                  AB 36
adda  -$b,s                                  AB 75
adda  -$b,u                                  AB 55
adda  -$b,x                                  AB 15
adda  -$b,y                                  AB 35
adda  -$c,s                                  AB 74
adda  -$c,u                                  AB 54
adda  -$c,x                                  AB 14
adda  -$c,y                                  AB 34
adda  -$d,s                                  AB 73
adda  -$d,u                                  AB 53
adda  -$d,x                                  AB 13
adda  -$d,y                                  AB 33
adda  -$e,s                                  AB 72
adda  -$e,u                                  AB 52
adda  -$e,x                                  AB 12
adda  -$e,y                                  AB 32
adda  -$f,s                                  AB 71
adda  -$f,u                                  AB 51
adda  -$f,x                                  AB 11
adda  -$f,y                                  AB 31
adda  a,s                                    AB E6
adda  a,u                                    AB C6
adda  a,x                                    AB 86
adda  a,y                                    AB A6
adda  b,s                                    AB E5
adda  b,u                                    AB C5
adda  b,x                                    AB 85
adda  b,y                                    AB A5
adda  d,s                                    AB EB
adda  d,u                                    AB CB
adda  d,x                                    AB 8B
adda  d,y                                    AB AB
adda  [$01,pc]                               AB 9C 01
adda  [$01,pc]                               AB BC 01
adda  [$01,pc]                               AB DC 01
adda  [$01,pc]                               AB FC 01
adda  [$01,s]                                AB F8 01
adda  [$01,u]                                AB D8 01
adda  [$01,x]                                AB 98 01
adda  [$01,y]                                AB B8 01
adda  [$beef,pc]                             AB 9D BE EF
adda  [$beef,pc]                             AB BD BE EF
adda  [$beef,pc]                             AB DD BE EF
adda  [$beef,pc]                             AB FD BE EF
adda  [$beef,s]                              AB F9 BE EF
adda  [$beef,u]                              AB D9 BE EF
adda  [$beef,x]                              AB 99 BE EF
adda  [$beef,y]                              AB B9 BE EF
adda  [$beef]                                AB 9F BE EF
adda  [$beef]                                AB BF BE EF
adda  [$beef]                                AB DF BE EF
adda  [$beef]                                AB FF BE EF
adda  [,--s]                                 AB F3
adda  [,--u]                                 AB D3
adda  [,--x]                                 AB 93
adda  [,--y]                                 AB B3
adda  [,s++]                                 AB F1
adda  [,s]                                   AB F4
adda  [,u++]                                 AB D1
adda  [,u]                                   AB D4
adda  [,x++]                                 AB 91
adda  [,x]                                   AB 94
adda  [,y++]                                 AB B1
adda  [,y]                                   AB B4
adda  [a,s]                                  AB F6
adda  [a,u]                                  AB D6
adda  [a,x]                                  AB 96
adda  [a,y]                                  AB B6
adda  [b,s]                                  AB F5
adda  [b,u]                                  AB D5
adda  [b,x]                                  AB 95
adda  [b,y]                                  AB B5
adda  [d,s]                                  AB FB
adda  [d,u]                                  AB DB
adda  [d,x]                                  AB 9B
adda  [d,y]                                  AB BB
adda  []                                     AB 97
adda  []                                     AB 9A
adda  []                                     AB 9E
adda  []                                     AB B7
adda  []                                     AB BA
adda  []                                     AB BE
adda  []                                     AB D7
adda  []                                     AB DA
adda  []                                     AB DE
adda  []                                     AB F7
adda  []                                     AB FA
adda  []                                     AB FE
addb  #$ff                                   CB FF
addb  $0,s                                   EB 60
addb  $0,u                                   EB 40
addb  $0,x                                   EB 00
addb  $0,y                                   EB 20
addb  $01,pc                                 EB 8C 01
addb  $01,pc                                 EB AC 01
addb  $01,pc                                 EB CC 01
addb  $01,pc                                 EB EC 01
addb  $01,s                                  EB E8 01
addb  $01,u                                  EB C8 01
addb  $01,x                                  EB 88 01
addb  $01,y                                  EB A8 01
addb  $1,s                                   EB 61
addb  $1,u                                   EB 41
addb  $1,x                                   EB 01
addb  $1,y                                   EB 21
addb  $2,s                                   EB 62
addb  $2,u                                   EB 42
addb  $2,x                                   EB 02
addb  $2,y                                   EB 22
addb  $3,s                                   EB 63
addb  $3,u                                   EB 43
addb  $3,x                                   EB 03
addb  $3,y                                   EB 23
addb  $4,s                                   EB 64
addb  $4,u                                   EB 44
addb  $4,x                                   EB 04
addb  $4,y                                   EB 24
addb  $5,s                                   EB 65
addb  $5,u                                   EB 45
addb  $5,x                                   EB 05
addb  $5,y                                   EB 25
addb  $6,s                                   EB 66
addb  $6,u                                   EB 46
addb  $6,x                                   EB 06
addb  $6,y                                   EB 26
addb  $7,s                                   EB 67
addb  $7,u                                   EB 47
addb  $7,x                                   EB 07
addb  $7,y                                   EB 27
addb  $8,s                                   EB 68
addb  $8,u                                   EB 48
addb  $8,x                                   EB 08
addb  $8,y                                   EB 28
addb  $9,s                                   EB 69
addb  $9,u                                   EB 49
addb  $9,x                                   EB 09
addb  $9,y                                   EB 29
addb  $a,s                                   EB 6A
addb  $a,u                                   EB 4A
addb  $a,x                                   EB 0A
addb  $a,y                                   EB 2A
addb  $b,s                                   EB 6B
addb  $b,u                                   EB 4B
addb  $b,x                                   EB 0B
addb  $b,y                                   EB 2B
addb  $beef                                  EB 8F BE EF
addb  $beef                                  EB AF BE EF
addb  $beef                                  EB CF BE EF
addb  $beef                                  EB EF BE EF
addb  $beef                                  FB BE EF
addb  $beef,pc                               EB 8D BE EF
addb  $beef,pc                               EB AD BE EF
addb  $beef,pc                               EB CD BE EF
addb  $beef,pc                               EB ED BE EF
addb  $beef,s                                EB E9 BE EF
addb  $beef,u                                EB C9 BE EF
addb  $beef,x                                EB 89 BE EF
addb  $beef,y                                EB A9 BE EF
addb  $c,s                                   EB 6C
addb  $c,u                                   EB 4C
addb  $c,x                                   EB 0C
addb  $c,y                                   EB 2C
addb  $d,s                                   EB 6D
addb  $d,u                                   EB 4D
addb  $d,x                                   EB 0D
addb  $d,y                                   EB 2D
addb  $e,s                                   EB 6E
addb  $e,u                                   EB 4E
addb  $e,x                                   EB 0E
addb  $e,y                                   EB 2E
addb  $f,s                                   EB 6F
addb  $f,u                                   EB 4F
addb  $f,x                                   EB 0F
addb  $f,y                                   EB 2F
addb  $ff                                    DB FF
addb  ,--s                                   EB E3
addb  ,--u                                   EB C3
addb  ,--x                                   EB 83
addb  ,--y                                   EB A3
addb  ,-s                                    EB E2
addb  ,-u                                    EB C2
addb  ,-x                                    EB 82
addb  ,-y                                    EB A2
addb  ,s                                     EB E4
addb  ,s+                                    EB E0
addb  ,s++                                   EB E1
addb  ,u                                     EB C4
addb  ,u+                                    EB C0
addb  ,u++                                   EB C1
addb  ,x                                     EB 84
addb  ,x+                                    EB 80
addb  ,x++                                   EB 81
addb  ,y                                     EB A4
addb  ,y+                                    EB A0
addb  ,y++                                   EB A1
addb  -$1,s                                  EB 7F
addb  -$1,u                                  EB 5F
addb  -$1,x                                  EB 1F
addb  -$1,y                                  EB 3F
addb  -$10,s                                 EB 70
addb  -$10,u                                 EB 50
addb  -$10,x                                 EB 10
addb  -$10,y                                 EB 30
addb  -$2,s                                  EB 7E
addb  -$2,u                                  EB 5E
addb  -$2,x                                  EB 1E
addb  -$2,y                                  EB 3E
addb  -$3,s                                  EB 7D
addb  -$3,u                                  EB 5D
addb  -$3,x                                  EB 1D
addb  -$3,y                                  EB 3D
addb  -$4,s                                  EB 7C
addb  -$4,u                                  EB 5C
addb  -$4,x                                  EB 1C
addb  -$4,y                                  EB 3C
addb  -$5,s                                  EB 7B
addb  -$5,u                                  EB 5B
addb  -$5,x                                  EB 1B
addb  -$5,y                                  EB 3B
addb  -$6,s                                  EB 7A
addb  -$6,u                                  EB 5A
addb  -$6,x                                  EB 1A
addb  -$6,y                                  EB 3A
addb  -$7,s                                  EB 79
addb  -$7,u                                  EB 59
addb  -$7,x                                  EB 19
addb  -$7,y                                  EB 39
addb  -$8,s                                  EB 78
addb  -$8,u                                  EB 58
addb  -$8,x                                  EB 18
addb  -$8,y                                  EB 38
addb  -$9,s                                  EB 77
addb  -$9,u                                  EB 57
addb  -$9,x                                  EB 17
addb  -$9,y                                  EB 37
addb  -$a,s                                  EB 76
addb  -$a,u                                  EB 56
addb  -$a,x                                  EB 16
addb  -$a,y                                  EB 36
addb  -$b,s                                  EB 75
addb  -$b,u                                  EB 55
addb  -$b,x                                  EB 15
addb  -$b,y                                  EB 35
addb  -$c,s                                  EB 74
addb  -$c,u                                  EB 54
addb  -$c,x                                  EB 14
addb  -$c,y                                  EB 34
addb  -$d,s                                  EB 73
addb  -$d,u                                  EB 53
addb  -$d,x                                  EB 13
addb  -$d,y                                  EB 33
addb  -$e,s                                  EB 72
addb  -$e,u                                  EB 52
addb  -$e,x                                  EB 12
addb  -$e,y                                  EB 32
addb  -$f,s                                  EB 71
addb  -$f,u                                  EB 51
addb  -$f,x                                  EB 11
addb  -$f,y                                  EB 31
addb  a,s                                    EB E6
addb  a,u                                    EB C6
addb  a,x                                    EB 86
addb  a,y                                    EB A6
addb  b,s                                    EB E5
addb  b,u                                    EB C5
addb  b,x                                    EB 85
addb  b,y                                    EB A5
addb  d,s                                    EB EB
addb  d,u                                    EB CB
addb  d,x                                    EB 8B
addb  d,y                                    EB AB
addb  [$01,pc]                               EB 9C 01
addb  [$01,pc]                               EB BC 01
addb  [$01,pc]                               EB DC 01
addb  [$01,pc]                               EB FC 01
addb  [$01,s]                                EB F8 01
addb  [$01,u]                                EB D8 01
addb  [$01,x]                                EB 98 01
addb  [$01,y]                                EB B8 01
addb  [$beef,pc]                             EB 9D BE EF
addb  [$beef,pc]                             EB BD BE EF
addb  [$beef,pc]                             EB DD BE EF
addb  [$beef,pc]                             EB FD BE EF
addb  [$beef,s]                              EB F9 BE EF
addb  [$beef,u]                              EB D9 BE EF
addb  [$beef,x]                              EB 99 BE EF
addb  [$beef,y]                              EB B9 BE EF
addb  [$beef]                                EB 9F BE EF
addb  [$beef]                                EB BF BE EF
addb  [$beef]                                EB DF BE EF
addb  [$beef]                                EB FF BE EF
addb  [,--s]                                 EB F3
addb  [,--u]                                 EB D3
addb  [,--x]                                 EB 93
addb  [,--y]                                 EB B3
addb  [,s++]                                 EB F1
addb  [,s]                                   EB F4
addb  [,u++]                                 EB D1
addb  [,u]                                   EB D4
addb  [,x++]                                 EB 91
addb  [,x]                                   EB 94
addb  [,y++]                                 EB B1
addb  [,y]                                   EB B4
addb  [a,s]                                  EB F6
addb  [a,u]                                  EB D6
addb  [a,x]                                  EB 96
addb  [a,y]                                  EB B6
addb  [b,s]                                  EB F5
addb  [b,u]                                  EB D5
addb  [b,x]                                  EB 95
addb  [b,y]                                  EB B5
addb  [d,s]                                  EB FB
addb  [d,u]                                  EB DB
addb  [d,x]                                  EB 9B
addb  [d,y]                                  EB BB
addb  []                                     EB 97
addb  []                                     EB 9A
addb  []                                     EB 9E
addb  []                                     EB B7
addb  []                                     EB BA
addb  []                                     EB BE
addb  []                                     EB D7
addb  []                                     EB DA
addb  []                                     EB DE
addb  []                                     EB F7
addb  []                                     EB FA
addb  []                                     EB FE
addd  #$beef                                 C3 BE EF
addd  $0,s                                   E3 60
addd  $0,u                                   E3 40
addd  $0,x                                   E3 00
addd  $0,y                                   E3 20
addd  $01,pc                                 E3 8C 01
addd  $01,pc                                 E3 AC 01
addd  $01,pc                                 E3 CC 01
addd  $01,pc                                 E3 EC 01
addd  $01,s                                  E3 E8 01
addd  $01,u                                  E3 C8 01
addd  $01,x                                  E3 88 01
addd  $01,y                                  E3 A8 01
addd  $1,s                                   E3 61
addd  $1,u                                   E3 41
addd  $1,x                                   E3 01
addd  $1,y                                   E3 21
addd  $2,s                                   E3 62
addd  $2,u                                   E3 42
addd  $2,x                                   E3 02
addd  $2,y                                   E3 22
addd  $3,s                                   E3 63
addd  $3,u                                   E3 43
addd  $3,x                                   E3 03
addd  $3,y                                   E3 23
addd  $4,s                                   E3 64
addd  $4,u                                   E3 44
addd  $4,x                                   E3 04
addd  $4,y                                   E3 24
addd  $5,s                                   E3 65
addd  $5,u                                   E3 45
addd  $5,x                                   E3 05
addd  $5,y                                   E3 25
addd  $6,s                                   E3 66
addd  $6,u                                   E3 46
addd  $6,x                                   E3 06
addd  $6,y                                   E3 26
addd  $7,s                                   E3 67
addd  $7,u                                   E3 47
addd  $7,x                                   E3 07
addd  $7,y                                   E3 27
addd  $8,s                                   E3 68
addd  $8,u                                   E3 48
addd  $8,x                                   E3 08
addd  $8,y                                   E3 28
addd  $9,s                                   E3 69
addd  $9,u                                   E3 49
addd  $9,x                                   E3 09
addd  $9,y                                   E3 29
addd  $a,s                                   E3 6A
addd  $a,u                                   E3 4A
addd  $a,x                                   E3 0A
addd  $a,y                                   E3 2A
addd  $b,s                                   E3 6B
addd  $b,u                                   E3 4B
addd  $b,x                                   E3 0B
addd  $b,y                                   E3 2B
addd  $beef                                  E3 8F BE EF
addd  $beef                                  E3 AF BE EF
addd  $beef                                  E3 CF BE EF
addd  $beef                                  E3 EF BE EF
addd  $beef                                  F3 BE EF
addd  $beef,pc                               E3 8D BE EF
addd  $beef,pc                               E3 AD BE EF
addd  $beef,pc                               E3 CD BE EF
addd  $beef,pc                               E3 ED BE EF
addd  $beef,s                                E3 E9 BE EF
addd  $beef,u                                E3 C9 BE EF
addd  $beef,x                                E3 89 BE EF
addd  $beef,y                                E3 A9 BE EF
addd  $c,s                                   E3 6C
addd  $c,u                                   E3 4C
addd  $c,x                                   E3 0C
addd  $c,y                                   E3 2C
addd  $d,s                                   E3 6D
addd  $d,u                                   E3 4D
addd  $d,x                                   E3 0D
addd  $d,y                                   E3 2D
addd  $e,s                                   E3 6E
addd  $e,u                                   E3 4E
addd  $e,x                                   E3 0E
addd  $e,y                                   E3 2E
addd  $f,s                                   E3 6F
addd  $f,u                                   E3 4F
addd  $f,x                                   E3 0F
addd  $f,y                                   E3 2F
addd  $ff                                    D3 FF
addd  ,--s                                   E3 E3
addd  ,--u                                   E3 C3
addd  ,--x                                   E3 83
addd  ,--y                                   E3 A3
addd  ,-s                                    E3 E2
addd  ,-u                                    E3 C2
addd  ,-x                                    E3 82
addd  ,-y                                    E3 A2
addd  ,s                                     E3 E4
addd  ,s+                                    E3 E0
addd  ,s++                                   E3 E1
addd  ,u                                     E3 C4
addd  ,u+                                    E3 C0
addd  ,u++                                   E3 C1
addd  ,x                                     E3 84
addd  ,x+                                    E3 80
addd  ,x++                                   E3 81
addd  ,y                                     E3 A4
addd  ,y+                                    E3 A0
addd  ,y++                                   E3 A1
addd  -$1,s                                  E3 7F
addd  -$1,u                                  E3 5F
addd  -$1,x                                  E3 1F
addd  -$1,y                                  E3 3F
addd  -$10,s                                 E3 70
addd  -$10,u                                 E3 50
addd  -$10,x                                 E3 10
addd  -$10,y                                 E3 30
addd  -$2,s                                  E3 7E
addd  -$2,u                                  E3 5E
addd  -$2,x                                  E3 1E
addd  -$2,y                                  E3 3E
addd  -$3,s                                  E3 7D
addd  -$3,u                                  E3 5D
addd  -$3,x                                  E3 1D
addd  -$3,y                                  E3 3D
addd  -$4,s                                  E3 7C
addd  -$4,u                                  E3 5C
addd  -$4,x                                  E3 1C
addd  -$4,y                                  E3 3C
addd  -$5,s                                  E3 7B
addd  -$5,u                                  E3 5B
addd  -$5,x                                  E3 1B
addd  -$5,y                                  E3 3B
addd  -$6,s                                  E3 7A
addd  -$6,u                                  E3 5A
addd  -$6,x                                  E3 1A
addd  -$6,y                                  E3 3A
addd  -$7,s                                  E3 79
addd  -$7,u                                  E3 59
addd  -$7,x                                  E3 19
addd  -$7,y                                  E3 39
addd  -$8,s                                  E3 78
addd  -$8,u                                  E3 58
addd  -$8,x                                  E3 18
addd  -$8,y                                  E3 38
addd  -$9,s                                  E3 77
addd  -$9,u                                  E3 57
addd  -$9,x                                  E3 17
addd  -$9,y                                  E3 37
addd  -$a,s                                  E3 76
addd  -$a,u                                  E3 56
addd  -$a,x                                  E3 16
addd  -$a,y                                  E3 36
addd  -$b,s                                  E3 75
addd  -$b,u                                  E3 55
addd  -$b,x                                  E3 15
addd  -$b,y                                  E3 35
addd  -$c,s                                  E3 74
addd  -$c,u                                  E3 54
addd  -$c,x                                  E3 14
addd  -$c,y                                  E3 34
addd  -$d,s                                  E3 73
addd  -$d,u                                  E3 53
addd  -$d,x                                  E3 13
addd  -$d,y                                  E3 33
addd  -$e,s                                  E3 72
addd  -$e,u                                  E3 52
addd  -$e,x                                  E3 12
addd  -$e,y                                  E3 32
addd  -$f,s                                  E3 71
addd  -$f,u                                  E3 51
addd  -$f,x                                  E3 11
addd  -$f,y                                  E3 31
addd  a,s                                    E3 E6
addd  a,u                                    E3 C6
addd  a,x                                    E3 86
addd  a,y                                    E3 A6
addd  b,s                                    E3 E5
addd  b,u                                    E3 C5
addd  b,x                                    E3 85
addd  b,y                                    E3 A5
addd  d,s                                    E3 EB
addd  d,u                                    E3 CB
addd  d,x                                    E3 8B
addd  d,y                                    E3 AB
addd  [$01,pc]                               E3 9C 01
addd  [$01,pc]                               E3 BC 01
addd  [$01,pc]                               E3 DC 01
addd  [$01,pc]                               E3 FC 01
addd  [$01,s]                                E3 F8 01
addd  [$01,u]                                E3 D8 01
addd  [$01,x]                                E3 98 01
addd  [$01,y]                                E3 B8 01
addd  [$beef,pc]                             E3 9D BE EF
addd  [$beef,pc]                             E3 BD BE EF
addd  [$beef,pc]                             E3 DD BE EF
addd  [$beef,pc]                             E3 FD BE EF
addd  [$beef,s]                              E3 F9 BE EF
addd  [$beef,u]                              E3 D9 BE EF
addd  [$beef,x]                              E3 99 BE EF
addd  [$beef,y]                              E3 B9 BE EF
addd  [$beef]                                E3 9F BE EF
addd  [$beef]                                E3 BF BE EF
addd  [$beef]                                E3 DF BE EF
addd  [$beef]                                E3 FF BE EF
addd  [,--s]                                 E3 F3
addd  [,--u]                                 E3 D3
addd  [,--x]                                 E3 93
addd  [,--y]                                 E3 B3
addd  [,s++]                                 E3 F1
addd  [,s]                                   E3 F4
addd  [,u++]                                 E3 D1
addd  [,u]                                   E3 D4
addd  [,x++]                                 E3 91
addd  [,x]                                   E3 94
addd  [,y++]                                 E3 B1
addd  [,y]                                   E3 B4
addd  [a,s]                                  E3 F6
addd  [a,u]                                  E3 D6
addd  [a,x]                                  E3 96
addd  [a,y]                                  E3 B6
addd  [b,s]                                  E3 F5
addd  [b,u]                                  E3 D5
addd  [b,x]                                  E3 95
addd  [b,y]                                  E3 B5
addd  [d,s]                                  E3 FB
addd  [d,u]                                  E3 DB
addd  [d,x]                                  E3 9B
addd  [d,y]                                  E3 BB
addd  []                                     E3 97
addd  []                                     E3 9A
addd  []                                     E3 9E
addd  []                                     E3 B7
addd  []                                     E3 BA
addd  []                                     E3 BE
addd  []                                     E3 D7
addd  []                                     E3 DA
addd  []                                     E3 DE
addd  []                                     E3 F7
addd  []                                     E3 FA
addd  []                                     E3 FE
anda  #$ff                                   84 FF
anda  $0,s                                   A4 60
anda  $0,u                                   A4 40
anda  $0,x                                   A4 00
anda  $0,y                                   A4 20
anda  $01,pc                                 A4 8C 01
anda  $01,pc                                 A4 AC 01
anda  $01,pc                                 A4 CC 01
anda  $01,pc                                 A4 EC 01
anda  $01,s                                  A4 E8 01
anda  $01,u                                  A4 C8 01
anda  $01,x                                  A4 88 01
anda  $01,y                                  A4 A8 01
anda  $1,s                                   A4 61
anda  $1,u                                   A4 41
anda  $1,x                                   A4 01
anda  $1,y                                   A4 21
anda  $2,s                                   A4 62
anda  $2,u                                   A4 42
anda  $2,x                                   A4 02
anda  $2,y                                   A4 22
anda  $3,s                                   A4 63
anda  $3,u                                   A4 43
anda  $3,x                                   A4 03
anda  $3,y                                   A4 23
anda  $4,s                                   A4 64
anda  $4,u                                   A4 44
anda  $4,x                                   A4 04
anda  $4,y                                   A4 24
anda  $5,s                                   A4 65
anda  $5,u                                   A4 45
anda  $5,x                                   A4 05
anda  $5,y                                   A4 25
anda  $6,s                                   A4 66
anda  $6,u                                   A4 46
anda  $6,x                                   A4 06
anda  $6,y                                   A4 26
anda  $7,s                                   A4 67
anda  $7,u                                   A4 47
anda  $7,x                                   A4 07
anda  $7,y                                   A4 27
anda  $8,s                                   A4 68
anda  $8,u                                   A4 48
anda  $8,x                                   A4 08
anda  $8,y                                   A4 28
anda  $9,s                                   A4 69
anda  $9,u                                   A4 49
anda  $9,x                                   A4 09
anda  $9,y                                   A4 29
anda  $a,s                                   A4 6A
anda  $a,u                                   A4 4A
anda  $a,x                                   A4 0A
anda  $a,y                                   A4 2A
anda  $b,s                                   A4 6B
anda  $b,u                                   A4 4B
anda  $b,x                                   A4 0B
anda  $b,y                                   A4 2B
anda  $beef                                  A4 8F BE EF
anda  $beef                                  A4 AF BE EF
anda  $beef                                  A4 CF BE EF
anda  $beef                                  A4 EF BE EF
anda  $beef                                  B4 BE EF
anda  $beef,pc                               A4 8D BE EF
anda  $beef,pc                               A4 AD BE EF
anda  $beef,pc                               A4 CD BE EF
anda  $beef,pc                               A4 ED BE EF
anda  $beef,s                                A4 E9 BE EF
anda  $beef,u                                A4 C9 BE EF
anda  $beef,x                                A4 89 BE EF
anda  $beef,y                                A4 A9 BE EF
anda  $c,s                                   A4 6C
anda  $c,u                                   A4 4C
anda  $c,x                                   A4 0C
anda  $c,y                                   A4 2C
anda  $d,s                                   A4 6D
anda  $d,u                                   A4 4D
anda  $d,x                                   A4 0D
anda  $d,y                                   A4 2D
anda  $e,s                                   A4 6E
anda  $e,u                                   A4 4E
anda  $e,x                                   A4 0E
anda  $e,y                                   A4 2E
anda  $f,s                                   A4 6F
anda  $f,u                                   A4 4F
anda  $f,x                                   A4 0F
anda  $f,y                                   A4 2F
anda  $ff                                    94 FF
anda  ,--s                                   A4 E3
anda  ,--u                                   A4 C3
anda  ,--x                                   A4 83
anda  ,--y                                   A4 A3
anda  ,-s                                    A4 E2
anda  ,-u                                    A4 C2
anda  ,-x                                    A4 82
anda  ,-y                                    A4 A2
anda  ,s                                     A4 E4
anda  ,s+                                    A4 E0
anda  ,s++                                   A4 E1
anda  ,u                                     A4 C4
anda  ,u+                                    A4 C0
anda  ,u++                                   A4 C1
anda  ,x                                     A4 84
anda  ,x+                                    A4 80
anda  ,x++                                   A4 81
anda  ,y                                     A4 A4
anda  ,y+                                    A4 A0
anda  ,y++                                   A4 A1
anda  -$1,s                                  A4 7F
anda  -$1,u                                  A4 5F
anda  -$1,x                                  A4 1F
anda  -$1,y                                  A4 3F
anda  -$10,s                                 A4 70
anda  -$10,u                                 A4 50
anda  -$10,x                                 A4 10
anda  -$10,y                                 A4 30
anda  -$2,s                                  A4 7E
anda  -$2,u                                  A4 5E
anda  -$2,x                                  A4 1E
anda  -$2,y                                  A4 3E
anda  -$3,s                                  A4 7D
anda  -$3,u                                  A4 5D
anda  -$3,x                                  A4 1D
anda  -$3,y                                  A4 3D
anda  -$4,s                                  A4 7C
anda  -$4,u                                  A4 5C
anda  -$4,x                                  A4 1C
anda  -$4,y                                  A4 3C
anda  -$5,s                                  A4 7B
anda  -$5,u                                  A4 5B
anda  -$5,x                                  A4 1B
anda  -$5,y                                  A4 3B
anda  -$6,s                                  A4 7A
anda  -$6,u                                  A4 5A
anda  -$6,x                                  A4 1A
anda  -$6,y                                  A4 3A
anda  -$7,s                                  A4 79
anda  -$7,u                                  A4 59
anda  -$7,x                                  A4 19
anda  -$7,y                                  A4 39
anda  -$8,s                                  A4 78
anda  -$8,u                                  A4 58
anda  -$8,x                                  A4 18
anda  -$8,y                                  A4 38
anda  -$9,s                                  A4 77
anda  -$9,u                                  A4 57
anda  -$9,x                                  A4 17
anda  -$9,y                                  A4 37
anda  -$a,s                                  A4 76
anda  -$a,u                                  A4 56
anda  -$a,x                                  A4 16
anda  -$a,y                                  A4 36
anda  -$b,s                                  A4 75
anda  -$b,u                                  A4 55
anda  -$b,x                                  A4 15
anda  -$b,y                                  A4 35
anda  -$c,s                                  A4 74
anda  -$c,u                                  A4 54
anda  -$c,x                                  A4 14
anda  -$c,y                                  A4 34
anda  -$d,s                                  A4 73
anda  -$d,u                                  A4 53
anda  -$d,x                                  A4 13
anda  -$d,y                                  A4 33
anda  -$e,s                                  A4 72
anda  -$e,u                                  A4 52
anda  -$e,x                                  A4 12
anda  -$e,y                                  A4 32
anda  -$f,s                                  A4 71
anda  -$f,u                                  A4 51
anda  -$f,x                                  A4 11
anda  -$f,y                                  A4 31
anda  a,s                                    A4 E6
anda  a,u                                    A4 C6
anda  a,x                                    A4 86
anda  a,y                                    A4 A6
anda  b,s                                    A4 E5
anda  b,u                                    A4 C5
anda  b,x                                    A4 85
anda  b,y                                    A4 A5
anda  d,s                                    A4 EB
anda  d,u                                    A4 CB
anda  d,x                                    A4 8B
anda  d,y                                    A4 AB
anda  [$01,pc]                               A4 9C 01
anda  [$01,pc]                               A4 BC 01
anda  [$01,pc]                               A4 DC 01
anda  [$01,pc]                               A4 FC 01
anda  [$01,s]                                A4 F8 01
anda  [$01,u]                                A4 D8 01
anda  [$01,x]                                A4 98 01
anda  [$01,y]                                A4 B8 01
anda  [$beef,pc]                             A4 9D BE EF
anda  [$beef,pc]                             A4 BD BE EF
anda  [$beef,pc]                             A4 DD BE EF
anda  [$beef,pc]                             A4 FD BE EF
anda  [$beef,s]                              A4 F9 BE EF
anda  [$beef,u]                              A4 D9 BE EF
anda  [$beef,x]                              A4 99 BE EF
anda  [$beef,y]                              A4 B9 BE EF
anda  [$beef]                                A4 9F BE EF
anda  [$beef]                                A4 BF BE EF
anda  [$beef]                                A4 DF BE EF
anda  [$beef]                                A4 FF BE EF
anda  [,--s]                                 A4 F3
anda  [,--u]                                 A4 D3
anda  [,--x]                                 A4 93
anda  [,--y]                                 A4 B3
anda  [,s++]                                 A4 F1
anda  [,s]                                   A4 F4
anda  [,u++]                                 A4 D1
anda  [,u]                                   A4 D4
anda  [,x++]                                 A4 91
anda  [,x]                                   A4 94
anda  [,y++]                                 A4 B1
anda  [,y]                                   A4 B4
anda  [a,s]                                  A4 F6
anda  [a,u]                                  A4 D6
anda  [a,x]                                  A4 96
anda  [a,y]                                  A4 B6
anda  [b,s]                                  A4 F5
anda  [b,u]                                  A4 D5
anda  [b,x]                                  A4 95
anda  [b,y]                                  A4 B5
anda  [d,s]                                  A4 FB
anda  [d,u]                                  A4 DB
anda  [d,x]                                  A4 9B
anda  [d,y]                                  A4 BB
anda  []                                     A4 97
anda  []                                     A4 9A
anda  []                                     A4 9E
anda  []                                     A4 B7
anda  []                                     A4 BA
anda  []                                     A4 BE
anda  []                                     A4 D7
anda  []                                     A4 DA
anda  []                                     A4 DE
anda  []                                     A4 F7
anda  []                                     A4 FA
anda  []                                     A4 FE
andb  #$ff                                   C4 FF
andb  $0,s                                   E4 60
andb  $0,u                                   E4 40
andb  $0,x                                   E4 00
andb  $0,y                                   E4 20
andb  $01,pc                                 E4 8C 01
andb  $01,pc                                 E4 AC 01
andb  $01,pc                                 E4 CC 01
andb  $01,pc                                 E4 EC 01
andb  $01,s                                  E4 E8 01
andb  $01,u                                  E4 C8 01
andb  $01,x                                  E4 88 01
andb  $01,y                                  E4 A8 01
andb  $1,s                                   E4 61
andb  $1,u                                   E4 41
andb  $1,x                                   E4 01
andb  $1,y                                   E4 21
andb  $2,s                                   E4 62
andb  $2,u                                   E4 42
andb  $2,x                                   E4 02
andb  $2,y                                   E4 22
andb  $3,s                                   E4 63
andb  $3,u                                   E4 43
andb  $3,x                                   E4 03
andb  $3,y                                   E4 23
andb  $4,s                                   E4 64
andb  $4,u                                   E4 44
andb  $4,x                                   E4 04
andb  $4,y                                   E4 24
andb  $5,s                                   E4 65
andb  $5,u                                   E4 45
andb  $5,x                                   E4 05
andb  $5,y                                   E4 25
andb  $6,s                                   E4 66
andb  $6,u                                   E4 46
andb  $6,x                                   E4 06
andb  $6,y                                   E4 26
andb  $7,s                                   E4 67
andb  $7,u                                   E4 47
andb  $7,x                                   E4 07
andb  $7,y                                   E4 27
andb  $8,s                                   E4 68
andb  $8,u                                   E4 48
andb  $8,x                                   E4 08
andb  $8,y                                   E4 28
andb  $9,s                                   E4 69
andb  $9,u                                   E4 49
andb  $9,x                                   E4 09
andb  $9,y                                   E4 29
andb  $a,s                                   E4 6A
andb  $a,u                                   E4 4A
andb  $a,x                                   E4 0A
andb  $a,y                                   E4 2A
andb  $b,s                                   E4 6B
andb  $b,u                                   E4 4B
andb  $b,x                                   E4 0B
andb  $b,y                                   E4 2B
andb  $beef                                  E4 8F BE EF
andb  $beef                                  E4 AF BE EF
andb  $beef                                  E4 CF BE EF
andb  $beef                                  E4 EF BE EF
andb  $beef                                  F4 BE EF
andb  $beef,pc                               E4 8D BE EF
andb  $beef,pc                               E4 AD BE EF
andb  $beef,pc                               E4 CD BE EF
andb  $beef,pc                               E4 ED BE EF
andb  $beef,s                                E4 E9 BE EF
andb  $beef,u                                E4 C9 BE EF
andb  $beef,x                                E4 89 BE EF
andb  $beef,y                                E4 A9 BE EF
andb  $c,s                                   E4 6C
andb  $c,u                                   E4 4C
andb  $c,x                                   E4 0C
andb  $c,y                                   E4 2C
andb  $d,s                                   E4 6D
andb  $d,u                                   E4 4D
andb  $d,x                                   E4 0D
andb  $d,y                                   E4 2D
andb  $e,s                                   E4 6E
andb  $e,u                                   E4 4E
andb  $e,x                                   E4 0E
andb  $e,y                                   E4 2E
andb  $f,s                                   E4 6F
andb  $f,u                                   E4 4F
andb  $f,x                                   E4 0F
andb  $f,y                                   E4 2F
andb  $ff                                    D4 FF
andb  ,--s                                   E4 E3
andb  ,--u                                   E4 C3
andb  ,--x                                   E4 83
andb  ,--y                                   E4 A3
andb  ,-s                                    E4 E2
andb  ,-u                                    E4 C2
andb  ,-x                                    E4 82
andb  ,-y                                    E4 A2
andb  ,s                                     E4 E4
andb  ,s+                                    E4 E0
andb  ,s++                                   E4 E1
andb  ,u                                     E4 C4
andb  ,u+                                    E4 C0
andb  ,u++                                   E4 C1
andb  ,x                                     E4 84
andb  ,x+                                    E4 80
andb  ,x++                                   E4 81
andb  ,y                                     E4 A4
andb  ,y+                                    E4 A0
andb  ,y++                                   E4 A1
andb  -$1,s                                  E4 7F
andb  -$1,u                                  E4 5F
andb  -$1,x                                  E4 1F
andb  -$1,y                                  E4 3F
andb  -$10,s                                 E4 70
andb  -$10,u                                 E4 50
andb  -$10,x                                 E4 10
andb  -$10,y                                 E4 30
andb  -$2,s                                  E4 7E
andb  -$2,u                                  E4 5E
andb  -$2,x                                  E4 1E
andb  -$2,y                                  E4 3E
andb  -$3,s                                  E4 7D
andb  -$3,u                                  E4 5D
andb  -$3,x                                  E4 1D
andb  -$3,y                                  E4 3D
andb  -$4,s                                  E4 7C
andb  -$4,u                                  E4 5C
andb  -$4,x                                  E4 1C
andb  -$4,y                                  E4 3C
andb  -$5,s                                  E4 7B
andb  -$5,u                                  E4 5B
andb  -$5,x                                  E4 1B
andb  -$5,y                                  E4 3B
andb  -$6,s                                  E4 7A
andb  -$6,u                                  E4 5A
andb  -$6,x                                  E4 1A
andb  -$6,y                                  E4 3A
andb  -$7,s                                  E4 79
andb  -$7,u                                  E4 59
andb  -$7,x                                  E4 19
andb  -$7,y                                  E4 39
andb  -$8,s                                  E4 78
andb  -$8,u                                  E4 58
andb  -$8,x                                  E4 18
andb  -$8,y                                  E4 38
andb  -$9,s                                  E4 77
andb  -$9,u                                  E4 57
andb  -$9,x                                  E4 17
andb  -$9,y                                  E4 37
andb  -$a,s                                  E4 76
andb  -$a,u                                  E4 56
andb  -$a,x                                  E4 16
andb  -$a,y                                  E4 36
andb  -$b,s                                  E4 75
andb  -$b,u                                  E4 55
andb  -$b,x                                  E4 15
andb  -$b,y                                  E4 35
andb  -$c,s                                  E4 74
andb  -$c,u                                  E4 54
andb  -$c,x                                  E4 14
andb  -$c,y                                  E4 34
andb  -$d,s                                  E4 73
andb  -$d,u                                  E4 53
andb  -$d,x                                  E4 13
andb  -$d,y                                  E4 33
andb  -$e,s                                  E4 72
andb  -$e,u                                  E4 52
andb  -$e,x                                  E4 12
andb  -$e,y                                  E4 32
andb  -$f,s                                  E4 71
andb  -$f,u                                  E4 51
andb  -$f,x                                  E4 11
andb  -$f,y                                  E4 31
andb  a,s                                    E4 E6
andb  a,u                                    E4 C6
andb  a,x                                    E4 86
andb  a,y                                    E4 A6
andb  b,s                                    E4 E5
andb  b,u                                    E4 C5
andb  b,x                                    E4 85
andb  b,y                                    E4 A5
andb  d,s                                    E4 EB
andb  d,u                                    E4 CB
andb  d,x                                    E4 8B
andb  d,y                                    E4 AB
andb  [$01,pc]                               E4 9C 01
andb  [$01,pc]                               E4 BC 01
andb  [$01,pc]                               E4 DC 01
andb  [$01,pc]                               E4 FC 01
andb  [$01,s]                                E4 F8 01
andb  [$01,u]                                E4 D8 01
andb  [$01,x]                                E4 98 01
andb  [$01,y]                                E4 B8 01
andb  [$beef,pc]                             E4 9D BE EF
andb  [$beef,pc]                             E4 BD BE EF
andb  [$beef,pc]                             E4 DD BE EF
andb  [$beef,pc]                             E4 FD BE EF
andb  [$beef,s]                              E4 F9 BE EF
andb  [$beef,u]                              E4 D9 BE EF
andb  [$beef,x]                              E4 99 BE EF
andb  [$beef,y]                              E4 B9 BE EF
andb  [$beef]                                E4 9F BE EF
andb  [$beef]                                E4 BF BE EF
andb  [$beef]                                E4 DF BE EF
andb  [$beef]                                E4 FF BE EF
andb  [,--s]                                 E4 F3
andb  [,--u]                                 E4 D3
andb  [,--x]                                 E4 93
andb  [,--y]                                 E4 B3
andb  [,s++]                                 E4 F1
andb  [,s]                                   E4 F4
andb  [,u++]                                 E4 D1
andb  [,u]                                   E4 D4
andb  [,x++]                                 E4 91
andb  [,x]                                   E4 94
andb  [,y++]                                 E4 B1
andb  [,y]                                   E4 B4
andb  [a,s]                                  E4 F6
andb  [a,u]                                  E4 D6
andb  [a,x]                                  E4 96
andb  [a,y]                                  E4 B6
andb  [b,s]                                  E4 F5
andb  [b,u]                                  E4 D5
andb  [b,x]                                  E4 95
andb  [b,y]                                  E4 B5
andb  [d,s]                                  E4 FB
andb  [d,u]                                  E4 DB
andb  [d,x]                                  E4 9B
andb  [d,y]                                  E4 BB
andb  []                                     E4 97
andb  []                                     E4 9A
andb  []                                     E4 9E
andb  []                                     E4 B7
andb  []                                     E4 BA
andb  []                                     E4 BE
andb  []                                     E4 D7
andb  []                                     E4 DA
andb  []                                     E4 DE
andb  []                                     E4 F7
andb  []                                     E4 FA
andb  []                                     E4 FE
andcc #$ff                                   1C FF
asl   $0,s                                   68 60
asl   $0,u                                   68 40
asl   $0,x                                   68 00
asl   $0,y                                   68 20
asl   $01,pc                                 68 8C 01
asl   $01,pc                                 68 AC 01
asl   $01,pc                                 68 CC 01
asl   $01,pc                                 68 EC 01
asl   $01,s                                  68 E8 01
asl   $01,u                                  68 C8 01
asl   $01,x                                  68 88 01
asl   $01,y                                  68 A8 01
asl   $1,s                                   68 61
asl   $1,u                                   68 41
asl   $1,x                                   68 01
asl   $1,y                                   68 21
asl   $2,s                                   68 62
asl   $2,u                                   68 42
asl   $2,x                                   68 02
asl   $2,y                                   68 22
asl   $3,s                                   68 63
asl   $3,u                                   68 43
asl   $3,x                                   68 03
asl   $3,y                                   68 23
asl   $4,s                                   68 64
asl   $4,u                                   68 44
asl   $4,x                                   68 04
asl   $4,y                                   68 24
asl   $5,s                                   68 65
asl   $5,u                                   68 45
asl   $5,x                                   68 05
asl   $5,y                                   68 25
asl   $6,s                                   68 66
asl   $6,u                                   68 46
asl   $6,x                                   68 06
asl   $6,y                                   68 26
asl   $7,s                                   68 67
asl   $7,u                                   68 47
asl   $7,x                                   68 07
asl   $7,y                                   68 27
asl   $8,s                                   68 68
asl   $8,u                                   68 48
asl   $8,x                                   68 08
asl   $8,y                                   68 28
asl   $9,s                                   68 69
asl   $9,u                                   68 49
asl   $9,x                                   68 09
asl   $9,y                                   68 29
asl   $a,s                                   68 6A
asl   $a,u                                   68 4A
asl   $a,x                                   68 0A
asl   $a,y                                   68 2A
asl   $b,s                                   68 6B
asl   $b,u                                   68 4B
asl   $b,x                                   68 0B
asl   $b,y                                   68 2B
asl   $beef                                  68 8F BE EF
asl   $beef                                  68 AF BE EF
asl   $beef                                  68 CF BE EF
asl   $beef                                  68 EF BE EF
asl   $beef                                  78 BE EF
asl   $beef,pc                               68 8D BE EF
asl   $beef,pc                               68 AD BE EF
asl   $beef,pc                               68 CD BE EF
asl   $beef,pc                               68 ED BE EF
asl   $beef,s                                68 E9 BE EF
asl   $beef,u                                68 C9 BE EF
asl   $beef,x                                68 89 BE EF
asl   $beef,y                                68 A9 BE EF
asl   $c,s                                   68 6C
asl   $c,u                                   68 4C
asl   $c,x                                   68 0C
asl   $c,y                                   68 2C
asl   $d,s                                   68 6D
asl   $d,u                                   68 4D
asl   $d,x                                   68 0D
asl   $d,y                                   68 2D
asl   $e,s                                   68 6E
asl   $e,u                                   68 4E
asl   $e,x                                   68 0E
asl   $e,y                                   68 2E
asl   $f,s                                   68 6F
asl   $f,u                                   68 4F
asl   $f,x                                   68 0F
asl   $f,y                                   68 2F
asl   $ff                                    08 FF
asl   ,--s                                   68 E3
asl   ,--u                                   68 C3
asl   ,--x                                   68 83
asl   ,--y                                   68 A3
asl   ,-s                                    68 E2
asl   ,-u                                    68 C2
asl   ,-x                                    68 82
asl   ,-y                                    68 A2
asl   ,s                                     68 E4
asl   ,s+                                    68 E0
asl   ,s++                                   68 E1
asl   ,u                                     68 C4
asl   ,u+                                    68 C0
asl   ,u++                                   68 C1
asl   ,x                                     68 84
asl   ,x+                                    68 80
asl   ,x++                                   68 81
asl   ,y                                     68 A4
asl   ,y+                                    68 A0
asl   ,y++                                   68 A1
asl   -$1,s                                  68 7F
asl   -$1,u                                  68 5F
asl   -$1,x                                  68 1F
asl   -$1,y                                  68 3F
asl   -$10,s                                 68 70
asl   -$10,u                                 68 50
asl   -$10,x                                 68 10
asl   -$10,y                                 68 30
asl   -$2,s                                  68 7E
asl   -$2,u                                  68 5E
asl   -$2,x                                  68 1E
asl   -$2,y                                  68 3E
asl   -$3,s                                  68 7D
asl   -$3,u                                  68 5D
asl   -$3,x                                  68 1D
asl   -$3,y                                  68 3D
asl   -$4,s                                  68 7C
asl   -$4,u                                  68 5C
asl   -$4,x                                  68 1C
asl   -$4,y                                  68 3C
asl   -$5,s                                  68 7B
asl   -$5,u                                  68 5B
asl   -$5,x                                  68 1B
asl   -$5,y                                  68 3B
asl   -$6,s                                  68 7A
asl   -$6,u                                  68 5A
asl   -$6,x                                  68 1A
asl   -$6,y                                  68 3A
asl   -$7,s                                  68 79
asl   -$7,u                                  68 59
asl   -$7,x                                  68 19
asl   -$7,y                                  68 39
asl   -$8,s                                  68 78
asl   -$8,u                                  68 58
asl   -$8,x                                  68 18
asl   -$8,y                                  68 38
asl   -$9,s                                  68 77
asl   -$9,u                                  68 57
asl   -$9,x                                  68 17
asl   -$9,y                                  68 37
asl   -$a,s                                  68 76
asl   -$a,u                                  68 56
asl   -$a,x                                  68 16
asl   -$a,y                                  68 36
asl   -$b,s                                  68 75
asl   -$b,u                                  68 55
asl   -$b,x                                  68 15
asl   -$b,y                                  68 35
asl   -$c,s                                  68 74
asl   -$c,u                                  68 54
asl   -$c,x                                  68 14
asl   -$c,y                                  68 34
asl   -$d,s                                  68 73
asl   -$d,u                                  68 53
asl   -$d,x                                  68 13
asl   -$d,y                                  68 33
asl   -$e,s                                  68 72
asl   -$e,u                                  68 52
asl   -$e,x                                  68 12
asl   -$e,y                                  68 32
asl   -$f,s                                  68 71
asl   -$f,u                                  68 51
asl   -$f,x                                  68 11
asl   -$f,y                                  68 31
asl   a,s                                    68 E6
asl   a,u                                    68 C6
asl   a,x                                    68 86
asl   a,y                                    68 A6
asl   b,s                                    68 E5
asl   b,u                                    68 C5
asl   b,x                                    68 85
asl   b,y                                    68 A5
asl   d,s                                    68 EB
asl   d,u                                    68 CB
asl   d,x                                    68 8B
asl   d,y                                    68 AB
asl   [$01,pc]                               68 9C 01
asl   [$01,pc]                               68 BC 01
asl   [$01,pc]                               68 DC 01
asl   [$01,pc]                               68 FC 01
asl   [$01,s]                                68 F8 01
asl   [$01,u]                                68 D8 01
asl   [$01,x]                                68 98 01
asl   [$01,y]                                68 B8 01
asl   [$beef,pc]                             68 9D BE EF
asl   [$beef,pc]                             68 BD BE EF
asl   [$beef,pc]                             68 DD BE EF
asl   [$beef,pc]                             68 FD BE EF
asl   [$beef,s]                              68 F9 BE EF
asl   [$beef,u]                              68 D9 BE EF
asl   [$beef,x]                              68 99 BE EF
asl   [$beef,y]                              68 B9 BE EF
asl   [$beef]                                68 9F BE EF
asl   [$beef]                                68 BF BE EF
asl   [$beef]                                68 DF BE EF
asl   [$beef]                                68 FF BE EF
asl   [,--s]                                 68 F3
asl   [,--u]                                 68 D3
asl   [,--x]                                 68 93
asl   [,--y]                                 68 B3
asl   [,s++]                                 68 F1
asl   [,s]                                   68 F4
asl   [,u++]                                 68 D1
asl   [,u]                                   68 D4
asl   [,x++]                                 68 91
asl   [,x]                                   68 94
asl   [,y++]                                 68 B1
asl   [,y]                                   68 B4
asl   [a,s]                                  68 F6
asl   [a,u]                                  68 D6
asl   [a,x]                                  68 96
asl   [a,y]                                  68 B6
asl   [b,s]                                  68 F5
asl   [b,u]                                  68 D5
asl   [b,x]                                  68 95
asl   [b,y]                                  68 B5
asl   [d,s]                                  68 FB
asl   [d,u]                                  68 DB
asl   [d,x]                                  68 9B
asl   [d,y]                                  68 BB
asl   []                                     68 97
asl   []                                     68 9A
asl   []                                     68 9E
asl   []                                     68 B7
asl   []                                     68 BA
asl   []                                     68 BE
asl   []                                     68 D7
asl   []                                     68 DA
asl   []                                     68 DE
asl   []                                     68 F7
asl   []                                     68 FA
asl   []                                     68 FE
asla                                         48
aslb                                         58
asr   $0,s                                   67 60
asr   $0,u                                   67 40
asr   $0,x                                   67 00
asr   $0,y                                   67 20
asr   $01,pc                                 67 8C 01
asr   $01,pc                                 67 AC 01
asr   $01,pc                                 67 CC 01
asr   $01,pc                                 67 EC 01
asr   $01,s                                  67 E8 01
asr   $01,u                                  67 C8 01
asr   $01,x                                  67 88 01
asr   $01,y                                  67 A8 01
asr   $1,s                                   67 61
asr   $1,u                                   67 41
asr   $1,x                                   67 01
asr   $1,y                                   67 21
asr   $2,s                                   67 62
asr   $2,u                                   67 42
asr   $2,x                                   67 02
asr   $2,y                                   67 22
asr   $3,s                                   67 63
asr   $3,u                                   67 43
asr   $3,x                                   67 03
asr   $3,y                                   67 23
asr   $4,s                                   67 64
asr   $4,u                                   67 44
asr   $4,x                                   67 04
asr   $4,y                                   67 24
asr   $5,s                                   67 65
asr   $5,u                                   67 45
asr   $5,x                                   67 05
asr   $5,y                                   67 25
asr   $6,s                                   67 66
asr   $6,u                                   67 46
asr   $6,x                                   67 06
asr   $6,y                                   67 26
asr   $7,s                                   67 67
asr   $7,u                                   67 47
asr   $7,x                                   67 07
asr   $7,y                                   67 27
asr   $8,s                                   67 68
asr   $8,u                                   67 48
asr   $8,x                                   67 08
asr   $8,y                                   67 28
asr   $9,s                                   67 69
asr   $9,u                                   67 49
asr   $9,x                                   67 09
asr   $9,y                                   67 29
asr   $a,s                                   67 6A
asr   $a,u                                   67 4A
asr   $a,x                                   67 0A
asr   $a,y                                   67 2A
asr   $b,s                                   67 6B
asr   $b,u                                   67 4B
asr   $b,x                                   67 0B
asr   $b,y                                   67 2B
asr   $beef                                  67 8F BE EF
asr   $beef                                  67 AF BE EF
asr   $beef                                  67 CF BE EF
asr   $beef                                  67 EF BE EF
asr   $beef                                  77 BE EF
asr   $beef,pc                               67 8D BE EF
asr   $beef,pc                               67 AD BE EF
asr   $beef,pc                               67 CD BE EF
asr   $beef,pc                               67 ED BE EF
asr   $beef,s                                67 E9 BE EF
asr   $beef,u                                67 C9 BE EF
asr   $beef,x                                67 89 BE EF
asr   $beef,y                                67 A9 BE EF
asr   $c,s                                   67 6C
asr   $c,u                                   67 4C
asr   $c,x                                   67 0C
asr   $c,y                                   67 2C
asr   $d,s                                   67 6D
asr   $d,u                                   67 4D
asr   $d,x                                   67 0D
asr   $d,y                                   67 2D
asr   $e,s                                   67 6E
asr   $e,u                                   67 4E
asr   $e,x                                   67 0E
asr   $e,y                                   67 2E
asr   $f,s                                   67 6F
asr   $f,u                                   67 4F
asr   $f,x                                   67 0F
asr   $f,y                                   67 2F
asr   $ff                                    07 FF
asr   ,--s                                   67 E3
asr   ,--u                                   67 C3
asr   ,--x                                   67 83
asr   ,--y                                   67 A3
asr   ,-s                                    67 E2
asr   ,-u                                    67 C2
asr   ,-x                                    67 82
asr   ,-y                                    67 A2
asr   ,s                                     67 E4
asr   ,s+                                    67 E0
asr   ,s++                                   67 E1
asr   ,u                                     67 C4
asr   ,u+                                    67 C0
asr   ,u++                                   67 C1
asr   ,x                                     67 84
asr   ,x+                                    67 80
asr   ,x++                                   67 81
asr   ,y                                     67 A4
asr   ,y+                                    67 A0
asr   ,y++                                   67 A1
asr   -$1,s                                  67 7F
asr   -$1,u                                  67 5F
asr   -$1,x                                  67 1F
asr   -$1,y                                  67 3F
asr   -$10,s                                 67 70
asr   -$10,u                                 67 50
asr   -$10,x                                 67 10
asr   -$10,y                                 67 30
asr   -$2,s                                  67 7E
asr   -$2,u                                  67 5E
asr   -$2,x                                  67 1E
asr   -$2,y                                  67 3E
asr   -$3,s                                  67 7D
asr   -$3,u                                  67 5D
asr   -$3,x                                  67 1D
asr   -$3,y                                  67 3D
asr   -$4,s                                  67 7C
asr   -$4,u                                  67 5C
asr   -$4,x                                  67 1C
asr   -$4,y                                  67 3C
asr   -$5,s                                  67 7B
asr   -$5,u                                  67 5B
asr   -$5,x                                  67 1B
asr   -$5,y                                  67 3B
asr   -$6,s                                  67 7A
asr   -$6,u                                  67 5A
asr   -$6,x                                  67 1A
asr   -$6,y                                  67 3A
asr   -$7,s                                  67 79
asr   -$7,u                                  67 59
asr   -$7,x                                  67 19
asr   -$7,y                                  67 39
asr   -$8,s                                  67 78
asr   -$8,u                                  67 58
asr   -$8,x                                  67 18
asr   -$8,y                                  67 38
asr   -$9,s                                  67 77
asr   -$9,u                                  67 57
asr   -$9,x                                  67 17
asr   -$9,y                                  67 37
asr   -$a,s                                  67 76
asr   -$a,u                                  67 56
asr   -$a,x                                  67 16
asr   -$a,y                                  67 36
asr   -$b,s                                  67 75
asr   -$b,u                                  67 55
asr   -$b,x                                  67 15
asr   -$b,y                                  67 35
asr   -$c,s                                  67 74
asr   -$c,u                                  67 54
asr   -$c,x                                  67 14
asr   -$c,y                                  67 34
asr   -$d,s                                  67 73
asr   -$d,u                                  67 53
asr   -$d,x                                  67 13
asr   -$d,y                                  67 33
asr   -$e,s                                  67 72
asr   -$e,u                                  67 52
asr   -$e,x                                  67 12
asr   -$e,y                                  67 32
asr   -$f,s                                  67 71
asr   -$f,u                                  67 51
asr   -$f,x                                  67 11
asr   -$f,y                                  67 31
asr   a,s                                    67 E6
asr   a,u                                    67 C6
asr   a,x                                    67 86
asr   a,y                                    67 A6
asr   b,s                                    67 E5
asr   b,u                                    67 C5
asr   b,x                                    67 85
asr   b,y                                    67 A5
asr   d,s                                    67 EB
asr   d,u                                    67 CB
asr   d,x                                    67 8B
asr   d,y                                    67 AB
asr   [$01,pc]                               67 9C 01
asr   [$01,pc]                               67 BC 01
asr   [$01,pc]                               67 DC 01
asr   [$01,pc]                               67 FC 01
asr   [$01,s]                                67 F8 01
asr   [$01,u]                                67 D8 01
asr   [$01,x]                                67 98 01
asr   [$01,y]                                67 B8 01
asr   [$beef,pc]                             67 9D BE EF
asr   [$beef,pc]                             67 BD BE EF
asr   [$beef,pc]                             67 DD BE EF
asr   [$beef,pc]                             67 FD BE EF
asr   [$beef,s]                              67 F9 BE EF
asr   [$beef,u]                              67 D9 BE EF
asr   [$beef,x]                              67 99 BE EF
asr   [$beef,y]                              67 B9 BE EF
asr   [$beef]                                67 9F BE EF
asr   [$beef]                                67 BF BE EF
asr   [$beef]                                67 DF BE EF
asr   [$beef]                                67 FF BE EF
asr   [,--s]                                 67 F3
asr   [,--u]                                 67 D3
asr   [,--x]                                 67 93
asr   [,--y]                                 67 B3
asr   [,s++]                                 67 F1
asr   [,s]                                   67 F4
asr   [,u++]                                 67 D1
asr   [,u]                                   67 D4
asr   [,x++]                                 67 91
asr   [,x]                                   67 94
asr   [,y++]                                 67 B1
asr   [,y]                                   67 B4
asr   [a,s]                                  67 F6
asr   [a,u]                                  67 D6
asr   [a,x]                                  67 96
asr   [a,y]                                  67 B6
asr   [b,s]                                  67 F5
asr   [b,u]                                  67 D5
asr   [b,x]                                  67 95
asr   [b,y]                                  67 B5
asr   [d,s]                                  67 FB
asr   [d,u]                                  67 DB
asr   [d,x]                                  67 9B
asr   [d,y]                                  67 BB
asr   []                                     67 97
asr   []                                     67 9A
asr   []                                     67 9E
asr   []                                     67 B7
asr   []                                     67 BA
asr   []                                     67 BE
asr   []                                     67 D7
asr   []                                     67 DA
asr   []                                     67 DE
asr   []                                     67 F7
asr   []                                     67 FA
asr   []                                     67 FE
asra                                         47
asrb                                         57
bcc   $+2                                    24 59
bcs   $+2                                    25 0F
beq   $+2                                    27 01
bge   $+2                                    2C 01
bgt   $+2                                    2E 4E
bhi   $+2                                    22 00
bita  #$ff                                   85 FF
bita  $0,s                                   A5 60
bita  $0,u                                   A5 40
bita  $0,x                                   A5 00
bita  $0,y                                   A5 20
bita  $01,pc                                 A5 8C 01
bita  $01,pc                                 A5 AC 01
bita  $01,pc                                 A5 CC 01
bita  $01,pc                                 A5 EC 01
bita  $01,s                                  A5 E8 01
bita  $01,u                                  A5 C8 01
bita  $01,x                                  A5 88 01
bita  $01,y                                  A5 A8 01
bita  $1,s                                   A5 61
bita  $1,u                                   A5 41
bita  $1,x                                   A5 01
bita  $1,y                                   A5 21
bita  $2,s                                   A5 62
bita  $2,u                                   A5 42
bita  $2,x                                   A5 02
bita  $2,y                                   A5 22
bita  $3,s                                   A5 63
bita  $3,u                                   A5 43
bita  $3,x                                   A5 03
bita  $3,y                                   A5 23
bita  $4,s                                   A5 64
bita  $4,u                                   A5 44
bita  $4,x                                   A5 04
bita  $4,y                                   A5 24
bita  $5,s                                   A5 65
bita  $5,u                                   A5 45
bita  $5,x                                   A5 05
bita  $5,y                                   A5 25
bita  $6,s                                   A5 66
bita  $6,u                                   A5 46
bita  $6,x                                   A5 06
bita  $6,y                                   A5 26
bita  $7,s                                   A5 67
bita  $7,u                                   A5 47
bita  $7,x                                   A5 07
bita  $7,y                                   A5 27
bita  $8,s                                   A5 68
bita  $8,u                                   A5 48
bita  $8,x                                   A5 08
bita  $8,y                                   A5 28
bita  $9,s                                   A5 69
bita  $9,u                                   A5 49
bita  $9,x                                   A5 09
bita  $9,y                                   A5 29
bita  $a,s                                   A5 6A
bita  $a,u                                   A5 4A
bita  $a,x                                   A5 0A
bita  $a,y                                   A5 2A
bita  $b,s                                   A5 6B
bita  $b,u                                   A5 4B
bita  $b,x                                   A5 0B
bita  $b,y                                   A5 2B
bita  $beef                                  A5 8F BE EF
bita  $beef                                  A5 AF BE EF
bita  $beef                                  A5 CF BE EF
bita  $beef                                  A5 EF BE EF
bita  $beef                                  B5 BE EF
bita  $beef,pc                               A5 8D BE EF
bita  $beef,pc                               A5 AD BE EF
bita  $beef,pc                               A5 CD BE EF
bita  $beef,pc                               A5 ED BE EF
bita  $beef,s                                A5 E9 BE EF
bita  $beef,u                                A5 C9 BE EF
bita  $beef,x                                A5 89 BE EF
bita  $beef,y                                A5 A9 BE EF
bita  $c,s                                   A5 6C
bita  $c,u                                   A5 4C
bita  $c,x                                   A5 0C
bita  $c,y                                   A5 2C
bita  $d,s                                   A5 6D
bita  $d,u                                   A5 4D
bita  $d,x                                   A5 0D
bita  $d,y                                   A5 2D
bita  $e,s                                   A5 6E
bita  $e,u                                   A5 4E
bita  $e,x                                   A5 0E
bita  $e,y                                   A5 2E
bita  $f,s                                   A5 6F
bita  $f,u                                   A5 4F
bita  $f,x                                   A5 0F
bita  $f,y                                   A5 2F
bita  $ff                                    95 FF
bita  ,--s                                   A5 E3
bita  ,--u                                   A5 C3
bita  ,--x                                   A5 83
bita  ,--y                                   A5 A3
bita  ,-s                                    A5 E2
bita  ,-u                                    A5 C2
bita  ,-x                                    A5 82
bita  ,-y                                    A5 A2
bita  ,s                                     A5 E4
bita  ,s+                                    A5 E0
bita  ,s++                                   A5 E1
bita  ,u                                     A5 C4
bita  ,u+                                    A5 C0
bita  ,u++                                   A5 C1
bita  ,x                                     A5 84
bita  ,x+                                    A5 80
bita  ,x++                                   A5 81
bita  ,y                                     A5 A4
bita  ,y+                                    A5 A0
bita  ,y++                                   A5 A1
bita  -$1,s                                  A5 7F
bita  -$1,u                                  A5 5F
bita  -$1,x                                  A5 1F
bita  -$1,y                                  A5 3F
bita  -$10,s                                 A5 70
bita  -$10,u                                 A5 50
bita  -$10,x                                 A5 10
bita  -$10,y                                 A5 30
bita  -$2,s                                  A5 7E
bita  -$2,u                                  A5 5E
bita  -$2,x                                  A5 1E
bita  -$2,y                                  A5 3E
bita  -$3,s                                  A5 7D
bita  -$3,u                                  A5 5D
bita  -$3,x                                  A5 1D
bita  -$3,y                                  A5 3D
bita  -$4,s                                  A5 7C
bita  -$4,u                                  A5 5C
bita  -$4,x                                  A5 1C
bita  -$4,y                                  A5 3C
bita  -$5,s                                  A5 7B
bita  -$5,u                                  A5 5B
bita  -$5,x                                  A5 1B
bita  -$5,y                                  A5 3B
bita  -$6,s                                  A5 7A
bita  -$6,u                                  A5 5A
bita  -$6,x                                  A5 1A
bita  -$6,y                                  A5 3A
bita  -$7,s                                  A5 79
bita  -$7,u                                  A5 59
bita  -$7,x                                  A5 19
bita  -$7,y                                  A5 39
bita  -$8,s                                  A5 78
bita  -$8,u                                  A5 58
bita  -$8,x                                  A5 18
bita  -$8,y                                  A5 38
bita  -$9,s                                  A5 77
bita  -$9,u                                  A5 57
bita  -$9,x                                  A5 17
bita  -$9,y                                  A5 37
bita  -$a,s                                  A5 76
bita  -$a,u                                  A5 56
bita  -$a,x                                  A5 16
bita  -$a,y                                  A5 36
bita  -$b,s                                  A5 75
bita  -$b,u                                  A5 55
bita  -$b,x                                  A5 15
bita  -$b,y                                  A5 35
bita  -$c,s                                  A5 74
bita  -$c,u                                  A5 54
bita  -$c,x                                  A5 14
bita  -$c,y                                  A5 34
bita  -$d,s                                  A5 73
bita  -$d,u                                  A5 53
bita  -$d,x                                  A5 13
bita  -$d,y                                  A5 33
bita  -$e,s                                  A5 72
bita  -$e,u                                  A5 52
bita  -$e,x                                  A5 12
bita  -$e,y                                  A5 32
bita  -$f,s                                  A5 71
bita  -$f,u                                  A5 51
bita  -$f,x                                  A5 11
bita  -$f,y                                  A5 31
bita  a,s                                    A5 E6
bita  a,u                                    A5 C6
bita  a,x                                    A5 86
bita  a,y                                    A5 A6
bita  b,s                                    A5 E5
bita  b,u                                    A5 C5
bita  b,x                                    A5 85
bita  b,y                                    A5 A5
bita  d,s                                    A5 EB
bita  d,u                                    A5 CB
bita  d,x                                    A5 8B
bita  d,y                                    A5 AB
bita  [$01,pc]                               A5 9C 01
bita  [$01,pc]                               A5 BC 01
bita  [$01,pc]                               A5 DC 01
bita  [$01,pc]                               A5 FC 01
bita  [$01,s]                                A5 F8 01
bita  [$01,u]                                A5 D8 01
bita  [$01,x]                                A5 98 01
bita  [$01,y]                                A5 B8 01
bita  [$beef,pc]                             A5 9D BE EF
bita  [$beef,pc]                             A5 BD BE EF
bita  [$beef,pc]                             A5 DD BE EF
bita  [$beef,pc]                             A5 FD BE EF
bita  [$beef,s]                              A5 F9 BE EF
bita  [$beef,u]                              A5 D9 BE EF
bita  [$beef,x]                              A5 99 BE EF
bita  [$beef,y]                              A5 B9 BE EF
bita  [$beef]                                A5 9F BE EF
bita  [$beef]                                A5 BF BE EF
bita  [$beef]                                A5 DF BE EF
bita  [$beef]                                A5 FF BE EF
bita  [,--s]                                 A5 F3
bita  [,--u]                                 A5 D3
bita  [,--x]                                 A5 93
bita  [,--y]                                 A5 B3
bita  [,s++]                                 A5 F1
bita  [,s]                                   A5 F4
bita  [,u++]                                 A5 D1
bita  [,u]                                   A5 D4
bita  [,x++]                                 A5 91
bita  [,x]                                   A5 94
bita  [,y++]                                 A5 B1
bita  [,y]                                   A5 B4
bita  [a,s]                                  A5 F6
bita  [a,u]                                  A5 D6
bita  [a,x]                                  A5 96
bita  [a,y]                                  A5 B6
bita  [b,s]                                  A5 F5
bita  [b,u]                                  A5 D5
bita  [b,x]                                  A5 95
bita  [b,y]                                  A5 B5
bita  [d,s]                                  A5 FB
bita  [d,u]                                  A5 DB
bita  [d,x]                                  A5 9B
bita  [d,y]                                  A5 BB
bita  []                                     A5 97
bita  []                                     A5 9A
bita  []                                     A5 9E
bita  []                                     A5 B7
bita  []                                     A5 BA
bita  []                                     A5 BE
bita  []                                     A5 D7
bita  []                                     A5 DA
bita  []                                     A5 DE
bita  []                                     A5 F7
bita  []                                     A5 FA
bita  []                                     A5 FE
bitb  #$ff                                   C5 FF
bitb  $0,s                                   E5 60
bitb  $0,u                                   E5 40
bitb  $0,x                                   E5 00
bitb  $0,y                                   E5 20
bitb  $01,pc                                 E5 8C 01
bitb  $01,pc                                 E5 AC 01
bitb  $01,pc                                 E5 CC 01
bitb  $01,pc                                 E5 EC 01
bitb  $01,s                                  E5 E8 01
bitb  $01,u                                  E5 C8 01
bitb  $01,x                                  E5 88 01
bitb  $01,y                                  E5 A8 01
bitb  $1,s                                   E5 61
bitb  $1,u                                   E5 41
bitb  $1,x                                   E5 01
bitb  $1,y                                   E5 21
bitb  $2,s                                   E5 62
bitb  $2,u                                   E5 42
bitb  $2,x                                   E5 02
bitb  $2,y                                   E5 22
bitb  $3,s                                   E5 63
bitb  $3,u                                   E5 43
bitb  $3,x                                   E5 03
bitb  $3,y                                   E5 23
bitb  $4,s                                   E5 64
bitb  $4,u                                   E5 44
bitb  $4,x                                   E5 04
bitb  $4,y                                   E5 24
bitb  $5,s                                   E5 65
bitb  $5,u                                   E5 45
bitb  $5,x                                   E5 05
bitb  $5,y                                   E5 25
bitb  $6,s                                   E5 66
bitb  $6,u                                   E5 46
bitb  $6,x                                   E5 06
bitb  $6,y                                   E5 26
bitb  $7,s                                   E5 67
bitb  $7,u                                   E5 47
bitb  $7,x                                   E5 07
bitb  $7,y                                   E5 27
bitb  $8,s                                   E5 68
bitb  $8,u                                   E5 48
bitb  $8,x                                   E5 08
bitb  $8,y                                   E5 28
bitb  $9,s                                   E5 69
bitb  $9,u                                   E5 49
bitb  $9,x                                   E5 09
bitb  $9,y                                   E5 29
bitb  $a,s                                   E5 6A
bitb  $a,u                                   E5 4A
bitb  $a,x                                   E5 0A
bitb  $a,y                                   E5 2A
bitb  $b,s                                   E5 6B
bitb  $b,u                                   E5 4B
bitb  $b,x                                   E5 0B
bitb  $b,y                                   E5 2B
bitb  $beef                                  E5 8F BE EF
bitb  $beef                                  E5 AF BE EF
bitb  $beef                                  E5 CF BE EF
bitb  $beef                                  E5 EF BE EF
bitb  $beef                                  F5 BE EF
bitb  $beef,pc                               E5 8D BE EF
bitb  $beef,pc                               E5 AD BE EF
bitb  $beef,pc                               E5 CD BE EF
bitb  $beef,pc                               E5 ED BE EF
bitb  $beef,s                                E5 E9 BE EF
bitb  $beef,u                                E5 C9 BE EF
bitb  $beef,x                                E5 89 BE EF
bitb  $beef,y                                E5 A9 BE EF
bitb  $c,s                                   E5 6C
bitb  $c,u                                   E5 4C
bitb  $c,x                                   E5 0C
bitb  $c,y                                   E5 2C
bitb  $d,s                                   E5 6D
bitb  $d,u                                   E5 4D
bitb  $d,x                                   E5 0D
bitb  $d,y                                   E5 2D
bitb  $e,s                                   E5 6E
bitb  $e,u                                   E5 4E
bitb  $e,x                                   E5 0E
bitb  $e,y                                   E5 2E
bitb  $f,s                                   E5 6F
bitb  $f,u                                   E5 4F
bitb  $f,x                                   E5 0F
bitb  $f,y                                   E5 2F
bitb  $ff                                    D5 FF
bitb  ,--s                                   E5 E3
bitb  ,--u                                   E5 C3
bitb  ,--x                                   E5 83
bitb  ,--y                                   E5 A3
bitb  ,-s                                    E5 E2
bitb  ,-u                                    E5 C2
bitb  ,-x                                    E5 82
bitb  ,-y                                    E5 A2
bitb  ,s                                     E5 E4
bitb  ,s+                                    E5 E0
bitb  ,s++                                   E5 E1
bitb  ,u                                     E5 C4
bitb  ,u+                                    E5 C0
bitb  ,u++                                   E5 C1
bitb  ,x                                     E5 84
bitb  ,x+                                    E5 80
bitb  ,x++                                   E5 81
bitb  ,y                                     E5 A4
bitb  ,y+                                    E5 A0
bitb  ,y++                                   E5 A1
bitb  -$1,s                                  E5 7F
bitb  -$1,u                                  E5 5F
bitb  -$1,x                                  E5 1F
bitb  -$1,y                                  E5 3F
bitb  -$10,s                                 E5 70
bitb  -$10,u                                 E5 50
bitb  -$10,x                                 E5 10
bitb  -$10,y                                 E5 30
bitb  -$2,s                                  E5 7E
bitb  -$2,u                                  E5 5E
bitb  -$2,x                                  E5 1E
bitb  -$2,y                                  E5 3E
bitb  -$3,s                                  E5 7D
bitb  -$3,u                                  E5 5D
bitb  -$3,x                                  E5 1D
bitb  -$3,y                                  E5 3D
bitb  -$4,s                                  E5 7C
bitb  -$4,u                                  E5 5C
bitb  -$4,x                                  E5 1C
bitb  -$4,y                                  E5 3C
bitb  -$5,s                                  E5 7B
bitb  -$5,u                                  E5 5B
bitb  -$5,x                                  E5 1B
bitb  -$5,y                                  E5 3B
bitb  -$6,s                                  E5 7A
bitb  -$6,u                                  E5 5A
bitb  -$6,x                                  E5 1A
bitb  -$6,y                                  E5 3A
bitb  -$7,s                                  E5 79
bitb  -$7,u                                  E5 59
bitb  -$7,x                                  E5 19
bitb  -$7,y                                  E5 39
bitb  -$8,s                                  E5 78
bitb  -$8,u                                  E5 58
bitb  -$8,x                                  E5 18
bitb  -$8,y                                  E5 38
bitb  -$9,s                                  E5 77
bitb  -$9,u                                  E5 57
bitb  -$9,x                                  E5 17
bitb  -$9,y                                  E5 37
bitb  -$a,s                                  E5 76
bitb  -$a,u                                  E5 56
bitb  -$a,x                                  E5 16
bitb  -$a,y                                  E5 36
bitb  -$b,s                                  E5 75
bitb  -$b,u                                  E5 55
bitb  -$b,x                                  E5 15
bitb  -$b,y                                  E5 35
bitb  -$c,s                                  E5 74
bitb  -$c,u                                  E5 54
bitb  -$c,x                                  E5 14
bitb  -$c,y                                  E5 34
bitb  -$d,s                                  E5 73
bitb  -$d,u                                  E5 53
bitb  -$d,x                                  E5 13
bitb  -$d,y                                  E5 33
bitb  -$e,s                                  E5 72
bitb  -$e,u                                  E5 52
bitb  -$e,x                                  E5 12
bitb  -$e,y                                  E5 32
bitb  -$f,s                                  E5 71
bitb  -$f,u                                  E5 51
bitb  -$f,x                                  E5 11
bitb  -$f,y                                  E5 31
bitb  a,s                                    E5 E6
bitb  a,u                                    E5 C6
bitb  a,x                                    E5 86
bitb  a,y                                    E5 A6
bitb  b,s                                    E5 E5
bitb  b,u                                    E5 C5
bitb  b,x                                    E5 85
bitb  b,y                                    E5 A5
bitb  d,s                                    E5 EB
bitb  d,u                                    E5 CB
bitb  d,x                                    E5 8B
bitb  d,y                                    E5 AB
bitb  [$01,pc]                               E5 9C 01
bitb  [$01,pc]                               E5 BC 01
bitb  [$01,pc]                               E5 DC 01
bitb  [$01,pc]                               E5 FC 01
bitb  [$01,s]                                E5 F8 01
bitb  [$01,u]                                E5 D8 01
bitb  [$01,x]                                E5 98 01
bitb  [$01,y]                                E5 B8 01
bitb  [$beef,pc]                             E5 9D BE EF
bitb  [$beef,pc]                             E5 BD BE EF
bitb  [$beef,pc]                             E5 DD BE EF
bitb  [$beef,pc]                             E5 FD BE EF
bitb  [$beef,s]                              E5 F9 BE EF
bitb  [$beef,u]                              E5 D9 BE EF
bitb  [$beef,x]                              E5 99 BE EF
bitb  [$beef,y]                              E5 B9 BE EF
bitb  [$beef]                                E5 9F BE EF
bitb  [$beef]                                E5 BF BE EF
bitb  [$beef]                                E5 DF BE EF
bitb  [$beef]                                E5 FF BE EF
bitb  [,--s]                                 E5 F3
bitb  [,--u]                                 E5 D3
bitb  [,--x]                                 E5 93
bitb  [,--y]                                 E5 B3
bitb  [,s++]                                 E5 F1
bitb  [,s]                                   E5 F4
bitb  [,u++]                                 E5 D1
bitb  [,u]                                   E5 D4
bitb  [,x++]                                 E5 91
bitb  [,x]                                   E5 94
bitb  [,y++]                                 E5 B1
bitb  [,y]                                   E5 B4
bitb  [a,s]                                  E5 F6
bitb  [a,u]                                  E5 D6
bitb  [a,x]                                  E5 96
bitb  [a,y]                                  E5 B6
bitb  [b,s]                                  E5 F5
bitb  [b,u]                                  E5 D5
bitb  [b,x]                                  E5 95
bitb  [b,y]                                  E5 B5
bitb  [d,s]                                  E5 FB
bitb  [d,u]                                  E5 DB
bitb  [d,x]                                  E5 9B
bitb  [d,y]                                  E5 BB
bitb  []                                     E5 97
bitb  []                                     E5 9A
bitb  []                                     E5 9E
bitb  []                                     E5 B7
bitb  []                                     E5 BA
bitb  []                                     E5 BE
bitb  []                                     E5 D7
bitb  []                                     E5 DA
bitb  []                                     E5 DE
bitb  []                                     E5 F7
bitb  []                                     E5 FA
bitb  []                                     E5 FE
ble   $+2                                    2F 0F
bls   $+2                                    23 29
blt   $+2                                    2D 01
bmi   $+2                                    2B 01
bne   $+2                                    26 14
bpl   $+2                                    2A 01
bra   $+2                                    20 00
brn   $+2                                    21 00
bsr   $c702                                  8D 00
bvc   $+2                                    28 01
bvs   $+2                                    29 03
clr   $0,s                                   6F 60
clr   $0,u                                   6F 40
clr   $0,x                                   6F 00
clr   $0,y                                   6F 20
clr   $01,pc                                 6F 8C 01
clr   $01,pc                                 6F AC 01
clr   $01,pc                                 6F CC 01
clr   $01,pc                                 6F EC 01
clr   $01,s                                  6F E8 01
clr   $01,u                                  6F C8 01
clr   $01,x                                  6F 88 01
clr   $01,y                                  6F A8 01
clr   $1,s                                   6F 61
clr   $1,u                                   6F 41
clr   $1,x                                   6F 01
clr   $1,y                                   6F 21
clr   $2,s                                   6F 62
clr   $2,u                                   6F 42
clr   $2,x                                   6F 02
clr   $2,y                                   6F 22
clr   $3,s                                   6F 63
clr   $3,u                                   6F 43
clr   $3,x                                   6F 03
clr   $3,y                                   6F 23
clr   $4,s                                   6F 64
clr   $4,u                                   6F 44
clr   $4,x                                   6F 04
clr   $4,y                                   6F 24
clr   $5,s                                   6F 65
clr   $5,u                                   6F 45
clr   $5,x                                   6F 05
clr   $5,y                                   6F 25
clr   $6,s                                   6F 66
clr   $6,u                                   6F 46
clr   $6,x                                   6F 06
clr   $6,y                                   6F 26
clr   $7,s                                   6F 67
clr   $7,u                                   6F 47
clr   $7,x                                   6F 07
clr   $7,y                                   6F 27
clr   $8,s                                   6F 68
clr   $8,u                                   6F 48
clr   $8,x                                   6F 08
clr   $8,y                                   6F 28
clr   $9,s                                   6F 69
clr   $9,u                                   6F 49
clr   $9,x                                   6F 09
clr   $9,y                                   6F 29
clr   $a,s                                   6F 6A
clr   $a,u                                   6F 4A
clr   $a,x                                   6F 0A
clr   $a,y                                   6F 2A
clr   $b,s                                   6F 6B
clr   $b,u                                   6F 4B
clr   $b,x                                   6F 0B
clr   $b,y                                   6F 2B
clr   $beef                                  6F 8F BE EF
clr   $beef                                  6F AF BE EF
clr   $beef                                  6F CF BE EF
clr   $beef                                  6F EF BE EF
clr   $beef                                  7F BE EF
clr   $beef,pc                               6F 8D BE EF
clr   $beef,pc                               6F AD BE EF
clr   $beef,pc                               6F CD BE EF
clr   $beef,pc                               6F ED BE EF
clr   $beef,s                                6F E9 BE EF
clr   $beef,u                                6F C9 BE EF
clr   $beef,x                                6F 89 BE EF
clr   $beef,y                                6F A9 BE EF
clr   $c,s                                   6F 6C
clr   $c,u                                   6F 4C
clr   $c,x                                   6F 0C
clr   $c,y                                   6F 2C
clr   $d,s                                   6F 6D
clr   $d,u                                   6F 4D
clr   $d,x                                   6F 0D
clr   $d,y                                   6F 2D
clr   $e,s                                   6F 6E
clr   $e,u                                   6F 4E
clr   $e,x                                   6F 0E
clr   $e,y                                   6F 2E
clr   $f,s                                   6F 6F
clr   $f,u                                   6F 4F
clr   $f,x                                   6F 0F
clr   $f,y                                   6F 2F
clr   $ff                                    0F FF
clr   ,--s                                   6F E3
clr   ,--u                                   6F C3
clr   ,--x                                   6F 83
clr   ,--y                                   6F A3
clr   ,-s                                    6F E2
clr   ,-u                                    6F C2
clr   ,-x                                    6F 82
clr   ,-y                                    6F A2
clr   ,s                                     6F E4
clr   ,s+                                    6F E0
clr   ,s++                                   6F E1
clr   ,u                                     6F C4
clr   ,u+                                    6F C0
clr   ,u++                                   6F C1
clr   ,x                                     6F 84
clr   ,x+                                    6F 80
clr   ,x++                                   6F 81
clr   ,y                                     6F A4
clr   ,y+                                    6F A0
clr   ,y++                                   6F A1
clr   -$1,s                                  6F 7F
clr   -$1,u                                  6F 5F
clr   -$1,x                                  6F 1F
clr   -$1,y                                  6F 3F
clr   -$10,s                                 6F 70
clr   -$10,u                                 6F 50
clr   -$10,x                                 6F 10
clr   -$10,y                                 6F 30
clr   -$2,s                                  6F 7E
clr   -$2,u                                  6F 5E
clr   -$2,x                                  6F 1E
clr   -$2,y                                  6F 3E
clr   -$3,s                                  6F 7D
clr   -$3,u                                  6F 5D
clr   -$3,x                                  6F 1D
clr   -$3,y                                  6F 3D
clr   -$4,s                                  6F 7C
clr   -$4,u                                  6F 5C
clr   -$4,x                                  6F 1C
clr   -$4,y                                  6F 3C
clr   -$5,s                                  6F 7B
clr   -$5,u                                  6F 5B
clr   -$5,x                                  6F 1B
clr   -$5,y                                  6F 3B
clr   -$6,s                                  6F 7A
clr   -$6,u                                  6F 5A
clr   -$6,x                                  6F 1A
clr   -$6,y                                  6F 3A
clr   -$7,s                                  6F 79
clr   -$7,u                                  6F 59
clr   -$7,x                                  6F 19
clr   -$7,y                                  6F 39
clr   -$8,s                                  6F 78
clr   -$8,u                                  6F 58
clr   -$8,x                                  6F 18
clr   -$8,y                                  6F 38
clr   -$9,s                                  6F 77
clr   -$9,u                                  6F 57
clr   -$9,x                                  6F 17
clr   -$9,y                                  6F 37
clr   -$a,s                                  6F 76
clr   -$a,u                                  6F 56
clr   -$a,x                                  6F 16
clr   -$a,y                                  6F 36
clr   -$b,s                                  6F 75
clr   -$b,u                                  6F 55
clr   -$b,x                                  6F 15
clr   -$b,y                                  6F 35
clr   -$c,s                                  6F 74
clr   -$c,u                                  6F 54
clr   -$c,x                                  6F 14
clr   -$c,y                                  6F 34
clr   -$d,s                                  6F 73
clr   -$d,u                                  6F 53
clr   -$d,x                                  6F 13
clr   -$d,y                                  6F 33
clr   -$e,s                                  6F 72
clr   -$e,u                                  6F 52
clr   -$e,x                                  6F 12
clr   -$e,y                                  6F 32
clr   -$f,s                                  6F 71
clr   -$f,u                                  6F 51
clr   -$f,x                                  6F 11
clr   -$f,y                                  6F 31
clr   a,s                                    6F E6
clr   a,u                                    6F C6
clr   a,x                                    6F 86
clr   a,y                                    6F A6
clr   b,s                                    6F E5
clr   b,u                                    6F C5
clr   b,x                                    6F 85
clr   b,y                                    6F A5
clr   d,s                                    6F EB
clr   d,u                                    6F CB
clr   d,x                                    6F 8B
clr   d,y                                    6F AB
clr   [$01,pc]                               6F 9C 01
clr   [$01,pc]                               6F BC 01
clr   [$01,pc]                               6F DC 01
clr   [$01,pc]                               6F FC 01
clr   [$01,s]                                6F F8 01
clr   [$01,u]                                6F D8 01
clr   [$01,x]                                6F 98 01
clr   [$01,y]                                6F B8 01
clr   [$beef,pc]                             6F 9D BE EF
clr   [$beef,pc]                             6F BD BE EF
clr   [$beef,pc]                             6F DD BE EF
clr   [$beef,pc]                             6F FD BE EF
clr   [$beef,s]                              6F F9 BE EF
clr   [$beef,u]                              6F D9 BE EF
clr   [$beef,x]                              6F 99 BE EF
clr   [$beef,y]                              6F B9 BE EF
clr   [$beef]                                6F 9F BE EF
clr   [$beef]                                6F BF BE EF
clr   [$beef]                                6F DF BE EF
clr   [$beef]                                6F FF BE EF
clr   [,--s]                                 6F F3
clr   [,--u]                                 6F D3
clr   [,--x]                                 6F 93
clr   [,--y]                                 6F B3
clr   [,s++]                                 6F F1
clr   [,s]                                   6F F4
clr   [,u++]                                 6F D1
clr   [,u]                                   6F D4
clr   [,x++]                                 6F 91
clr   [,x]                                   6F 94
clr   [,y++]                                 6F B1
clr   [,y]                                   6F B4
clr   [a,s]                                  6F F6
clr   [a,u]                                  6F D6
clr   [a,x]                                  6F 96
clr   [a,y]                                  6F B6
clr   [b,s]                                  6F F5
clr   [b,u]                                  6F D5
clr   [b,x]                                  6F 95
clr   [b,y]                                  6F B5
clr   [d,s]                                  6F FB
clr   [d,u]                                  6F DB
clr   [d,x]                                  6F 9B
clr   [d,y]                                  6F BB
clr   []                                     6F 97
clr   []                                     6F 9A
clr   []                                     6F 9E
clr   []                                     6F B7
clr   []                                     6F BA
clr   []                                     6F BE
clr   []                                     6F D7
clr   []                                     6F DA
clr   []                                     6F DE
clr   []                                     6F F7
clr   []                                     6F FA
clr   []                                     6F FE
clra                                         4F
clrb                                         5F
cmpa  #$ff                                   81 FF
cmpa  $0,s                                   A1 60
cmpa  $0,u                                   A1 40
cmpa  $0,x                                   A1 00
cmpa  $0,y                                   A1 20
cmpa  $01,pc                                 A1 8C 01
cmpa  $01,pc                                 A1 AC 01
cmpa  $01,pc                                 A1 CC 01
cmpa  $01,pc                                 A1 EC 01
cmpa  $01,s                                  A1 E8 01
cmpa  $01,u                                  A1 C8 01
cmpa  $01,x                                  A1 88 01
cmpa  $01,y                                  A1 A8 01
cmpa  $1,s                                   A1 61
cmpa  $1,u                                   A1 41
cmpa  $1,x                                   A1 01
cmpa  $1,y                                   A1 21
cmpa  $2,s                                   A1 62
cmpa  $2,u                                   A1 42
cmpa  $2,x                                   A1 02
cmpa  $2,y                                   A1 22
cmpa  $3,s                                   A1 63
cmpa  $3,u                                   A1 43
cmpa  $3,x                                   A1 03
cmpa  $3,y                                   A1 23
cmpa  $4,s                                   A1 64
cmpa  $4,u                                   A1 44
cmpa  $4,x                                   A1 04
cmpa  $4,y                                   A1 24
cmpa  $5,s                                   A1 65
cmpa  $5,u                                   A1 45
cmpa  $5,x                                   A1 05
cmpa  $5,y                                   A1 25
cmpa  $6,s                                   A1 66
cmpa  $6,u                                   A1 46
cmpa  $6,x                                   A1 06
cmpa  $6,y                                   A1 26
cmpa  $7,s                                   A1 67
cmpa  $7,u                                   A1 47
cmpa  $7,x                                   A1 07
cmpa  $7,y                                   A1 27
cmpa  $8,s                                   A1 68
cmpa  $8,u                                   A1 48
cmpa  $8,x                                   A1 08
cmpa  $8,y                                   A1 28
cmpa  $9,s                                   A1 69
cmpa  $9,u                                   A1 49
cmpa  $9,x                                   A1 09
cmpa  $9,y                                   A1 29
cmpa  $a,s                                   A1 6A
cmpa  $a,u                                   A1 4A
cmpa  $a,x                                   A1 0A
cmpa  $a,y                                   A1 2A
cmpa  $b,s                                   A1 6B
cmpa  $b,u                                   A1 4B
cmpa  $b,x                                   A1 0B
cmpa  $b,y                                   A1 2B
cmpa  $beef                                  A1 8F BE EF
cmpa  $beef                                  A1 AF BE EF
cmpa  $beef                                  A1 CF BE EF
cmpa  $beef                                  A1 EF BE EF
cmpa  $beef                                  B1 BE EF
cmpa  $beef,pc                               A1 8D BE EF
cmpa  $beef,pc                               A1 AD BE EF
cmpa  $beef,pc                               A1 CD BE EF
cmpa  $beef,pc                               A1 ED BE EF
cmpa  $beef,s                                A1 E9 BE EF
cmpa  $beef,u                                A1 C9 BE EF
cmpa  $beef,x                                A1 89 BE EF
cmpa  $beef,y                                A1 A9 BE EF
cmpa  $c,s                                   A1 6C
cmpa  $c,u                                   A1 4C
cmpa  $c,x                                   A1 0C
cmpa  $c,y                                   A1 2C
cmpa  $d,s                                   A1 6D
cmpa  $d,u                                   A1 4D
cmpa  $d,x                                   A1 0D
cmpa  $d,y                                   A1 2D
cmpa  $e,s                                   A1 6E
cmpa  $e,u                                   A1 4E
cmpa  $e,x                                   A1 0E
cmpa  $e,y                                   A1 2E
cmpa  $f,s                                   A1 6F
cmpa  $f,u                                   A1 4F
cmpa  $f,x                                   A1 0F
cmpa  $f,y                                   A1 2F
cmpa  $ff                                    91 FF
cmpa  ,--s                                   A1 E3
cmpa  ,--u                                   A1 C3
cmpa  ,--x                                   A1 83
cmpa  ,--y                                   A1 A3
cmpa  ,-s                                    A1 E2
cmpa  ,-u                                    A1 C2
cmpa  ,-x                                    A1 82
cmpa  ,-y                                    A1 A2
cmpa  ,s                                     A1 E4
cmpa  ,s+                                    A1 E0
cmpa  ,s++                                   A1 E1
cmpa  ,u                                     A1 C4
cmpa  ,u+                                    A1 C0
cmpa  ,u++                                   A1 C1
cmpa  ,x                                     A1 84
cmpa  ,x+                                    A1 80
cmpa  ,x++                                   A1 81
cmpa  ,y                                     A1 A4
cmpa  ,y+                                    A1 A0
cmpa  ,y++                                   A1 A1
cmpa  -$1,s                                  A1 7F
cmpa  -$1,u                                  A1 5F
cmpa  -$1,x                                  A1 1F
cmpa  -$1,y                                  A1 3F
cmpa  -$10,s                                 A1 70
cmpa  -$10,u                                 A1 50
cmpa  -$10,x                                 A1 10
cmpa  -$10,y                                 A1 30
cmpa  -$2,s                                  A1 7E
cmpa  -$2,u                                  A1 5E
cmpa  -$2,x                                  A1 1E
cmpa  -$2,y                                  A1 3E
cmpa  -$3,s                                  A1 7D
cmpa  -$3,u                                  A1 5D
cmpa  -$3,x                                  A1 1D
cmpa  -$3,y                                  A1 3D
cmpa  -$4,s                                  A1 7C
cmpa  -$4,u                                  A1 5C
cmpa  -$4,x                                  A1 1C
cmpa  -$4,y                                  A1 3C
cmpa  -$5,s                                  A1 7B
cmpa  -$5,u                                  A1 5B
cmpa  -$5,x                                  A1 1B
cmpa  -$5,y                                  A1 3B
cmpa  -$6,s                                  A1 7A
cmpa  -$6,u                                  A1 5A
cmpa  -$6,x                                  A1 1A
cmpa  -$6,y                                  A1 3A
cmpa  -$7,s                                  A1 79
cmpa  -$7,u                                  A1 59
cmpa  -$7,x                                  A1 19
cmpa  -$7,y                                  A1 39
cmpa  -$8,s                                  A1 78
cmpa  -$8,u                                  A1 58
cmpa  -$8,x                                  A1 18
cmpa  -$8,y                                  A1 38
cmpa  -$9,s                                  A1 77
cmpa  -$9,u                                  A1 57
cmpa  -$9,x                                  A1 17
cmpa  -$9,y                                  A1 37
cmpa  -$a,s                                  A1 76
cmpa  -$a,u                                  A1 56
cmpa  -$a,x                                  A1 16
cmpa  -$a,y                                  A1 36
cmpa  -$b,s                                  A1 75
cmpa  -$b,u                                  A1 55
cmpa  -$b,x                                  A1 15
cmpa  -$b,y                                  A1 35
cmpa  -$c,s                                  A1 74
cmpa  -$c,u                                  A1 54
cmpa  -$c,x                                  A1 14
cmpa  -$c,y                                  A1 34
cmpa  -$d,s                                  A1 73
cmpa  -$d,u                                  A1 53
cmpa  -$d,x                                  A1 13
cmpa  -$d,y                                  A1 33
cmpa  -$e,s                                  A1 72
cmpa  -$e,u                                  A1 52
cmpa  -$e,x                                  A1 12
cmpa  -$e,y                                  A1 32
cmpa  -$f,s                                  A1 71
cmpa  -$f,u                                  A1 51
cmpa  -$f,x                                  A1 11
cmpa  -$f,y                                  A1 31
cmpa  a,s                                    A1 E6
cmpa  a,u                                    A1 C6
cmpa  a,x                                    A1 86
cmpa  a,y                                    A1 A6
cmpa  b,s                                    A1 E5
cmpa  b,u                                    A1 C5
cmpa  b,x                                    A1 85
cmpa  b,y                                    A1 A5
cmpa  d,s                                    A1 EB
cmpa  d,u                                    A1 CB
cmpa  d,x                                    A1 8B
cmpa  d,y                                    A1 AB
cmpa  [$01,pc]                               A1 9C 01
cmpa  [$01,pc]                               A1 BC 01
cmpa  [$01,pc]                               A1 DC 01
cmpa  [$01,pc]                               A1 FC 01
cmpa  [$01,s]                                A1 F8 01
cmpa  [$01,u]                                A1 D8 01
cmpa  [$01,x]                                A1 98 01
cmpa  [$01,y]                                A1 B8 01
cmpa  [$beef,pc]                             A1 9D BE EF
cmpa  [$beef,pc]                             A1 BD BE EF
cmpa  [$beef,pc]                             A1 DD BE EF
cmpa  [$beef,pc]                             A1 FD BE EF
cmpa  [$beef,s]                              A1 F9 BE EF
cmpa  [$beef,u]                              A1 D9 BE EF
cmpa  [$beef,x]                              A1 99 BE EF
cmpa  [$beef,y]                              A1 B9 BE EF
cmpa  [$beef]                                A1 9F BE EF
cmpa  [$beef]                                A1 BF BE EF
cmpa  [$beef]                                A1 DF BE EF
cmpa  [$beef]                                A1 FF BE EF
cmpa  [,--s]                                 A1 F3
cmpa  [,--u]                                 A1 D3
cmpa  [,--x]                                 A1 93
cmpa  [,--y]                                 A1 B3
cmpa  [,s++]                                 A1 F1
cmpa  [,s]                                   A1 F4
cmpa  [,u++]                                 A1 D1
cmpa  [,u]                                   A1 D4
cmpa  [,x++]                                 A1 91
cmpa  [,x]                                   A1 94
cmpa  [,y++]                                 A1 B1
cmpa  [,y]                                   A1 B4
cmpa  [a,s]                                  A1 F6
cmpa  [a,u]                                  A1 D6
cmpa  [a,x]                                  A1 96
cmpa  [a,y]                                  A1 B6
cmpa  [b,s]                                  A1 F5
cmpa  [b,u]                                  A1 D5
cmpa  [b,x]                                  A1 95
cmpa  [b,y]                                  A1 B5
cmpa  [d,s]                                  A1 FB
cmpa  [d,u]                                  A1 DB
cmpa  [d,x]                                  A1 9B
cmpa  [d,y]                                  A1 BB
cmpa  []                                     A1 97
cmpa  []                                     A1 9A
cmpa  []                                     A1 9E
cmpa  []                                     A1 B7
cmpa  []                                     A1 BA
cmpa  []                                     A1 BE
cmpa  []                                     A1 D7
cmpa  []                                     A1 DA
cmpa  []                                     A1 DE
cmpa  []                                     A1 F7
cmpa  []                                     A1 FA
cmpa  []                                     A1 FE
cmpb  #$ff                                   C1 FF
cmpb  $0,s                                   E1 60
cmpb  $0,u                                   E1 40
cmpb  $0,x                                   E1 00
cmpb  $0,y                                   E1 20
cmpb  $01,pc                                 E1 8C 01
cmpb  $01,pc                                 E1 AC 01
cmpb  $01,pc                                 E1 CC 01
cmpb  $01,pc                                 E1 EC 01
cmpb  $01,s                                  E1 E8 01
cmpb  $01,u                                  E1 C8 01
cmpb  $01,x                                  E1 88 01
cmpb  $01,y                                  E1 A8 01
cmpb  $1,s                                   E1 61
cmpb  $1,u                                   E1 41
cmpb  $1,x                                   E1 01
cmpb  $1,y                                   E1 21
cmpb  $2,s                                   E1 62
cmpb  $2,u                                   E1 42
cmpb  $2,x                                   E1 02
cmpb  $2,y                                   E1 22
cmpb  $3,s                                   E1 63
cmpb  $3,u                                   E1 43
cmpb  $3,x                                   E1 03
cmpb  $3,y                                   E1 23
cmpb  $4,s                                   E1 64
cmpb  $4,u                                   E1 44
cmpb  $4,x                                   E1 04
cmpb  $4,y                                   E1 24
cmpb  $5,s                                   E1 65
cmpb  $5,u                                   E1 45
cmpb  $5,x                                   E1 05
cmpb  $5,y                                   E1 25
cmpb  $6,s                                   E1 66
cmpb  $6,u                                   E1 46
cmpb  $6,x                                   E1 06
cmpb  $6,y                                   E1 26
cmpb  $7,s                                   E1 67
cmpb  $7,u                                   E1 47
cmpb  $7,x                                   E1 07
cmpb  $7,y                                   E1 27
cmpb  $8,s                                   E1 68
cmpb  $8,u                                   E1 48
cmpb  $8,x                                   E1 08
cmpb  $8,y                                   E1 28
cmpb  $9,s                                   E1 69
cmpb  $9,u                                   E1 49
cmpb  $9,x                                   E1 09
cmpb  $9,y                                   E1 29
cmpb  $a,s                                   E1 6A
cmpb  $a,u                                   E1 4A
cmpb  $a,x                                   E1 0A
cmpb  $a,y                                   E1 2A
cmpb  $b,s                                   E1 6B
cmpb  $b,u                                   E1 4B
cmpb  $b,x                                   E1 0B
cmpb  $b,y                                   E1 2B
cmpb  $beef                                  E1 8F BE EF
cmpb  $beef                                  E1 AF BE EF
cmpb  $beef                                  E1 CF BE EF
cmpb  $beef                                  E1 EF BE EF
cmpb  $beef                                  F1 BE EF
cmpb  $beef,pc                               E1 8D BE EF
cmpb  $beef,pc                               E1 AD BE EF
cmpb  $beef,pc                               E1 CD BE EF
cmpb  $beef,pc                               E1 ED BE EF
cmpb  $beef,s                                E1 E9 BE EF
cmpb  $beef,u                                E1 C9 BE EF
cmpb  $beef,x                                E1 89 BE EF
cmpb  $beef,y                                E1 A9 BE EF
cmpb  $c,s                                   E1 6C
cmpb  $c,u                                   E1 4C
cmpb  $c,x                                   E1 0C
cmpb  $c,y                                   E1 2C
cmpb  $d,s                                   E1 6D
cmpb  $d,u                                   E1 4D
cmpb  $d,x                                   E1 0D
cmpb  $d,y                                   E1 2D
cmpb  $e,s                                   E1 6E
cmpb  $e,u                                   E1 4E
cmpb  $e,x                                   E1 0E
cmpb  $e,y                                   E1 2E
cmpb  $f,s                                   E1 6F
cmpb  $f,u                                   E1 4F
cmpb  $f,x                                   E1 0F
cmpb  $f,y                                   E1 2F
cmpb  $ff                                    D1 FF
cmpb  ,--s                                   E1 E3
cmpb  ,--u                                   E1 C3
cmpb  ,--x                                   E1 83
cmpb  ,--y                                   E1 A3
cmpb  ,-s                                    E1 E2
cmpb  ,-u                                    E1 C2
cmpb  ,-x                                    E1 82
cmpb  ,-y                                    E1 A2
cmpb  ,s                                     E1 E4
cmpb  ,s+                                    E1 E0
cmpb  ,s++                                   E1 E1
cmpb  ,u                                     E1 C4
cmpb  ,u+                                    E1 C0
cmpb  ,u++                                   E1 C1
cmpb  ,x                                     E1 84
cmpb  ,x+                                    E1 80
cmpb  ,x++                                   E1 81
cmpb  ,y                                     E1 A4
cmpb  ,y+                                    E1 A0
cmpb  ,y++                                   E1 A1
cmpb  -$1,s                                  E1 7F
cmpb  -$1,u                                  E1 5F
cmpb  -$1,x                                  E1 1F
cmpb  -$1,y                                  E1 3F
cmpb  -$10,s                                 E1 70
cmpb  -$10,u                                 E1 50
cmpb  -$10,x                                 E1 10
cmpb  -$10,y                                 E1 30
cmpb  -$2,s                                  E1 7E
cmpb  -$2,u                                  E1 5E
cmpb  -$2,x                                  E1 1E
cmpb  -$2,y                                  E1 3E
cmpb  -$3,s                                  E1 7D
cmpb  -$3,u                                  E1 5D
cmpb  -$3,x                                  E1 1D
cmpb  -$3,y                                  E1 3D
cmpb  -$4,s                                  E1 7C
cmpb  -$4,u                                  E1 5C
cmpb  -$4,x                                  E1 1C
cmpb  -$4,y                                  E1 3C
cmpb  -$5,s                                  E1 7B
cmpb  -$5,u                                  E1 5B
cmpb  -$5,x                                  E1 1B
cmpb  -$5,y                                  E1 3B
cmpb  -$6,s                                  E1 7A
cmpb  -$6,u                                  E1 5A
cmpb  -$6,x                                  E1 1A
cmpb  -$6,y                                  E1 3A
cmpb  -$7,s                                  E1 79
cmpb  -$7,u                                  E1 59
cmpb  -$7,x                                  E1 19
cmpb  -$7,y                                  E1 39
cmpb  -$8,s                                  E1 78
cmpb  -$8,u                                  E1 58
cmpb  -$8,x                                  E1 18
cmpb  -$8,y                                  E1 38
cmpb  -$9,s                                  E1 77
cmpb  -$9,u                                  E1 57
cmpb  -$9,x                                  E1 17
cmpb  -$9,y                                  E1 37
cmpb  -$a,s                                  E1 76
cmpb  -$a,u                                  E1 56
cmpb  -$a,x                                  E1 16
cmpb  -$a,y                                  E1 36
cmpb  -$b,s                                  E1 75
cmpb  -$b,u                                  E1 55
cmpb  -$b,x                                  E1 15
cmpb  -$b,y                                  E1 35
cmpb  -$c,s                                  E1 74
cmpb  -$c,u                                  E1 54
cmpb  -$c,x                                  E1 14
cmpb  -$c,y                                  E1 34
cmpb  -$d,s                                  E1 73
cmpb  -$d,u                                  E1 53
cmpb  -$d,x                                  E1 13
cmpb  -$d,y                                  E1 33
cmpb  -$e,s                                  E1 72
cmpb  -$e,u                                  E1 52
cmpb  -$e,x                                  E1 12
cmpb  -$e,y                                  E1 32
cmpb  -$f,s                                  E1 71
cmpb  -$f,u                                  E1 51
cmpb  -$f,x                                  E1 11
cmpb  -$f,y                                  E1 31
cmpb  a,s                                    E1 E6
cmpb  a,u                                    E1 C6
cmpb  a,x                                    E1 86
cmpb  a,y                                    E1 A6
cmpb  b,s                                    E1 E5
cmpb  b,u                                    E1 C5
cmpb  b,x                                    E1 85
cmpb  b,y                                    E1 A5
cmpb  d,s                                    E1 EB
cmpb  d,u                                    E1 CB
cmpb  d,x                                    E1 8B
cmpb  d,y                                    E1 AB
cmpb  [$01,pc]                               E1 9C 01
cmpb  [$01,pc]                               E1 BC 01
cmpb  [$01,pc]                               E1 DC 01
cmpb  [$01,pc]                               E1 FC 01
cmpb  [$01,s]                                E1 F8 01
cmpb  [$01,u]                                E1 D8 01
cmpb  [$01,x]                                E1 98 01
cmpb  [$01,y]                                E1 B8 01
cmpb  [$beef,pc]                             E1 9D BE EF
cmpb  [$beef,pc]                             E1 BD BE EF
cmpb  [$beef,pc]                             E1 DD BE EF
cmpb  [$beef,pc]                             E1 FD BE EF
cmpb  [$beef,s]                              E1 F9 BE EF
cmpb  [$beef,u]                              E1 D9 BE EF
cmpb  [$beef,x]                              E1 99 BE EF
cmpb  [$beef,y]                              E1 B9 BE EF
cmpb  [$beef]                                E1 9F BE EF
cmpb  [$beef]                                E1 BF BE EF
cmpb  [$beef]                                E1 DF BE EF
cmpb  [$beef]                                E1 FF BE EF
cmpb  [,--s]                                 E1 F3
cmpb  [,--u]                                 E1 D3
cmpb  [,--x]                                 E1 93
cmpb  [,--y]                                 E1 B3
cmpb  [,s++]                                 E1 F1
cmpb  [,s]                                   E1 F4
cmpb  [,u++]                                 E1 D1
cmpb  [,u]                                   E1 D4
cmpb  [,x++]                                 E1 91
cmpb  [,x]                                   E1 94
cmpb  [,y++]                                 E1 B1
cmpb  [,y]                                   E1 B4
cmpb  [a,s]                                  E1 F6
cmpb  [a,u]                                  E1 D6
cmpb  [a,x]                                  E1 96
cmpb  [a,y]                                  E1 B6
cmpb  [b,s]                                  E1 F5
cmpb  [b,u]                                  E1 D5
cmpb  [b,x]                                  E1 95
cmpb  [b,y]                                  E1 B5
cmpb  [d,s]                                  E1 FB
cmpb  [d,u]                                  E1 DB
cmpb  [d,x]                                  E1 9B
cmpb  [d,y]                                  E1 BB
cmpb  []                                     E1 97
cmpb  []                                     E1 9A
cmpb  []                                     E1 9E
cmpb  []                                     E1 B7
cmpb  []                                     E1 BA
cmpb  []                                     E1 BE
cmpb  []                                     E1 D7
cmpb  []                                     E1 DA
cmpb  []                                     E1 DE
cmpb  []                                     E1 F7
cmpb  []                                     E1 FA
cmpb  []                                     E1 FE
cmpd  #$beef                                 10 83 BE EF
cmpd  $01                                    10 93 01
cmpd  $1,x                                   10 A3 01
cmpd  $beef                                  10 B3 BE EF
cmps  #$beef                                 11 8C BE EF
cmps  $01                                    11 9C 01
cmps  $1,x                                   11 AC 01
cmps  $beef                                  11 BC BE EF
cmpu  #$beef                                 11 83 BE EF
cmpu  $01                                    11 93 01
cmpu  $1,x                                   11 A3 01
cmpu  $beef                                  11 B3 BE EF
cmpx  #$beef                                 8C BE EF
cmpx  $0,s                                   AC 60
cmpx  $0,u                                   AC 40
cmpx  $0,x                                   AC 00
cmpx  $0,y                                   AC 20
cmpx  $01,pc                                 AC 8C 01
cmpx  $01,pc                                 AC AC 01
cmpx  $01,pc                                 AC CC 01
cmpx  $01,pc                                 AC EC 01
cmpx  $01,s                                  AC E8 01
cmpx  $01,u                                  AC C8 01
cmpx  $01,x                                  AC 88 01
cmpx  $01,y                                  AC A8 01
cmpx  $1,s                                   AC 61
cmpx  $1,u                                   AC 41
cmpx  $1,x                                   AC 01
cmpx  $1,y                                   AC 21
cmpx  $2,s                                   AC 62
cmpx  $2,u                                   AC 42
cmpx  $2,x                                   AC 02
cmpx  $2,y                                   AC 22
cmpx  $3,s                                   AC 63
cmpx  $3,u                                   AC 43
cmpx  $3,x                                   AC 03
cmpx  $3,y                                   AC 23
cmpx  $4,s                                   AC 64
cmpx  $4,u                                   AC 44
cmpx  $4,x                                   AC 04
cmpx  $4,y                                   AC 24
cmpx  $5,s                                   AC 65
cmpx  $5,u                                   AC 45
cmpx  $5,x                                   AC 05
cmpx  $5,y                                   AC 25
cmpx  $6,s                                   AC 66
cmpx  $6,u                                   AC 46
cmpx  $6,x                                   AC 06
cmpx  $6,y                                   AC 26
cmpx  $7,s                                   AC 67
cmpx  $7,u                                   AC 47
cmpx  $7,x                                   AC 07
cmpx  $7,y                                   AC 27
cmpx  $8,s                                   AC 68
cmpx  $8,u                                   AC 48
cmpx  $8,x                                   AC 08
cmpx  $8,y                                   AC 28
cmpx  $9,s                                   AC 69
cmpx  $9,u                                   AC 49
cmpx  $9,x                                   AC 09
cmpx  $9,y                                   AC 29
cmpx  $a,s                                   AC 6A
cmpx  $a,u                                   AC 4A
cmpx  $a,x                                   AC 0A
cmpx  $a,y                                   AC 2A
cmpx  $b,s                                   AC 6B
cmpx  $b,u                                   AC 4B
cmpx  $b,x                                   AC 0B
cmpx  $b,y                                   AC 2B
cmpx  $beef                                  AC 8F BE EF
cmpx  $beef                                  AC AF BE EF
cmpx  $beef                                  AC CF BE EF
cmpx  $beef                                  AC EF BE EF
cmpx  $beef                                  BC BE EF
cmpx  $beef,pc                               AC 8D BE EF
cmpx  $beef,pc                               AC AD BE EF
cmpx  $beef,pc                               AC CD BE EF
cmpx  $beef,pc                               AC ED BE EF
cmpx  $beef,s                                AC E9 BE EF
cmpx  $beef,u                                AC C9 BE EF
cmpx  $beef,x                                AC 89 BE EF
cmpx  $beef,y                                AC A9 BE EF
cmpx  $c,s                                   AC 6C
cmpx  $c,u                                   AC 4C
cmpx  $c,x                                   AC 0C
cmpx  $c,y                                   AC 2C
cmpx  $d,s                                   AC 6D
cmpx  $d,u                                   AC 4D
cmpx  $d,x                                   AC 0D
cmpx  $d,y                                   AC 2D
cmpx  $e,s                                   AC 6E
cmpx  $e,u                                   AC 4E
cmpx  $e,x                                   AC 0E
cmpx  $e,y                                   AC 2E
cmpx  $f,s                                   AC 6F
cmpx  $f,u                                   AC 4F
cmpx  $f,x                                   AC 0F
cmpx  $f,y                                   AC 2F
cmpx  $ff                                    9C FF
cmpx  ,--s                                   AC E3
cmpx  ,--u                                   AC C3
cmpx  ,--x                                   AC 83
cmpx  ,--y                                   AC A3
cmpx  ,-s                                    AC E2
cmpx  ,-u                                    AC C2
cmpx  ,-x                                    AC 82
cmpx  ,-y                                    AC A2
cmpx  ,s                                     AC E4
cmpx  ,s+                                    AC E0
cmpx  ,s++                                   AC E1
cmpx  ,u                                     AC C4
cmpx  ,u+                                    AC C0
cmpx  ,u++                                   AC C1
cmpx  ,x                                     AC 84
cmpx  ,x+                                    AC 80
cmpx  ,x++                                   AC 81
cmpx  ,y                                     AC A4
cmpx  ,y+                                    AC A0
cmpx  ,y++                                   AC A1
cmpx  -$1,s                                  AC 7F
cmpx  -$1,u                                  AC 5F
cmpx  -$1,x                                  AC 1F
cmpx  -$1,y                                  AC 3F
cmpx  -$10,s                                 AC 70
cmpx  -$10,u                                 AC 50
cmpx  -$10,x                                 AC 10
cmpx  -$10,y                                 AC 30
cmpx  -$2,s                                  AC 7E
cmpx  -$2,u                                  AC 5E
cmpx  -$2,x                                  AC 1E
cmpx  -$2,y                                  AC 3E
cmpx  -$3,s                                  AC 7D
cmpx  -$3,u                                  AC 5D
cmpx  -$3,x                                  AC 1D
cmpx  -$3,y                                  AC 3D
cmpx  -$4,s                                  AC 7C
cmpx  -$4,u                                  AC 5C
cmpx  -$4,x                                  AC 1C
cmpx  -$4,y                                  AC 3C
cmpx  -$5,s                                  AC 7B
cmpx  -$5,u                                  AC 5B
cmpx  -$5,x                                  AC 1B
cmpx  -$5,y                                  AC 3B
cmpx  -$6,s                                  AC 7A
cmpx  -$6,u                                  AC 5A
cmpx  -$6,x                                  AC 1A
cmpx  -$6,y                                  AC 3A
cmpx  -$7,s                                  AC 79
cmpx  -$7,u                                  AC 59
cmpx  -$7,x                                  AC 19
cmpx  -$7,y                                  AC 39
cmpx  -$8,s                                  AC 78
cmpx  -$8,u                                  AC 58
cmpx  -$8,x                                  AC 18
cmpx  -$8,y                                  AC 38
cmpx  -$9,s                                  AC 77
cmpx  -$9,u                                  AC 57
cmpx  -$9,x                                  AC 17
cmpx  -$9,y                                  AC 37
cmpx  -$a,s                                  AC 76
cmpx  -$a,u                                  AC 56
cmpx  -$a,x                                  AC 16
cmpx  -$a,y                                  AC 36
cmpx  -$b,s                                  AC 75
cmpx  -$b,u                                  AC 55
cmpx  -$b,x                                  AC 15
cmpx  -$b,y                                  AC 35
cmpx  -$c,s                                  AC 74
cmpx  -$c,u                                  AC 54
cmpx  -$c,x                                  AC 14
cmpx  -$c,y                                  AC 34
cmpx  -$d,s                                  AC 73
cmpx  -$d,u                                  AC 53
cmpx  -$d,x                                  AC 13
cmpx  -$d,y                                  AC 33
cmpx  -$e,s                                  AC 72
cmpx  -$e,u                                  AC 52
cmpx  -$e,x                                  AC 12
cmpx  -$e,y                                  AC 32
cmpx  -$f,s                                  AC 71
cmpx  -$f,u                                  AC 51
cmpx  -$f,x                                  AC 11
cmpx  -$f,y                                  AC 31
cmpx  a,s                                    AC E6
cmpx  a,u                                    AC C6
cmpx  a,x                                    AC 86
cmpx  a,y                                    AC A6
cmpx  b,s                                    AC E5
cmpx  b,u                                    AC C5
cmpx  b,x                                    AC 85
cmpx  b,y                                    AC A5
cmpx  d,s                                    AC EB
cmpx  d,u                                    AC CB
cmpx  d,x                                    AC 8B
cmpx  d,y                                    AC AB
cmpx  [$01,pc]                               AC 9C 01
cmpx  [$01,pc]                               AC BC 01
cmpx  [$01,pc]                               AC DC 01
cmpx  [$01,pc]                               AC FC 01
cmpx  [$01,s]                                AC F8 01
cmpx  [$01,u]                                AC D8 01
cmpx  [$01,x]                                AC 98 01
cmpx  [$01,y]                                AC B8 01
cmpx  [$beef,pc]                             AC 9D BE EF
cmpx  [$beef,pc]                             AC BD BE EF
cmpx  [$beef,pc]                             AC DD BE EF
cmpx  [$beef,pc]                             AC FD BE EF
cmpx  [$beef,s]                              AC F9 BE EF
cmpx  [$beef,u]                              AC D9 BE EF
cmpx  [$beef,x]                              AC 99 BE EF
cmpx  [$beef,y]                              AC B9 BE EF
cmpx  [$beef]                                AC 9F BE EF
cmpx  [$beef]                                AC BF BE EF
cmpx  [$beef]                                AC DF BE EF
cmpx  [$beef]                                AC FF BE EF
cmpx  [,--s]                                 AC F3
cmpx  [,--u]                                 AC D3
cmpx  [,--x]                                 AC 93
cmpx  [,--y]                                 AC B3
cmpx  [,s++]                                 AC F1
cmpx  [,s]                                   AC F4
cmpx  [,u++]                                 AC D1
cmpx  [,u]                                   AC D4
cmpx  [,x++]                                 AC 91
cmpx  [,x]                                   AC 94
cmpx  [,y++]                                 AC B1
cmpx  [,y]                                   AC B4
cmpx  [a,s]                                  AC F6
cmpx  [a,u]                                  AC D6
cmpx  [a,x]                                  AC 96
cmpx  [a,y]                                  AC B6
cmpx  [b,s]                                  AC F5
cmpx  [b,u]                                  AC D5
cmpx  [b,x]                                  AC 95
cmpx  [b,y]                                  AC B5
cmpx  [d,s]                                  AC FB
cmpx  [d,u]                                  AC DB
cmpx  [d,x]                                  AC 9B
cmpx  [d,y]                                  AC BB
cmpx  []                                     AC 97
cmpx  []                                     AC 9A
cmpx  []                                     AC 9E
cmpx  []                                     AC B7
cmpx  []                                     AC BA
cmpx  []                                     AC BE
cmpx  []                                     AC D7
cmpx  []                                     AC DA
cmpx  []                                     AC DE
cmpx  []                                     AC F7
cmpx  []                                     AC FA
cmpx  []                                     AC FE
cmpy  #$beef                                 10 8C BE EF
cmpy  $01                                    10 9C 01
cmpy  $1,x                                   10 AC 01
cmpy  $beef                                  10 BC BE EF
com   $0,s                                   63 60
com   $0,u                                   63 40
com   $0,x                                   63 00
com   $0,y                                   63 20
com   $01,pc                                 63 8C 01
com   $01,pc                                 63 AC 01
com   $01,pc                                 63 CC 01
com   $01,pc                                 63 EC 01
com   $01,s                                  63 E8 01
com   $01,u                                  63 C8 01
com   $01,x                                  63 88 01
com   $01,y                                  63 A8 01
com   $1,s                                   63 61
com   $1,u                                   63 41
com   $1,x                                   63 01
com   $1,y                                   63 21
com   $2,s                                   63 62
com   $2,u                                   63 42
com   $2,x                                   63 02
com   $2,y                                   63 22
com   $3,s                                   63 63
com   $3,u                                   63 43
com   $3,x                                   63 03
com   $3,y                                   63 23
com   $4,s                                   63 64
com   $4,u                                   63 44
com   $4,x                                   63 04
com   $4,y                                   63 24
com   $5,s                                   63 65
com   $5,u                                   63 45
com   $5,x                                   63 05
com   $5,y                                   63 25
com   $6,s                                   63 66
com   $6,u                                   63 46
com   $6,x                                   63 06
com   $6,y                                   63 26
com   $7,s                                   63 67
com   $7,u                                   63 47
com   $7,x                                   63 07
com   $7,y                                   63 27
com   $8,s                                   63 68
com   $8,u                                   63 48
com   $8,x                                   63 08
com   $8,y                                   63 28
com   $9,s                                   63 69
com   $9,u                                   63 49
com   $9,x                                   63 09
com   $9,y                                   63 29
com   $a,s                                   63 6A
com   $a,u                                   63 4A
com   $a,x                                   63 0A
com   $a,y                                   63 2A
com   $b,s                                   63 6B
com   $b,u                                   63 4B
com   $b,x                                   63 0B
com   $b,y                                   63 2B
com   $beef                                  63 8F BE EF
com   $beef                                  63 AF BE EF
com   $beef                                  63 CF BE EF
com   $beef                                  63 EF BE EF
com   $beef                                  73 BE EF
com   $beef,pc                               63 8D BE EF
com   $beef,pc                               63 AD BE EF
com   $beef,pc                               63 CD BE EF
com   $beef,pc                               63 ED BE EF
com   $beef,s                                63 E9 BE EF
com   $beef,u                                63 C9 BE EF
com   $beef,x                                63 89 BE EF
com   $beef,y                                63 A9 BE EF
com   $c,s                                   63 6C
com   $c,u                                   63 4C
com   $c,x                                   63 0C
com   $c,y                                   63 2C
com   $d,s                                   63 6D
com   $d,u                                   63 4D
com   $d,x                                   63 0D
com   $d,y                                   63 2D
com   $e,s                                   63 6E
com   $e,u                                   63 4E
com   $e,x                                   63 0E
com   $e,y                                   63 2E
com   $f,s                                   63 6F
com   $f,u                                   63 4F
com   $f,x                                   63 0F
com   $f,y                                   63 2F
com   $ff                                    03 FF
com   ,--s                                   63 E3
com   ,--u                                   63 C3
com   ,--x                                   63 83
com   ,--y                                   63 A3
com   ,-s                                    63 E2
com   ,-u                                    63 C2
com   ,-x                                    63 82
com   ,-y                                    63 A2
com   ,s                                     63 E4
com   ,s+                                    63 E0
com   ,s++                                   63 E1
com   ,u                                     63 C4
com   ,u+                                    63 C0
com   ,u++                                   63 C1
com   ,x                                     63 84
com   ,x+                                    63 80
com   ,x++                                   63 81
com   ,y                                     63 A4
com   ,y+                                    63 A0
com   ,y++                                   63 A1
com   -$1,s                                  63 7F
com   -$1,u                                  63 5F
com   -$1,x                                  63 1F
com   -$1,y                                  63 3F
com   -$10,s                                 63 70
com   -$10,u                                 63 50
com   -$10,x                                 63 10
com   -$10,y                                 63 30
com   -$2,s                                  63 7E
com   -$2,u                                  63 5E
com   -$2,x                                  63 1E
com   -$2,y                                  63 3E
com   -$3,s                                  63 7D
com   -$3,u                                  63 5D
com   -$3,x                                  63 1D
com   -$3,y                                  63 3D
com   -$4,s                                  63 7C
com   -$4,u                                  63 5C
com   -$4,x                                  63 1C
com   -$4,y                                  63 3C
com   -$5,s                                  63 7B
com   -$5,u                                  63 5B
com   -$5,x                                  63 1B
com   -$5,y                                  63 3B
com   -$6,s                                  63 7A
com   -$6,u                                  63 5A
com   -$6,x                                  63 1A
com   -$6,y                                  63 3A
com   -$7,s                                  63 79
com   -$7,u                                  63 59
com   -$7,x                                  63 19
com   -$7,y                                  63 39
com   -$8,s                                  63 78
com   -$8,u                                  63 58
com   -$8,x                                  63 18
com   -$8,y                                  63 38
com   -$9,s                                  63 77
com   -$9,u                                  63 57
com   -$9,x                                  63 17
com   -$9,y                                  63 37
com   -$a,s                                  63 76
com   -$a,u                                  63 56
com   -$a,x                                  63 16
com   -$a,y                                  63 36
com   -$b,s                                  63 75
com   -$b,u                                  63 55
com   -$b,x                                  63 15
com   -$b,y                                  63 35
com   -$c,s                                  63 74
com   -$c,u                                  63 54
com   -$c,x                                  63 14
com   -$c,y                                  63 34
com   -$d,s                                  63 73
com   -$d,u                                  63 53
com   -$d,x                                  63 13
com   -$d,y                                  63 33
com   -$e,s                                  63 72
com   -$e,u                                  63 52
com   -$e,x                                  63 12
com   -$e,y                                  63 32
com   -$f,s                                  63 71
com   -$f,u                                  63 51
com   -$f,x                                  63 11
com   -$f,y                                  63 31
com   a,s                                    63 E6
com   a,u                                    63 C6
com   a,x                                    63 86
com   a,y                                    63 A6
com   b,s                                    63 E5
com   b,u                                    63 C5
com   b,x                                    63 85
com   b,y                                    63 A5
com   d,s                                    63 EB
com   d,u                                    63 CB
com   d,x                                    63 8B
com   d,y                                    63 AB
com   [$01,pc]                               63 9C 01
com   [$01,pc]                               63 BC 01
com   [$01,pc]                               63 DC 01
com   [$01,pc]                               63 FC 01
com   [$01,s]                                63 F8 01
com   [$01,u]                                63 D8 01
com   [$01,x]                                63 98 01
com   [$01,y]                                63 B8 01
com   [$beef,pc]                             63 9D BE EF
com   [$beef,pc]                             63 BD BE EF
com   [$beef,pc]                             63 DD BE EF
com   [$beef,pc]                             63 FD BE EF
com   [$beef,s]                              63 F9 BE EF
com   [$beef,u]                              63 D9 BE EF
com   [$beef,x]                              63 99 BE EF
com   [$beef,y]                              63 B9 BE EF
com   [$beef]                                63 9F BE EF
com   [$beef]                                63 BF BE EF
com   [$beef]                                63 DF BE EF
com   [$beef]                                63 FF BE EF
com   [,--s]                                 63 F3
com   [,--u]                                 63 D3
com   [,--x]                                 63 93
com   [,--y]                                 63 B3
com   [,s++]                                 63 F1
com   [,s]                                   63 F4
com   [,u++]                                 63 D1
com   [,u]                                   63 D4
com   [,x++]                                 63 91
com   [,x]                                   63 94
com   [,y++]                                 63 B1
com   [,y]                                   63 B4
com   [a,s]                                  63 F6
com   [a,u]                                  63 D6
com   [a,x]                                  63 96
com   [a,y]                                  63 B6
com   [b,s]                                  63 F5
com   [b,u]                                  63 D5
com   [b,x]                                  63 95
com   [b,y]                                  63 B5
com   [d,s]                                  63 FB
com   [d,u]                                  63 DB
com   [d,x]                                  63 9B
com   [d,y]                                  63 BB
com   []                                     63 97
com   []                                     63 9A
com   []                                     63 9E
com   []                                     63 B7
com   []                                     63 BA
com   []                                     63 BE
com   []                                     63 D7
com   []                                     63 DA
com   []                                     63 DE
com   []                                     63 F7
com   []                                     63 FA
com   []                                     63 FE
coma                                         43
comb                                         53
cwai  #$ff                                   3C FF
daa                                          19
dec   $0,s                                   6A 60
dec   $0,u                                   6A 40
dec   $0,x                                   6A 00
dec   $0,y                                   6A 20
dec   $01,pc                                 6A 8C 01
dec   $01,pc                                 6A AC 01
dec   $01,pc                                 6A CC 01
dec   $01,pc                                 6A EC 01
dec   $01,s                                  6A E8 01
dec   $01,u                                  6A C8 01
dec   $01,x                                  6A 88 01
dec   $01,y                                  6A A8 01
dec   $1,s                                   6A 61
dec   $1,u                                   6A 41
dec   $1,x                                   6A 01
dec   $1,y                                   6A 21
dec   $2,s                                   6A 62
dec   $2,u                                   6A 42
dec   $2,x                                   6A 02
dec   $2,y                                   6A 22
dec   $3,s                                   6A 63
dec   $3,u                                   6A 43
dec   $3,x                                   6A 03
dec   $3,y                                   6A 23
dec   $4,s                                   6A 64
dec   $4,u                                   6A 44
dec   $4,x                                   6A 04
dec   $4,y                                   6A 24
dec   $5,s                                   6A 65
dec   $5,u                                   6A 45
dec   $5,x                                   6A 05
dec   $5,y                                   6A 25
dec   $6,s                                   6A 66
dec   $6,u                                   6A 46
dec   $6,x                                   6A 06
dec   $6,y                                   6A 26
dec   $7,s                                   6A 67
dec   $7,u                                   6A 47
dec   $7,x                                   6A 07
dec   $7,y                                   6A 27
dec   $8,s                                   6A 68
dec   $8,u                                   6A 48
dec   $8,x                                   6A 08
dec   $8,y                                   6A 28
dec   $9,s                                   6A 69
dec   $9,u                                   6A 49
dec   $9,x                                   6A 09
dec   $9,y                                   6A 29
dec   $a,s                                   6A 6A
dec   $a,u                                   6A 4A
dec   $a,x                                   6A 0A
dec   $a,y                                   6A 2A
dec   $b,s                                   6A 6B
dec   $b,u                                   6A 4B
dec   $b,x                                   6A 0B
dec   $b,y                                   6A 2B
dec   $beef                                  6A 8F BE EF
dec   $beef                                  6A AF BE EF
dec   $beef                                  6A CF BE EF
dec   $beef                                  6A EF BE EF
dec   $beef                                  7A BE EF
dec   $beef,pc                               6A 8D BE EF
dec   $beef,pc                               6A AD BE EF
dec   $beef,pc                               6A CD BE EF
dec   $beef,pc                               6A ED BE EF
dec   $beef,s                                6A E9 BE EF
dec   $beef,u                                6A C9 BE EF
dec   $beef,x                                6A 89 BE EF
dec   $beef,y                                6A A9 BE EF
dec   $c,s                                   6A 6C
dec   $c,u                                   6A 4C
dec   $c,x                                   6A 0C
dec   $c,y                                   6A 2C
dec   $d,s                                   6A 6D
dec   $d,u                                   6A 4D
dec   $d,x                                   6A 0D
dec   $d,y                                   6A 2D
dec   $e,s                                   6A 6E
dec   $e,u                                   6A 4E
dec   $e,x                                   6A 0E
dec   $e,y                                   6A 2E
dec   $f,s                                   6A 6F
dec   $f,u                                   6A 4F
dec   $f,x                                   6A 0F
dec   $f,y                                   6A 2F
dec   $ff                                    0A FF
dec   ,--s                                   6A E3
dec   ,--u                                   6A C3
dec   ,--x                                   6A 83
dec   ,--y                                   6A A3
dec   ,-s                                    6A E2
dec   ,-u                                    6A C2
dec   ,-x                                    6A 82
dec   ,-y                                    6A A2
dec   ,s                                     6A E4
dec   ,s+                                    6A E0
dec   ,s++                                   6A E1
dec   ,u                                     6A C4
dec   ,u+                                    6A C0
dec   ,u++                                   6A C1
dec   ,x                                     6A 84
dec   ,x+                                    6A 80
dec   ,x++                                   6A 81
dec   ,y                                     6A A4
dec   ,y+                                    6A A0
dec   ,y++                                   6A A1
dec   -$1,s                                  6A 7F
dec   -$1,u                                  6A 5F
dec   -$1,x                                  6A 1F
dec   -$1,y                                  6A 3F
dec   -$10,s                                 6A 70
dec   -$10,u                                 6A 50
dec   -$10,x                                 6A 10
dec   -$10,y                                 6A 30
dec   -$2,s                                  6A 7E
dec   -$2,u                                  6A 5E
dec   -$2,x                                  6A 1E
dec   -$2,y                                  6A 3E
dec   -$3,s                                  6A 7D
dec   -$3,u                                  6A 5D
dec   -$3,x                                  6A 1D
dec   -$3,y                                  6A 3D
dec   -$4,s                                  6A 7C
dec   -$4,u                                  6A 5C
dec   -$4,x                                  6A 1C
dec   -$4,y                                  6A 3C
dec   -$5,s                                  6A 7B
dec   -$5,u                                  6A 5B
dec   -$5,x                                  6A 1B
dec   -$5,y                                  6A 3B
dec   -$6,s                                  6A 7A
dec   -$6,u                                  6A 5A
dec   -$6,x                                  6A 1A
dec   -$6,y                                  6A 3A
dec   -$7,s                                  6A 79
dec   -$7,u                                  6A 59
dec   -$7,x                                  6A 19
dec   -$7,y                                  6A 39
dec   -$8,s                                  6A 78
dec   -$8,u                                  6A 58
dec   -$8,x                                  6A 18
dec   -$8,y                                  6A 38
dec   -$9,s                                  6A 77
dec   -$9,u                                  6A 57
dec   -$9,x                                  6A 17
dec   -$9,y                                  6A 37
dec   -$a,s                                  6A 76
dec   -$a,u                                  6A 56
dec   -$a,x                                  6A 16
dec   -$a,y                                  6A 36
dec   -$b,s                                  6A 75
dec   -$b,u                                  6A 55
dec   -$b,x                                  6A 15
dec   -$b,y                                  6A 35
dec   -$c,s                                  6A 74
dec   -$c,u                                  6A 54
dec   -$c,x                                  6A 14
dec   -$c,y                                  6A 34
dec   -$d,s                                  6A 73
dec   -$d,u                                  6A 53
dec   -$d,x                                  6A 13
dec   -$d,y                                  6A 33
dec   -$e,s                                  6A 72
dec   -$e,u                                  6A 52
dec   -$e,x                                  6A 12
dec   -$e,y                                  6A 32
dec   -$f,s                                  6A 71
dec   -$f,u                                  6A 51
dec   -$f,x                                  6A 11
dec   -$f,y                                  6A 31
dec   a,s                                    6A E6
dec   a,u                                    6A C6
dec   a,x                                    6A 86
dec   a,y                                    6A A6
dec   b,s                                    6A E5
dec   b,u                                    6A C5
dec   b,x                                    6A 85
dec   b,y                                    6A A5
dec   d,s                                    6A EB
dec   d,u                                    6A CB
dec   d,x                                    6A 8B
dec   d,y                                    6A AB
dec   [$01,pc]                               6A 9C 01
dec   [$01,pc]                               6A BC 01
dec   [$01,pc]                               6A DC 01
dec   [$01,pc]                               6A FC 01
dec   [$01,s]                                6A F8 01
dec   [$01,u]                                6A D8 01
dec   [$01,x]                                6A 98 01
dec   [$01,y]                                6A B8 01
dec   [$beef,pc]                             6A 9D BE EF
dec   [$beef,pc]                             6A BD BE EF
dec   [$beef,pc]                             6A DD BE EF
dec   [$beef,pc]                             6A FD BE EF
dec   [$beef,s]                              6A F9 BE EF
dec   [$beef,u]                              6A D9 BE EF
dec   [$beef,x]                              6A 99 BE EF
dec   [$beef,y]                              6A B9 BE EF
dec   [$beef]                                6A 9F BE EF
dec   [$beef]                                6A BF BE EF
dec   [$beef]                                6A DF BE EF
dec   [$beef]                                6A FF BE EF
dec   [,--s]                                 6A F3
dec   [,--u]                                 6A D3
dec   [,--x]                                 6A 93
dec   [,--y]                                 6A B3
dec   [,s++]                                 6A F1
dec   [,s]                                   6A F4
dec   [,u++]                                 6A D1
dec   [,u]                                   6A D4
dec   [,x++]                                 6A 91
dec   [,x]                                   6A 94
dec   [,y++]                                 6A B1
dec   [,y]                                   6A B4
dec   [a,s]                                  6A F6
dec   [a,u]                                  6A D6
dec   [a,x]                                  6A 96
dec   [a,y]                                  6A B6
dec   [b,s]                                  6A F5
dec   [b,u]                                  6A D5
dec   [b,x]                                  6A 95
dec   [b,y]                                  6A B5
dec   [d,s]                                  6A FB
dec   [d,u]                                  6A DB
dec   [d,x]                                  6A 9B
dec   [d,y]                                  6A BB
dec   []                                     6A 97
dec   []                                     6A 9A
dec   []                                     6A 9E
dec   []                                     6A B7
dec   []                                     6A BA
dec   []                                     6A BE
dec   []                                     6A D7
dec   []                                     6A DA
dec   []                                     6A DE
dec   []                                     6A F7
dec   []                                     6A FA
dec   []                                     6A FE
deca                                         4A
decb                                         5A
eora  $0,s                                   A8 60
eora  $0,u                                   A8 40
eora  $0,x                                   A8 00
eora  $0,y                                   A8 20
eora  $01,pc                                 A8 8C 01
eora  $01,pc                                 A8 AC 01
eora  $01,pc                                 A8 CC 01
eora  $01,pc                                 A8 EC 01
eora  $01,s                                  A8 E8 01
eora  $01,u                                  A8 C8 01
eora  $01,x                                  A8 88 01
eora  $01,y                                  A8 A8 01
eora  $1,s                                   A8 61
eora  $1,u                                   A8 41
eora  $1,x                                   A8 01
eora  $1,y                                   A8 21
eora  $2,s                                   A8 62
eora  $2,u                                   A8 42
eora  $2,x                                   A8 02
eora  $2,y                                   A8 22
eora  $3,s                                   A8 63
eora  $3,u                                   A8 43
eora  $3,x                                   A8 03
eora  $3,y                                   A8 23
eora  $4,s                                   A8 64
eora  $4,u                                   A8 44
eora  $4,x                                   A8 04
eora  $4,y                                   A8 24
eora  $5,s                                   A8 65
eora  $5,u                                   A8 45
eora  $5,x                                   A8 05
eora  $5,y                                   A8 25
eora  $6,s                                   A8 66
eora  $6,u                                   A8 46
eora  $6,x                                   A8 06
eora  $6,y                                   A8 26
eora  $7,s                                   A8 67
eora  $7,u                                   A8 47
eora  $7,x                                   A8 07
eora  $7,y                                   A8 27
eora  $8,s                                   A8 68
eora  $8,u                                   A8 48
eora  $8,x                                   A8 08
eora  $8,y                                   A8 28
eora  $9,s                                   A8 69
eora  $9,u                                   A8 49
eora  $9,x                                   A8 09
eora  $9,y                                   A8 29
eora  $a,s                                   A8 6A
eora  $a,u                                   A8 4A
eora  $a,x                                   A8 0A
eora  $a,y                                   A8 2A
eora  $b,s                                   A8 6B
eora  $b,u                                   A8 4B
eora  $b,x                                   A8 0B
eora  $b,y                                   A8 2B
eora  $beef                                  A8 8F BE EF
eora  $beef                                  A8 AF BE EF
eora  $beef                                  A8 CF BE EF
eora  $beef                                  A8 EF BE EF
eora  $beef                                  B8 BE EF
eora  $beef,pc                               A8 8D BE EF
eora  $beef,pc                               A8 AD BE EF
eora  $beef,pc                               A8 CD BE EF
eora  $beef,pc                               A8 ED BE EF
eora  $beef,s                                A8 E9 BE EF
eora  $beef,u                                A8 C9 BE EF
eora  $beef,x                                A8 89 BE EF
eora  $beef,y                                A8 A9 BE EF
eora  $c,s                                   A8 6C
eora  $c,u                                   A8 4C
eora  $c,x                                   A8 0C
eora  $c,y                                   A8 2C
eora  $d,s                                   A8 6D
eora  $d,u                                   A8 4D
eora  $d,x                                   A8 0D
eora  $d,y                                   A8 2D
eora  $e,s                                   A8 6E
eora  $e,u                                   A8 4E
eora  $e,x                                   A8 0E
eora  $e,y                                   A8 2E
eora  $f,s                                   A8 6F
eora  $f,u                                   A8 4F
eora  $f,x                                   A8 0F
eora  $f,y                                   A8 2F
eora  $ff                                    98 FF
eora  ,--s                                   A8 E3
eora  ,--u                                   A8 C3
eora  ,--x                                   A8 83
eora  ,--y                                   A8 A3
eora  ,-s                                    A8 E2
eora  ,-u                                    A8 C2
eora  ,-x                                    A8 82
eora  ,-y                                    A8 A2
eora  ,s                                     A8 E4
eora  ,s+                                    A8 E0
eora  ,s++                                   A8 E1
eora  ,u                                     A8 C4
eora  ,u+                                    A8 C0
eora  ,u++                                   A8 C1
eora  ,x                                     A8 84
eora  ,x+                                    A8 80
eora  ,x++                                   A8 81
eora  ,y                                     A8 A4
eora  ,y+                                    A8 A0
eora  ,y++                                   A8 A1
eora  -$1,s                                  A8 7F
eora  -$1,u                                  A8 5F
eora  -$1,x                                  A8 1F
eora  -$1,y                                  A8 3F
eora  -$10,s                                 A8 70
eora  -$10,u                                 A8 50
eora  -$10,x                                 A8 10
eora  -$10,y                                 A8 30
eora  -$2,s                                  A8 7E
eora  -$2,u                                  A8 5E
eora  -$2,x                                  A8 1E
eora  -$2,y                                  A8 3E
eora  -$3,s                                  A8 7D
eora  -$3,u                                  A8 5D
eora  -$3,x                                  A8 1D
eora  -$3,y                                  A8 3D
eora  -$4,s                                  A8 7C
eora  -$4,u                                  A8 5C
eora  -$4,x                                  A8 1C
eora  -$4,y                                  A8 3C
eora  -$5,s                                  A8 7B
eora  -$5,u                                  A8 5B
eora  -$5,x                                  A8 1B
eora  -$5,y                                  A8 3B
eora  -$6,s                                  A8 7A
eora  -$6,u                                  A8 5A
eora  -$6,x                                  A8 1A
eora  -$6,y                                  A8 3A
eora  -$7,s                                  A8 79
eora  -$7,u                                  A8 59
eora  -$7,x                                  A8 19
eora  -$7,y                                  A8 39
eora  -$8,s                                  A8 78
eora  -$8,u                                  A8 58
eora  -$8,x                                  A8 18
eora  -$8,y                                  A8 38
eora  -$9,s                                  A8 77
eora  -$9,u                                  A8 57
eora  -$9,x                                  A8 17
eora  -$9,y                                  A8 37
eora  -$a,s                                  A8 76
eora  -$a,u                                  A8 56
eora  -$a,x                                  A8 16
eora  -$a,y                                  A8 36
eora  -$b,s                                  A8 75
eora  -$b,u                                  A8 55
eora  -$b,x                                  A8 15
eora  -$b,y                                  A8 35
eora  -$c,s                                  A8 74
eora  -$c,u                                  A8 54
eora  -$c,x                                  A8 14
eora  -$c,y                                  A8 34
eora  -$d,s                                  A8 73
eora  -$d,u                                  A8 53
eora  -$d,x                                  A8 13
eora  -$d,y                                  A8 33
eora  -$e,s                                  A8 72
eora  -$e,u                                  A8 52
eora  -$e,x                                  A8 12
eora  -$e,y                                  A8 32
eora  -$f,s                                  A8 71
eora  -$f,u                                  A8 51
eora  -$f,x                                  A8 11
eora  -$f,y                                  A8 31
eora  a,s                                    A8 E6
eora  a,u                                    A8 C6
eora  a,x                                    A8 86
eora  a,y                                    A8 A6
eora  b,s                                    A8 E5
eora  b,u                                    A8 C5
eora  b,x                                    A8 85
eora  b,y                                    A8 A5
eora  d,s                                    A8 EB
eora  d,u                                    A8 CB
eora  d,x                                    A8 8B
eora  d,y                                    A8 AB
eora  [$01,pc]                               A8 9C 01
eora  [$01,pc]                               A8 BC 01
eora  [$01,pc]                               A8 DC 01
eora  [$01,pc]                               A8 FC 01
eora  [$01,s]                                A8 F8 01
eora  [$01,u]                                A8 D8 01
eora  [$01,x]                                A8 98 01
eora  [$01,y]                                A8 B8 01
eora  [$beef,pc]                             A8 9D BE EF
eora  [$beef,pc]                             A8 BD BE EF
eora  [$beef,pc]                             A8 DD BE EF
eora  [$beef,pc]                             A8 FD BE EF
eora  [$beef,s]                              A8 F9 BE EF
eora  [$beef,u]                              A8 D9 BE EF
eora  [$beef,x]                              A8 99 BE EF
eora  [$beef,y]                              A8 B9 BE EF
eora  [$beef]                                A8 9F BE EF
eora  [$beef]                                A8 BF BE EF
eora  [$beef]                                A8 DF BE EF
eora  [$beef]                                A8 FF BE EF
eora  [,--s]                                 A8 F3
eora  [,--u]                                 A8 D3
eora  [,--x]                                 A8 93
eora  [,--y]                                 A8 B3
eora  [,s++]                                 A8 F1
eora  [,s]                                   A8 F4
eora  [,u++]                                 A8 D1
eora  [,u]                                   A8 D4
eora  [,x++]                                 A8 91
eora  [,x]                                   A8 94
eora  [,y++]                                 A8 B1
eora  [,y]                                   A8 B4
eora  [a,s]                                  A8 F6
eora  [a,u]                                  A8 D6
eora  [a,x]                                  A8 96
eora  [a,y]                                  A8 B6
eora  [b,s]                                  A8 F5
eora  [b,u]                                  A8 D5
eora  [b,x]                                  A8 95
eora  [b,y]                                  A8 B5
eora  [d,s]                                  A8 FB
eora  [d,u]                                  A8 DB
eora  [d,x]                                  A8 9B
eora  [d,y]                                  A8 BB
eora  []                                     A8 97
eora  []                                     A8 9A
eora  []                                     A8 9E
eora  []                                     A8 B7
eora  []                                     A8 BA
eora  []                                     A8 BE
eora  []                                     A8 D7
eora  []                                     A8 DA
eora  []                                     A8 DE
eora  []                                     A8 F7
eora  []                                     A8 FA
eora  []                                     A8 FE
eorb  #$ff                                   C8 FF
eorb  $0,s                                   E8 60
eorb  $0,u                                   E8 40
eorb  $0,x                                   E8 00
eorb  $0,y                                   E8 20
eorb  $01,pc                                 E8 8C 01
eorb  $01,pc                                 E8 AC 01
eorb  $01,pc                                 E8 CC 01
eorb  $01,pc                                 E8 EC 01
eorb  $01,s                                  E8 E8 01
eorb  $01,u                                  E8 C8 01
eorb  $01,x                                  E8 88 01
eorb  $01,y                                  E8 A8 01
eorb  $1,s                                   E8 61
eorb  $1,u                                   E8 41
eorb  $1,x                                   E8 01
eorb  $1,y                                   E8 21
eorb  $2,s                                   E8 62
eorb  $2,u                                   E8 42
eorb  $2,x                                   E8 02
eorb  $2,y                                   E8 22
eorb  $3,s                                   E8 63
eorb  $3,u                                   E8 43
eorb  $3,x                                   E8 03
eorb  $3,y                                   E8 23
eorb  $4,s                                   E8 64
eorb  $4,u                                   E8 44
eorb  $4,x                                   E8 04
eorb  $4,y                                   E8 24
eorb  $5,s                                   E8 65
eorb  $5,u                                   E8 45
eorb  $5,x                                   E8 05
eorb  $5,y                                   E8 25
eorb  $6,s                                   E8 66
eorb  $6,u                                   E8 46
eorb  $6,x                                   E8 06
eorb  $6,y                                   E8 26
eorb  $7,s                                   E8 67
eorb  $7,u                                   E8 47
eorb  $7,x                                   E8 07
eorb  $7,y                                   E8 27
eorb  $8,s                                   E8 68
eorb  $8,u                                   E8 48
eorb  $8,x                                   E8 08
eorb  $8,y                                   E8 28
eorb  $9,s                                   E8 69
eorb  $9,u                                   E8 49
eorb  $9,x                                   E8 09
eorb  $9,y                                   E8 29
eorb  $a,s                                   E8 6A
eorb  $a,u                                   E8 4A
eorb  $a,x                                   E8 0A
eorb  $a,y                                   E8 2A
eorb  $b,s                                   E8 6B
eorb  $b,u                                   E8 4B
eorb  $b,x                                   E8 0B
eorb  $b,y                                   E8 2B
eorb  $beef                                  E8 8F BE EF
eorb  $beef                                  E8 AF BE EF
eorb  $beef                                  E8 CF BE EF
eorb  $beef                                  E8 EF BE EF
eorb  $beef                                  F8 BE EF
eorb  $beef,pc                               E8 8D BE EF
eorb  $beef,pc                               E8 AD BE EF
eorb  $beef,pc                               E8 CD BE EF
eorb  $beef,pc                               E8 ED BE EF
eorb  $beef,s                                E8 E9 BE EF
eorb  $beef,u                                E8 C9 BE EF
eorb  $beef,x                                E8 89 BE EF
eorb  $beef,y                                E8 A9 BE EF
eorb  $c,s                                   E8 6C
eorb  $c,u                                   E8 4C
eorb  $c,x                                   E8 0C
eorb  $c,y                                   E8 2C
eorb  $d,s                                   E8 6D
eorb  $d,u                                   E8 4D
eorb  $d,x                                   E8 0D
eorb  $d,y                                   E8 2D
eorb  $e,s                                   E8 6E
eorb  $e,u                                   E8 4E
eorb  $e,x                                   E8 0E
eorb  $e,y                                   E8 2E
eorb  $f,s                                   E8 6F
eorb  $f,u                                   E8 4F
eorb  $f,x                                   E8 0F
eorb  $f,y                                   E8 2F
eorb  $ff                                    D8 FF
eorb  ,--s                                   E8 E3
eorb  ,--u                                   E8 C3
eorb  ,--x                                   E8 83
eorb  ,--y                                   E8 A3
eorb  ,-s                                    E8 E2
eorb  ,-u                                    E8 C2
eorb  ,-x                                    E8 82
eorb  ,-y                                    E8 A2
eorb  ,s                                     E8 E4
eorb  ,s+                                    E8 E0
eorb  ,s++                                   E8 E1
eorb  ,u                                     E8 C4
eorb  ,u+                                    E8 C0
eorb  ,u++                                   E8 C1
eorb  ,x                                     E8 84
eorb  ,x+                                    E8 80
eorb  ,x++                                   E8 81
eorb  ,y                                     E8 A4
eorb  ,y+                                    E8 A0
eorb  ,y++                                   E8 A1
eorb  -$1,s                                  E8 7F
eorb  -$1,u                                  E8 5F
eorb  -$1,x                                  E8 1F
eorb  -$1,y                                  E8 3F
eorb  -$10,s                                 E8 70
eorb  -$10,u                                 E8 50
eorb  -$10,x                                 E8 10
eorb  -$10,y                                 E8 30
eorb  -$2,s                                  E8 7E
eorb  -$2,u                                  E8 5E
eorb  -$2,x                                  E8 1E
eorb  -$2,y                                  E8 3E
eorb  -$3,s                                  E8 7D
eorb  -$3,u                                  E8 5D
eorb  -$3,x                                  E8 1D
eorb  -$3,y                                  E8 3D
eorb  -$4,s                                  E8 7C
eorb  -$4,u                                  E8 5C
eorb  -$4,x                                  E8 1C
eorb  -$4,y                                  E8 3C
eorb  -$5,s                                  E8 7B
eorb  -$5,u                                  E8 5B
eorb  -$5,x                                  E8 1B
eorb  -$5,y                                  E8 3B
eorb  -$6,s                                  E8 7A
eorb  -$6,u                                  E8 5A
eorb  -$6,x                                  E8 1A
eorb  -$6,y                                  E8 3A
eorb  -$7,s                                  E8 79
eorb  -$7,u                                  E8 59
eorb  -$7,x                                  E8 19
eorb  -$7,y                                  E8 39
eorb  -$8,s                                  E8 78
eorb  -$8,u                                  E8 58
eorb  -$8,x                                  E8 18
eorb  -$8,y                                  E8 38
eorb  -$9,s                                  E8 77
eorb  -$9,u                                  E8 57
eorb  -$9,x                                  E8 17
eorb  -$9,y                                  E8 37
eorb  -$a,s                                  E8 76
eorb  -$a,u                                  E8 56
eorb  -$a,x                                  E8 16
eorb  -$a,y                                  E8 36
eorb  -$b,s                                  E8 75
eorb  -$b,u                                  E8 55
eorb  -$b,x                                  E8 15
eorb  -$b,y                                  E8 35
eorb  -$c,s                                  E8 74
eorb  -$c,u                                  E8 54
eorb  -$c,x                                  E8 14
eorb  -$c,y                                  E8 34
eorb  -$d,s                                  E8 73
eorb  -$d,u                                  E8 53
eorb  -$d,x                                  E8 13
eorb  -$d,y                                  E8 33
eorb  -$e,s                                  E8 72
eorb  -$e,u                                  E8 52
eorb  -$e,x                                  E8 12
eorb  -$e,y                                  E8 32
eorb  -$f,s                                  E8 71
eorb  -$f,u                                  E8 51
eorb  -$f,x                                  E8 11
eorb  -$f,y                                  E8 31
eorb  a,s                                    E8 E6
eorb  a,u                                    E8 C6
eorb  a,x                                    E8 86
eorb  a,y                                    E8 A6
eorb  b,s                                    E8 E5
eorb  b,u                                    E8 C5
eorb  b,x                                    E8 85
eorb  b,y                                    E8 A5
eorb  d,s                                    E8 EB
eorb  d,u                                    E8 CB
eorb  d,x                                    E8 8B
eorb  d,y                                    E8 AB
eorb  [$01,pc]                               E8 9C 01
eorb  [$01,pc]                               E8 BC 01
eorb  [$01,pc]                               E8 DC 01
eorb  [$01,pc]                               E8 FC 01
eorb  [$01,s]                                E8 F8 01
eorb  [$01,u]                                E8 D8 01
eorb  [$01,x]                                E8 98 01
eorb  [$01,y]                                E8 B8 01
eorb  [$beef,pc]                             E8 9D BE EF
eorb  [$beef,pc]                             E8 BD BE EF
eorb  [$beef,pc]                             E8 DD BE EF
eorb  [$beef,pc]                             E8 FD BE EF
eorb  [$beef,s]                              E8 F9 BE EF
eorb  [$beef,u]                              E8 D9 BE EF
eorb  [$beef,x]                              E8 99 BE EF
eorb  [$beef,y]                              E8 B9 BE EF
eorb  [$beef]                                E8 9F BE EF
eorb  [$beef]                                E8 BF BE EF
eorb  [$beef]                                E8 DF BE EF
eorb  [$beef]                                E8 FF BE EF
eorb  [,--s]                                 E8 F3
eorb  [,--u]                                 E8 D3
eorb  [,--x]                                 E8 93
eorb  [,--y]                                 E8 B3
eorb  [,s++]                                 E8 F1
eorb  [,s]                                   E8 F4
eorb  [,u++]                                 E8 D1
eorb  [,u]                                   E8 D4
eorb  [,x++]                                 E8 91
eorb  [,x]                                   E8 94
eorb  [,y++]                                 E8 B1
eorb  [,y]                                   E8 B4
eorb  [a,s]                                  E8 F6
eorb  [a,u]                                  E8 D6
eorb  [a,x]                                  E8 96
eorb  [a,y]                                  E8 B6
eorb  [b,s]                                  E8 F5
eorb  [b,u]                                  E8 D5
eorb  [b,x]                                  E8 95
eorb  [b,y]                                  E8 B5
eorb  [d,s]                                  E8 FB
eorb  [d,u]                                  E8 DB
eorb  [d,x]                                  E8 9B
eorb  [d,y]                                  E8 BB
eorb  []                                     E8 97
eorb  []                                     E8 9A
eorb  []                                     E8 9E
eorb  []                                     E8 B7
eorb  []                                     E8 BA
eorb  []                                     E8 BE
eorb  []                                     E8 D7
eorb  []                                     E8 DA
eorb  []                                     E8 DE
eorb  []                                     E8 F7
eorb  []                                     E8 FA
eorb  []                                     E8 FE
exg   a,a                                    1E 88
exg   a,b                                    1E 89
exg   a,cc                                   1E 8A
exg   a,d                                    1E 80
exg   a,dp                                   1E 8B
exg   a,inv                                  1E 86
exg   a,inv                                  1E 87
exg   a,inv                                  1E 8C
exg   a,inv                                  1E 8D
exg   a,inv                                  1E 8E
exg   a,inv                                  1E 8F
exg   a,pc                                   1E 85
exg   a,s                                    1E 84
exg   a,u                                    1E 83
exg   a,x                                    1E 81
exg   a,y                                    1E 82
exg   b,a                                    1E 98
exg   b,b                                    1E 99
exg   b,cc                                   1E 9A
exg   b,d                                    1E 90
exg   b,dp                                   1E 9B
exg   b,inv                                  1E 96
exg   b,inv                                  1E 97
exg   b,inv                                  1E 9C
exg   b,inv                                  1E 9D
exg   b,inv                                  1E 9E
exg   b,inv                                  1E 9F
exg   b,pc                                   1E 95
exg   b,s                                    1E 94
exg   b,u                                    1E 93
exg   b,x                                    1E 91
exg   b,y                                    1E 92
exg   cc,a                                   1E A8
exg   cc,b                                   1E A9
exg   cc,cc                                  1E AA
exg   cc,d                                   1E A0
exg   cc,dp                                  1E AB
exg   cc,inv                                 1E A6
exg   cc,inv                                 1E A7
exg   cc,inv                                 1E AC
exg   cc,inv                                 1E AD
exg   cc,inv                                 1E AE
exg   cc,inv                                 1E AF
exg   cc,pc                                  1E A5
exg   cc,s                                   1E A4
exg   cc,u                                   1E A3
exg   cc,x                                   1E A1
exg   cc,y                                   1E A2
exg   d,a                                    1E 08
exg   d,b                                    1E 09
exg   d,cc                                   1E 0A
exg   d,d                                    1E 00
exg   d,dp                                   1E 0B
exg   d,inv                                  1E 06
exg   d,inv                                  1E 07
exg   d,inv                                  1E 0C
exg   d,inv                                  1E 0D
exg   d,inv                                  1E 0E
exg   d,inv                                  1E 0F
exg   d,pc                                   1E 05
exg   d,s                                    1E 04
exg   d,u                                    1E 03
exg   d,x                                    1E 01
exg   d,y                                    1E 02
exg   dp,a                                   1E B8
exg   dp,b                                   1E B9
exg   dp,cc                                  1E BA
exg   dp,d                                   1E B0
exg   dp,dp                                  1E BB
exg   dp,inv                                 1E B6
exg   dp,inv                                 1E B7
exg   dp,inv                                 1E BC
exg   dp,inv                                 1E BD
exg   dp,inv                                 1E BE
exg   dp,inv                                 1E BF
exg   dp,pc                                  1E B5
exg   dp,s                                   1E B4
exg   dp,u                                   1E B3
exg   dp,x                                   1E B1
exg   dp,y                                   1E B2
exg   inv,a                                  1E 68
exg   inv,a                                  1E 78
exg   inv,a                                  1E C8
exg   inv,a                                  1E D8
exg   inv,a                                  1E E8
exg   inv,a                                  1E F8
exg   inv,b                                  1E 69
exg   inv,b                                  1E 79
exg   inv,b                                  1E C9
exg   inv,b                                  1E D9
exg   inv,b                                  1E E9
exg   inv,b                                  1E F9
exg   inv,cc                                 1E 6A
exg   inv,cc                                 1E 7A
exg   inv,cc                                 1E CA
exg   inv,cc                                 1E DA
exg   inv,cc                                 1E EA
exg   inv,cc                                 1E FA
exg   inv,d                                  1E 60
exg   inv,d                                  1E 70
exg   inv,d                                  1E C0
exg   inv,d                                  1E D0
exg   inv,d                                  1E E0
exg   inv,d                                  1E F0
exg   inv,dp                                 1E 6B
exg   inv,dp                                 1E 7B
exg   inv,dp                                 1E CB
exg   inv,dp                                 1E DB
exg   inv,dp                                 1E EB
exg   inv,dp                                 1E FB
exg   inv,inv                                1E 66
exg   inv,inv                                1E 67
exg   inv,inv                                1E 6C
exg   inv,inv                                1E 6D
exg   inv,inv                                1E 6E
exg   inv,inv                                1E 6F
exg   inv,inv                                1E 76
exg   inv,inv                                1E 77
exg   inv,inv                                1E 7C
exg   inv,inv                                1E 7D
exg   inv,inv                                1E 7E
exg   inv,inv                                1E 7F
exg   inv,inv                                1E C6
exg   inv,inv                                1E C7
exg   inv,inv                                1E CC
exg   inv,inv                                1E CD
exg   inv,inv                                1E CE
exg   inv,inv                                1E CF
exg   inv,inv                                1E D6
exg   inv,inv                                1E D7
exg   inv,inv                                1E DC
exg   inv,inv                                1E DD
exg   inv,inv                                1E DE
exg   inv,inv                                1E DF
exg   inv,inv                                1E E6
exg   inv,inv                                1E E7
exg   inv,inv                                1E EC
exg   inv,inv                                1E ED
exg   inv,inv                                1E EE
exg   inv,inv                                1E EF
exg   inv,inv                                1E F6
exg   inv,inv                                1E F7
exg   inv,inv                                1E FC
exg   inv,inv                                1E FD
exg   inv,inv                                1E FE
exg   inv,inv                                1E FF
exg   inv,pc                                 1E 65
exg   inv,pc                                 1E 75
exg   inv,pc                                 1E C5
exg   inv,pc                                 1E D5
exg   inv,pc                                 1E E5
exg   inv,pc                                 1E F5
exg   inv,s                                  1E 64
exg   inv,s                                  1E 74
exg   inv,s                                  1E C4
exg   inv,s                                  1E D4
exg   inv,s                                  1E E4
exg   inv,s                                  1E F4
exg   inv,u                                  1E 63
exg   inv,u                                  1E 73
exg   inv,u                                  1E C3
exg   inv,u                                  1E D3
exg   inv,u                                  1E E3
exg   inv,u                                  1E F3
exg   inv,x                                  1E 61
exg   inv,x                                  1E 71
exg   inv,x                                  1E C1
exg   inv,x                                  1E D1
exg   inv,x                                  1E E1
exg   inv,x                                  1E F1
exg   inv,y                                  1E 62
exg   inv,y                                  1E 72
exg   inv,y                                  1E C2
exg   inv,y                                  1E D2
exg   inv,y                                  1E E2
exg   inv,y                                  1E F2
exg   pc,a                                   1E 58
exg   pc,b                                   1E 59
exg   pc,cc                                  1E 5A
exg   pc,d                                   1E 50
exg   pc,dp                                  1E 5B
exg   pc,inv                                 1E 56
exg   pc,inv                                 1E 57
exg   pc,inv                                 1E 5C
exg   pc,inv                                 1E 5D
exg   pc,inv                                 1E 5E
exg   pc,inv                                 1E 5F
exg   pc,pc                                  1E 55
exg   pc,s                                   1E 54
exg   pc,u                                   1E 53
exg   pc,x                                   1E 51
exg   pc,y                                   1E 52
exg   s,a                                    1E 48
exg   s,b                                    1E 49
exg   s,cc                                   1E 4A
exg   s,d                                    1E 40
exg   s,dp                                   1E 4B
exg   s,inv                                  1E 46
exg   s,inv                                  1E 47
exg   s,inv                                  1E 4C
exg   s,inv                                  1E 4D
exg   s,inv                                  1E 4E
exg   s,inv                                  1E 4F
exg   s,pc                                   1E 45
exg   s,s                                    1E 44
exg   s,u                                    1E 43
exg   s,x                                    1E 41
exg   s,y                                    1E 42
exg   u,a                                    1E 38
exg   u,b                                    1E 39
exg   u,cc                                   1E 3A
exg   u,d                                    1E 30
exg   u,dp                                   1E 3B
exg   u,inv                                  1E 36
exg   u,inv                                  1E 37
exg   u,inv                                  1E 3C
exg   u,inv                                  1E 3D
exg   u,inv                                  1E 3E
exg   u,inv                                  1E 3F
exg   u,pc                                   1E 35
exg   u,s                                    1E 34
exg   u,u                                    1E 33
exg   u,x                                    1E 31
exg   u,y                                    1E 32
exg   x,a                                    1E 18
exg   x,b                                    1E 19
exg   x,cc                                   1E 1A
exg   x,d                                    1E 10
exg   x,dp                                   1E 1B
exg   x,inv                                  1E 16
exg   x,inv                                  1E 17
exg   x,inv                                  1E 1C
exg   x,inv                                  1E 1D
exg   x,inv                                  1E 1E
exg   x,inv                                  1E 1F
exg   x,pc                                   1E 15
exg   x,s                                    1E 14
exg   x,u                                    1E 13
exg   x,x                                    1E 11
exg   x,y                                    1E 12
exg   y,a                                    1E 28
exg   y,b                                    1E 29
exg   y,cc                                   1E 2A
exg   y,d                                    1E 20
exg   y,dp                                   1E 2B
exg   y,inv                                  1E 26
exg   y,inv                                  1E 27
exg   y,inv                                  1E 2C
exg   y,inv                                  1E 2D
exg   y,inv                                  1E 2E
exg   y,inv                                  1E 2F
exg   y,pc                                   1E 25
exg   y,s                                    1E 24
exg   y,u                                    1E 23
exg   y,x                                    1E 21
exg   y,y                                    1E 22
inc   $0,s                                   6C 60
inc   $0,u                                   6C 40
inc   $0,x                                   6C 00
inc   $0,y                                   6C 20
inc   $01,pc                                 6C 8C 01
inc   $01,pc                                 6C AC 01
inc   $01,pc                                 6C CC 01
inc   $01,pc                                 6C EC 01
inc   $01,s                                  6C E8 01
inc   $01,u                                  6C C8 01
inc   $01,x                                  6C 88 01
inc   $01,y                                  6C A8 01
inc   $1,s                                   6C 61
inc   $1,u                                   6C 41
inc   $1,x                                   6C 01
inc   $1,y                                   6C 21
inc   $2,s                                   6C 62
inc   $2,u                                   6C 42
inc   $2,x                                   6C 02
inc   $2,y                                   6C 22
inc   $3,s                                   6C 63
inc   $3,u                                   6C 43
inc   $3,x                                   6C 03
inc   $3,y                                   6C 23
inc   $4,s                                   6C 64
inc   $4,u                                   6C 44
inc   $4,x                                   6C 04
inc   $4,y                                   6C 24
inc   $5,s                                   6C 65
inc   $5,u                                   6C 45
inc   $5,x                                   6C 05
inc   $5,y                                   6C 25
inc   $6,s                                   6C 66
inc   $6,u                                   6C 46
inc   $6,x                                   6C 06
inc   $6,y                                   6C 26
inc   $7,s                                   6C 67
inc   $7,u                                   6C 47
inc   $7,x                                   6C 07
inc   $7,y                                   6C 27
inc   $8,s                                   6C 68
inc   $8,u                                   6C 48
inc   $8,x                                   6C 08
inc   $8,y                                   6C 28
inc   $9,s                                   6C 69
inc   $9,u                                   6C 49
inc   $9,x                                   6C 09
inc   $9,y                                   6C 29
inc   $a,s                                   6C 6A
inc   $a,u                                   6C 4A
inc   $a,x                                   6C 0A
inc   $a,y                                   6C 2A
inc   $b,s                                   6C 6B
inc   $b,u                                   6C 4B
inc   $b,x                                   6C 0B
inc   $b,y                                   6C 2B
inc   $beef                                  6C 8F BE EF
inc   $beef                                  6C AF BE EF
inc   $beef                                  6C CF BE EF
inc   $beef                                  6C EF BE EF
inc   $beef                                  7C BE EF
inc   $beef,pc                               6C 8D BE EF
inc   $beef,pc                               6C AD BE EF
inc   $beef,pc                               6C CD BE EF
inc   $beef,pc                               6C ED BE EF
inc   $beef,s                                6C E9 BE EF
inc   $beef,u                                6C C9 BE EF
inc   $beef,x                                6C 89 BE EF
inc   $beef,y                                6C A9 BE EF
inc   $c,s                                   6C 6C
inc   $c,u                                   6C 4C
inc   $c,x                                   6C 0C
inc   $c,y                                   6C 2C
inc   $d,s                                   6C 6D
inc   $d,u                                   6C 4D
inc   $d,x                                   6C 0D
inc   $d,y                                   6C 2D
inc   $e,s                                   6C 6E
inc   $e,u                                   6C 4E
inc   $e,x                                   6C 0E
inc   $e,y                                   6C 2E
inc   $f,s                                   6C 6F
inc   $f,u                                   6C 4F
inc   $f,x                                   6C 0F
inc   $f,y                                   6C 2F
inc   $ff                                    0C FF
inc   ,--s                                   6C E3
inc   ,--u                                   6C C3
inc   ,--x                                   6C 83
inc   ,--y                                   6C A3
inc   ,-s                                    6C E2
inc   ,-u                                    6C C2
inc   ,-x                                    6C 82
inc   ,-y                                    6C A2
inc   ,s                                     6C E4
inc   ,s+                                    6C E0
inc   ,s++                                   6C E1
inc   ,u                                     6C C4
inc   ,u+                                    6C C0
inc   ,u++                                   6C C1
inc   ,x                                     6C 84
inc   ,x+                                    6C 80
inc   ,x++                                   6C 81
inc   ,y                                     6C A4
inc   ,y+                                    6C A0
inc   ,y++                                   6C A1
inc   -$1,s                                  6C 7F
inc   -$1,u                                  6C 5F
inc   -$1,x                                  6C 1F
inc   -$1,y                                  6C 3F
inc   -$10,s                                 6C 70
inc   -$10,u                                 6C 50
inc   -$10,x                                 6C 10
inc   -$10,y                                 6C 30
inc   -$2,s                                  6C 7E
inc   -$2,u                                  6C 5E
inc   -$2,x                                  6C 1E
inc   -$2,y                                  6C 3E
inc   -$3,s                                  6C 7D
inc   -$3,u                                  6C 5D
inc   -$3,x                                  6C 1D
inc   -$3,y                                  6C 3D
inc   -$4,s                                  6C 7C
inc   -$4,u                                  6C 5C
inc   -$4,x                                  6C 1C
inc   -$4,y                                  6C 3C
inc   -$5,s                                  6C 7B
inc   -$5,u                                  6C 5B
inc   -$5,x                                  6C 1B
inc   -$5,y                                  6C 3B
inc   -$6,s                                  6C 7A
inc   -$6,u                                  6C 5A
inc   -$6,x                                  6C 1A
inc   -$6,y                                  6C 3A
inc   -$7,s                                  6C 79
inc   -$7,u                                  6C 59
inc   -$7,x                                  6C 19
inc   -$7,y                                  6C 39
inc   -$8,s                                  6C 78
inc   -$8,u                                  6C 58
inc   -$8,x                                  6C 18
inc   -$8,y                                  6C 38
inc   -$9,s                                  6C 77
inc   -$9,u                                  6C 57
inc   -$9,x                                  6C 17
inc   -$9,y                                  6C 37
inc   -$a,s                                  6C 76
inc   -$a,u                                  6C 56
inc   -$a,x                                  6C 16
inc   -$a,y                                  6C 36
inc   -$b,s                                  6C 75
inc   -$b,u                                  6C 55
inc   -$b,x                                  6C 15
inc   -$b,y                                  6C 35
inc   -$c,s                                  6C 74
inc   -$c,u                                  6C 54
inc   -$c,x                                  6C 14
inc   -$c,y                                  6C 34
inc   -$d,s                                  6C 73
inc   -$d,u                                  6C 53
inc   -$d,x                                  6C 13
inc   -$d,y                                  6C 33
inc   -$e,s                                  6C 72
inc   -$e,u                                  6C 52
inc   -$e,x                                  6C 12
inc   -$e,y                                  6C 32
inc   -$f,s                                  6C 71
inc   -$f,u                                  6C 51
inc   -$f,x                                  6C 11
inc   -$f,y                                  6C 31
inc   a,s                                    6C E6
inc   a,u                                    6C C6
inc   a,x                                    6C 86
inc   a,y                                    6C A6
inc   b,s                                    6C E5
inc   b,u                                    6C C5
inc   b,x                                    6C 85
inc   b,y                                    6C A5
inc   d,s                                    6C EB
inc   d,u                                    6C CB
inc   d,x                                    6C 8B
inc   d,y                                    6C AB
inc   [$01,pc]                               6C 9C 01
inc   [$01,pc]                               6C BC 01
inc   [$01,pc]                               6C DC 01
inc   [$01,pc]                               6C FC 01
inc   [$01,s]                                6C F8 01
inc   [$01,u]                                6C D8 01
inc   [$01,x]                                6C 98 01
inc   [$01,y]                                6C B8 01
inc   [$beef,pc]                             6C 9D BE EF
inc   [$beef,pc]                             6C BD BE EF
inc   [$beef,pc]                             6C DD BE EF
inc   [$beef,pc]                             6C FD BE EF
inc   [$beef,s]                              6C F9 BE EF
inc   [$beef,u]                              6C D9 BE EF
inc   [$beef,x]                              6C 99 BE EF
inc   [$beef,y]                              6C B9 BE EF
inc   [$beef]                                6C 9F BE EF
inc   [$beef]                                6C BF BE EF
inc   [$beef]                                6C DF BE EF
inc   [$beef]                                6C FF BE EF
inc   [,--s]                                 6C F3
inc   [,--u]                                 6C D3
inc   [,--x]                                 6C 93
inc   [,--y]                                 6C B3
inc   [,s++]                                 6C F1
inc   [,s]                                   6C F4
inc   [,u++]                                 6C D1
inc   [,u]                                   6C D4
inc   [,x++]                                 6C 91
inc   [,x]                                   6C 94
inc   [,y++]                                 6C B1
inc   [,y]                                   6C B4
inc   [a,s]                                  6C F6
inc   [a,u]                                  6C D6
inc   [a,x]                                  6C 96
inc   [a,y]                                  6C B6
inc   [b,s]                                  6C F5
inc   [b,u]                                  6C D5
inc   [b,x]                                  6C 95
inc   [b,y]                                  6C B5
inc   [d,s]                                  6C FB
inc   [d,u]                                  6C DB
inc   [d,x]                                  6C 9B
inc   [d,y]                                  6C BB
inc   []                                     6C 97
inc   []                                     6C 9A
inc   []                                     6C 9E
inc   []                                     6C B7
inc   []                                     6C BA
inc   []                                     6C BE
inc   []                                     6C D7
inc   []                                     6C DA
inc   []                                     6C DE
inc   []                                     6C F7
inc   []                                     6C FA
inc   []                                     6C FE
inca                                         4C
incb                                         5C
jmp   $0,s                                   6E 60
jmp   $0,u                                   6E 40
jmp   $0,x                                   6E 00
jmp   $0,y                                   6E 20
jmp   $01,pc                                 6E 8C 01
jmp   $01,pc                                 6E AC 01
jmp   $01,pc                                 6E CC 01
jmp   $01,pc                                 6E EC 01
jmp   $01,s                                  6E E8 01
jmp   $01,u                                  6E C8 01
jmp   $01,x                                  6E 88 01
jmp   $01,y                                  6E A8 01
jmp   $1,s                                   6E 61
jmp   $1,u                                   6E 41
jmp   $1,x                                   6E 01
jmp   $1,y                                   6E 21
jmp   $2,s                                   6E 62
jmp   $2,u                                   6E 42
jmp   $2,x                                   6E 02
jmp   $2,y                                   6E 22
jmp   $3,s                                   6E 63
jmp   $3,u                                   6E 43
jmp   $3,x                                   6E 03
jmp   $3,y                                   6E 23
jmp   $4,s                                   6E 64
jmp   $4,u                                   6E 44
jmp   $4,x                                   6E 04
jmp   $4,y                                   6E 24
jmp   $5,s                                   6E 65
jmp   $5,u                                   6E 45
jmp   $5,x                                   6E 05
jmp   $5,y                                   6E 25
jmp   $6,s                                   6E 66
jmp   $6,u                                   6E 46
jmp   $6,x                                   6E 06
jmp   $6,y                                   6E 26
jmp   $7,s                                   6E 67
jmp   $7,u                                   6E 47
jmp   $7,x                                   6E 07
jmp   $7,y                                   6E 27
jmp   $8,s                                   6E 68
jmp   $8,u                                   6E 48
jmp   $8,x                                   6E 08
jmp   $8,y                                   6E 28
jmp   $9,s                                   6E 69
jmp   $9,u                                   6E 49
jmp   $9,x                                   6E 09
jmp   $9,y                                   6E 29
jmp   $a,s                                   6E 6A
jmp   $a,u                                   6E 4A
jmp   $a,x                                   6E 0A
jmp   $a,y                                   6E 2A
jmp   $b,s                                   6E 6B
jmp   $b,u                                   6E 4B
jmp   $b,x                                   6E 0B
jmp   $b,y                                   6E 2B
jmp   $beef                                  6E 8F BE EF
jmp   $beef                                  6E AF BE EF
jmp   $beef                                  6E CF BE EF
jmp   $beef                                  6E EF BE EF
jmp   $beef                                  7E BE EF
jmp   $beef,pc                               6E 8D BE EF
jmp   $beef,pc                               6E AD BE EF
jmp   $beef,pc                               6E CD BE EF
jmp   $beef,pc                               6E ED BE EF
jmp   $beef,s                                6E E9 BE EF
jmp   $beef,u                                6E C9 BE EF
jmp   $beef,x                                6E 89 BE EF
jmp   $beef,y                                6E A9 BE EF
jmp   $c,s                                   6E 6C
jmp   $c,u                                   6E 4C
jmp   $c,x                                   6E 0C
jmp   $c,y                                   6E 2C
jmp   $d,s                                   6E 6D
jmp   $d,u                                   6E 4D
jmp   $d,x                                   6E 0D
jmp   $d,y                                   6E 2D
jmp   $e,s                                   6E 6E
jmp   $e,u                                   6E 4E
jmp   $e,x                                   6E 0E
jmp   $e,y                                   6E 2E
jmp   $f,s                                   6E 6F
jmp   $f,u                                   6E 4F
jmp   $f,x                                   6E 0F
jmp   $f,y                                   6E 2F
jmp   $ff                                    0E FF
jmp   ,--s                                   6E E3
jmp   ,--u                                   6E C3
jmp   ,--x                                   6E 83
jmp   ,--y                                   6E A3
jmp   ,-s                                    6E E2
jmp   ,-u                                    6E C2
jmp   ,-x                                    6E 82
jmp   ,-y                                    6E A2
jmp   ,s                                     6E E4
jmp   ,s+                                    6E E0
jmp   ,s++                                   6E E1
jmp   ,u                                     6E C4
jmp   ,u+                                    6E C0
jmp   ,u++                                   6E C1
jmp   ,x                                     6E 84
jmp   ,x+                                    6E 80
jmp   ,x++                                   6E 81
jmp   ,y                                     6E A4
jmp   ,y+                                    6E A0
jmp   ,y++                                   6E A1
jmp   -$1,s                                  6E 7F
jmp   -$1,u                                  6E 5F
jmp   -$1,x                                  6E 1F
jmp   -$1,y                                  6E 3F
jmp   -$10,s                                 6E 70
jmp   -$10,u                                 6E 50
jmp   -$10,x                                 6E 10
jmp   -$10,y                                 6E 30
jmp   -$2,s                                  6E 7E
jmp   -$2,u                                  6E 5E
jmp   -$2,x                                  6E 1E
jmp   -$2,y                                  6E 3E
jmp   -$3,s                                  6E 7D
jmp   -$3,u                                  6E 5D
jmp   -$3,x                                  6E 1D
jmp   -$3,y                                  6E 3D
jmp   -$4,s                                  6E 7C
jmp   -$4,u                                  6E 5C
jmp   -$4,x                                  6E 1C
jmp   -$4,y                                  6E 3C
jmp   -$5,s                                  6E 7B
jmp   -$5,u                                  6E 5B
jmp   -$5,x                                  6E 1B
jmp   -$5,y                                  6E 3B
jmp   -$6,s                                  6E 7A
jmp   -$6,u                                  6E 5A
jmp   -$6,x                                  6E 1A
jmp   -$6,y                                  6E 3A
jmp   -$7,s                                  6E 79
jmp   -$7,u                                  6E 59
jmp   -$7,x                                  6E 19
jmp   -$7,y                                  6E 39
jmp   -$8,s                                  6E 78
jmp   -$8,u                                  6E 58
jmp   -$8,x                                  6E 18
jmp   -$8,y                                  6E 38
jmp   -$9,s                                  6E 77
jmp   -$9,u                                  6E 57
jmp   -$9,x                                  6E 17
jmp   -$9,y                                  6E 37
jmp   -$a,s                                  6E 76
jmp   -$a,u                                  6E 56
jmp   -$a,x                                  6E 16
jmp   -$a,y                                  6E 36
jmp   -$b,s                                  6E 75
jmp   -$b,u                                  6E 55
jmp   -$b,x                                  6E 15
jmp   -$b,y                                  6E 35
jmp   -$c,s                                  6E 74
jmp   -$c,u                                  6E 54
jmp   -$c,x                                  6E 14
jmp   -$c,y                                  6E 34
jmp   -$d,s                                  6E 73
jmp   -$d,u                                  6E 53
jmp   -$d,x                                  6E 13
jmp   -$d,y                                  6E 33
jmp   -$e,s                                  6E 72
jmp   -$e,u                                  6E 52
jmp   -$e,x                                  6E 12
jmp   -$e,y                                  6E 32
jmp   -$f,s                                  6E 71
jmp   -$f,u                                  6E 51
jmp   -$f,x                                  6E 11
jmp   -$f,y                                  6E 31
jmp   a,s                                    6E E6
jmp   a,u                                    6E C6
jmp   a,x                                    6E 86
jmp   a,y                                    6E A6
jmp   b,s                                    6E E5
jmp   b,u                                    6E C5
jmp   b,x                                    6E 85
jmp   b,y                                    6E A5
jmp   d,s                                    6E EB
jmp   d,u                                    6E CB
jmp   d,x                                    6E 8B
jmp   d,y                                    6E AB
jmp   [$01,pc]                               6E 9C 01
jmp   [$01,pc]                               6E BC 01
jmp   [$01,pc]                               6E DC 01
jmp   [$01,pc]                               6E FC 01
jmp   [$01,s]                                6E F8 01
jmp   [$01,u]                                6E D8 01
jmp   [$01,x]                                6E 98 01
jmp   [$01,y]                                6E B8 01
jmp   [$beef,pc]                             6E 9D BE EF
jmp   [$beef,pc]                             6E BD BE EF
jmp   [$beef,pc]                             6E DD BE EF
jmp   [$beef,pc]                             6E FD BE EF
jmp   [$beef,s]                              6E F9 BE EF
jmp   [$beef,u]                              6E D9 BE EF
jmp   [$beef,x]                              6E 99 BE EF
jmp   [$beef,y]                              6E B9 BE EF
jmp   [$beef]                                6E 9F BE EF
jmp   [$beef]                                6E BF BE EF
jmp   [$beef]                                6E DF BE EF
jmp   [$beef]                                6E FF BE EF
jmp   [,--s]                                 6E F3
jmp   [,--u]                                 6E D3
jmp   [,--x]                                 6E 93
jmp   [,--y]                                 6E B3
jmp   [,s++]                                 6E F1
jmp   [,s]                                   6E F4
jmp   [,u++]                                 6E D1
jmp   [,u]                                   6E D4
jmp   [,x++]                                 6E 91
jmp   [,x]                                   6E 94
jmp   [,y++]                                 6E B1
jmp   [,y]                                   6E B4
jmp   [a,s]                                  6E F6
jmp   [a,u]                                  6E D6
jmp   [a,x]                                  6E 96
jmp   [a,y]                                  6E B6
jmp   [b,s]                                  6E F5
jmp   [b,u]                                  6E D5
jmp   [b,x]                                  6E 95
jmp   [b,y]                                  6E B5
jmp   [d,s]                                  6E FB
jmp   [d,u]                                  6E DB
jmp   [d,x]                                  6E 9B
jmp   [d,y]                                  6E BB
jmp   []                                     6E 97
jmp   []                                     6E 9A
jmp   []                                     6E 9E
jmp   []                                     6E B7
jmp   []                                     6E BA
jmp   []                                     6E BE
jmp   []                                     6E D7
jmp   []                                     6E DA
jmp   []                                     6E DE
jmp   []                                     6E F7
jmp   []                                     6E FA
jmp   []                                     6E FE
jsr   $0,s                                   AD 60
jsr   $0,u                                   AD 40
jsr   $0,x                                   AD 00
jsr   $0,y                                   AD 20
jsr   $01,pc                                 AD 8C 01
jsr   $01,pc                                 AD AC 01
jsr   $01,pc                                 AD CC 01
jsr   $01,pc                                 AD EC 01
jsr   $01,s                                  AD E8 01
jsr   $01,u                                  AD C8 01
jsr   $01,x                                  AD 88 01
jsr   $01,y                                  AD A8 01
jsr   $1,s                                   AD 61
jsr   $1,u                                   AD 41
jsr   $1,x                                   AD 01
jsr   $1,y                                   AD 21
jsr   $2,s                                   AD 62
jsr   $2,u                                   AD 42
jsr   $2,x                                   AD 02
jsr   $2,y                                   AD 22
jsr   $3,s                                   AD 63
jsr   $3,u                                   AD 43
jsr   $3,x                                   AD 03
jsr   $3,y                                   AD 23
jsr   $4,s                                   AD 64
jsr   $4,u                                   AD 44
jsr   $4,x                                   AD 04
jsr   $4,y                                   AD 24
jsr   $5,s                                   AD 65
jsr   $5,u                                   AD 45
jsr   $5,x                                   AD 05
jsr   $5,y                                   AD 25
jsr   $6,s                                   AD 66
jsr   $6,u                                   AD 46
jsr   $6,x                                   AD 06
jsr   $6,y                                   AD 26
jsr   $7,s                                   AD 67
jsr   $7,u                                   AD 47
jsr   $7,x                                   AD 07
jsr   $7,y                                   AD 27
jsr   $8,s                                   AD 68
jsr   $8,u                                   AD 48
jsr   $8,x                                   AD 08
jsr   $8,y                                   AD 28
jsr   $9,s                                   AD 69
jsr   $9,u                                   AD 49
jsr   $9,x                                   AD 09
jsr   $9,y                                   AD 29
jsr   $a,s                                   AD 6A
jsr   $a,u                                   AD 4A
jsr   $a,x                                   AD 0A
jsr   $a,y                                   AD 2A
jsr   $b,s                                   AD 6B
jsr   $b,u                                   AD 4B
jsr   $b,x                                   AD 0B
jsr   $b,y                                   AD 2B
jsr   $beef                                  AD 8F BE EF
jsr   $beef                                  AD AF BE EF
jsr   $beef                                  AD CF BE EF
jsr   $beef                                  AD EF BE EF
jsr   $beef                                  BD BE EF
jsr   $beef,pc                               AD 8D BE EF
jsr   $beef,pc                               AD AD BE EF
jsr   $beef,pc                               AD CD BE EF
jsr   $beef,pc                               AD ED BE EF
jsr   $beef,s                                AD E9 BE EF
jsr   $beef,u                                AD C9 BE EF
jsr   $beef,x                                AD 89 BE EF
jsr   $beef,y                                AD A9 BE EF
jsr   $c,s                                   AD 6C
jsr   $c,u                                   AD 4C
jsr   $c,x                                   AD 0C
jsr   $c,y                                   AD 2C
jsr   $d,s                                   AD 6D
jsr   $d,u                                   AD 4D
jsr   $d,x                                   AD 0D
jsr   $d,y                                   AD 2D
jsr   $e,s                                   AD 6E
jsr   $e,u                                   AD 4E
jsr   $e,x                                   AD 0E
jsr   $e,y                                   AD 2E
jsr   $f,s                                   AD 6F
jsr   $f,u                                   AD 4F
jsr   $f,x                                   AD 0F
jsr   $f,y                                   AD 2F
jsr   $ff                                    9D FF
jsr   ,--s                                   AD E3
jsr   ,--u                                   AD C3
jsr   ,--x                                   AD 83
jsr   ,--y                                   AD A3
jsr   ,-s                                    AD E2
jsr   ,-u                                    AD C2
jsr   ,-x                                    AD 82
jsr   ,-y                                    AD A2
jsr   ,s                                     AD E4
jsr   ,s+                                    AD E0
jsr   ,s++                                   AD E1
jsr   ,u                                     AD C4
jsr   ,u+                                    AD C0
jsr   ,u++                                   AD C1
jsr   ,x                                     AD 84
jsr   ,x+                                    AD 80
jsr   ,x++                                   AD 81
jsr   ,y                                     AD A4
jsr   ,y+                                    AD A0
jsr   ,y++                                   AD A1
jsr   -$1,s                                  AD 7F
jsr   -$1,u                                  AD 5F
jsr   -$1,x                                  AD 1F
jsr   -$1,y                                  AD 3F
jsr   -$10,s                                 AD 70
jsr   -$10,u                                 AD 50
jsr   -$10,x                                 AD 10
jsr   -$10,y                                 AD 30
jsr   -$2,s                                  AD 7E
jsr   -$2,u                                  AD 5E
jsr   -$2,x                                  AD 1E
jsr   -$2,y                                  AD 3E
jsr   -$3,s                                  AD 7D
jsr   -$3,u                                  AD 5D
jsr   -$3,x                                  AD 1D
jsr   -$3,y                                  AD 3D
jsr   -$4,s                                  AD 7C
jsr   -$4,u                                  AD 5C
jsr   -$4,x                                  AD 1C
jsr   -$4,y                                  AD 3C
jsr   -$5,s                                  AD 7B
jsr   -$5,u                                  AD 5B
jsr   -$5,x                                  AD 1B
jsr   -$5,y                                  AD 3B
jsr   -$6,s                                  AD 7A
jsr   -$6,u                                  AD 5A
jsr   -$6,x                                  AD 1A
jsr   -$6,y                                  AD 3A
jsr   -$7,s                                  AD 79
jsr   -$7,u                                  AD 59
jsr   -$7,x                                  AD 19
jsr   -$7,y                                  AD 39
jsr   -$8,s                                  AD 78
jsr   -$8,u                                  AD 58
jsr   -$8,x                                  AD 18
jsr   -$8,y                                  AD 38
jsr   -$9,s                                  AD 77
jsr   -$9,u                                  AD 57
jsr   -$9,x                                  AD 17
jsr   -$9,y                                  AD 37
jsr   -$a,s                                  AD 76
jsr   -$a,u                                  AD 56
jsr   -$a,x                                  AD 16
jsr   -$a,y                                  AD 36
jsr   -$b,s                                  AD 75
jsr   -$b,u                                  AD 55
jsr   -$b,x                                  AD 15
jsr   -$b,y                                  AD 35
jsr   -$c,s                                  AD 74
jsr   -$c,u                                  AD 54
jsr   -$c,x                                  AD 14
jsr   -$c,y                                  AD 34
jsr   -$d,s                                  AD 73
jsr   -$d,u                                  AD 53
jsr   -$d,x                                  AD 13
jsr   -$d,y                                  AD 33
jsr   -$e,s                                  AD 72
jsr   -$e,u                                  AD 52
jsr   -$e,x                                  AD 12
jsr   -$e,y                                  AD 32
jsr   -$f,s                                  AD 71
jsr   -$f,u                                  AD 51
jsr   -$f,x                                  AD 11
jsr   -$f,y                                  AD 31
jsr   a,s                                    AD E6
jsr   a,u                                    AD C6
jsr   a,x                                    AD 86
jsr   a,y                                    AD A6
jsr   b,s                                    AD E5
jsr   b,u                                    AD C5
jsr   b,x                                    AD 85
jsr   b,y                                    AD A5
jsr   d,s                                    AD EB
jsr   d,u                                    AD CB
jsr   d,x                                    AD 8B
jsr   d,y                                    AD AB
jsr   [$01,pc]                               AD 9C 01
jsr   [$01,pc]                               AD BC 01
jsr   [$01,pc]                               AD DC 01
jsr   [$01,pc]                               AD FC 01
jsr   [$01,s]                                AD F8 01
jsr   [$01,u]                                AD D8 01
jsr   [$01,x]                                AD 98 01
jsr   [$01,y]                                AD B8 01
jsr   [$beef,pc]                             AD 9D BE EF
jsr   [$beef,pc]                             AD BD BE EF
jsr   [$beef,pc]                             AD DD BE EF
jsr   [$beef,pc]                             AD FD BE EF
jsr   [$beef,s]                              AD F9 BE EF
jsr   [$beef,u]                              AD D9 BE EF
jsr   [$beef,x]                              AD 99 BE EF
jsr   [$beef,y]                              AD B9 BE EF
jsr   [$beef]                                AD 9F BE EF
jsr   [$beef]                                AD BF BE EF
jsr   [$beef]                                AD DF BE EF
jsr   [$beef]                                AD FF BE EF
jsr   [,--s]                                 AD F3
jsr   [,--u]                                 AD D3
jsr   [,--x]                                 AD 93
jsr   [,--y]                                 AD B3
jsr   [,s++]                                 AD F1
jsr   [,s]                                   AD F4
jsr   [,u++]                                 AD D1
jsr   [,u]                                   AD D4
jsr   [,x++]                                 AD 91
jsr   [,x]                                   AD 94
jsr   [,y++]                                 AD B1
jsr   [,y]                                   AD B4
jsr   [a,s]                                  AD F6
jsr   [a,u]                                  AD D6
jsr   [a,x]                                  AD 96
jsr   [a,y]                                  AD B6
jsr   [b,s]                                  AD F5
jsr   [b,u]                                  AD D5
jsr   [b,x]                                  AD 95
jsr   [b,y]                                  AD B5
jsr   [d,s]                                  AD FB
jsr   [d,u]                                  AD DB
jsr   [d,x]                                  AD 9B
jsr   [d,y]                                  AD BB
jsr   []                                     AD 97
jsr   []                                     AD 9A
jsr   []                                     AD 9E
jsr   []                                     AD B7
jsr   []                                     AD BA
jsr   []                                     AD BE
jsr   []                                     AD D7
jsr   []                                     AD DA
jsr   []                                     AD DE
jsr   []                                     AD F7
jsr   []                                     AD FA
jsr   []                                     AD FE
lbcc  $+7fff                                 10 24 7F FF
lbcs  $+7fff                                 10 25 7F FF
lbeq  $+7fff                                 10 27 7F FF
lbge  $+7fff                                 10 2C 7F FF
lbgt  $+7fff                                 10 2E 7F FF
lbhi  $+7fff                                 10 22 7F FF
lble  $+7fff                                 10 2F 7F FF
lbls  $+7fff                                 10 23 7F FF
lblt  $+7fff                                 10 2D 7F FF
lbmi  $+7fff                                 10 2B 7F FF
lbne  $+7fff                                 10 26 7F FF
lbpl  $+7fff                                 10 2A 7F FF
lbra  $+7fff                                 16 7F FF
lbrn  $+7fff                                 10 21 7F FF
lbsr  $+7fff                                 17 7F FF
lbvc  $+7fff                                 10 28 7F FF
lbvs  $+7fff                                 10 29 7F FF
lda   #$ff                                   86 FF
lda   $0,s                                   A6 60
lda   $0,u                                   A6 40
lda   $0,x                                   A6 00
lda   $0,y                                   A6 20
lda   $01,pc                                 A6 8C 01
lda   $01,pc                                 A6 AC 01
lda   $01,pc                                 A6 CC 01
lda   $01,pc                                 A6 EC 01
lda   $01,s                                  A6 E8 01
lda   $01,u                                  A6 C8 01
lda   $01,x                                  A6 88 01
lda   $01,y                                  A6 A8 01
lda   $1,s                                   A6 61
lda   $1,u                                   A6 41
lda   $1,x                                   A6 01
lda   $1,y                                   A6 21
lda   $2,s                                   A6 62
lda   $2,u                                   A6 42
lda   $2,x                                   A6 02
lda   $2,y                                   A6 22
lda   $3,s                                   A6 63
lda   $3,u                                   A6 43
lda   $3,x                                   A6 03
lda   $3,y                                   A6 23
lda   $4,s                                   A6 64
lda   $4,u                                   A6 44
lda   $4,x                                   A6 04
lda   $4,y                                   A6 24
lda   $5,s                                   A6 65
lda   $5,u                                   A6 45
lda   $5,x                                   A6 05
lda   $5,y                                   A6 25
lda   $6,s                                   A6 66
lda   $6,u                                   A6 46
lda   $6,x                                   A6 06
lda   $6,y                                   A6 26
lda   $7,s                                   A6 67
lda   $7,u                                   A6 47
lda   $7,x                                   A6 07
lda   $7,y                                   A6 27
lda   $8,s                                   A6 68
lda   $8,u                                   A6 48
lda   $8,x                                   A6 08
lda   $8,y                                   A6 28
lda   $9,s                                   A6 69
lda   $9,u                                   A6 49
lda   $9,x                                   A6 09
lda   $9,y                                   A6 29
lda   $a,s                                   A6 6A
lda   $a,u                                   A6 4A
lda   $a,x                                   A6 0A
lda   $a,y                                   A6 2A
lda   $b,s                                   A6 6B
lda   $b,u                                   A6 4B
lda   $b,x                                   A6 0B
lda   $b,y                                   A6 2B
lda   $beef                                  A6 8F BE EF
lda   $beef                                  A6 AF BE EF
lda   $beef                                  A6 CF BE EF
lda   $beef                                  A6 EF BE EF
lda   $beef                                  B6 BE EF
lda   $beef,pc                               A6 8D BE EF
lda   $beef,pc                               A6 AD BE EF
lda   $beef,pc                               A6 CD BE EF
lda   $beef,pc                               A6 ED BE EF
lda   $beef,s                                A6 E9 BE EF
lda   $beef,u                                A6 C9 BE EF
lda   $beef,x                                A6 89 BE EF
lda   $beef,y                                A6 A9 BE EF
lda   $c,s                                   A6 6C
lda   $c,u                                   A6 4C
lda   $c,x                                   A6 0C
lda   $c,y                                   A6 2C
lda   $d,s                                   A6 6D
lda   $d,u                                   A6 4D
lda   $d,x                                   A6 0D
lda   $d,y                                   A6 2D
lda   $e,s                                   A6 6E
lda   $e,u                                   A6 4E
lda   $e,x                                   A6 0E
lda   $e,y                                   A6 2E
lda   $f,s                                   A6 6F
lda   $f,u                                   A6 4F
lda   $f,x                                   A6 0F
lda   $f,y                                   A6 2F
lda   $ff                                    96 FF
lda   ,--s                                   A6 E3
lda   ,--u                                   A6 C3
lda   ,--x                                   A6 83
lda   ,--y                                   A6 A3
lda   ,-s                                    A6 E2
lda   ,-u                                    A6 C2
lda   ,-x                                    A6 82
lda   ,-y                                    A6 A2
lda   ,s                                     A6 E4
lda   ,s+                                    A6 E0
lda   ,s++                                   A6 E1
lda   ,u                                     A6 C4
lda   ,u+                                    A6 C0
lda   ,u++                                   A6 C1
lda   ,x                                     A6 84
lda   ,x+                                    A6 80
lda   ,x++                                   A6 81
lda   ,y                                     A6 A4
lda   ,y+                                    A6 A0
lda   ,y++                                   A6 A1
lda   -$1,s                                  A6 7F
lda   -$1,u                                  A6 5F
lda   -$1,x                                  A6 1F
lda   -$1,y                                  A6 3F
lda   -$10,s                                 A6 70
lda   -$10,u                                 A6 50
lda   -$10,x                                 A6 10
lda   -$10,y                                 A6 30
lda   -$2,s                                  A6 7E
lda   -$2,u                                  A6 5E
lda   -$2,x                                  A6 1E
lda   -$2,y                                  A6 3E
lda   -$3,s                                  A6 7D
lda   -$3,u                                  A6 5D
lda   -$3,x                                  A6 1D
lda   -$3,y                                  A6 3D
lda   -$4,s                                  A6 7C
lda   -$4,u                                  A6 5C
lda   -$4,x                                  A6 1C
lda   -$4,y                                  A6 3C
lda   -$5,s                                  A6 7B
lda   -$5,u                                  A6 5B
lda   -$5,x                                  A6 1B
lda   -$5,y                                  A6 3B
lda   -$6,s                                  A6 7A
lda   -$6,u                                  A6 5A
lda   -$6,x                                  A6 1A
lda   -$6,y                                  A6 3A
lda   -$7,s                                  A6 79
lda   -$7,u                                  A6 59
lda   -$7,x                                  A6 19
lda   -$7,y                                  A6 39
lda   -$8,s                                  A6 78
lda   -$8,u                                  A6 58
lda   -$8,x                                  A6 18
lda   -$8,y                                  A6 38
lda   -$9,s                                  A6 77
lda   -$9,u                                  A6 57
lda   -$9,x                                  A6 17
lda   -$9,y                                  A6 37
lda   -$a,s                                  A6 76
lda   -$a,u                                  A6 56
lda   -$a,x                                  A6 16
lda   -$a,y                                  A6 36
lda   -$b,s                                  A6 75
lda   -$b,u                                  A6 55
lda   -$b,x                                  A6 15
lda   -$b,y                                  A6 35
lda   -$c,s                                  A6 74
lda   -$c,u                                  A6 54
lda   -$c,x                                  A6 14
lda   -$c,y                                  A6 34
lda   -$d,s                                  A6 73
lda   -$d,u                                  A6 53
lda   -$d,x                                  A6 13
lda   -$d,y                                  A6 33
lda   -$e,s                                  A6 72
lda   -$e,u                                  A6 52
lda   -$e,x                                  A6 12
lda   -$e,y                                  A6 32
lda   -$f,s                                  A6 71
lda   -$f,u                                  A6 51
lda   -$f,x                                  A6 11
lda   -$f,y                                  A6 31
lda   a,s                                    A6 E6
lda   a,u                                    A6 C6
lda   a,x                                    A6 86
lda   a,y                                    A6 A6
lda   b,s                                    A6 E5
lda   b,u                                    A6 C5
lda   b,x                                    A6 85
lda   b,y                                    A6 A5
lda   d,s                                    A6 EB
lda   d,u                                    A6 CB
lda   d,x                                    A6 8B
lda   d,y                                    A6 AB
lda   [$01,pc]                               A6 9C 01
lda   [$01,pc]                               A6 BC 01
lda   [$01,pc]                               A6 DC 01
lda   [$01,pc]                               A6 FC 01
lda   [$01,s]                                A6 F8 01
lda   [$01,u]                                A6 D8 01
lda   [$01,x]                                A6 98 01
lda   [$01,y]                                A6 B8 01
lda   [$beef,pc]                             A6 9D BE EF
lda   [$beef,pc]                             A6 BD BE EF
lda   [$beef,pc]                             A6 DD BE EF
lda   [$beef,pc]                             A6 FD BE EF
lda   [$beef,s]                              A6 F9 BE EF
lda   [$beef,u]                              A6 D9 BE EF
lda   [$beef,x]                              A6 99 BE EF
lda   [$beef,y]                              A6 B9 BE EF
lda   [$beef]                                A6 9F BE EF
lda   [$beef]                                A6 BF BE EF
lda   [$beef]                                A6 DF BE EF
lda   [$beef]                                A6 FF BE EF
lda   [,--s]                                 A6 F3
lda   [,--u]                                 A6 D3
lda   [,--x]                                 A6 93
lda   [,--y]                                 A6 B3
lda   [,s++]                                 A6 F1
lda   [,s]                                   A6 F4
lda   [,u++]                                 A6 D1
lda   [,u]                                   A6 D4
lda   [,x++]                                 A6 91
lda   [,x]                                   A6 94
lda   [,y++]                                 A6 B1
lda   [,y]                                   A6 B4
lda   [a,s]                                  A6 F6
lda   [a,u]                                  A6 D6
lda   [a,x]                                  A6 96
lda   [a,y]                                  A6 B6
lda   [b,s]                                  A6 F5
lda   [b,u]                                  A6 D5
lda   [b,x]                                  A6 95
lda   [b,y]                                  A6 B5
lda   [d,s]                                  A6 FB
lda   [d,u]                                  A6 DB
lda   [d,x]                                  A6 9B
lda   [d,y]                                  A6 BB
lda   []                                     A6 97
lda   []                                     A6 9A
lda   []                                     A6 9E
lda   []                                     A6 B7
lda   []                                     A6 BA
lda   []                                     A6 BE
lda   []                                     A6 D7
lda   []                                     A6 DA
lda   []                                     A6 DE
lda   []                                     A6 F7
lda   []                                     A6 FA
lda   []                                     A6 FE
ldb   #$ff                                   C6 FF
ldb   $0,s                                   E6 60
ldb   $0,u                                   E6 40
ldb   $0,x                                   E6 00
ldb   $0,y                                   E6 20
ldb   $01,pc                                 E6 8C 01
ldb   $01,pc                                 E6 AC 01
ldb   $01,pc                                 E6 CC 01
ldb   $01,pc                                 E6 EC 01
ldb   $01,s                                  E6 E8 01
ldb   $01,u                                  E6 C8 01
ldb   $01,x                                  E6 88 01
ldb   $01,y                                  E6 A8 01
ldb   $1,s                                   E6 61
ldb   $1,u                                   E6 41
ldb   $1,x                                   E6 01
ldb   $1,y                                   E6 21
ldb   $2,s                                   E6 62
ldb   $2,u                                   E6 42
ldb   $2,x                                   E6 02
ldb   $2,y                                   E6 22
ldb   $3,s                                   E6 63
ldb   $3,u                                   E6 43
ldb   $3,x                                   E6 03
ldb   $3,y                                   E6 23
ldb   $4,s                                   E6 64
ldb   $4,u                                   E6 44
ldb   $4,x                                   E6 04
ldb   $4,y                                   E6 24
ldb   $5,s                                   E6 65
ldb   $5,u                                   E6 45
ldb   $5,x                                   E6 05
ldb   $5,y                                   E6 25
ldb   $6,s                                   E6 66
ldb   $6,u                                   E6 46
ldb   $6,x                                   E6 06
ldb   $6,y                                   E6 26
ldb   $7,s                                   E6 67
ldb   $7,u                                   E6 47
ldb   $7,x                                   E6 07
ldb   $7,y                                   E6 27
ldb   $8,s                                   E6 68
ldb   $8,u                                   E6 48
ldb   $8,x                                   E6 08
ldb   $8,y                                   E6 28
ldb   $9,s                                   E6 69
ldb   $9,u                                   E6 49
ldb   $9,x                                   E6 09
ldb   $9,y                                   E6 29
ldb   $a,s                                   E6 6A
ldb   $a,u                                   E6 4A
ldb   $a,x                                   E6 0A
ldb   $a,y                                   E6 2A
ldb   $b,s                                   E6 6B
ldb   $b,u                                   E6 4B
ldb   $b,x                                   E6 0B
ldb   $b,y                                   E6 2B
ldb   $beef                                  E6 8F BE EF
ldb   $beef                                  E6 AF BE EF
ldb   $beef                                  E6 CF BE EF
ldb   $beef                                  E6 EF BE EF
ldb   $beef                                  F6 BE EF
ldb   $beef,pc                               E6 8D BE EF
ldb   $beef,pc                               E6 AD BE EF
ldb   $beef,pc                               E6 CD BE EF
ldb   $beef,pc                               E6 ED BE EF
ldb   $beef,s                                E6 E9 BE EF
ldb   $beef,u                                E6 C9 BE EF
ldb   $beef,x                                E6 89 BE EF
ldb   $beef,y                                E6 A9 BE EF
ldb   $c,s                                   E6 6C
ldb   $c,u                                   E6 4C
ldb   $c,x                                   E6 0C
ldb   $c,y                                   E6 2C
ldb   $d,s                                   E6 6D
ldb   $d,u                                   E6 4D
ldb   $d,x                                   E6 0D
ldb   $d,y                                   E6 2D
ldb   $e,s                                   E6 6E
ldb   $e,u                                   E6 4E
ldb   $e,x                                   E6 0E
ldb   $e,y                                   E6 2E
ldb   $f,s                                   E6 6F
ldb   $f,u                                   E6 4F
ldb   $f,x                                   E6 0F
ldb   $f,y                                   E6 2F
ldb   $ff                                    D6 FF
ldb   ,--s                                   E6 E3
ldb   ,--u                                   E6 C3
ldb   ,--x                                   E6 83
ldb   ,--y                                   E6 A3
ldb   ,-s                                    E6 E2
ldb   ,-u                                    E6 C2
ldb   ,-x                                    E6 82
ldb   ,-y                                    E6 A2
ldb   ,s                                     E6 E4
ldb   ,s+                                    E6 E0
ldb   ,s++                                   E6 E1
ldb   ,u                                     E6 C4
ldb   ,u+                                    E6 C0
ldb   ,u++                                   E6 C1
ldb   ,x                                     E6 84
ldb   ,x+                                    E6 80
ldb   ,x++                                   E6 81
ldb   ,y                                     E6 A4
ldb   ,y+                                    E6 A0
ldb   ,y++                                   E6 A1
ldb   -$1,s                                  E6 7F
ldb   -$1,u                                  E6 5F
ldb   -$1,x                                  E6 1F
ldb   -$1,y                                  E6 3F
ldb   -$10,s                                 E6 70
ldb   -$10,u                                 E6 50
ldb   -$10,x                                 E6 10
ldb   -$10,y                                 E6 30
ldb   -$2,s                                  E6 7E
ldb   -$2,u                                  E6 5E
ldb   -$2,x                                  E6 1E
ldb   -$2,y                                  E6 3E
ldb   -$3,s                                  E6 7D
ldb   -$3,u                                  E6 5D
ldb   -$3,x                                  E6 1D
ldb   -$3,y                                  E6 3D
ldb   -$4,s                                  E6 7C
ldb   -$4,u                                  E6 5C
ldb   -$4,x                                  E6 1C
ldb   -$4,y                                  E6 3C
ldb   -$5,s                                  E6 7B
ldb   -$5,u                                  E6 5B
ldb   -$5,x                                  E6 1B
ldb   -$5,y                                  E6 3B
ldb   -$6,s                                  E6 7A
ldb   -$6,u                                  E6 5A
ldb   -$6,x                                  E6 1A
ldb   -$6,y                                  E6 3A
ldb   -$7,s                                  E6 79
ldb   -$7,u                                  E6 59
ldb   -$7,x                                  E6 19
ldb   -$7,y                                  E6 39
ldb   -$8,s                                  E6 78
ldb   -$8,u                                  E6 58
ldb   -$8,x                                  E6 18
ldb   -$8,y                                  E6 38
ldb   -$9,s                                  E6 77
ldb   -$9,u                                  E6 57
ldb   -$9,x                                  E6 17
ldb   -$9,y                                  E6 37
ldb   -$a,s                                  E6 76
ldb   -$a,u                                  E6 56
ldb   -$a,x                                  E6 16
ldb   -$a,y                                  E6 36
ldb   -$b,s                                  E6 75
ldb   -$b,u                                  E6 55
ldb   -$b,x                                  E6 15
ldb   -$b,y                                  E6 35
ldb   -$c,s                                  E6 74
ldb   -$c,u                                  E6 54
ldb   -$c,x                                  E6 14
ldb   -$c,y                                  E6 34
ldb   -$d,s                                  E6 73
ldb   -$d,u                                  E6 53
ldb   -$d,x                                  E6 13
ldb   -$d,y                                  E6 33
ldb   -$e,s                                  E6 72
ldb   -$e,u                                  E6 52
ldb   -$e,x                                  E6 12
ldb   -$e,y                                  E6 32
ldb   -$f,s                                  E6 71
ldb   -$f,u                                  E6 51
ldb   -$f,x                                  E6 11
ldb   -$f,y                                  E6 31
ldb   a,s                                    E6 E6
ldb   a,u                                    E6 C6
ldb   a,x                                    E6 86
ldb   a,y                                    E6 A6
ldb   b,s                                    E6 E5
ldb   b,u                                    E6 C5
ldb   b,x                                    E6 85
ldb   b,y                                    E6 A5
ldb   d,s                                    E6 EB
ldb   d,u                                    E6 CB
ldb   d,x                                    E6 8B
ldb   d,y                                    E6 AB
ldb   [$01,pc]                               E6 9C 01
ldb   [$01,pc]                               E6 BC 01
ldb   [$01,pc]                               E6 DC 01
ldb   [$01,pc]                               E6 FC 01
ldb   [$01,s]                                E6 F8 01
ldb   [$01,u]                                E6 D8 01
ldb   [$01,x]                                E6 98 01
ldb   [$01,y]                                E6 B8 01
ldb   [$beef,pc]                             E6 9D BE EF
ldb   [$beef,pc]                             E6 BD BE EF
ldb   [$beef,pc]                             E6 DD BE EF
ldb   [$beef,pc]                             E6 FD BE EF
ldb   [$beef,s]                              E6 F9 BE EF
ldb   [$beef,u]                              E6 D9 BE EF
ldb   [$beef,x]                              E6 99 BE EF
ldb   [$beef,y]                              E6 B9 BE EF
ldb   [$beef]                                E6 9F BE EF
ldb   [$beef]                                E6 BF BE EF
ldb   [$beef]                                E6 DF BE EF
ldb   [$beef]                                E6 FF BE EF
ldb   [,--s]                                 E6 F3
ldb   [,--u]                                 E6 D3
ldb   [,--x]                                 E6 93
ldb   [,--y]                                 E6 B3
ldb   [,s++]                                 E6 F1
ldb   [,s]                                   E6 F4
ldb   [,u++]                                 E6 D1
ldb   [,u]                                   E6 D4
ldb   [,x++]                                 E6 91
ldb   [,x]                                   E6 94
ldb   [,y++]                                 E6 B1
ldb   [,y]                                   E6 B4
ldb   [a,s]                                  E6 F6
ldb   [a,u]                                  E6 D6
ldb   [a,x]                                  E6 96
ldb   [a,y]                                  E6 B6
ldb   [b,s]                                  E6 F5
ldb   [b,u]                                  E6 D5
ldb   [b,x]                                  E6 95
ldb   [b,y]                                  E6 B5
ldb   [d,s]                                  E6 FB
ldb   [d,u]                                  E6 DB
ldb   [d,x]                                  E6 9B
ldb   [d,y]                                  E6 BB
ldb   []                                     E6 97
ldb   []                                     E6 9A
ldb   []                                     E6 9E
ldb   []                                     E6 B7
ldb   []                                     E6 BA
ldb   []                                     E6 BE
ldb   []                                     E6 D7
ldb   []                                     E6 DA
ldb   []                                     E6 DE
ldb   []                                     E6 F7
ldb   []                                     E6 FA
ldb   []                                     E6 FE
ldd   #$beef                                 CC BE EF
ldd   $0,s                                   EC 60
ldd   $0,u                                   EC 40
ldd   $0,x                                   EC 00
ldd   $0,y                                   EC 20
ldd   $01,pc                                 EC 8C 01
ldd   $01,pc                                 EC AC 01
ldd   $01,pc                                 EC CC 01
ldd   $01,pc                                 EC EC 01
ldd   $01,s                                  EC E8 01
ldd   $01,u                                  EC C8 01
ldd   $01,x                                  EC 88 01
ldd   $01,y                                  EC A8 01
ldd   $1,s                                   EC 61
ldd   $1,u                                   EC 41
ldd   $1,x                                   EC 01
ldd   $1,y                                   EC 21
ldd   $2,s                                   EC 62
ldd   $2,u                                   EC 42
ldd   $2,x                                   EC 02
ldd   $2,y                                   EC 22
ldd   $3,s                                   EC 63
ldd   $3,u                                   EC 43
ldd   $3,x                                   EC 03
ldd   $3,y                                   EC 23
ldd   $4,s                                   EC 64
ldd   $4,u                                   EC 44
ldd   $4,x                                   EC 04
ldd   $4,y                                   EC 24
ldd   $5,s                                   EC 65
ldd   $5,u                                   EC 45
ldd   $5,x                                   EC 05
ldd   $5,y                                   EC 25
ldd   $6,s                                   EC 66
ldd   $6,u                                   EC 46
ldd   $6,x                                   EC 06
ldd   $6,y                                   EC 26
ldd   $7,s                                   EC 67
ldd   $7,u                                   EC 47
ldd   $7,x                                   EC 07
ldd   $7,y                                   EC 27
ldd   $8,s                                   EC 68
ldd   $8,u                                   EC 48
ldd   $8,x                                   EC 08
ldd   $8,y                                   EC 28
ldd   $9,s                                   EC 69
ldd   $9,u                                   EC 49
ldd   $9,x                                   EC 09
ldd   $9,y                                   EC 29
ldd   $a,s                                   EC 6A
ldd   $a,u                                   EC 4A
ldd   $a,x                                   EC 0A
ldd   $a,y                                   EC 2A
ldd   $b,s                                   EC 6B
ldd   $b,u                                   EC 4B
ldd   $b,x                                   EC 0B
ldd   $b,y                                   EC 2B
ldd   $beef                                  EC 8F BE EF
ldd   $beef                                  EC AF BE EF
ldd   $beef                                  EC CF BE EF
ldd   $beef                                  EC EF BE EF
ldd   $beef                                  FC BE EF
ldd   $beef,pc                               EC 8D BE EF
ldd   $beef,pc                               EC AD BE EF
ldd   $beef,pc                               EC CD BE EF
ldd   $beef,pc                               EC ED BE EF
ldd   $beef,s                                EC E9 BE EF
ldd   $beef,u                                EC C9 BE EF
ldd   $beef,x                                EC 89 BE EF
ldd   $beef,y                                EC A9 BE EF
ldd   $c,s                                   EC 6C
ldd   $c,u                                   EC 4C
ldd   $c,x                                   EC 0C
ldd   $c,y                                   EC 2C
ldd   $d,s                                   EC 6D
ldd   $d,u                                   EC 4D
ldd   $d,x                                   EC 0D
ldd   $d,y                                   EC 2D
ldd   $e,s                                   EC 6E
ldd   $e,u                                   EC 4E
ldd   $e,x                                   EC 0E
ldd   $e,y                                   EC 2E
ldd   $f,s                                   EC 6F
ldd   $f,u                                   EC 4F
ldd   $f,x                                   EC 0F
ldd   $f,y                                   EC 2F
ldd   $ff                                    DC FF
ldd   ,--s                                   EC E3
ldd   ,--u                                   EC C3
ldd   ,--x                                   EC 83
ldd   ,--y                                   EC A3
ldd   ,-s                                    EC E2
ldd   ,-u                                    EC C2
ldd   ,-x                                    EC 82
ldd   ,-y                                    EC A2
ldd   ,s                                     EC E4
ldd   ,s+                                    EC E0
ldd   ,s++                                   EC E1
ldd   ,u                                     EC C4
ldd   ,u+                                    EC C0
ldd   ,u++                                   EC C1
ldd   ,x                                     EC 84
ldd   ,x+                                    EC 80
ldd   ,x++                                   EC 81
ldd   ,y                                     EC A4
ldd   ,y+                                    EC A0
ldd   ,y++                                   EC A1
ldd   -$1,s                                  EC 7F
ldd   -$1,u                                  EC 5F
ldd   -$1,x                                  EC 1F
ldd   -$1,y                                  EC 3F
ldd   -$10,s                                 EC 70
ldd   -$10,u                                 EC 50
ldd   -$10,x                                 EC 10
ldd   -$10,y                                 EC 30
ldd   -$2,s                                  EC 7E
ldd   -$2,u                                  EC 5E
ldd   -$2,x                                  EC 1E
ldd   -$2,y                                  EC 3E
ldd   -$3,s                                  EC 7D
ldd   -$3,u                                  EC 5D
ldd   -$3,x                                  EC 1D
ldd   -$3,y                                  EC 3D
ldd   -$4,s                                  EC 7C
ldd   -$4,u                                  EC 5C
ldd   -$4,x                                  EC 1C
ldd   -$4,y                                  EC 3C
ldd   -$5,s                                  EC 7B
ldd   -$5,u                                  EC 5B
ldd   -$5,x                                  EC 1B
ldd   -$5,y                                  EC 3B
ldd   -$6,s                                  EC 7A
ldd   -$6,u                                  EC 5A
ldd   -$6,x                                  EC 1A
ldd   -$6,y                                  EC 3A
ldd   -$7,s                                  EC 79
ldd   -$7,u                                  EC 59
ldd   -$7,x                                  EC 19
ldd   -$7,y                                  EC 39
ldd   -$8,s                                  EC 78
ldd   -$8,u                                  EC 58
ldd   -$8,x                                  EC 18
ldd   -$8,y                                  EC 38
ldd   -$9,s                                  EC 77
ldd   -$9,u                                  EC 57
ldd   -$9,x                                  EC 17
ldd   -$9,y                                  EC 37
ldd   -$a,s                                  EC 76
ldd   -$a,u                                  EC 56
ldd   -$a,x                                  EC 16
ldd   -$a,y                                  EC 36
ldd   -$b,s                                  EC 75
ldd   -$b,u                                  EC 55
ldd   -$b,x                                  EC 15
ldd   -$b,y                                  EC 35
ldd   -$c,s                                  EC 74
ldd   -$c,u                                  EC 54
ldd   -$c,x                                  EC 14
ldd   -$c,y                                  EC 34
ldd   -$d,s                                  EC 73
ldd   -$d,u                                  EC 53
ldd   -$d,x                                  EC 13
ldd   -$d,y                                  EC 33
ldd   -$e,s                                  EC 72
ldd   -$e,u                                  EC 52
ldd   -$e,x                                  EC 12
ldd   -$e,y                                  EC 32
ldd   -$f,s                                  EC 71
ldd   -$f,u                                  EC 51
ldd   -$f,x                                  EC 11
ldd   -$f,y                                  EC 31
ldd   a,s                                    EC E6
ldd   a,u                                    EC C6
ldd   a,x                                    EC 86
ldd   a,y                                    EC A6
ldd   b,s                                    EC E5
ldd   b,u                                    EC C5
ldd   b,x                                    EC 85
ldd   b,y                                    EC A5
ldd   d,s                                    EC EB
ldd   d,u                                    EC CB
ldd   d,x                                    EC 8B
ldd   d,y                                    EC AB
ldd   [$01,pc]                               EC 9C 01
ldd   [$01,pc]                               EC BC 01
ldd   [$01,pc]                               EC DC 01
ldd   [$01,pc]                               EC FC 01
ldd   [$01,s]                                EC F8 01
ldd   [$01,u]                                EC D8 01
ldd   [$01,x]                                EC 98 01
ldd   [$01,y]                                EC B8 01
ldd   [$beef,pc]                             EC 9D BE EF
ldd   [$beef,pc]                             EC BD BE EF
ldd   [$beef,pc]                             EC DD BE EF
ldd   [$beef,pc]                             EC FD BE EF
ldd   [$beef,s]                              EC F9 BE EF
ldd   [$beef,u]                              EC D9 BE EF
ldd   [$beef,x]                              EC 99 BE EF
ldd   [$beef,y]                              EC B9 BE EF
ldd   [$beef]                                EC 9F BE EF
ldd   [$beef]                                EC BF BE EF
ldd   [$beef]                                EC DF BE EF
ldd   [$beef]                                EC FF BE EF
ldd   [,--s]                                 EC F3
ldd   [,--u]                                 EC D3
ldd   [,--x]                                 EC 93
ldd   [,--y]                                 EC B3
ldd   [,s++]                                 EC F1
ldd   [,s]                                   EC F4
ldd   [,u++]                                 EC D1
ldd   [,u]                                   EC D4
ldd   [,x++]                                 EC 91
ldd   [,x]                                   EC 94
ldd   [,y++]                                 EC B1
ldd   [,y]                                   EC B4
ldd   [a,s]                                  EC F6
ldd   [a,u]                                  EC D6
ldd   [a,x]                                  EC 96
ldd   [a,y]                                  EC B6
ldd   [b,s]                                  EC F5
ldd   [b,u]                                  EC D5
ldd   [b,x]                                  EC 95
ldd   [b,y]                                  EC B5
ldd   [d,s]                                  EC FB
ldd   [d,u]                                  EC DB
ldd   [d,x]                                  EC 9B
ldd   [d,y]                                  EC BB
ldd   []                                     EC 97
ldd   []                                     EC 9A
ldd   []                                     EC 9E
ldd   []                                     EC B7
ldd   []                                     EC BA
ldd   []                                     EC BE
ldd   []                                     EC D7
ldd   []                                     EC DA
ldd   []                                     EC DE
ldd   []                                     EC F7
ldd   []                                     EC FA
ldd   []                                     EC FE
lds   #$beef                                 10 CE BE EF
lds   $01                                    10 DE 01
lds   $1,x                                   10 EE 01
lds   $beef                                  10 FE BE EF
ldu   #$beef                                 CE BE EF
ldu   $0,s                                   EE 60
ldu   $0,u                                   EE 40
ldu   $0,x                                   EE 00
ldu   $0,y                                   EE 20
ldu   $01,pc                                 EE 8C 01
ldu   $01,pc                                 EE AC 01
ldu   $01,pc                                 EE CC 01
ldu   $01,pc                                 EE EC 01
ldu   $01,s                                  EE E8 01
ldu   $01,u                                  EE C8 01
ldu   $01,x                                  EE 88 01
ldu   $01,y                                  EE A8 01
ldu   $1,s                                   EE 61
ldu   $1,u                                   EE 41
ldu   $1,x                                   EE 01
ldu   $1,y                                   EE 21
ldu   $2,s                                   EE 62
ldu   $2,u                                   EE 42
ldu   $2,x                                   EE 02
ldu   $2,y                                   EE 22
ldu   $3,s                                   EE 63
ldu   $3,u                                   EE 43
ldu   $3,x                                   EE 03
ldu   $3,y                                   EE 23
ldu   $4,s                                   EE 64
ldu   $4,u                                   EE 44
ldu   $4,x                                   EE 04
ldu   $4,y                                   EE 24
ldu   $5,s                                   EE 65
ldu   $5,u                                   EE 45
ldu   $5,x                                   EE 05
ldu   $5,y                                   EE 25
ldu   $6,s                                   EE 66
ldu   $6,u                                   EE 46
ldu   $6,x                                   EE 06
ldu   $6,y                                   EE 26
ldu   $7,s                                   EE 67
ldu   $7,u                                   EE 47
ldu   $7,x                                   EE 07
ldu   $7,y                                   EE 27
ldu   $8,s                                   EE 68
ldu   $8,u                                   EE 48
ldu   $8,x                                   EE 08
ldu   $8,y                                   EE 28
ldu   $9,s                                   EE 69
ldu   $9,u                                   EE 49
ldu   $9,x                                   EE 09
ldu   $9,y                                   EE 29
ldu   $a,s                                   EE 6A
ldu   $a,u                                   EE 4A
ldu   $a,x                                   EE 0A
ldu   $a,y                                   EE 2A
ldu   $b,s                                   EE 6B
ldu   $b,u                                   EE 4B
ldu   $b,x                                   EE 0B
ldu   $b,y                                   EE 2B
ldu   $beef                                  EE 8F BE EF
ldu   $beef                                  EE AF BE EF
ldu   $beef                                  EE CF BE EF
ldu   $beef                                  EE EF BE EF
ldu   $beef                                  FE BE EF
ldu   $beef,pc                               EE 8D BE EF
ldu   $beef,pc                               EE AD BE EF
ldu   $beef,pc                               EE CD BE EF
ldu   $beef,pc                               EE ED BE EF
ldu   $beef,s                                EE E9 BE EF
ldu   $beef,u                                EE C9 BE EF
ldu   $beef,x                                EE 89 BE EF
ldu   $beef,y                                EE A9 BE EF
ldu   $c,s                                   EE 6C
ldu   $c,u                                   EE 4C
ldu   $c,x                                   EE 0C
ldu   $c,y                                   EE 2C
ldu   $d,s                                   EE 6D
ldu   $d,u                                   EE 4D
ldu   $d,x                                   EE 0D
ldu   $d,y                                   EE 2D
ldu   $e,s                                   EE 6E
ldu   $e,u                                   EE 4E
ldu   $e,x                                   EE 0E
ldu   $e,y                                   EE 2E
ldu   $f,s                                   EE 6F
ldu   $f,u                                   EE 4F
ldu   $f,x                                   EE 0F
ldu   $f,y                                   EE 2F
ldu   $ff                                    DE FF
ldu   ,--s                                   EE E3
ldu   ,--u                                   EE C3
ldu   ,--x                                   EE 83
ldu   ,--y                                   EE A3
ldu   ,-s                                    EE E2
ldu   ,-u                                    EE C2
ldu   ,-x                                    EE 82
ldu   ,-y                                    EE A2
ldu   ,s                                     EE E4
ldu   ,s+                                    EE E0
ldu   ,s++                                   EE E1
ldu   ,u                                     EE C4
ldu   ,u+                                    EE C0
ldu   ,u++                                   EE C1
ldu   ,x                                     EE 84
ldu   ,x+                                    EE 80
ldu   ,x++                                   EE 81
ldu   ,y                                     EE A4
ldu   ,y+                                    EE A0
ldu   ,y++                                   EE A1
ldu   -$1,s                                  EE 7F
ldu   -$1,u                                  EE 5F
ldu   -$1,x                                  EE 1F
ldu   -$1,y                                  EE 3F
ldu   -$10,s                                 EE 70
ldu   -$10,u                                 EE 50
ldu   -$10,x                                 EE 10
ldu   -$10,y                                 EE 30
ldu   -$2,s                                  EE 7E
ldu   -$2,u                                  EE 5E
ldu   -$2,x                                  EE 1E
ldu   -$2,y                                  EE 3E
ldu   -$3,s                                  EE 7D
ldu   -$3,u                                  EE 5D
ldu   -$3,x                                  EE 1D
ldu   -$3,y                                  EE 3D
ldu   -$4,s                                  EE 7C
ldu   -$4,u                                  EE 5C
ldu   -$4,x                                  EE 1C
ldu   -$4,y                                  EE 3C
ldu   -$5,s                                  EE 7B
ldu   -$5,u                                  EE 5B
ldu   -$5,x                                  EE 1B
ldu   -$5,y                                  EE 3B
ldu   -$6,s                                  EE 7A
ldu   -$6,u                                  EE 5A
ldu   -$6,x                                  EE 1A
ldu   -$6,y                                  EE 3A
ldu   -$7,s                                  EE 79
ldu   -$7,u                                  EE 59
ldu   -$7,x                                  EE 19
ldu   -$7,y                                  EE 39
ldu   -$8,s                                  EE 78
ldu   -$8,u                                  EE 58
ldu   -$8,x                                  EE 18
ldu   -$8,y                                  EE 38
ldu   -$9,s                                  EE 77
ldu   -$9,u                                  EE 57
ldu   -$9,x                                  EE 17
ldu   -$9,y                                  EE 37
ldu   -$a,s                                  EE 76
ldu   -$a,u                                  EE 56
ldu   -$a,x                                  EE 16
ldu   -$a,y                                  EE 36
ldu   -$b,s                                  EE 75
ldu   -$b,u                                  EE 55
ldu   -$b,x                                  EE 15
ldu   -$b,y                                  EE 35
ldu   -$c,s                                  EE 74
ldu   -$c,u                                  EE 54
ldu   -$c,x                                  EE 14
ldu   -$c,y                                  EE 34
ldu   -$d,s                                  EE 73
ldu   -$d,u                                  EE 53
ldu   -$d,x                                  EE 13
ldu   -$d,y                                  EE 33
ldu   -$e,s                                  EE 72
ldu   -$e,u                                  EE 52
ldu   -$e,x                                  EE 12
ldu   -$e,y                                  EE 32
ldu   -$f,s                                  EE 71
ldu   -$f,u                                  EE 51
ldu   -$f,x                                  EE 11
ldu   -$f,y                                  EE 31
ldu   a,s                                    EE E6
ldu   a,u                                    EE C6
ldu   a,x                                    EE 86
ldu   a,y                                    EE A6
ldu   b,s                                    EE E5
ldu   b,u                                    EE C5
ldu   b,x                                    EE 85
ldu   b,y                                    EE A5
ldu   d,s                                    EE EB
ldu   d,u                                    EE CB
ldu   d,x                                    EE 8B
ldu   d,y                                    EE AB
ldu   [$01,pc]                               EE 9C 01
ldu   [$01,pc]                               EE BC 01
ldu   [$01,pc]                               EE DC 01
ldu   [$01,pc]                               EE FC 01
ldu   [$01,s]                                EE F8 01
ldu   [$01,u]                                EE D8 01
ldu   [$01,x]                                EE 98 01
ldu   [$01,y]                                EE B8 01
ldu   [$beef,pc]                             EE 9D BE EF
ldu   [$beef,pc]                             EE BD BE EF
ldu   [$beef,pc]                             EE DD BE EF
ldu   [$beef,pc]                             EE FD BE EF
ldu   [$beef,s]                              EE F9 BE EF
ldu   [$beef,u]                              EE D9 BE EF
ldu   [$beef,x]                              EE 99 BE EF
ldu   [$beef,y]                              EE B9 BE EF
ldu   [$beef]                                EE 9F BE EF
ldu   [$beef]                                EE BF BE EF
ldu   [$beef]                                EE DF BE EF
ldu   [$beef]                                EE FF BE EF
ldu   [,--s]                                 EE F3
ldu   [,--u]                                 EE D3
ldu   [,--x]                                 EE 93
ldu   [,--y]                                 EE B3
ldu   [,s++]                                 EE F1
ldu   [,s]                                   EE F4
ldu   [,u++]                                 EE D1
ldu   [,u]                                   EE D4
ldu   [,x++]                                 EE 91
ldu   [,x]                                   EE 94
ldu   [,y++]                                 EE B1
ldu   [,y]                                   EE B4
ldu   [a,s]                                  EE F6
ldu   [a,u]                                  EE D6
ldu   [a,x]                                  EE 96
ldu   [a,y]                                  EE B6
ldu   [b,s]                                  EE F5
ldu   [b,u]                                  EE D5
ldu   [b,x]                                  EE 95
ldu   [b,y]                                  EE B5
ldu   [d,s]                                  EE FB
ldu   [d,u]                                  EE DB
ldu   [d,x]                                  EE 9B
ldu   [d,y]                                  EE BB
ldu   []                                     EE 97
ldu   []                                     EE 9A
ldu   []                                     EE 9E
ldu   []                                     EE B7
ldu   []                                     EE BA
ldu   []                                     EE BE
ldu   []                                     EE D7
ldu   []                                     EE DA
ldu   []                                     EE DE
ldu   []                                     EE F7
ldu   []                                     EE FA
ldu   []                                     EE FE
ldx   #$beef                                 8E BE EF
ldx   $0,s                                   AE 60
ldx   $0,u                                   AE 40
ldx   $0,x                                   AE 00
ldx   $0,y                                   AE 20
ldx   $01,pc                                 AE 8C 01
ldx   $01,pc                                 AE AC 01
ldx   $01,pc                                 AE CC 01
ldx   $01,pc                                 AE EC 01
ldx   $01,s                                  AE E8 01
ldx   $01,u                                  AE C8 01
ldx   $01,x                                  AE 88 01
ldx   $01,y                                  AE A8 01
ldx   $1,s                                   AE 61
ldx   $1,u                                   AE 41
ldx   $1,x                                   AE 01
ldx   $1,y                                   AE 21
ldx   $2,s                                   AE 62
ldx   $2,u                                   AE 42
ldx   $2,x                                   AE 02
ldx   $2,y                                   AE 22
ldx   $3,s                                   AE 63
ldx   $3,u                                   AE 43
ldx   $3,x                                   AE 03
ldx   $3,y                                   AE 23
ldx   $4,s                                   AE 64
ldx   $4,u                                   AE 44
ldx   $4,x                                   AE 04
ldx   $4,y                                   AE 24
ldx   $5,s                                   AE 65
ldx   $5,u                                   AE 45
ldx   $5,x                                   AE 05
ldx   $5,y                                   AE 25
ldx   $6,s                                   AE 66
ldx   $6,u                                   AE 46
ldx   $6,x                                   AE 06
ldx   $6,y                                   AE 26
ldx   $7,s                                   AE 67
ldx   $7,u                                   AE 47
ldx   $7,x                                   AE 07
ldx   $7,y                                   AE 27
ldx   $8,s                                   AE 68
ldx   $8,u                                   AE 48
ldx   $8,x                                   AE 08
ldx   $8,y                                   AE 28
ldx   $9,s                                   AE 69
ldx   $9,u                                   AE 49
ldx   $9,x                                   AE 09
ldx   $9,y                                   AE 29
ldx   $a,s                                   AE 6A
ldx   $a,u                                   AE 4A
ldx   $a,x                                   AE 0A
ldx   $a,y                                   AE 2A
ldx   $b,s                                   AE 6B
ldx   $b,u                                   AE 4B
ldx   $b,x                                   AE 0B
ldx   $b,y                                   AE 2B
ldx   $beef                                  AE 8F BE EF
ldx   $beef                                  AE AF BE EF
ldx   $beef                                  AE CF BE EF
ldx   $beef                                  AE EF BE EF
ldx   $beef                                  BE BE EF
ldx   $beef,pc                               AE 8D BE EF
ldx   $beef,pc                               AE AD BE EF
ldx   $beef,pc                               AE CD BE EF
ldx   $beef,pc                               AE ED BE EF
ldx   $beef,s                                AE E9 BE EF
ldx   $beef,u                                AE C9 BE EF
ldx   $beef,x                                AE 89 BE EF
ldx   $beef,y                                AE A9 BE EF
ldx   $c,s                                   AE 6C
ldx   $c,u                                   AE 4C
ldx   $c,x                                   AE 0C
ldx   $c,y                                   AE 2C
ldx   $d,s                                   AE 6D
ldx   $d,u                                   AE 4D
ldx   $d,x                                   AE 0D
ldx   $d,y                                   AE 2D
ldx   $e,s                                   AE 6E
ldx   $e,u                                   AE 4E
ldx   $e,x                                   AE 0E
ldx   $e,y                                   AE 2E
ldx   $f,s                                   AE 6F
ldx   $f,u                                   AE 4F
ldx   $f,x                                   AE 0F
ldx   $f,y                                   AE 2F
ldx   $ff                                    9E FF
ldx   ,--s                                   AE E3
ldx   ,--u                                   AE C3
ldx   ,--x                                   AE 83
ldx   ,--y                                   AE A3
ldx   ,-s                                    AE E2
ldx   ,-u                                    AE C2
ldx   ,-x                                    AE 82
ldx   ,-y                                    AE A2
ldx   ,s                                     AE E4
ldx   ,s+                                    AE E0
ldx   ,s++                                   AE E1
ldx   ,u                                     AE C4
ldx   ,u+                                    AE C0
ldx   ,u++                                   AE C1
ldx   ,x                                     AE 84
ldx   ,x+                                    AE 80
ldx   ,x++                                   AE 81
ldx   ,y                                     AE A4
ldx   ,y+                                    AE A0
ldx   ,y++                                   AE A1
ldx   -$1,s                                  AE 7F
ldx   -$1,u                                  AE 5F
ldx   -$1,x                                  AE 1F
ldx   -$1,y                                  AE 3F
ldx   -$10,s                                 AE 70
ldx   -$10,u                                 AE 50
ldx   -$10,x                                 AE 10
ldx   -$10,y                                 AE 30
ldx   -$2,s                                  AE 7E
ldx   -$2,u                                  AE 5E
ldx   -$2,x                                  AE 1E
ldx   -$2,y                                  AE 3E
ldx   -$3,s                                  AE 7D
ldx   -$3,u                                  AE 5D
ldx   -$3,x                                  AE 1D
ldx   -$3,y                                  AE 3D
ldx   -$4,s                                  AE 7C
ldx   -$4,u                                  AE 5C
ldx   -$4,x                                  AE 1C
ldx   -$4,y                                  AE 3C
ldx   -$5,s                                  AE 7B
ldx   -$5,u                                  AE 5B
ldx   -$5,x                                  AE 1B
ldx   -$5,y                                  AE 3B
ldx   -$6,s                                  AE 7A
ldx   -$6,u                                  AE 5A
ldx   -$6,x                                  AE 1A
ldx   -$6,y                                  AE 3A
ldx   -$7,s                                  AE 79
ldx   -$7,u                                  AE 59
ldx   -$7,x                                  AE 19
ldx   -$7,y                                  AE 39
ldx   -$8,s                                  AE 78
ldx   -$8,u                                  AE 58
ldx   -$8,x                                  AE 18
ldx   -$8,y                                  AE 38
ldx   -$9,s                                  AE 77
ldx   -$9,u                                  AE 57
ldx   -$9,x                                  AE 17
ldx   -$9,y                                  AE 37
ldx   -$a,s                                  AE 76
ldx   -$a,u                                  AE 56
ldx   -$a,x                                  AE 16
ldx   -$a,y                                  AE 36
ldx   -$b,s                                  AE 75
ldx   -$b,u                                  AE 55
ldx   -$b,x                                  AE 15
ldx   -$b,y                                  AE 35
ldx   -$c,s                                  AE 74
ldx   -$c,u                                  AE 54
ldx   -$c,x                                  AE 14
ldx   -$c,y                                  AE 34
ldx   -$d,s                                  AE 73
ldx   -$d,u                                  AE 53
ldx   -$d,x                                  AE 13
ldx   -$d,y                                  AE 33
ldx   -$e,s                                  AE 72
ldx   -$e,u                                  AE 52
ldx   -$e,x                                  AE 12
ldx   -$e,y                                  AE 32
ldx   -$f,s                                  AE 71
ldx   -$f,u                                  AE 51
ldx   -$f,x                                  AE 11
ldx   -$f,y                                  AE 31
ldx   a,s                                    AE E6
ldx   a,u                                    AE C6
ldx   a,x                                    AE 86
ldx   a,y                                    AE A6
ldx   b,s                                    AE E5
ldx   b,u                                    AE C5
ldx   b,x                                    AE 85
ldx   b,y                                    AE A5
ldx   d,s                                    AE EB
ldx   d,u                                    AE CB
ldx   d,x                                    AE 8B
ldx   d,y                                    AE AB
ldx   [$01,pc]                               AE 9C 01
ldx   [$01,pc]                               AE BC 01
ldx   [$01,pc]                               AE DC 01
ldx   [$01,pc]                               AE FC 01
ldx   [$01,s]                                AE F8 01
ldx   [$01,u]                                AE D8 01
ldx   [$01,x]                                AE 98 01
ldx   [$01,y]                                AE B8 01
ldx   [$beef,pc]                             AE 9D BE EF
ldx   [$beef,pc]                             AE BD BE EF
ldx   [$beef,pc]                             AE DD BE EF
ldx   [$beef,pc]                             AE FD BE EF
ldx   [$beef,s]                              AE F9 BE EF
ldx   [$beef,u]                              AE D9 BE EF
ldx   [$beef,x]                              AE 99 BE EF
ldx   [$beef,y]                              AE B9 BE EF
ldx   [$beef]                                AE 9F BE EF
ldx   [$beef]                                AE BF BE EF
ldx   [$beef]                                AE DF BE EF
ldx   [$beef]                                AE FF BE EF
ldx   [,--s]                                 AE F3
ldx   [,--u]                                 AE D3
ldx   [,--x]                                 AE 93
ldx   [,--y]                                 AE B3
ldx   [,s++]                                 AE F1
ldx   [,s]                                   AE F4
ldx   [,u++]                                 AE D1
ldx   [,u]                                   AE D4
ldx   [,x++]                                 AE 91
ldx   [,x]                                   AE 94
ldx   [,y++]                                 AE B1
ldx   [,y]                                   AE B4
ldx   [a,s]                                  AE F6
ldx   [a,u]                                  AE D6
ldx   [a,x]                                  AE 96
ldx   [a,y]                                  AE B6
ldx   [b,s]                                  AE F5
ldx   [b,u]                                  AE D5
ldx   [b,x]                                  AE 95
ldx   [b,y]                                  AE B5
ldx   [d,s]                                  AE FB
ldx   [d,u]                                  AE DB
ldx   [d,x]                                  AE 9B
ldx   [d,y]                                  AE BB
ldx   []                                     AE 97
ldx   []                                     AE 9A
ldx   []                                     AE 9E
ldx   []                                     AE B7
ldx   []                                     AE BA
ldx   []                                     AE BE
ldx   []                                     AE D7
ldx   []                                     AE DA
ldx   []                                     AE DE
ldx   []                                     AE F7
ldx   []                                     AE FA
ldx   []                                     AE FE
ldy   #$beef                                 10 8E BE EF
ldy   $01                                    10 9E 01
ldy   $1,x                                   10 AE 01
ldy   $beef                                  10 BE BE EF
leas  $0,s                                   32 60
leas  $0,u                                   32 40
leas  $0,x                                   32 00
leas  $0,y                                   32 20
leas  $01,pc                                 32 8C 01
leas  $01,pc                                 32 AC 01
leas  $01,pc                                 32 CC 01
leas  $01,pc                                 32 EC 01
leas  $01,s                                  32 E8 01
leas  $01,u                                  32 C8 01
leas  $01,x                                  32 88 01
leas  $01,y                                  32 A8 01
leas  $1,s                                   32 61
leas  $1,u                                   32 41
leas  $1,x                                   32 01
leas  $1,y                                   32 21
leas  $2,s                                   32 62
leas  $2,u                                   32 42
leas  $2,x                                   32 02
leas  $2,y                                   32 22
leas  $3,s                                   32 63
leas  $3,u                                   32 43
leas  $3,x                                   32 03
leas  $3,y                                   32 23
leas  $4,s                                   32 64
leas  $4,u                                   32 44
leas  $4,x                                   32 04
leas  $4,y                                   32 24
leas  $5,s                                   32 65
leas  $5,u                                   32 45
leas  $5,x                                   32 05
leas  $5,y                                   32 25
leas  $6,s                                   32 66
leas  $6,u                                   32 46
leas  $6,x                                   32 06
leas  $6,y                                   32 26
leas  $7,s                                   32 67
leas  $7,u                                   32 47
leas  $7,x                                   32 07
leas  $7,y                                   32 27
leas  $8,s                                   32 68
leas  $8,u                                   32 48
leas  $8,x                                   32 08
leas  $8,y                                   32 28
leas  $9,s                                   32 69
leas  $9,u                                   32 49
leas  $9,x                                   32 09
leas  $9,y                                   32 29
leas  $a,s                                   32 6A
leas  $a,u                                   32 4A
leas  $a,x                                   32 0A
leas  $a,y                                   32 2A
leas  $b,s                                   32 6B
leas  $b,u                                   32 4B
leas  $b,x                                   32 0B
leas  $b,y                                   32 2B
leas  $beef                                  32 8F BE EF
leas  $beef                                  32 AF BE EF
leas  $beef                                  32 CF BE EF
leas  $beef                                  32 EF BE EF
leas  $beef,pc                               32 8D BE EF
leas  $beef,pc                               32 AD BE EF
leas  $beef,pc                               32 CD BE EF
leas  $beef,pc                               32 ED BE EF
leas  $beef,s                                32 E9 BE EF
leas  $beef,u                                32 C9 BE EF
leas  $beef,x                                32 89 BE EF
leas  $beef,y                                32 A9 BE EF
leas  $c,s                                   32 6C
leas  $c,u                                   32 4C
leas  $c,x                                   32 0C
leas  $c,y                                   32 2C
leas  $d,s                                   32 6D
leas  $d,u                                   32 4D
leas  $d,x                                   32 0D
leas  $d,y                                   32 2D
leas  $e,s                                   32 6E
leas  $e,u                                   32 4E
leas  $e,x                                   32 0E
leas  $e,y                                   32 2E
leas  $f,s                                   32 6F
leas  $f,u                                   32 4F
leas  $f,x                                   32 0F
leas  $f,y                                   32 2F
leas  ,--s                                   32 E3
leas  ,--u                                   32 C3
leas  ,--x                                   32 83
leas  ,--y                                   32 A3
leas  ,-s                                    32 E2
leas  ,-u                                    32 C2
leas  ,-x                                    32 82
leas  ,-y                                    32 A2
leas  ,s                                     32 E4
leas  ,s+                                    32 E0
leas  ,s++                                   32 E1
leas  ,u                                     32 C4
leas  ,u+                                    32 C0
leas  ,u++                                   32 C1
leas  ,x                                     32 84
leas  ,x+                                    32 80
leas  ,x++                                   32 81
leas  ,y                                     32 A4
leas  ,y+                                    32 A0
leas  ,y++                                   32 A1
leas  -$1,s                                  32 7F
leas  -$1,u                                  32 5F
leas  -$1,x                                  32 1F
leas  -$1,y                                  32 3F
leas  -$10,s                                 32 70
leas  -$10,u                                 32 50
leas  -$10,x                                 32 10
leas  -$10,y                                 32 30
leas  -$2,s                                  32 7E
leas  -$2,u                                  32 5E
leas  -$2,x                                  32 1E
leas  -$2,y                                  32 3E
leas  -$3,s                                  32 7D
leas  -$3,u                                  32 5D
leas  -$3,x                                  32 1D
leas  -$3,y                                  32 3D
leas  -$4,s                                  32 7C
leas  -$4,u                                  32 5C
leas  -$4,x                                  32 1C
leas  -$4,y                                  32 3C
leas  -$5,s                                  32 7B
leas  -$5,u                                  32 5B
leas  -$5,x                                  32 1B
leas  -$5,y                                  32 3B
leas  -$6,s                                  32 7A
leas  -$6,u                                  32 5A
leas  -$6,x                                  32 1A
leas  -$6,y                                  32 3A
leas  -$7,s                                  32 79
leas  -$7,u                                  32 59
leas  -$7,x                                  32 19
leas  -$7,y                                  32 39
leas  -$8,s                                  32 78
leas  -$8,u                                  32 58
leas  -$8,x                                  32 18
leas  -$8,y                                  32 38
leas  -$9,s                                  32 77
leas  -$9,u                                  32 57
leas  -$9,x                                  32 17
leas  -$9,y                                  32 37
leas  -$a,s                                  32 76
leas  -$a,u                                  32 56
leas  -$a,x                                  32 16
leas  -$a,y                                  32 36
leas  -$b,s                                  32 75
leas  -$b,u                                  32 55
leas  -$b,x                                  32 15
leas  -$b,y                                  32 35
leas  -$c,s                                  32 74
leas  -$c,u                                  32 54
leas  -$c,x                                  32 14
leas  -$c,y                                  32 34
leas  -$d,s                                  32 73
leas  -$d,u                                  32 53
leas  -$d,x                                  32 13
leas  -$d,y                                  32 33
leas  -$e,s                                  32 72
leas  -$e,u                                  32 52
leas  -$e,x                                  32 12
leas  -$e,y                                  32 32
leas  -$f,s                                  32 71
leas  -$f,u                                  32 51
leas  -$f,x                                  32 11
leas  -$f,y                                  32 31
leas  a,s                                    32 E6
leas  a,u                                    32 C6
leas  a,x                                    32 86
leas  a,y                                    32 A6
leas  b,s                                    32 E5
leas  b,u                                    32 C5
leas  b,x                                    32 85
leas  b,y                                    32 A5
leas  d,s                                    32 EB
leas  d,u                                    32 CB
leas  d,x                                    32 8B
leas  d,y                                    32 AB
leas  [$01,pc]                               32 9C 01
leas  [$01,pc]                               32 BC 01
leas  [$01,pc]                               32 DC 01
leas  [$01,pc]                               32 FC 01
leas  [$01,s]                                32 F8 01
leas  [$01,u]                                32 D8 01
leas  [$01,x]                                32 98 01
leas  [$01,y]                                32 B8 01
leas  [$beef,pc]                             32 9D BE EF
leas  [$beef,pc]                             32 BD BE EF
leas  [$beef,pc]                             32 DD BE EF
leas  [$beef,pc]                             32 FD BE EF
leas  [$beef,s]                              32 F9 BE EF
leas  [$beef,u]                              32 D9 BE EF
leas  [$beef,x]                              32 99 BE EF
leas  [$beef,y]                              32 B9 BE EF
leas  [$beef]                                32 9F BE EF
leas  [$beef]                                32 BF BE EF
leas  [$beef]                                32 DF BE EF
leas  [$beef]                                32 FF BE EF
leas  [,--s]                                 32 F3
leas  [,--u]                                 32 D3
leas  [,--x]                                 32 93
leas  [,--y]                                 32 B3
leas  [,s++]                                 32 F1
leas  [,s]                                   32 F4
leas  [,u++]                                 32 D1
leas  [,u]                                   32 D4
leas  [,x++]                                 32 91
leas  [,x]                                   32 94
leas  [,y++]                                 32 B1
leas  [,y]                                   32 B4
leas  [a,s]                                  32 F6
leas  [a,u]                                  32 D6
leas  [a,x]                                  32 96
leas  [a,y]                                  32 B6
leas  [b,s]                                  32 F5
leas  [b,u]                                  32 D5
leas  [b,x]                                  32 95
leas  [b,y]                                  32 B5
leas  [d,s]                                  32 FB
leas  [d,u]                                  32 DB
leas  [d,x]                                  32 9B
leas  [d,y]                                  32 BB
leas  []                                     32 97
leas  []                                     32 9A
leas  []                                     32 9E
leas  []                                     32 B7
leas  []                                     32 BA
leas  []                                     32 BE
leas  []                                     32 D7
leas  []                                     32 DA
leas  []                                     32 DE
leas  []                                     32 F7
leas  []                                     32 FA
leas  []                                     32 FE
leau  $0,s                                   33 60
leau  $0,u                                   33 40
leau  $0,x                                   33 00
leau  $0,y                                   33 20
leau  $01,pc                                 33 8C 01
leau  $01,pc                                 33 AC 01
leau  $01,pc                                 33 CC 01
leau  $01,pc                                 33 EC 01
leau  $01,s                                  33 E8 01
leau  $01,u                                  33 C8 01
leau  $01,x                                  33 88 01
leau  $01,y                                  33 A8 01
leau  $1,s                                   33 61
leau  $1,u                                   33 41
leau  $1,x                                   33 01
leau  $1,y                                   33 21
leau  $2,s                                   33 62
leau  $2,u                                   33 42
leau  $2,x                                   33 02
leau  $2,y                                   33 22
leau  $3,s                                   33 63
leau  $3,u                                   33 43
leau  $3,x                                   33 03
leau  $3,y                                   33 23
leau  $4,s                                   33 64
leau  $4,u                                   33 44
leau  $4,x                                   33 04
leau  $4,y                                   33 24
leau  $5,s                                   33 65
leau  $5,u                                   33 45
leau  $5,x                                   33 05
leau  $5,y                                   33 25
leau  $6,s                                   33 66
leau  $6,u                                   33 46
leau  $6,x                                   33 06
leau  $6,y                                   33 26
leau  $7,s                                   33 67
leau  $7,u                                   33 47
leau  $7,x                                   33 07
leau  $7,y                                   33 27
leau  $8,s                                   33 68
leau  $8,u                                   33 48
leau  $8,x                                   33 08
leau  $8,y                                   33 28
leau  $9,s                                   33 69
leau  $9,u                                   33 49
leau  $9,x                                   33 09
leau  $9,y                                   33 29
leau  $a,s                                   33 6A
leau  $a,u                                   33 4A
leau  $a,x                                   33 0A
leau  $a,y                                   33 2A
leau  $b,s                                   33 6B
leau  $b,u                                   33 4B
leau  $b,x                                   33 0B
leau  $b,y                                   33 2B
leau  $beef                                  33 8F BE EF
leau  $beef                                  33 AF BE EF
leau  $beef                                  33 CF BE EF
leau  $beef                                  33 EF BE EF
leau  $beef,pc                               33 8D BE EF
leau  $beef,pc                               33 AD BE EF
leau  $beef,pc                               33 CD BE EF
leau  $beef,pc                               33 ED BE EF
leau  $beef,s                                33 E9 BE EF
leau  $beef,u                                33 C9 BE EF
leau  $beef,x                                33 89 BE EF
leau  $beef,y                                33 A9 BE EF
leau  $c,s                                   33 6C
leau  $c,u                                   33 4C
leau  $c,x                                   33 0C
leau  $c,y                                   33 2C
leau  $d,s                                   33 6D
leau  $d,u                                   33 4D
leau  $d,x                                   33 0D
leau  $d,y                                   33 2D
leau  $e,s                                   33 6E
leau  $e,u                                   33 4E
leau  $e,x                                   33 0E
leau  $e,y                                   33 2E
leau  $f,s                                   33 6F
leau  $f,u                                   33 4F
leau  $f,x                                   33 0F
leau  $f,y                                   33 2F
leau  ,--s                                   33 E3
leau  ,--u                                   33 C3
leau  ,--x                                   33 83
leau  ,--y                                   33 A3
leau  ,-s                                    33 E2
leau  ,-u                                    33 C2
leau  ,-x                                    33 82
leau  ,-y                                    33 A2
leau  ,s                                     33 E4
leau  ,s+                                    33 E0
leau  ,s++                                   33 E1
leau  ,u                                     33 C4
leau  ,u+                                    33 C0
leau  ,u++                                   33 C1
leau  ,x                                     33 84
leau  ,x+                                    33 80
leau  ,x++                                   33 81
leau  ,y                                     33 A4
leau  ,y+                                    33 A0
leau  ,y++                                   33 A1
leau  -$1,s                                  33 7F
leau  -$1,u                                  33 5F
leau  -$1,x                                  33 1F
leau  -$1,y                                  33 3F
leau  -$10,s                                 33 70
leau  -$10,u                                 33 50
leau  -$10,x                                 33 10
leau  -$10,y                                 33 30
leau  -$2,s                                  33 7E
leau  -$2,u                                  33 5E
leau  -$2,x                                  33 1E
leau  -$2,y                                  33 3E
leau  -$3,s                                  33 7D
leau  -$3,u                                  33 5D
leau  -$3,x                                  33 1D
leau  -$3,y                                  33 3D
leau  -$4,s                                  33 7C
leau  -$4,u                                  33 5C
leau  -$4,x                                  33 1C
leau  -$4,y                                  33 3C
leau  -$5,s                                  33 7B
leau  -$5,u                                  33 5B
leau  -$5,x                                  33 1B
leau  -$5,y                                  33 3B
leau  -$6,s                                  33 7A
leau  -$6,u                                  33 5A
leau  -$6,x                                  33 1A
leau  -$6,y                                  33 3A
leau  -$7,s                                  33 79
leau  -$7,u                                  33 59
leau  -$7,x                                  33 19
leau  -$7,y                                  33 39
leau  -$8,s                                  33 78
leau  -$8,u                                  33 58
leau  -$8,x                                  33 18
leau  -$8,y                                  33 38
leau  -$9,s                                  33 77
leau  -$9,u                                  33 57
leau  -$9,x                                  33 17
leau  -$9,y                                  33 37
leau  -$a,s                                  33 76
leau  -$a,u                                  33 56
leau  -$a,x                                  33 16
leau  -$a,y                                  33 36
leau  -$b,s                                  33 75
leau  -$b,u                                  33 55
leau  -$b,x                                  33 15
leau  -$b,y                                  33 35
leau  -$c,s                                  33 74
leau  -$c,u                                  33 54
leau  -$c,x                                  33 14
leau  -$c,y                                  33 34
leau  -$d,s                                  33 73
leau  -$d,u                                  33 53
leau  -$d,x                                  33 13
leau  -$d,y                                  33 33
leau  -$e,s                                  33 72
leau  -$e,u                                  33 52
leau  -$e,x                                  33 12
leau  -$e,y                                  33 32
leau  -$f,s                                  33 71
leau  -$f,u                                  33 51
leau  -$f,x                                  33 11
leau  -$f,y                                  33 31
leau  a,s                                    33 E6
leau  a,u                                    33 C6
leau  a,x                                    33 86
leau  a,y                                    33 A6
leau  b,s                                    33 E5
leau  b,u                                    33 C5
leau  b,x                                    33 85
leau  b,y                                    33 A5
leau  d,s                                    33 EB
leau  d,u                                    33 CB
leau  d,x                                    33 8B
leau  d,y                                    33 AB
leau  [$01,pc]                               33 9C 01
leau  [$01,pc]                               33 BC 01
leau  [$01,pc]                               33 DC 01
leau  [$01,pc]                               33 FC 01
leau  [$01,s]                                33 F8 01
leau  [$01,u]                                33 D8 01
leau  [$01,x]                                33 98 01
leau  [$01,y]                                33 B8 01
leau  [$beef,pc]                             33 9D BE EF
leau  [$beef,pc]                             33 BD BE EF
leau  [$beef,pc]                             33 DD BE EF
leau  [$beef,pc]                             33 FD BE EF
leau  [$beef,s]                              33 F9 BE EF
leau  [$beef,u]                              33 D9 BE EF
leau  [$beef,x]                              33 99 BE EF
leau  [$beef,y]                              33 B9 BE EF
leau  [$beef]                                33 9F BE EF
leau  [$beef]                                33 BF BE EF
leau  [$beef]                                33 DF BE EF
leau  [$beef]                                33 FF BE EF
leau  [,--s]                                 33 F3
leau  [,--u]                                 33 D3
leau  [,--x]                                 33 93
leau  [,--y]                                 33 B3
leau  [,s++]                                 33 F1
leau  [,s]                                   33 F4
leau  [,u++]                                 33 D1
leau  [,u]                                   33 D4
leau  [,x++]                                 33 91
leau  [,x]                                   33 94
leau  [,y++]                                 33 B1
leau  [,y]                                   33 B4
leau  [a,s]                                  33 F6
leau  [a,u]                                  33 D6
leau  [a,x]                                  33 96
leau  [a,y]                                  33 B6
leau  [b,s]                                  33 F5
leau  [b,u]                                  33 D5
leau  [b,x]                                  33 95
leau  [b,y]                                  33 B5
leau  [d,s]                                  33 FB
leau  [d,u]                                  33 DB
leau  [d,x]                                  33 9B
leau  [d,y]                                  33 BB
leau  []                                     33 97
leau  []                                     33 9A
leau  []                                     33 9E
leau  []                                     33 B7
leau  []                                     33 BA
leau  []                                     33 BE
leau  []                                     33 D7
leau  []                                     33 DA
leau  []                                     33 DE
leau  []                                     33 F7
leau  []                                     33 FA
leau  []                                     33 FE
leax  $0,s                                   30 60
leax  $0,u                                   30 40
leax  $0,x                                   30 00
leax  $0,y                                   30 20
leax  $01,pc                                 30 8C 01
leax  $01,pc                                 30 AC 01
leax  $01,pc                                 30 CC 01
leax  $01,pc                                 30 EC 01
leax  $01,s                                  30 E8 01
leax  $01,u                                  30 C8 01
leax  $01,x                                  30 88 01
leax  $01,y                                  30 A8 01
leax  $1,s                                   30 61
leax  $1,u                                   30 41
leax  $1,x                                   30 01
leax  $1,y                                   30 21
leax  $2,s                                   30 62
leax  $2,u                                   30 42
leax  $2,x                                   30 02
leax  $2,y                                   30 22
leax  $3,s                                   30 63
leax  $3,u                                   30 43
leax  $3,x                                   30 03
leax  $3,y                                   30 23
leax  $4,s                                   30 64
leax  $4,u                                   30 44
leax  $4,x                                   30 04
leax  $4,y                                   30 24
leax  $5,s                                   30 65
leax  $5,u                                   30 45
leax  $5,x                                   30 05
leax  $5,y                                   30 25
leax  $6,s                                   30 66
leax  $6,u                                   30 46
leax  $6,x                                   30 06
leax  $6,y                                   30 26
leax  $7,s                                   30 67
leax  $7,u                                   30 47
leax  $7,x                                   30 07
leax  $7,y                                   30 27
leax  $8,s                                   30 68
leax  $8,u                                   30 48
leax  $8,x                                   30 08
leax  $8,y                                   30 28
leax  $9,s                                   30 69
leax  $9,u                                   30 49
leax  $9,x                                   30 09
leax  $9,y                                   30 29
leax  $a,s                                   30 6A
leax  $a,u                                   30 4A
leax  $a,x                                   30 0A
leax  $a,y                                   30 2A
leax  $b,s                                   30 6B
leax  $b,u                                   30 4B
leax  $b,x                                   30 0B
leax  $b,y                                   30 2B
leax  $beef                                  30 8F BE EF
leax  $beef                                  30 AF BE EF
leax  $beef                                  30 CF BE EF
leax  $beef                                  30 EF BE EF
leax  $beef,pc                               30 8D BE EF
leax  $beef,pc                               30 AD BE EF
leax  $beef,pc                               30 CD BE EF
leax  $beef,pc                               30 ED BE EF
leax  $beef,s                                30 E9 BE EF
leax  $beef,u                                30 C9 BE EF
leax  $beef,x                                30 89 BE EF
leax  $beef,y                                30 A9 BE EF
leax  $c,s                                   30 6C
leax  $c,u                                   30 4C
leax  $c,x                                   30 0C
leax  $c,y                                   30 2C
leax  $d,s                                   30 6D
leax  $d,u                                   30 4D
leax  $d,x                                   30 0D
leax  $d,y                                   30 2D
leax  $e,s                                   30 6E
leax  $e,u                                   30 4E
leax  $e,x                                   30 0E
leax  $e,y                                   30 2E
leax  $f,s                                   30 6F
leax  $f,u                                   30 4F
leax  $f,x                                   30 0F
leax  $f,y                                   30 2F
leax  ,--s                                   30 E3
leax  ,--u                                   30 C3
leax  ,--x                                   30 83
leax  ,--y                                   30 A3
leax  ,-s                                    30 E2
leax  ,-u                                    30 C2
leax  ,-x                                    30 82
leax  ,-y                                    30 A2
leax  ,s                                     30 E4
leax  ,s+                                    30 E0
leax  ,s++                                   30 E1
leax  ,u                                     30 C4
leax  ,u+                                    30 C0
leax  ,u++                                   30 C1
leax  ,x                                     30 84
leax  ,x+                                    30 80
leax  ,x++                                   30 81
leax  ,y                                     30 A4
leax  ,y+                                    30 A0
leax  ,y++                                   30 A1
leax  -$1,s                                  30 7F
leax  -$1,u                                  30 5F
leax  -$1,x                                  30 1F
leax  -$1,y                                  30 3F
leax  -$10,s                                 30 70
leax  -$10,u                                 30 50
leax  -$10,x                                 30 10
leax  -$10,y                                 30 30
leax  -$2,s                                  30 7E
leax  -$2,u                                  30 5E
leax  -$2,x                                  30 1E
leax  -$2,y                                  30 3E
leax  -$3,s                                  30 7D
leax  -$3,u                                  30 5D
leax  -$3,x                                  30 1D
leax  -$3,y                                  30 3D
leax  -$4,s                                  30 7C
leax  -$4,u                                  30 5C
leax  -$4,x                                  30 1C
leax  -$4,y                                  30 3C
leax  -$5,s                                  30 7B
leax  -$5,u                                  30 5B
leax  -$5,x                                  30 1B
leax  -$5,y                                  30 3B
leax  -$6,s                                  30 7A
leax  -$6,u                                  30 5A
leax  -$6,x                                  30 1A
leax  -$6,y                                  30 3A
leax  -$7,s                                  30 79
leax  -$7,u                                  30 59
leax  -$7,x                                  30 19
leax  -$7,y                                  30 39
leax  -$8,s                                  30 78
leax  -$8,u                                  30 58
leax  -$8,x                                  30 18
leax  -$8,y                                  30 38
leax  -$9,s                                  30 77
leax  -$9,u                                  30 57
leax  -$9,x                                  30 17
leax  -$9,y                                  30 37
leax  -$a,s                                  30 76
leax  -$a,u                                  30 56
leax  -$a,x                                  30 16
leax  -$a,y                                  30 36
leax  -$b,s                                  30 75
leax  -$b,u                                  30 55
leax  -$b,x                                  30 15
leax  -$b,y                                  30 35
leax  -$c,s                                  30 74
leax  -$c,u                                  30 54
leax  -$c,x                                  30 14
leax  -$c,y                                  30 34
leax  -$d,s                                  30 73
leax  -$d,u                                  30 53
leax  -$d,x                                  30 13
leax  -$d,y                                  30 33
leax  -$e,s                                  30 72
leax  -$e,u                                  30 52
leax  -$e,x                                  30 12
leax  -$e,y                                  30 32
leax  -$f,s                                  30 71
leax  -$f,u                                  30 51
leax  -$f,x                                  30 11
leax  -$f,y                                  30 31
leax  a,s                                    30 E6
leax  a,u                                    30 C6
leax  a,x                                    30 86
leax  a,y                                    30 A6
leax  b,s                                    30 E5
leax  b,u                                    30 C5
leax  b,x                                    30 85
leax  b,y                                    30 A5
leax  d,s                                    30 EB
leax  d,u                                    30 CB
leax  d,x                                    30 8B
leax  d,y                                    30 AB
leax  [$01,pc]                               30 9C 01
leax  [$01,pc]                               30 BC 01
leax  [$01,pc]                               30 DC 01
leax  [$01,pc]                               30 FC 01
leax  [$01,s]                                30 F8 01
leax  [$01,u]                                30 D8 01
leax  [$01,x]                                30 98 01
leax  [$01,y]                                30 B8 01
leax  [$beef,pc]                             30 9D BE EF
leax  [$beef,pc]                             30 BD BE EF
leax  [$beef,pc]                             30 DD BE EF
leax  [$beef,pc]                             30 FD BE EF
leax  [$beef,s]                              30 F9 BE EF
leax  [$beef,u]                              30 D9 BE EF
leax  [$beef,x]                              30 99 BE EF
leax  [$beef,y]                              30 B9 BE EF
leax  [$beef]                                30 9F BE EF
leax  [$beef]                                30 BF BE EF
leax  [$beef]                                30 DF BE EF
leax  [$beef]                                30 FF BE EF
leax  [,--s]                                 30 F3
leax  [,--u]                                 30 D3
leax  [,--x]                                 30 93
leax  [,--y]                                 30 B3
leax  [,s++]                                 30 F1
leax  [,s]                                   30 F4
leax  [,u++]                                 30 D1
leax  [,u]                                   30 D4
leax  [,x++]                                 30 91
leax  [,x]                                   30 94
leax  [,y++]                                 30 B1
leax  [,y]                                   30 B4
leax  [a,s]                                  30 F6
leax  [a,u]                                  30 D6
leax  [a,x]                                  30 96
leax  [a,y]                                  30 B6
leax  [b,s]                                  30 F5
leax  [b,u]                                  30 D5
leax  [b,x]                                  30 95
leax  [b,y]                                  30 B5
leax  [d,s]                                  30 FB
leax  [d,u]                                  30 DB
leax  [d,x]                                  30 9B
leax  [d,y]                                  30 BB
leax  []                                     30 97
leax  []                                     30 9A
leax  []                                     30 9E
leax  []                                     30 B7
leax  []                                     30 BA
leax  []                                     30 BE
leax  []                                     30 D7
leax  []                                     30 DA
leax  []                                     30 DE
leax  []                                     30 F7
leax  []                                     30 FA
leax  []                                     30 FE
leay  $0,s                                   31 60
leay  $0,u                                   31 40
leay  $0,x                                   31 00
leay  $0,y                                   31 20
leay  $01,pc                                 31 8C 01
leay  $01,pc                                 31 AC 01
leay  $01,pc                                 31 CC 01
leay  $01,pc                                 31 EC 01
leay  $01,s                                  31 E8 01
leay  $01,u                                  31 C8 01
leay  $01,x                                  31 88 01
leay  $01,y                                  31 A8 01
leay  $1,s                                   31 61
leay  $1,u                                   31 41
leay  $1,x                                   31 01
leay  $1,y                                   31 21
leay  $2,s                                   31 62
leay  $2,u                                   31 42
leay  $2,x                                   31 02
leay  $2,y                                   31 22
leay  $3,s                                   31 63
leay  $3,u                                   31 43
leay  $3,x                                   31 03
leay  $3,y                                   31 23
leay  $4,s                                   31 64
leay  $4,u                                   31 44
leay  $4,x                                   31 04
leay  $4,y                                   31 24
leay  $5,s                                   31 65
leay  $5,u                                   31 45
leay  $5,x                                   31 05
leay  $5,y                                   31 25
leay  $6,s                                   31 66
leay  $6,u                                   31 46
leay  $6,x                                   31 06
leay  $6,y                                   31 26
leay  $7,s                                   31 67
leay  $7,u                                   31 47
leay  $7,x                                   31 07
leay  $7,y                                   31 27
leay  $8,s                                   31 68
leay  $8,u                                   31 48
leay  $8,x                                   31 08
leay  $8,y                                   31 28
leay  $9,s                                   31 69
leay  $9,u                                   31 49
leay  $9,x                                   31 09
leay  $9,y                                   31 29
leay  $a,s                                   31 6A
leay  $a,u                                   31 4A
leay  $a,x                                   31 0A
leay  $a,y                                   31 2A
leay  $b,s                                   31 6B
leay  $b,u                                   31 4B
leay  $b,x                                   31 0B
leay  $b,y                                   31 2B
leay  $beef                                  31 8F BE EF
leay  $beef                                  31 AF BE EF
leay  $beef                                  31 CF BE EF
leay  $beef                                  31 EF BE EF
leay  $beef,pc                               31 8D BE EF
leay  $beef,pc                               31 AD BE EF
leay  $beef,pc                               31 CD BE EF
leay  $beef,pc                               31 ED BE EF
leay  $beef,s                                31 E9 BE EF
leay  $beef,u                                31 C9 BE EF
leay  $beef,x                                31 89 BE EF
leay  $beef,y                                31 A9 BE EF
leay  $c,s                                   31 6C
leay  $c,u                                   31 4C
leay  $c,x                                   31 0C
leay  $c,y                                   31 2C
leay  $d,s                                   31 6D
leay  $d,u                                   31 4D
leay  $d,x                                   31 0D
leay  $d,y                                   31 2D
leay  $e,s                                   31 6E
leay  $e,u                                   31 4E
leay  $e,x                                   31 0E
leay  $e,y                                   31 2E
leay  $f,s                                   31 6F
leay  $f,u                                   31 4F
leay  $f,x                                   31 0F
leay  $f,y                                   31 2F
leay  ,--s                                   31 E3
leay  ,--u                                   31 C3
leay  ,--x                                   31 83
leay  ,--y                                   31 A3
leay  ,-s                                    31 E2
leay  ,-u                                    31 C2
leay  ,-x                                    31 82
leay  ,-y                                    31 A2
leay  ,s                                     31 E4
leay  ,s+                                    31 E0
leay  ,s++                                   31 E1
leay  ,u                                     31 C4
leay  ,u+                                    31 C0
leay  ,u++                                   31 C1
leay  ,x                                     31 84
leay  ,x+                                    31 80
leay  ,x++                                   31 81
leay  ,y                                     31 A4
leay  ,y+                                    31 A0
leay  ,y++                                   31 A1
leay  -$1,s                                  31 7F
leay  -$1,u                                  31 5F
leay  -$1,x                                  31 1F
leay  -$1,y                                  31 3F
leay  -$10,s                                 31 70
leay  -$10,u                                 31 50
leay  -$10,x                                 31 10
leay  -$10,y                                 31 30
leay  -$2,s                                  31 7E
leay  -$2,u                                  31 5E
leay  -$2,x                                  31 1E
leay  -$2,y                                  31 3E
leay  -$3,s                                  31 7D
leay  -$3,u                                  31 5D
leay  -$3,x                                  31 1D
leay  -$3,y                                  31 3D
leay  -$4,s                                  31 7C
leay  -$4,u                                  31 5C
leay  -$4,x                                  31 1C
leay  -$4,y                                  31 3C
leay  -$5,s                                  31 7B
leay  -$5,u                                  31 5B
leay  -$5,x                                  31 1B
leay  -$5,y                                  31 3B
leay  -$6,s                                  31 7A
leay  -$6,u                                  31 5A
leay  -$6,x                                  31 1A
leay  -$6,y                                  31 3A
leay  -$7,s                                  31 79
leay  -$7,u                                  31 59
leay  -$7,x                                  31 19
leay  -$7,y                                  31 39
leay  -$8,s                                  31 78
leay  -$8,u                                  31 58
leay  -$8,x                                  31 18
leay  -$8,y                                  31 38
leay  -$9,s                                  31 77
leay  -$9,u                                  31 57
leay  -$9,x                                  31 17
leay  -$9,y                                  31 37
leay  -$a,s                                  31 76
leay  -$a,u                                  31 56
leay  -$a,x                                  31 16
leay  -$a,y                                  31 36
leay  -$b,s                                  31 75
leay  -$b,u                                  31 55
leay  -$b,x                                  31 15
leay  -$b,y                                  31 35
leay  -$c,s                                  31 74
leay  -$c,u                                  31 54
leay  -$c,x                                  31 14
leay  -$c,y                                  31 34
leay  -$d,s                                  31 73
leay  -$d,u                                  31 53
leay  -$d,x                                  31 13
leay  -$d,y                                  31 33
leay  -$e,s                                  31 72
leay  -$e,u                                  31 52
leay  -$e,x                                  31 12
leay  -$e,y                                  31 32
leay  -$f,s                                  31 71
leay  -$f,u                                  31 51
leay  -$f,x                                  31 11
leay  -$f,y                                  31 31
leay  a,s                                    31 E6
leay  a,u                                    31 C6
leay  a,x                                    31 86
leay  a,y                                    31 A6
leay  b,s                                    31 E5
leay  b,u                                    31 C5
leay  b,x                                    31 85
leay  b,y                                    31 A5
leay  d,s                                    31 EB
leay  d,u                                    31 CB
leay  d,x                                    31 8B
leay  d,y                                    31 AB
leay  [$01,pc]                               31 9C 01
leay  [$01,pc]                               31 BC 01
leay  [$01,pc]                               31 DC 01
leay  [$01,pc]                               31 FC 01
leay  [$01,s]                                31 F8 01
leay  [$01,u]                                31 D8 01
leay  [$01,x]                                31 98 01
leay  [$01,y]                                31 B8 01
leay  [$beef,pc]                             31 9D BE EF
leay  [$beef,pc]                             31 BD BE EF
leay  [$beef,pc]                             31 DD BE EF
leay  [$beef,pc]                             31 FD BE EF
leay  [$beef,s]                              31 F9 BE EF
leay  [$beef,u]                              31 D9 BE EF
leay  [$beef,x]                              31 99 BE EF
leay  [$beef,y]                              31 B9 BE EF
leay  [$beef]                                31 9F BE EF
leay  [$beef]                                31 BF BE EF
leay  [$beef]                                31 DF BE EF
leay  [$beef]                                31 FF BE EF
leay  [,--s]                                 31 F3
leay  [,--u]                                 31 D3
leay  [,--x]                                 31 93
leay  [,--y]                                 31 B3
leay  [,s++]                                 31 F1
leay  [,s]                                   31 F4
leay  [,u++]                                 31 D1
leay  [,u]                                   31 D4
leay  [,x++]                                 31 91
leay  [,x]                                   31 94
leay  [,y++]                                 31 B1
leay  [,y]                                   31 B4
leay  [a,s]                                  31 F6
leay  [a,u]                                  31 D6
leay  [a,x]                                  31 96
leay  [a,y]                                  31 B6
leay  [b,s]                                  31 F5
leay  [b,u]                                  31 D5
leay  [b,x]                                  31 95
leay  [b,y]                                  31 B5
leay  [d,s]                                  31 FB
leay  [d,u]                                  31 DB
leay  [d,x]                                  31 9B
leay  [d,y]                                  31 BB
leay  []                                     31 97
leay  []                                     31 9A
leay  []                                     31 9E
leay  []                                     31 B7
leay  []                                     31 BA
leay  []                                     31 BE
leay  []                                     31 D7
leay  []                                     31 DA
leay  []                                     31 DE
leay  []                                     31 F7
leay  []                                     31 FA
leay  []                                     31 FE
lsr   $0,s                                   64 60
lsr   $0,u                                   64 40
lsr   $0,x                                   64 00
lsr   $0,y                                   64 20
lsr   $01,pc                                 64 8C 01
lsr   $01,pc                                 64 AC 01
lsr   $01,pc                                 64 CC 01
lsr   $01,pc                                 64 EC 01
lsr   $01,s                                  64 E8 01
lsr   $01,u                                  64 C8 01
lsr   $01,x                                  64 88 01
lsr   $01,y                                  64 A8 01
lsr   $1,s                                   64 61
lsr   $1,u                                   64 41
lsr   $1,x                                   64 01
lsr   $1,y                                   64 21
lsr   $2,s                                   64 62
lsr   $2,u                                   64 42
lsr   $2,x                                   64 02
lsr   $2,y                                   64 22
lsr   $3,s                                   64 63
lsr   $3,u                                   64 43
lsr   $3,x                                   64 03
lsr   $3,y                                   64 23
lsr   $4,s                                   64 64
lsr   $4,u                                   64 44
lsr   $4,x                                   64 04
lsr   $4,y                                   64 24
lsr   $5,s                                   64 65
lsr   $5,u                                   64 45
lsr   $5,x                                   64 05
lsr   $5,y                                   64 25
lsr   $6,s                                   64 66
lsr   $6,u                                   64 46
lsr   $6,x                                   64 06
lsr   $6,y                                   64 26
lsr   $7,s                                   64 67
lsr   $7,u                                   64 47
lsr   $7,x                                   64 07
lsr   $7,y                                   64 27
lsr   $8,s                                   64 68
lsr   $8,u                                   64 48
lsr   $8,x                                   64 08
lsr   $8,y                                   64 28
lsr   $9,s                                   64 69
lsr   $9,u                                   64 49
lsr   $9,x                                   64 09
lsr   $9,y                                   64 29
lsr   $a,s                                   64 6A
lsr   $a,u                                   64 4A
lsr   $a,x                                   64 0A
lsr   $a,y                                   64 2A
lsr   $b,s                                   64 6B
lsr   $b,u                                   64 4B
lsr   $b,x                                   64 0B
lsr   $b,y                                   64 2B
lsr   $beef                                  64 8F BE EF
lsr   $beef                                  64 AF BE EF
lsr   $beef                                  64 CF BE EF
lsr   $beef                                  64 EF BE EF
lsr   $beef                                  74 BE EF
lsr   $beef,pc                               64 8D BE EF
lsr   $beef,pc                               64 AD BE EF
lsr   $beef,pc                               64 CD BE EF
lsr   $beef,pc                               64 ED BE EF
lsr   $beef,s                                64 E9 BE EF
lsr   $beef,u                                64 C9 BE EF
lsr   $beef,x                                64 89 BE EF
lsr   $beef,y                                64 A9 BE EF
lsr   $c,s                                   64 6C
lsr   $c,u                                   64 4C
lsr   $c,x                                   64 0C
lsr   $c,y                                   64 2C
lsr   $d,s                                   64 6D
lsr   $d,u                                   64 4D
lsr   $d,x                                   64 0D
lsr   $d,y                                   64 2D
lsr   $e,s                                   64 6E
lsr   $e,u                                   64 4E
lsr   $e,x                                   64 0E
lsr   $e,y                                   64 2E
lsr   $f,s                                   64 6F
lsr   $f,u                                   64 4F
lsr   $f,x                                   64 0F
lsr   $f,y                                   64 2F
lsr   $ff                                    04 FF
lsr   ,--s                                   64 E3
lsr   ,--u                                   64 C3
lsr   ,--x                                   64 83
lsr   ,--y                                   64 A3
lsr   ,-s                                    64 E2
lsr   ,-u                                    64 C2
lsr   ,-x                                    64 82
lsr   ,-y                                    64 A2
lsr   ,s                                     64 E4
lsr   ,s+                                    64 E0
lsr   ,s++                                   64 E1
lsr   ,u                                     64 C4
lsr   ,u+                                    64 C0
lsr   ,u++                                   64 C1
lsr   ,x                                     64 84
lsr   ,x+                                    64 80
lsr   ,x++                                   64 81
lsr   ,y                                     64 A4
lsr   ,y+                                    64 A0
lsr   ,y++                                   64 A1
lsr   -$1,s                                  64 7F
lsr   -$1,u                                  64 5F
lsr   -$1,x                                  64 1F
lsr   -$1,y                                  64 3F
lsr   -$10,s                                 64 70
lsr   -$10,u                                 64 50
lsr   -$10,x                                 64 10
lsr   -$10,y                                 64 30
lsr   -$2,s                                  64 7E
lsr   -$2,u                                  64 5E
lsr   -$2,x                                  64 1E
lsr   -$2,y                                  64 3E
lsr   -$3,s                                  64 7D
lsr   -$3,u                                  64 5D
lsr   -$3,x                                  64 1D
lsr   -$3,y                                  64 3D
lsr   -$4,s                                  64 7C
lsr   -$4,u                                  64 5C
lsr   -$4,x                                  64 1C
lsr   -$4,y                                  64 3C
lsr   -$5,s                                  64 7B
lsr   -$5,u                                  64 5B
lsr   -$5,x                                  64 1B
lsr   -$5,y                                  64 3B
lsr   -$6,s                                  64 7A
lsr   -$6,u                                  64 5A
lsr   -$6,x                                  64 1A
lsr   -$6,y                                  64 3A
lsr   -$7,s                                  64 79
lsr   -$7,u                                  64 59
lsr   -$7,x                                  64 19
lsr   -$7,y                                  64 39
lsr   -$8,s                                  64 78
lsr   -$8,u                                  64 58
lsr   -$8,x                                  64 18
lsr   -$8,y                                  64 38
lsr   -$9,s                                  64 77
lsr   -$9,u                                  64 57
lsr   -$9,x                                  64 17
lsr   -$9,y                                  64 37
lsr   -$a,s                                  64 76
lsr   -$a,u                                  64 56
lsr   -$a,x                                  64 16
lsr   -$a,y                                  64 36
lsr   -$b,s                                  64 75
lsr   -$b,u                                  64 55
lsr   -$b,x                                  64 15
lsr   -$b,y                                  64 35
lsr   -$c,s                                  64 74
lsr   -$c,u                                  64 54
lsr   -$c,x                                  64 14
lsr   -$c,y                                  64 34
lsr   -$d,s                                  64 73
lsr   -$d,u                                  64 53
lsr   -$d,x                                  64 13
lsr   -$d,y                                  64 33
lsr   -$e,s                                  64 72
lsr   -$e,u                                  64 52
lsr   -$e,x                                  64 12
lsr   -$e,y                                  64 32
lsr   -$f,s                                  64 71
lsr   -$f,u                                  64 51
lsr   -$f,x                                  64 11
lsr   -$f,y                                  64 31
lsr   a,s                                    64 E6
lsr   a,u                                    64 C6
lsr   a,x                                    64 86
lsr   a,y                                    64 A6
lsr   b,s                                    64 E5
lsr   b,u                                    64 C5
lsr   b,x                                    64 85
lsr   b,y                                    64 A5
lsr   d,s                                    64 EB
lsr   d,u                                    64 CB
lsr   d,x                                    64 8B
lsr   d,y                                    64 AB
lsr   [$01,pc]                               64 9C 01
lsr   [$01,pc]                               64 BC 01
lsr   [$01,pc]                               64 DC 01
lsr   [$01,pc]                               64 FC 01
lsr   [$01,s]                                64 F8 01
lsr   [$01,u]                                64 D8 01
lsr   [$01,x]                                64 98 01
lsr   [$01,y]                                64 B8 01
lsr   [$beef,pc]                             64 9D BE EF
lsr   [$beef,pc]                             64 BD BE EF
lsr   [$beef,pc]                             64 DD BE EF
lsr   [$beef,pc]                             64 FD BE EF
lsr   [$beef,s]                              64 F9 BE EF
lsr   [$beef,u]                              64 D9 BE EF
lsr   [$beef,x]                              64 99 BE EF
lsr   [$beef,y]                              64 B9 BE EF
lsr   [$beef]                                64 9F BE EF
lsr   [$beef]                                64 BF BE EF
lsr   [$beef]                                64 DF BE EF
lsr   [$beef]                                64 FF BE EF
lsr   [,--s]                                 64 F3
lsr   [,--u]                                 64 D3
lsr   [,--x]                                 64 93
lsr   [,--y]                                 64 B3
lsr   [,s++]                                 64 F1
lsr   [,s]                                   64 F4
lsr   [,u++]                                 64 D1
lsr   [,u]                                   64 D4
lsr   [,x++]                                 64 91
lsr   [,x]                                   64 94
lsr   [,y++]                                 64 B1
lsr   [,y]                                   64 B4
lsr   [a,s]                                  64 F6
lsr   [a,u]                                  64 D6
lsr   [a,x]                                  64 96
lsr   [a,y]                                  64 B6
lsr   [b,s]                                  64 F5
lsr   [b,u]                                  64 D5
lsr   [b,x]                                  64 95
lsr   [b,y]                                  64 B5
lsr   [d,s]                                  64 FB
lsr   [d,u]                                  64 DB
lsr   [d,x]                                  64 9B
lsr   [d,y]                                  64 BB
lsr   []                                     64 97
lsr   []                                     64 9A
lsr   []                                     64 9E
lsr   []                                     64 B7
lsr   []                                     64 BA
lsr   []                                     64 BE
lsr   []                                     64 D7
lsr   []                                     64 DA
lsr   []                                     64 DE
lsr   []                                     64 F7
lsr   []                                     64 FA
lsr   []                                     64 FE
lsra                                         44
lsrb                                         54
mul                                          3D
neg   $0,s                                   60 60
neg   $0,u                                   60 40
neg   $0,x                                   60 00
neg   $0,y                                   60 20
neg   $01,pc                                 60 8C 01
neg   $01,pc                                 60 AC 01
neg   $01,pc                                 60 CC 01
neg   $01,pc                                 60 EC 01
neg   $01,s                                  60 E8 01
neg   $01,u                                  60 C8 01
neg   $01,x                                  60 88 01
neg   $01,y                                  60 A8 01
neg   $1,s                                   60 61
neg   $1,u                                   60 41
neg   $1,x                                   60 01
neg   $1,y                                   60 21
neg   $2,s                                   60 62
neg   $2,u                                   60 42
neg   $2,x                                   60 02
neg   $2,y                                   60 22
neg   $3,s                                   60 63
neg   $3,u                                   60 43
neg   $3,x                                   60 03
neg   $3,y                                   60 23
neg   $4,s                                   60 64
neg   $4,u                                   60 44
neg   $4,x                                   60 04
neg   $4,y                                   60 24
neg   $5,s                                   60 65
neg   $5,u                                   60 45
neg   $5,x                                   60 05
neg   $5,y                                   60 25
neg   $6,s                                   60 66
neg   $6,u                                   60 46
neg   $6,x                                   60 06
neg   $6,y                                   60 26
neg   $7,s                                   60 67
neg   $7,u                                   60 47
neg   $7,x                                   60 07
neg   $7,y                                   60 27
neg   $8,s                                   60 68
neg   $8,u                                   60 48
neg   $8,x                                   60 08
neg   $8,y                                   60 28
neg   $9,s                                   60 69
neg   $9,u                                   60 49
neg   $9,x                                   60 09
neg   $9,y                                   60 29
neg   $a,s                                   60 6A
neg   $a,u                                   60 4A
neg   $a,x                                   60 0A
neg   $a,y                                   60 2A
neg   $b,s                                   60 6B
neg   $b,u                                   60 4B
neg   $b,x                                   60 0B
neg   $b,y                                   60 2B
neg   $beef                                  60 8F BE EF
neg   $beef                                  60 AF BE EF
neg   $beef                                  60 CF BE EF
neg   $beef                                  60 EF BE EF
neg   $beef                                  70 BE EF
neg   $beef,pc                               60 8D BE EF
neg   $beef,pc                               60 AD BE EF
neg   $beef,pc                               60 CD BE EF
neg   $beef,pc                               60 ED BE EF
neg   $beef,s                                60 E9 BE EF
neg   $beef,u                                60 C9 BE EF
neg   $beef,x                                60 89 BE EF
neg   $beef,y                                60 A9 BE EF
neg   $c,s                                   60 6C
neg   $c,u                                   60 4C
neg   $c,x                                   60 0C
neg   $c,y                                   60 2C
neg   $d,s                                   60 6D
neg   $d,u                                   60 4D
neg   $d,x                                   60 0D
neg   $d,y                                   60 2D
neg   $e,s                                   60 6E
neg   $e,u                                   60 4E
neg   $e,x                                   60 0E
neg   $e,y                                   60 2E
neg   $f,s                                   60 6F
neg   $f,u                                   60 4F
neg   $f,x                                   60 0F
neg   $f,y                                   60 2F
neg   $ff                                    00 FF
neg   ,--s                                   60 E3
neg   ,--u                                   60 C3
neg   ,--x                                   60 83
neg   ,--y                                   60 A3
neg   ,-s                                    60 E2
neg   ,-u                                    60 C2
neg   ,-x                                    60 82
neg   ,-y                                    60 A2
neg   ,s                                     60 E4
neg   ,s+                                    60 E0
neg   ,s++                                   60 E1
neg   ,u                                     60 C4
neg   ,u+                                    60 C0
neg   ,u++                                   60 C1
neg   ,x                                     60 84
neg   ,x+                                    60 80
neg   ,x++                                   60 81
neg   ,y                                     60 A4
neg   ,y+                                    60 A0
neg   ,y++                                   60 A1
neg   -$1,s                                  60 7F
neg   -$1,u                                  60 5F
neg   -$1,x                                  60 1F
neg   -$1,y                                  60 3F
neg   -$10,s                                 60 70
neg   -$10,u                                 60 50
neg   -$10,x                                 60 10
neg   -$10,y                                 60 30
neg   -$2,s                                  60 7E
neg   -$2,u                                  60 5E
neg   -$2,x                                  60 1E
neg   -$2,y                                  60 3E
neg   -$3,s                                  60 7D
neg   -$3,u                                  60 5D
neg   -$3,x                                  60 1D
neg   -$3,y                                  60 3D
neg   -$4,s                                  60 7C
neg   -$4,u                                  60 5C
neg   -$4,x                                  60 1C
neg   -$4,y                                  60 3C
neg   -$5,s                                  60 7B
neg   -$5,u                                  60 5B
neg   -$5,x                                  60 1B
neg   -$5,y                                  60 3B
neg   -$6,s                                  60 7A
neg   -$6,u                                  60 5A
neg   -$6,x                                  60 1A
neg   -$6,y                                  60 3A
neg   -$7,s                                  60 79
neg   -$7,u                                  60 59
neg   -$7,x                                  60 19
neg   -$7,y                                  60 39
neg   -$8,s                                  60 78
neg   -$8,u                                  60 58
neg   -$8,x                                  60 18
neg   -$8,y                                  60 38
neg   -$9,s                                  60 77
neg   -$9,u                                  60 57
neg   -$9,x                                  60 17
neg   -$9,y                                  60 37
neg   -$a,s                                  60 76
neg   -$a,u                                  60 56
neg   -$a,x                                  60 16
neg   -$a,y                                  60 36
neg   -$b,s                                  60 75
neg   -$b,u                                  60 55
neg   -$b,x                                  60 15
neg   -$b,y                                  60 35
neg   -$c,s                                  60 74
neg   -$c,u                                  60 54
neg   -$c,x                                  60 14
neg   -$c,y                                  60 34
neg   -$d,s                                  60 73
neg   -$d,u                                  60 53
neg   -$d,x                                  60 13
neg   -$d,y                                  60 33
neg   -$e,s                                  60 72
neg   -$e,u                                  60 52
neg   -$e,x                                  60 12
neg   -$e,y                                  60 32
neg   -$f,s                                  60 71
neg   -$f,u                                  60 51
neg   -$f,x                                  60 11
neg   -$f,y                                  60 31
neg   a,s                                    60 E6
neg   a,u                                    60 C6
neg   a,x                                    60 86
neg   a,y                                    60 A6
neg   b,s                                    60 E5
neg   b,u                                    60 C5
neg   b,x                                    60 85
neg   b,y                                    60 A5
neg   d,s                                    60 EB
neg   d,u                                    60 CB
neg   d,x                                    60 8B
neg   d,y                                    60 AB
neg   [$01,pc]                               60 9C 01
neg   [$01,pc]                               60 BC 01
neg   [$01,pc]                               60 DC 01
neg   [$01,pc]                               60 FC 01
neg   [$01,s]                                60 F8 01
neg   [$01,u]                                60 D8 01
neg   [$01,x]                                60 98 01
neg   [$01,y]                                60 B8 01
neg   [$beef,pc]                             60 9D BE EF
neg   [$beef,pc]                             60 BD BE EF
neg   [$beef,pc]                             60 DD BE EF
neg   [$beef,pc]                             60 FD BE EF
neg   [$beef,s]                              60 F9 BE EF
neg   [$beef,u]                              60 D9 BE EF
neg   [$beef,x]                              60 99 BE EF
neg   [$beef,y]                              60 B9 BE EF
neg   [$beef]                                60 9F BE EF
neg   [$beef]                                60 BF BE EF
neg   [$beef]                                60 DF BE EF
neg   [$beef]                                60 FF BE EF
neg   [,--s]                                 60 F3
neg   [,--u]                                 60 D3
neg   [,--x]                                 60 93
neg   [,--y]                                 60 B3
neg   [,s++]                                 60 F1
neg   [,s]                                   60 F4
neg   [,u++]                                 60 D1
neg   [,u]                                   60 D4
neg   [,x++]                                 60 91
neg   [,x]                                   60 94
neg   [,y++]                                 60 B1
neg   [,y]                                   60 B4
neg   [a,s]                                  60 F6
neg   [a,u]                                  60 D6
neg   [a,x]                                  60 96
neg   [a,y]                                  60 B6
neg   [b,s]                                  60 F5
neg   [b,u]                                  60 D5
neg   [b,x]                                  60 95
neg   [b,y]                                  60 B5
neg   [d,s]                                  60 FB
neg   [d,u]                                  60 DB
neg   [d,x]                                  60 9B
neg   [d,y]                                  60 BB
neg   []                                     60 97
neg   []                                     60 9A
neg   []                                     60 9E
neg   []                                     60 B7
neg   []                                     60 BA
neg   []                                     60 BE
neg   []                                     60 D7
neg   []                                     60 DA
neg   []                                     60 DE
neg   []                                     60 F7
neg   []                                     60 FA
neg   []                                     60 FE
nega                                         40
negb                                         50
nop                                          12
ora   #$ff                                   8A FF
ora   $0,s                                   AA 60
ora   $0,u                                   AA 40
ora   $0,x                                   AA 00
ora   $0,y                                   AA 20
ora   $01,pc                                 AA 8C 01
ora   $01,pc                                 AA AC 01
ora   $01,pc                                 AA CC 01
ora   $01,pc                                 AA EC 01
ora   $01,s                                  AA E8 01
ora   $01,u                                  AA C8 01
ora   $01,x                                  AA 88 01
ora   $01,y                                  AA A8 01
ora   $1,s                                   AA 61
ora   $1,u                                   AA 41
ora   $1,x                                   AA 01
ora   $1,y                                   AA 21
ora   $2,s                                   AA 62
ora   $2,u                                   AA 42
ora   $2,x                                   AA 02
ora   $2,y                                   AA 22
ora   $3,s                                   AA 63
ora   $3,u                                   AA 43
ora   $3,x                                   AA 03
ora   $3,y                                   AA 23
ora   $4,s                                   AA 64
ora   $4,u                                   AA 44
ora   $4,x                                   AA 04
ora   $4,y                                   AA 24
ora   $5,s                                   AA 65
ora   $5,u                                   AA 45
ora   $5,x                                   AA 05
ora   $5,y                                   AA 25
ora   $6,s                                   AA 66
ora   $6,u                                   AA 46
ora   $6,x                                   AA 06
ora   $6,y                                   AA 26
ora   $7,s                                   AA 67
ora   $7,u                                   AA 47
ora   $7,x                                   AA 07
ora   $7,y                                   AA 27
ora   $8,s                                   AA 68
ora   $8,u                                   AA 48
ora   $8,x                                   AA 08
ora   $8,y                                   AA 28
ora   $9,s                                   AA 69
ora   $9,u                                   AA 49
ora   $9,x                                   AA 09
ora   $9,y                                   AA 29
ora   $a,s                                   AA 6A
ora   $a,u                                   AA 4A
ora   $a,x                                   AA 0A
ora   $a,y                                   AA 2A
ora   $b,s                                   AA 6B
ora   $b,u                                   AA 4B
ora   $b,x                                   AA 0B
ora   $b,y                                   AA 2B
ora   $beef                                  AA 8F BE EF
ora   $beef                                  AA AF BE EF
ora   $beef                                  AA CF BE EF
ora   $beef                                  AA EF BE EF
ora   $beef                                  BA BE EF
ora   $beef,pc                               AA 8D BE EF
ora   $beef,pc                               AA AD BE EF
ora   $beef,pc                               AA CD BE EF
ora   $beef,pc                               AA ED BE EF
ora   $beef,s                                AA E9 BE EF
ora   $beef,u                                AA C9 BE EF
ora   $beef,x                                AA 89 BE EF
ora   $beef,y                                AA A9 BE EF
ora   $c,s                                   AA 6C
ora   $c,u                                   AA 4C
ora   $c,x                                   AA 0C
ora   $c,y                                   AA 2C
ora   $d,s                                   AA 6D
ora   $d,u                                   AA 4D
ora   $d,x                                   AA 0D
ora   $d,y                                   AA 2D
ora   $e,s                                   AA 6E
ora   $e,u                                   AA 4E
ora   $e,x                                   AA 0E
ora   $e,y                                   AA 2E
ora   $f,s                                   AA 6F
ora   $f,u                                   AA 4F
ora   $f,x                                   AA 0F
ora   $f,y                                   AA 2F
ora   $ff                                    9A FF
ora   ,--s                                   AA E3
ora   ,--u                                   AA C3
ora   ,--x                                   AA 83
ora   ,--y                                   AA A3
ora   ,-s                                    AA E2
ora   ,-u                                    AA C2
ora   ,-x                                    AA 82
ora   ,-y                                    AA A2
ora   ,s                                     AA E4
ora   ,s+                                    AA E0
ora   ,s++                                   AA E1
ora   ,u                                     AA C4
ora   ,u+                                    AA C0
ora   ,u++                                   AA C1
ora   ,x                                     AA 84
ora   ,x+                                    AA 80
ora   ,x++                                   AA 81
ora   ,y                                     AA A4
ora   ,y+                                    AA A0
ora   ,y++                                   AA A1
ora   -$1,s                                  AA 7F
ora   -$1,u                                  AA 5F
ora   -$1,x                                  AA 1F
ora   -$1,y                                  AA 3F
ora   -$10,s                                 AA 70
ora   -$10,u                                 AA 50
ora   -$10,x                                 AA 10
ora   -$10,y                                 AA 30
ora   -$2,s                                  AA 7E
ora   -$2,u                                  AA 5E
ora   -$2,x                                  AA 1E
ora   -$2,y                                  AA 3E
ora   -$3,s                                  AA 7D
ora   -$3,u                                  AA 5D
ora   -$3,x                                  AA 1D
ora   -$3,y                                  AA 3D
ora   -$4,s                                  AA 7C
ora   -$4,u                                  AA 5C
ora   -$4,x                                  AA 1C
ora   -$4,y                                  AA 3C
ora   -$5,s                                  AA 7B
ora   -$5,u                                  AA 5B
ora   -$5,x                                  AA 1B
ora   -$5,y                                  AA 3B
ora   -$6,s                                  AA 7A
ora   -$6,u                                  AA 5A
ora   -$6,x                                  AA 1A
ora   -$6,y                                  AA 3A
ora   -$7,s                                  AA 79
ora   -$7,u                                  AA 59
ora   -$7,x                                  AA 19
ora   -$7,y                                  AA 39
ora   -$8,s                                  AA 78
ora   -$8,u                                  AA 58
ora   -$8,x                                  AA 18
ora   -$8,y                                  AA 38
ora   -$9,s                                  AA 77
ora   -$9,u                                  AA 57
ora   -$9,x                                  AA 17
ora   -$9,y                                  AA 37
ora   -$a,s                                  AA 76
ora   -$a,u                                  AA 56
ora   -$a,x                                  AA 16
ora   -$a,y                                  AA 36
ora   -$b,s                                  AA 75
ora   -$b,u                                  AA 55
ora   -$b,x                                  AA 15
ora   -$b,y                                  AA 35
ora   -$c,s                                  AA 74
ora   -$c,u                                  AA 54
ora   -$c,x                                  AA 14
ora   -$c,y                                  AA 34
ora   -$d,s                                  AA 73
ora   -$d,u                                  AA 53
ora   -$d,x                                  AA 13
ora   -$d,y                                  AA 33
ora   -$e,s                                  AA 72
ora   -$e,u                                  AA 52
ora   -$e,x                                  AA 12
ora   -$e,y                                  AA 32
ora   -$f,s                                  AA 71
ora   -$f,u                                  AA 51
ora   -$f,x                                  AA 11
ora   -$f,y                                  AA 31
ora   a,s                                    AA E6
ora   a,u                                    AA C6
ora   a,x                                    AA 86
ora   a,y                                    AA A6
ora   b,s                                    AA E5
ora   b,u                                    AA C5
ora   b,x                                    AA 85
ora   b,y                                    AA A5
ora   d,s                                    AA EB
ora   d,u                                    AA CB
ora   d,x                                    AA 8B
ora   d,y                                    AA AB
ora   [$01,pc]                               AA 9C 01
ora   [$01,pc]                               AA BC 01
ora   [$01,pc]                               AA DC 01
ora   [$01,pc]                               AA FC 01
ora   [$01,s]                                AA F8 01
ora   [$01,u]                                AA D8 01
ora   [$01,x]                                AA 98 01
ora   [$01,y]                                AA B8 01
ora   [$beef,pc]                             AA 9D BE EF
ora   [$beef,pc]                             AA BD BE EF
ora   [$beef,pc]                             AA DD BE EF
ora   [$beef,pc]                             AA FD BE EF
ora   [$beef,s]                              AA F9 BE EF
ora   [$beef,u]                              AA D9 BE EF
ora   [$beef,x]                              AA 99 BE EF
ora   [$beef,y]                              AA B9 BE EF
ora   [$beef]                                AA 9F BE EF
ora   [$beef]                                AA BF BE EF
ora   [$beef]                                AA DF BE EF
ora   [$beef]                                AA FF BE EF
ora   [,--s]                                 AA F3
ora   [,--u]                                 AA D3
ora   [,--x]                                 AA 93
ora   [,--y]                                 AA B3
ora   [,s++]                                 AA F1
ora   [,s]                                   AA F4
ora   [,u++]                                 AA D1
ora   [,u]                                   AA D4
ora   [,x++]                                 AA 91
ora   [,x]                                   AA 94
ora   [,y++]                                 AA B1
ora   [,y]                                   AA B4
ora   [a,s]                                  AA F6
ora   [a,u]                                  AA D6
ora   [a,x]                                  AA 96
ora   [a,y]                                  AA B6
ora   [b,s]                                  AA F5
ora   [b,u]                                  AA D5
ora   [b,x]                                  AA 95
ora   [b,y]                                  AA B5
ora   [d,s]                                  AA FB
ora   [d,u]                                  AA DB
ora   [d,x]                                  AA 9B
ora   [d,y]                                  AA BB
ora   []                                     AA 97
ora   []                                     AA 9A
ora   []                                     AA 9E
ora   []                                     AA B7
ora   []                                     AA BA
ora   []                                     AA BE
ora   []                                     AA D7
ora   []                                     AA DA
ora   []                                     AA DE
ora   []                                     AA F7
ora   []                                     AA FA
ora   []                                     AA FE
orb   #$ff                                   CA FF
orb   $0,s                                   EA 60
orb   $0,u                                   EA 40
orb   $0,x                                   EA 00
orb   $0,y                                   EA 20
orb   $01,pc                                 EA 8C 01
orb   $01,pc                                 EA AC 01
orb   $01,pc                                 EA CC 01
orb   $01,pc                                 EA EC 01
orb   $01,s                                  EA E8 01
orb   $01,u                                  EA C8 01
orb   $01,x                                  EA 88 01
orb   $01,y                                  EA A8 01
orb   $1,s                                   EA 61
orb   $1,u                                   EA 41
orb   $1,x                                   EA 01
orb   $1,y                                   EA 21
orb   $2,s                                   EA 62
orb   $2,u                                   EA 42
orb   $2,x                                   EA 02
orb   $2,y                                   EA 22
orb   $3,s                                   EA 63
orb   $3,u                                   EA 43
orb   $3,x                                   EA 03
orb   $3,y                                   EA 23
orb   $4,s                                   EA 64
orb   $4,u                                   EA 44
orb   $4,x                                   EA 04
orb   $4,y                                   EA 24
orb   $5,s                                   EA 65
orb   $5,u                                   EA 45
orb   $5,x                                   EA 05
orb   $5,y                                   EA 25
orb   $6,s                                   EA 66
orb   $6,u                                   EA 46
orb   $6,x                                   EA 06
orb   $6,y                                   EA 26
orb   $7,s                                   EA 67
orb   $7,u                                   EA 47
orb   $7,x                                   EA 07
orb   $7,y                                   EA 27
orb   $8,s                                   EA 68
orb   $8,u                                   EA 48
orb   $8,x                                   EA 08
orb   $8,y                                   EA 28
orb   $9,s                                   EA 69
orb   $9,u                                   EA 49
orb   $9,x                                   EA 09
orb   $9,y                                   EA 29
orb   $a,s                                   EA 6A
orb   $a,u                                   EA 4A
orb   $a,x                                   EA 0A
orb   $a,y                                   EA 2A
orb   $b,s                                   EA 6B
orb   $b,u                                   EA 4B
orb   $b,x                                   EA 0B
orb   $b,y                                   EA 2B
orb   $beef                                  EA 8F BE EF
orb   $beef                                  EA AF BE EF
orb   $beef                                  EA CF BE EF
orb   $beef                                  EA EF BE EF
orb   $beef                                  FA BE EF
orb   $beef,pc                               EA 8D BE EF
orb   $beef,pc                               EA AD BE EF
orb   $beef,pc                               EA CD BE EF
orb   $beef,pc                               EA ED BE EF
orb   $beef,s                                EA E9 BE EF
orb   $beef,u                                EA C9 BE EF
orb   $beef,x                                EA 89 BE EF
orb   $beef,y                                EA A9 BE EF
orb   $c,s                                   EA 6C
orb   $c,u                                   EA 4C
orb   $c,x                                   EA 0C
orb   $c,y                                   EA 2C
orb   $d,s                                   EA 6D
orb   $d,u                                   EA 4D
orb   $d,x                                   EA 0D
orb   $d,y                                   EA 2D
orb   $e,s                                   EA 6E
orb   $e,u                                   EA 4E
orb   $e,x                                   EA 0E
orb   $e,y                                   EA 2E
orb   $f,s                                   EA 6F
orb   $f,u                                   EA 4F
orb   $f,x                                   EA 0F
orb   $f,y                                   EA 2F
orb   $ff                                    DA FF
orb   ,--s                                   EA E3
orb   ,--u                                   EA C3
orb   ,--x                                   EA 83
orb   ,--y                                   EA A3
orb   ,-s                                    EA E2
orb   ,-u                                    EA C2
orb   ,-x                                    EA 82
orb   ,-y                                    EA A2
orb   ,s                                     EA E4
orb   ,s+                                    EA E0
orb   ,s++                                   EA E1
orb   ,u                                     EA C4
orb   ,u+                                    EA C0
orb   ,u++                                   EA C1
orb   ,x                                     EA 84
orb   ,x+                                    EA 80
orb   ,x++                                   EA 81
orb   ,y                                     EA A4
orb   ,y+                                    EA A0
orb   ,y++                                   EA A1
orb   -$1,s                                  EA 7F
orb   -$1,u                                  EA 5F
orb   -$1,x                                  EA 1F
orb   -$1,y                                  EA 3F
orb   -$10,s                                 EA 70
orb   -$10,u                                 EA 50
orb   -$10,x                                 EA 10
orb   -$10,y                                 EA 30
orb   -$2,s                                  EA 7E
orb   -$2,u                                  EA 5E
orb   -$2,x                                  EA 1E
orb   -$2,y                                  EA 3E
orb   -$3,s                                  EA 7D
orb   -$3,u                                  EA 5D
orb   -$3,x                                  EA 1D
orb   -$3,y                                  EA 3D
orb   -$4,s                                  EA 7C
orb   -$4,u                                  EA 5C
orb   -$4,x                                  EA 1C
orb   -$4,y                                  EA 3C
orb   -$5,s                                  EA 7B
orb   -$5,u                                  EA 5B
orb   -$5,x                                  EA 1B
orb   -$5,y                                  EA 3B
orb   -$6,s                                  EA 7A
orb   -$6,u                                  EA 5A
orb   -$6,x                                  EA 1A
orb   -$6,y                                  EA 3A
orb   -$7,s                                  EA 79
orb   -$7,u                                  EA 59
orb   -$7,x                                  EA 19
orb   -$7,y                                  EA 39
orb   -$8,s                                  EA 78
orb   -$8,u                                  EA 58
orb   -$8,x                                  EA 18
orb   -$8,y                                  EA 38
orb   -$9,s                                  EA 77
orb   -$9,u                                  EA 57
orb   -$9,x                                  EA 17
orb   -$9,y                                  EA 37
orb   -$a,s                                  EA 76
orb   -$a,u                                  EA 56
orb   -$a,x                                  EA 16
orb   -$a,y                                  EA 36
orb   -$b,s                                  EA 75
orb   -$b,u                                  EA 55
orb   -$b,x                                  EA 15
orb   -$b,y                                  EA 35
orb   -$c,s                                  EA 74
orb   -$c,u                                  EA 54
orb   -$c,x                                  EA 14
orb   -$c,y                                  EA 34
orb   -$d,s                                  EA 73
orb   -$d,u                                  EA 53
orb   -$d,x                                  EA 13
orb   -$d,y                                  EA 33
orb   -$e,s                                  EA 72
orb   -$e,u                                  EA 52
orb   -$e,x                                  EA 12
orb   -$e,y                                  EA 32
orb   -$f,s                                  EA 71
orb   -$f,u                                  EA 51
orb   -$f,x                                  EA 11
orb   -$f,y                                  EA 31
orb   a,s                                    EA E6
orb   a,u                                    EA C6
orb   a,x                                    EA 86
orb   a,y                                    EA A6
orb   b,s                                    EA E5
orb   b,u                                    EA C5
orb   b,x                                    EA 85
orb   b,y                                    EA A5
orb   d,s                                    EA EB
orb   d,u                                    EA CB
orb   d,x                                    EA 8B
orb   d,y                                    EA AB
orb   [$01,pc]                               EA 9C 01
orb   [$01,pc]                               EA BC 01
orb   [$01,pc]                               EA DC 01
orb   [$01,pc]                               EA FC 01
orb   [$01,s]                                EA F8 01
orb   [$01,u]                                EA D8 01
orb   [$01,x]                                EA 98 01
orb   [$01,y]                                EA B8 01
orb   [$beef,pc]                             EA 9D BE EF
orb   [$beef,pc]                             EA BD BE EF
orb   [$beef,pc]                             EA DD BE EF
orb   [$beef,pc]                             EA FD BE EF
orb   [$beef,s]                              EA F9 BE EF
orb   [$beef,u]                              EA D9 BE EF
orb   [$beef,x]                              EA 99 BE EF
orb   [$beef,y]                              EA B9 BE EF
orb   [$beef]                                EA 9F BE EF
orb   [$beef]                                EA BF BE EF
orb   [$beef]                                EA DF BE EF
orb   [$beef]                                EA FF BE EF
orb   [,--s]                                 EA F3
orb   [,--u]                                 EA D3
orb   [,--x]                                 EA 93
orb   [,--y]                                 EA B3
orb   [,s++]                                 EA F1
orb   [,s]                                   EA F4
orb   [,u++]                                 EA D1
orb   [,u]                                   EA D4
orb   [,x++]                                 EA 91
orb   [,x]                                   EA 94
orb   [,y++]                                 EA B1
orb   [,y]                                   EA B4
orb   [a,s]                                  EA F6
orb   [a,u]                                  EA D6
orb   [a,x]                                  EA 96
orb   [a,y]                                  EA B6
orb   [b,s]                                  EA F5
orb   [b,u]                                  EA D5
orb   [b,x]                                  EA 95
orb   [b,y]                                  EA B5
orb   [d,s]                                  EA FB
orb   [d,u]                                  EA DB
orb   [d,x]                                  EA 9B
orb   [d,y]                                  EA BB
orb   []                                     EA 97
orb   []                                     EA 9A
orb   []                                     EA 9E
orb   []                                     EA B7
orb   []                                     EA BA
orb   []                                     EA BE
orb   []                                     EA D7
orb   []                                     EA DA
orb   []                                     EA DE
orb   []                                     EA F7
orb   []                                     EA FA
orb   []                                     EA FE
orcc  #$ff                                   1A FF
pshs                                         34 00
pshs  a                                      34 02
pshs  a,cc                                   34 03
pshs  b                                      34 04
pshs  b,a                                    34 06
pshs  b,a,cc                                 34 07
pshs  b,cc                                   34 05
pshs  cc                                     34 01
pshs  dp                                     34 08
pshs  dp,a                                   34 0A
pshs  dp,a,cc                                34 0B
pshs  dp,b                                   34 0C
pshs  dp,b,a                                 34 0E
pshs  dp,b,a,cc                              34 0F
pshs  dp,b,cc                                34 0D
pshs  dp,cc                                  34 09
pshs  pc                                     34 80
pshs  pc,a                                   34 82
pshs  pc,a,cc                                34 83
pshs  pc,b                                   34 84
pshs  pc,b,a                                 34 86
pshs  pc,b,a,cc                              34 87
pshs  pc,b,cc                                34 85
pshs  pc,cc                                  34 81
pshs  pc,dp                                  34 88
pshs  pc,dp,a                                34 8A
pshs  pc,dp,a,cc                             34 8B
pshs  pc,dp,b                                34 8C
pshs  pc,dp,b,a                              34 8E
pshs  pc,dp,b,a,cc                           34 8F
pshs  pc,dp,b,cc                             34 8D
pshs  pc,dp,cc                               34 89
pshs  pc,u                                   34 C0
pshs  pc,u,a                                 34 C2
pshs  pc,u,a,cc                              34 C3
pshs  pc,u,b                                 34 C4
pshs  pc,u,b,a                               34 C6
pshs  pc,u,b,a,cc                            34 C7
pshs  pc,u,b,cc                              34 C5
pshs  pc,u,cc                                34 C1
pshs  pc,u,dp                                34 C8
pshs  pc,u,dp,a                              34 CA
pshs  pc,u,dp,a,cc                           34 CB
pshs  pc,u,dp,b                              34 CC
pshs  pc,u,dp,b,a                            34 CE
pshs  pc,u,dp,b,a,cc                         34 CF
pshs  pc,u,dp,b,cc                           34 CD
pshs  pc,u,dp,cc                             34 C9
pshs  pc,u,x                                 34 D0
pshs  pc,u,x,a                               34 D2
pshs  pc,u,x,a,cc                            34 D3
pshs  pc,u,x,b                               34 D4
pshs  pc,u,x,b,a                             34 D6
pshs  pc,u,x,b,a,cc                          34 D7
pshs  pc,u,x,b,cc                            34 D5
pshs  pc,u,x,cc                              34 D1
pshs  pc,u,x,dp                              34 D8
pshs  pc,u,x,dp,a                            34 DA
pshs  pc,u,x,dp,a,cc                         34 DB
pshs  pc,u,x,dp,b                            34 DC
pshs  pc,u,x,dp,b,a                          34 DE
pshs  pc,u,x,dp,b,a,cc                       34 DF
pshs  pc,u,x,dp,b,cc                         34 DD
pshs  pc,u,x,dp,cc                           34 D9
pshs  pc,u,y                                 34 E0
pshs  pc,u,y,a                               34 E2
pshs  pc,u,y,a,cc                            34 E3
pshs  pc,u,y,b                               34 E4
pshs  pc,u,y,b,a                             34 E6
pshs  pc,u,y,b,a,cc                          34 E7
pshs  pc,u,y,b,cc                            34 E5
pshs  pc,u,y,cc                              34 E1
pshs  pc,u,y,dp                              34 E8
pshs  pc,u,y,dp,a                            34 EA
pshs  pc,u,y,dp,a,cc                         34 EB
pshs  pc,u,y,dp,b                            34 EC
pshs  pc,u,y,dp,b,a                          34 EE
pshs  pc,u,y,dp,b,a,cc                       34 EF
pshs  pc,u,y,dp,b,cc                         34 ED
pshs  pc,u,y,dp,cc                           34 E9
pshs  pc,u,y,x                               34 F0
pshs  pc,u,y,x,a                             34 F2
pshs  pc,u,y,x,a,cc                          34 F3
pshs  pc,u,y,x,b                             34 F4
pshs  pc,u,y,x,b,a                           34 F6
pshs  pc,u,y,x,b,a,cc                        34 F7
pshs  pc,u,y,x,b,cc                          34 F5
pshs  pc,u,y,x,cc                            34 F1
pshs  pc,u,y,x,dp                            34 F8
pshs  pc,u,y,x,dp,a                          34 FA
pshs  pc,u,y,x,dp,a,cc                       34 FB
pshs  pc,u,y,x,dp,b                          34 FC
pshs  pc,u,y,x,dp,b,a                        34 FE
pshs  pc,u,y,x,dp,b,a,cc                     34 FF
pshs  pc,u,y,x,dp,b,cc                       34 FD
pshs  pc,u,y,x,dp,cc                         34 F9
pshs  pc,x                                   34 90
pshs  pc,x,a                                 34 92
pshs  pc,x,a,cc                              34 93
pshs  pc,x,b                                 34 94
pshs  pc,x,b,a                               34 96
pshs  pc,x,b,a,cc                            34 97
pshs  pc,x,b,cc                              34 95
pshs  pc,x,cc                                34 91
pshs  pc,x,dp                                34 98
pshs  pc,x,dp,a                              34 9A
pshs  pc,x,dp,a,cc                           34 9B
pshs  pc,x,dp,b                              34 9C
pshs  pc,x,dp,b,a                            34 9E
pshs  pc,x,dp,b,a,cc                         34 9F
pshs  pc,x,dp,b,cc                           34 9D
pshs  pc,x,dp,cc                             34 99
pshs  pc,y                                   34 A0
pshs  pc,y,a                                 34 A2
pshs  pc,y,a,cc                              34 A3
pshs  pc,y,b                                 34 A4
pshs  pc,y,b,a                               34 A6
pshs  pc,y,b,a,cc                            34 A7
pshs  pc,y,b,cc                              34 A5
pshs  pc,y,cc                                34 A1
pshs  pc,y,dp                                34 A8
pshs  pc,y,dp,a                              34 AA
pshs  pc,y,dp,a,cc                           34 AB
pshs  pc,y,dp,b                              34 AC
pshs  pc,y,dp,b,a                            34 AE
pshs  pc,y,dp,b,a,cc                         34 AF
pshs  pc,y,dp,b,cc                           34 AD
pshs  pc,y,dp,cc                             34 A9
pshs  pc,y,x                                 34 B0
pshs  pc,y,x,a                               34 B2
pshs  pc,y,x,a,cc                            34 B3
pshs  pc,y,x,b                               34 B4
pshs  pc,y,x,b,a                             34 B6
pshs  pc,y,x,b,a,cc                          34 B7
pshs  pc,y,x,b,cc                            34 B5
pshs  pc,y,x,cc                              34 B1
pshs  pc,y,x,dp                              34 B8
pshs  pc,y,x,dp,a                            34 BA
pshs  pc,y,x,dp,a,cc                         34 BB
pshs  pc,y,x,dp,b                            34 BC
pshs  pc,y,x,dp,b,a                          34 BE
pshs  pc,y,x,dp,b,a,cc                       34 BF
pshs  pc,y,x,dp,b,cc                         34 BD
pshs  pc,y,x,dp,cc                           34 B9
pshs  u                                      34 40
pshs  u,a                                    34 42
pshs  u,a,cc                                 34 43
pshs  u,b                                    34 44
pshs  u,b,a                                  34 46
pshs  u,b,a,cc                               34 47
pshs  u,b,cc                                 34 45
pshs  u,cc                                   34 41
pshs  u,dp                                   34 48
pshs  u,dp,a                                 34 4A
pshs  u,dp,a,cc                              34 4B
pshs  u,dp,b                                 34 4C
pshs  u,dp,b,a                               34 4E
pshs  u,dp,b,a,cc                            34 4F
pshs  u,dp,b,cc                              34 4D
pshs  u,dp,cc                                34 49
pshs  u,x                                    34 50
pshs  u,x,a                                  34 52
pshs  u,x,a,cc                               34 53
pshs  u,x,b                                  34 54
pshs  u,x,b,a                                34 56
pshs  u,x,b,a,cc                             34 57
pshs  u,x,b,cc                               34 55
pshs  u,x,cc                                 34 51
pshs  u,x,dp                                 34 58
pshs  u,x,dp,a                               34 5A
pshs  u,x,dp,a,cc                            34 5B
pshs  u,x,dp,b                               34 5C
pshs  u,x,dp,b,a                             34 5E
pshs  u,x,dp,b,a,cc                          34 5F
pshs  u,x,dp,b,cc                            34 5D
pshs  u,x,dp,cc                              34 59
pshs  u,y                                    34 60
pshs  u,y,a                                  34 62
pshs  u,y,a,cc                               34 63
pshs  u,y,b                                  34 64
pshs  u,y,b,a                                34 66
pshs  u,y,b,a,cc                             34 67
pshs  u,y,b,cc                               34 65
pshs  u,y,cc                                 34 61
pshs  u,y,dp                                 34 68
pshs  u,y,dp,a                               34 6A
pshs  u,y,dp,a,cc                            34 6B
pshs  u,y,dp,b                               34 6C
pshs  u,y,dp,b,a                             34 6E
pshs  u,y,dp,b,a,cc                          34 6F
pshs  u,y,dp,b,cc                            34 6D
pshs  u,y,dp,cc                              34 69
pshs  u,y,x                                  34 70
pshs  u,y,x,a                                34 72
pshs  u,y,x,a,cc                             34 73
pshs  u,y,x,b                                34 74
pshs  u,y,x,b,a                              34 76
pshs  u,y,x,b,a,cc                           34 77
pshs  u,y,x,b,cc                             34 75
pshs  u,y,x,cc                               34 71
pshs  u,y,x,dp                               34 78
pshs  u,y,x,dp,a                             34 7A
pshs  u,y,x,dp,a,cc                          34 7B
pshs  u,y,x,dp,b                             34 7C
pshs  u,y,x,dp,b,a                           34 7E
pshs  u,y,x,dp,b,a,cc                        34 7F
pshs  u,y,x,dp,b,cc                          34 7D
pshs  u,y,x,dp,cc                            34 79
pshs  x                                      34 10
pshs  x,a                                    34 12
pshs  x,a,cc                                 34 13
pshs  x,b                                    34 14
pshs  x,b,a                                  34 16
pshs  x,b,a,cc                               34 17
pshs  x,b,cc                                 34 15
pshs  x,cc                                   34 11
pshs  x,dp                                   34 18
pshs  x,dp,a                                 34 1A
pshs  x,dp,a,cc                              34 1B
pshs  x,dp,b                                 34 1C
pshs  x,dp,b,a                               34 1E
pshs  x,dp,b,a,cc                            34 1F
pshs  x,dp,b,cc                              34 1D
pshs  x,dp,cc                                34 19
pshs  y                                      34 20
pshs  y,a                                    34 22
pshs  y,a,cc                                 34 23
pshs  y,b                                    34 24
pshs  y,b,a                                  34 26
pshs  y,b,a,cc                               34 27
pshs  y,b,cc                                 34 25
pshs  y,cc                                   34 21
pshs  y,dp                                   34 28
pshs  y,dp,a                                 34 2A
pshs  y,dp,a,cc                              34 2B
pshs  y,dp,b                                 34 2C
pshs  y,dp,b,a                               34 2E
pshs  y,dp,b,a,cc                            34 2F
pshs  y,dp,b,cc                              34 2D
pshs  y,dp,cc                                34 29
pshs  y,x                                    34 30
pshs  y,x,a                                  34 32
pshs  y,x,a,cc                               34 33
pshs  y,x,b                                  34 34
pshs  y,x,b,a                                34 36
pshs  y,x,b,a,cc                             34 37
pshs  y,x,b,cc                               34 35
pshs  y,x,cc                                 34 31
pshs  y,x,dp                                 34 38
pshs  y,x,dp,a                               34 3A
pshs  y,x,dp,a,cc                            34 3B
pshs  y,x,dp,b                               34 3C
pshs  y,x,dp,b,a                             34 3E
pshs  y,x,dp,b,a,cc                          34 3F
pshs  y,x,dp,b,cc                            34 3D
pshs  y,x,dp,cc                              34 39
pshu                                         36 00
pshu  a                                      36 02
pshu  a,cc                                   36 03
pshu  b                                      36 04
pshu  b,a                                    36 06
pshu  b,a,cc                                 36 07
pshu  b,cc                                   36 05
pshu  cc                                     36 01
pshu  dp                                     36 08
pshu  dp,a                                   36 0A
pshu  dp,a,cc                                36 0B
pshu  dp,b                                   36 0C
pshu  dp,b,a                                 36 0E
pshu  dp,b,a,cc                              36 0F
pshu  dp,b,cc                                36 0D
pshu  dp,cc                                  36 09
pshu  pc                                     36 80
pshu  pc,a                                   36 82
pshu  pc,a,cc                                36 83
pshu  pc,b                                   36 84
pshu  pc,b,a                                 36 86
pshu  pc,b,a,cc                              36 87
pshu  pc,b,cc                                36 85
pshu  pc,cc                                  36 81
pshu  pc,dp                                  36 88
pshu  pc,dp,a                                36 8A
pshu  pc,dp,a,cc                             36 8B
pshu  pc,dp,b                                36 8C
pshu  pc,dp,b,a                              36 8E
pshu  pc,dp,b,a,cc                           36 8F
pshu  pc,dp,b,cc                             36 8D
pshu  pc,dp,cc                               36 89
pshu  pc,s                                   36 C0
pshu  pc,s,a                                 36 C2
pshu  pc,s,a,cc                              36 C3
pshu  pc,s,b                                 36 C4
pshu  pc,s,b,a                               36 C6
pshu  pc,s,b,a,cc                            36 C7
pshu  pc,s,b,cc                              36 C5
pshu  pc,s,cc                                36 C1
pshu  pc,s,dp                                36 C8
pshu  pc,s,dp,a                              36 CA
pshu  pc,s,dp,a,cc                           36 CB
pshu  pc,s,dp,b                              36 CC
pshu  pc,s,dp,b,a                            36 CE
pshu  pc,s,dp,b,a,cc                         36 CF
pshu  pc,s,dp,b,cc                           36 CD
pshu  pc,s,dp,cc                             36 C9
pshu  pc,s,x                                 36 D0
pshu  pc,s,x,a                               36 D2
pshu  pc,s,x,a,cc                            36 D3
pshu  pc,s,x,b                               36 D4
pshu  pc,s,x,b,a                             36 D6
pshu  pc,s,x,b,a,cc                          36 D7
pshu  pc,s,x,b,cc                            36 D5
pshu  pc,s,x,cc                              36 D1
pshu  pc,s,x,dp                              36 D8
pshu  pc,s,x,dp,a                            36 DA
pshu  pc,s,x,dp,a,cc                         36 DB
pshu  pc,s,x,dp,b                            36 DC
pshu  pc,s,x,dp,b,a                          36 DE
pshu  pc,s,x,dp,b,a,cc                       36 DF
pshu  pc,s,x,dp,b,cc                         36 DD
pshu  pc,s,x,dp,cc                           36 D9
pshu  pc,s,y                                 36 E0
pshu  pc,s,y,a                               36 E2
pshu  pc,s,y,a,cc                            36 E3
pshu  pc,s,y,b                               36 E4
pshu  pc,s,y,b,a                             36 E6
pshu  pc,s,y,b,a,cc                          36 E7
pshu  pc,s,y,b,cc                            36 E5
pshu  pc,s,y,cc                              36 E1
pshu  pc,s,y,dp                              36 E8
pshu  pc,s,y,dp,a                            36 EA
pshu  pc,s,y,dp,a,cc                         36 EB
pshu  pc,s,y,dp,b                            36 EC
pshu  pc,s,y,dp,b,a                          36 EE
pshu  pc,s,y,dp,b,a,cc                       36 EF
pshu  pc,s,y,dp,b,cc                         36 ED
pshu  pc,s,y,dp,cc                           36 E9
pshu  pc,s,y,x                               36 F0
pshu  pc,s,y,x,a                             36 F2
pshu  pc,s,y,x,a,cc                          36 F3
pshu  pc,s,y,x,b                             36 F4
pshu  pc,s,y,x,b,a                           36 F6
pshu  pc,s,y,x,b,a,cc                        36 F7
pshu  pc,s,y,x,b,cc                          36 F5
pshu  pc,s,y,x,cc                            36 F1
pshu  pc,s,y,x,dp                            36 F8
pshu  pc,s,y,x,dp,a                          36 FA
pshu  pc,s,y,x,dp,a,cc                       36 FB
pshu  pc,s,y,x,dp,b                          36 FC
pshu  pc,s,y,x,dp,b,a                        36 FE
pshu  pc,s,y,x,dp,b,a,cc                     36 FF
pshu  pc,s,y,x,dp,b,cc                       36 FD
pshu  pc,s,y,x,dp,cc                         36 F9
pshu  pc,x                                   36 90
pshu  pc,x,a                                 36 92
pshu  pc,x,a,cc                              36 93
pshu  pc,x,b                                 36 94
pshu  pc,x,b,a                               36 96
pshu  pc,x,b,a,cc                            36 97
pshu  pc,x,b,cc                              36 95
pshu  pc,x,cc                                36 91
pshu  pc,x,dp                                36 98
pshu  pc,x,dp,a                              36 9A
pshu  pc,x,dp,a,cc                           36 9B
pshu  pc,x,dp,b                              36 9C
pshu  pc,x,dp,b,a                            36 9E
pshu  pc,x,dp,b,a,cc                         36 9F
pshu  pc,x,dp,b,cc                           36 9D
pshu  pc,x,dp,cc                             36 99
pshu  pc,y                                   36 A0
pshu  pc,y,a                                 36 A2
pshu  pc,y,a,cc                              36 A3
pshu  pc,y,b                                 36 A4
pshu  pc,y,b,a                               36 A6
pshu  pc,y,b,a,cc                            36 A7
pshu  pc,y,b,cc                              36 A5
pshu  pc,y,cc                                36 A1
pshu  pc,y,dp                                36 A8
pshu  pc,y,dp,a                              36 AA
pshu  pc,y,dp,a,cc                           36 AB
pshu  pc,y,dp,b                              36 AC
pshu  pc,y,dp,b,a                            36 AE
pshu  pc,y,dp,b,a,cc                         36 AF
pshu  pc,y,dp,b,cc                           36 AD
pshu  pc,y,dp,cc                             36 A9
pshu  pc,y,x                                 36 B0
pshu  pc,y,x,a                               36 B2
pshu  pc,y,x,a,cc                            36 B3
pshu  pc,y,x,b                               36 B4
pshu  pc,y,x,b,a                             36 B6
pshu  pc,y,x,b,a,cc                          36 B7
pshu  pc,y,x,b,cc                            36 B5
pshu  pc,y,x,cc                              36 B1
pshu  pc,y,x,dp                              36 B8
pshu  pc,y,x,dp,a                            36 BA
pshu  pc,y,x,dp,a,cc                         36 BB
pshu  pc,y,x,dp,b                            36 BC
pshu  pc,y,x,dp,b,a                          36 BE
pshu  pc,y,x,dp,b,a,cc                       36 BF
pshu  pc,y,x,dp,b,cc                         36 BD
pshu  pc,y,x,dp,cc                           36 B9
pshu  s                                      36 40
pshu  s,a                                    36 42
pshu  s,a,cc                                 36 43
pshu  s,b                                    36 44
pshu  s,b,a                                  36 46
pshu  s,b,a,cc                               36 47
pshu  s,b,cc                                 36 45
pshu  s,cc                                   36 41
pshu  s,dp                                   36 48
pshu  s,dp,a                                 36 4A
pshu  s,dp,a,cc                              36 4B
pshu  s,dp,b                                 36 4C
pshu  s,dp,b,a                               36 4E
pshu  s,dp,b,a,cc                            36 4F
pshu  s,dp,b,cc                              36 4D
pshu  s,dp,cc                                36 49
pshu  s,x                                    36 50
pshu  s,x,a                                  36 52
pshu  s,x,a,cc                               36 53
pshu  s,x,b                                  36 54
pshu  s,x,b,a                                36 56
pshu  s,x,b,a,cc                             36 57
pshu  s,x,b,cc                               36 55
pshu  s,x,cc                                 36 51
pshu  s,x,dp                                 36 58
pshu  s,x,dp,a                               36 5A
pshu  s,x,dp,a,cc                            36 5B
pshu  s,x,dp,b                               36 5C
pshu  s,x,dp,b,a                             36 5E
pshu  s,x,dp,b,a,cc                          36 5F
pshu  s,x,dp,b,cc                            36 5D
pshu  s,x,dp,cc                              36 59
pshu  s,y                                    36 60
pshu  s,y,a                                  36 62
pshu  s,y,a,cc                               36 63
pshu  s,y,b                                  36 64
pshu  s,y,b,a                                36 66
pshu  s,y,b,a,cc                             36 67
pshu  s,y,b,cc                               36 65
pshu  s,y,cc                                 36 61
pshu  s,y,dp                                 36 68
pshu  s,y,dp,a                               36 6A
pshu  s,y,dp,a,cc                            36 6B
pshu  s,y,dp,b                               36 6C
pshu  s,y,dp,b,a                             36 6E
pshu  s,y,dp,b,a,cc                          36 6F
pshu  s,y,dp,b,cc                            36 6D
pshu  s,y,dp,cc                              36 69
pshu  s,y,x                                  36 70
pshu  s,y,x,a                                36 72
pshu  s,y,x,a,cc                             36 73
pshu  s,y,x,b                                36 74
pshu  s,y,x,b,a                              36 76
pshu  s,y,x,b,a,cc                           36 77
pshu  s,y,x,b,cc                             36 75
pshu  s,y,x,cc                               36 71
pshu  s,y,x,dp                               36 78
pshu  s,y,x,dp,a                             36 7A
pshu  s,y,x,dp,a,cc                          36 7B
pshu  s,y,x,dp,b                             36 7C
pshu  s,y,x,dp,b,a                           36 7E
pshu  s,y,x,dp,b,a,cc                        36 7F
pshu  s,y,x,dp,b,cc                          36 7D
pshu  s,y,x,dp,cc                            36 79
pshu  x                                      36 10
pshu  x,a                                    36 12
pshu  x,a,cc                                 36 13
pshu  x,b                                    36 14
pshu  x,b,a                                  36 16
pshu  x,b,a,cc                               36 17
pshu  x,b,cc                                 36 15
pshu  x,cc                                   36 11
pshu  x,dp                                   36 18
pshu  x,dp,a                                 36 1A
pshu  x,dp,a,cc                              36 1B
pshu  x,dp,b                                 36 1C
pshu  x,dp,b,a                               36 1E
pshu  x,dp,b,a,cc                            36 1F
pshu  x,dp,b,cc                              36 1D
pshu  x,dp,cc                                36 19
pshu  y                                      36 20
pshu  y,a                                    36 22
pshu  y,a,cc                                 36 23
pshu  y,b                                    36 24
pshu  y,b,a                                  36 26
pshu  y,b,a,cc                               36 27
pshu  y,b,cc                                 36 25
pshu  y,cc                                   36 21
pshu  y,dp                                   36 28
pshu  y,dp,a                                 36 2A
pshu  y,dp,a,cc                              36 2B
pshu  y,dp,b                                 36 2C
pshu  y,dp,b,a                               36 2E
pshu  y,dp,b,a,cc                            36 2F
pshu  y,dp,b,cc                              36 2D
pshu  y,dp,cc                                36 29
pshu  y,x                                    36 30
pshu  y,x,a                                  36 32
pshu  y,x,a,cc                               36 33
pshu  y,x,b                                  36 34
pshu  y,x,b,a                                36 36
pshu  y,x,b,a,cc                             36 37
pshu  y,x,b,cc                               36 35
pshu  y,x,cc                                 36 31
pshu  y,x,dp                                 36 38
pshu  y,x,dp,a                               36 3A
pshu  y,x,dp,a,cc                            36 3B
pshu  y,x,dp,b                               36 3C
pshu  y,x,dp,b,a                             36 3E
pshu  y,x,dp,b,a,cc                          36 3F
pshu  y,x,dp,b,cc                            36 3D
pshu  y,x,dp,cc                              36 39
puls                                         35 00
puls  a                                      35 02
puls  a,b                                    35 06
puls  a,b,dp                                 35 0E
puls  a,b,dp,pc ; (pul? pc=rts)              35 8E
puls  a,b,dp,u                               35 4E
puls  a,b,dp,u,pc ; (pul? pc=rts)            35 CE
puls  a,b,dp,x                               35 1E
puls  a,b,dp,x,pc ; (pul? pc=rts)            35 9E
puls  a,b,dp,x,u                             35 5E
puls  a,b,dp,x,u,pc ; (pul? pc=rts)          35 DE
puls  a,b,dp,x,y                             35 3E
puls  a,b,dp,x,y,pc ; (pul? pc=rts)          35 BE
puls  a,b,dp,x,y,u                           35 7E
puls  a,b,dp,x,y,u,pc ; (pul? pc=rts)        35 FE
puls  a,b,dp,y                               35 2E
puls  a,b,dp,y,pc ; (pul? pc=rts)            35 AE
puls  a,b,dp,y,u                             35 6E
puls  a,b,dp,y,u,pc ; (pul? pc=rts)          35 EE
puls  a,b,pc ; (pul? pc=rts)                 35 86
puls  a,b,u                                  35 46
puls  a,b,u,pc ; (pul? pc=rts)               35 C6
puls  a,b,x                                  35 16
puls  a,b,x,pc ; (pul? pc=rts)               35 96
puls  a,b,x,u                                35 56
puls  a,b,x,u,pc ; (pul? pc=rts)             35 D6
puls  a,b,x,y                                35 36
puls  a,b,x,y,pc ; (pul? pc=rts)             35 B6
puls  a,b,x,y,u                              35 76
puls  a,b,x,y,u,pc ; (pul? pc=rts)           35 F6
puls  a,b,y                                  35 26
puls  a,b,y,pc ; (pul? pc=rts)               35 A6
puls  a,b,y,u                                35 66
puls  a,b,y,u,pc ; (pul? pc=rts)             35 E6
puls  a,dp                                   35 0A
puls  a,dp,pc ; (pul? pc=rts)                35 8A
puls  a,dp,u                                 35 4A
puls  a,dp,u,pc ; (pul? pc=rts)              35 CA
puls  a,dp,x                                 35 1A
puls  a,dp,x,pc ; (pul? pc=rts)              35 9A
puls  a,dp,x,u                               35 5A
puls  a,dp,x,u,pc ; (pul? pc=rts)            35 DA
puls  a,dp,x,y                               35 3A
puls  a,dp,x,y,pc ; (pul? pc=rts)            35 BA
puls  a,dp,x,y,u                             35 7A
puls  a,dp,x,y,u,pc ; (pul? pc=rts)          35 FA
puls  a,dp,y                                 35 2A
puls  a,dp,y,pc ; (pul? pc=rts)              35 AA
puls  a,dp,y,u                               35 6A
puls  a,dp,y,u,pc ; (pul? pc=rts)            35 EA
puls  a,pc ; (pul? pc=rts)                   35 82
puls  a,u                                    35 42
puls  a,u,pc ; (pul? pc=rts)                 35 C2
puls  a,x                                    35 12
puls  a,x,pc ; (pul? pc=rts)                 35 92
puls  a,x,u                                  35 52
puls  a,x,u,pc ; (pul? pc=rts)               35 D2
puls  a,x,y                                  35 32
puls  a,x,y,pc ; (pul? pc=rts)               35 B2
puls  a,x,y,u                                35 72
puls  a,x,y,u,pc ; (pul? pc=rts)             35 F2
puls  a,y                                    35 22
puls  a,y,pc ; (pul? pc=rts)                 35 A2
puls  a,y,u                                  35 62
puls  a,y,u,pc ; (pul? pc=rts)               35 E2
puls  b                                      35 04
puls  b,dp                                   35 0C
puls  b,dp,pc ; (pul? pc=rts)                35 8C
puls  b,dp,u                                 35 4C
puls  b,dp,u,pc ; (pul? pc=rts)              35 CC
puls  b,dp,x                                 35 1C
puls  b,dp,x,pc ; (pul? pc=rts)              35 9C
puls  b,dp,x,u                               35 5C
puls  b,dp,x,u,pc ; (pul? pc=rts)            35 DC
puls  b,dp,x,y                               35 3C
puls  b,dp,x,y,pc ; (pul? pc=rts)            35 BC
puls  b,dp,x,y,u                             35 7C
puls  b,dp,x,y,u,pc ; (pul? pc=rts)          35 FC
puls  b,dp,y                                 35 2C
puls  b,dp,y,pc ; (pul? pc=rts)              35 AC
puls  b,dp,y,u                               35 6C
puls  b,dp,y,u,pc ; (pul? pc=rts)            35 EC
puls  b,pc ; (pul? pc=rts)                   35 84
puls  b,u                                    35 44
puls  b,u,pc ; (pul? pc=rts)                 35 C4
puls  b,x                                    35 14
puls  b,x,pc ; (pul? pc=rts)                 35 94
puls  b,x,u                                  35 54
puls  b,x,u,pc ; (pul? pc=rts)               35 D4
puls  b,x,y                                  35 34
puls  b,x,y,pc ; (pul? pc=rts)               35 B4
puls  b,x,y,u                                35 74
puls  b,x,y,u,pc ; (pul? pc=rts)             35 F4
puls  b,y                                    35 24
puls  b,y,pc ; (pul? pc=rts)                 35 A4
puls  b,y,u                                  35 64
puls  b,y,u,pc ; (pul? pc=rts)               35 E4
puls  cc                                     35 01
puls  cc,a                                   35 03
puls  cc,a,b                                 35 07
puls  cc,a,b,dp                              35 0F
puls  cc,a,b,dp,pc ; (pul? pc=rts)           35 8F
puls  cc,a,b,dp,u                            35 4F
puls  cc,a,b,dp,u,pc ; (pul? pc=rts)         35 CF
puls  cc,a,b,dp,x                            35 1F
puls  cc,a,b,dp,x,pc ; (pul? pc=rts)         35 9F
puls  cc,a,b,dp,x,u                          35 5F
puls  cc,a,b,dp,x,u,pc ; (pul? pc=rts)       35 DF
puls  cc,a,b,dp,x,y                          35 3F
puls  cc,a,b,dp,x,y,pc ; (pul? pc=rts)       35 BF
puls  cc,a,b,dp,x,y,u                        35 7F
puls  cc,a,b,dp,x,y,u,pc ; (pul? pc=rts)     35 FF
puls  cc,a,b,dp,y                            35 2F
puls  cc,a,b,dp,y,pc ; (pul? pc=rts)         35 AF
puls  cc,a,b,dp,y,u                          35 6F
puls  cc,a,b,dp,y,u,pc ; (pul? pc=rts)       35 EF
puls  cc,a,b,pc ; (pul? pc=rts)              35 87
puls  cc,a,b,u                               35 47
puls  cc,a,b,u,pc ; (pul? pc=rts)            35 C7
puls  cc,a,b,x                               35 17
puls  cc,a,b,x,pc ; (pul? pc=rts)            35 97
puls  cc,a,b,x,u                             35 57
puls  cc,a,b,x,u,pc ; (pul? pc=rts)          35 D7
puls  cc,a,b,x,y                             35 37
puls  cc,a,b,x,y,pc ; (pul? pc=rts)          35 B7
puls  cc,a,b,x,y,u                           35 77
puls  cc,a,b,x,y,u,pc ; (pul? pc=rts)        35 F7
puls  cc,a,b,y                               35 27
puls  cc,a,b,y,pc ; (pul? pc=rts)            35 A7
puls  cc,a,b,y,u                             35 67
puls  cc,a,b,y,u,pc ; (pul? pc=rts)          35 E7
puls  cc,a,dp                                35 0B
puls  cc,a,dp,pc ; (pul? pc=rts)             35 8B
puls  cc,a,dp,u                              35 4B
puls  cc,a,dp,u,pc ; (pul? pc=rts)           35 CB
puls  cc,a,dp,x                              35 1B
puls  cc,a,dp,x,pc ; (pul? pc=rts)           35 9B
puls  cc,a,dp,x,u                            35 5B
puls  cc,a,dp,x,u,pc ; (pul? pc=rts)         35 DB
puls  cc,a,dp,x,y                            35 3B
puls  cc,a,dp,x,y,pc ; (pul? pc=rts)         35 BB
puls  cc,a,dp,x,y,u                          35 7B
puls  cc,a,dp,x,y,u,pc ; (pul? pc=rts)       35 FB
puls  cc,a,dp,y                              35 2B
puls  cc,a,dp,y,pc ; (pul? pc=rts)           35 AB
puls  cc,a,dp,y,u                            35 6B
puls  cc,a,dp,y,u,pc ; (pul? pc=rts)         35 EB
puls  cc,a,pc ; (pul? pc=rts)                35 83
puls  cc,a,u                                 35 43
puls  cc,a,u,pc ; (pul? pc=rts)              35 C3
puls  cc,a,x                                 35 13
puls  cc,a,x,pc ; (pul? pc=rts)              35 93
puls  cc,a,x,u                               35 53
puls  cc,a,x,u,pc ; (pul? pc=rts)            35 D3
puls  cc,a,x,y                               35 33
puls  cc,a,x,y,pc ; (pul? pc=rts)            35 B3
puls  cc,a,x,y,u                             35 73
puls  cc,a,x,y,u,pc ; (pul? pc=rts)          35 F3
puls  cc,a,y                                 35 23
puls  cc,a,y,pc ; (pul? pc=rts)              35 A3
puls  cc,a,y,u                               35 63
puls  cc,a,y,u,pc ; (pul? pc=rts)            35 E3
puls  cc,b                                   35 05
puls  cc,b,dp                                35 0D
puls  cc,b,dp,pc ; (pul? pc=rts)             35 8D
puls  cc,b,dp,u                              35 4D
puls  cc,b,dp,u,pc ; (pul? pc=rts)           35 CD
puls  cc,b,dp,x                              35 1D
puls  cc,b,dp,x,pc ; (pul? pc=rts)           35 9D
puls  cc,b,dp,x,u                            35 5D
puls  cc,b,dp,x,u,pc ; (pul? pc=rts)         35 DD
puls  cc,b,dp,x,y                            35 3D
puls  cc,b,dp,x,y,pc ; (pul? pc=rts)         35 BD
puls  cc,b,dp,x,y,u                          35 7D
puls  cc,b,dp,x,y,u,pc ; (pul? pc=rts)       35 FD
puls  cc,b,dp,y                              35 2D
puls  cc,b,dp,y,pc ; (pul? pc=rts)           35 AD
puls  cc,b,dp,y,u                            35 6D
puls  cc,b,dp,y,u,pc ; (pul? pc=rts)         35 ED
puls  cc,b,pc ; (pul? pc=rts)                35 85
puls  cc,b,u                                 35 45
puls  cc,b,u,pc ; (pul? pc=rts)              35 C5
puls  cc,b,x                                 35 15
puls  cc,b,x,pc ; (pul? pc=rts)              35 95
puls  cc,b,x,u                               35 55
puls  cc,b,x,u,pc ; (pul? pc=rts)            35 D5
puls  cc,b,x,y                               35 35
puls  cc,b,x,y,pc ; (pul? pc=rts)            35 B5
puls  cc,b,x,y,u                             35 75
puls  cc,b,x,y,u,pc ; (pul? pc=rts)          35 F5
puls  cc,b,y                                 35 25
puls  cc,b,y,pc ; (pul? pc=rts)              35 A5
puls  cc,b,y,u                               35 65
puls  cc,b,y,u,pc ; (pul? pc=rts)            35 E5
puls  cc,dp                                  35 09
puls  cc,dp,pc ; (pul? pc=rts)               35 89
puls  cc,dp,u                                35 49
puls  cc,dp,u,pc ; (pul? pc=rts)             35 C9
puls  cc,dp,x                                35 19
puls  cc,dp,x,pc ; (pul? pc=rts)             35 99
puls  cc,dp,x,u                              35 59
puls  cc,dp,x,u,pc ; (pul? pc=rts)           35 D9
puls  cc,dp,x,y                              35 39
puls  cc,dp,x,y,pc ; (pul? pc=rts)           35 B9
puls  cc,dp,x,y,u                            35 79
puls  cc,dp,x,y,u,pc ; (pul? pc=rts)         35 F9
puls  cc,dp,y                                35 29
puls  cc,dp,y,pc ; (pul? pc=rts)             35 A9
puls  cc,dp,y,u                              35 69
puls  cc,dp,y,u,pc ; (pul? pc=rts)           35 E9
puls  cc,pc ; (pul? pc=rts)                  35 81
puls  cc,u                                   35 41
puls  cc,u,pc ; (pul? pc=rts)                35 C1
puls  cc,x                                   35 11
puls  cc,x,pc ; (pul? pc=rts)                35 91
puls  cc,x,u                                 35 51
puls  cc,x,u,pc ; (pul? pc=rts)              35 D1
puls  cc,x,y                                 35 31
puls  cc,x,y,pc ; (pul? pc=rts)              35 B1
puls  cc,x,y,u                               35 71
puls  cc,x,y,u,pc ; (pul? pc=rts)            35 F1
puls  cc,y                                   35 21
puls  cc,y,pc ; (pul? pc=rts)                35 A1
puls  cc,y,u                                 35 61
puls  cc,y,u,pc ; (pul? pc=rts)              35 E1
puls  dp                                     35 08
puls  dp,pc ; (pul? pc=rts)                  35 88
puls  dp,u                                   35 48
puls  dp,u,pc ; (pul? pc=rts)                35 C8
puls  dp,x                                   35 18
puls  dp,x,pc ; (pul? pc=rts)                35 98
puls  dp,x,u                                 35 58
puls  dp,x,u,pc ; (pul? pc=rts)              35 D8
puls  dp,x,y                                 35 38
puls  dp,x,y,pc ; (pul? pc=rts)              35 B8
puls  dp,x,y,u                               35 78
puls  dp,x,y,u,pc ; (pul? pc=rts)            35 F8
puls  dp,y                                   35 28
puls  dp,y,pc ; (pul? pc=rts)                35 A8
puls  dp,y,u                                 35 68
puls  dp,y,u,pc ; (pul? pc=rts)              35 E8
puls  pc ; (pul? pc=rts)                     35 80
puls  u                                      35 40
puls  u,pc ; (pul? pc=rts)                   35 C0
puls  x                                      35 10
puls  x,pc ; (pul? pc=rts)                   35 90
puls  x,u                                    35 50
puls  x,u,pc ; (pul? pc=rts)                 35 D0
puls  x,y                                    35 30
puls  x,y,pc ; (pul? pc=rts)                 35 B0
puls  x,y,u                                  35 70
puls  x,y,u,pc ; (pul? pc=rts)               35 F0
puls  y                                      35 20
puls  y,pc ; (pul? pc=rts)                   35 A0
puls  y,u                                    35 60
puls  y,u,pc ; (pul? pc=rts)                 35 E0
pulu                                         37 00
pulu  a                                      37 02
pulu  a,b                                    37 06
pulu  a,b,dp                                 37 0E
pulu  a,b,dp,pc ; (pul? pc=rts)              37 8E
pulu  a,b,dp,s                               37 4E
pulu  a,b,dp,s,pc ; (pul? pc=rts)            37 CE
pulu  a,b,dp,x                               37 1E
pulu  a,b,dp,x,pc ; (pul? pc=rts)            37 9E
pulu  a,b,dp,x,s                             37 5E
pulu  a,b,dp,x,s,pc ; (pul? pc=rts)          37 DE
pulu  a,b,dp,x,y                             37 3E
pulu  a,b,dp,x,y,pc ; (pul? pc=rts)          37 BE
pulu  a,b,dp,x,y,s                           37 7E
pulu  a,b,dp,x,y,s,pc ; (pul? pc=rts)        37 FE
pulu  a,b,dp,y                               37 2E
pulu  a,b,dp,y,pc ; (pul? pc=rts)            37 AE
pulu  a,b,dp,y,s                             37 6E
pulu  a,b,dp,y,s,pc ; (pul? pc=rts)          37 EE
pulu  a,b,pc ; (pul? pc=rts)                 37 86
pulu  a,b,s                                  37 46
pulu  a,b,s,pc ; (pul? pc=rts)               37 C6
pulu  a,b,x                                  37 16
pulu  a,b,x,pc ; (pul? pc=rts)               37 96
pulu  a,b,x,s                                37 56
pulu  a,b,x,s,pc ; (pul? pc=rts)             37 D6
pulu  a,b,x,y                                37 36
pulu  a,b,x,y,pc ; (pul? pc=rts)             37 B6
pulu  a,b,x,y,s                              37 76
pulu  a,b,x,y,s,pc ; (pul? pc=rts)           37 F6
pulu  a,b,y                                  37 26
pulu  a,b,y,pc ; (pul? pc=rts)               37 A6
pulu  a,b,y,s                                37 66
pulu  a,b,y,s,pc ; (pul? pc=rts)             37 E6
pulu  a,dp                                   37 0A
pulu  a,dp,pc ; (pul? pc=rts)                37 8A
pulu  a,dp,s                                 37 4A
pulu  a,dp,s,pc ; (pul? pc=rts)              37 CA
pulu  a,dp,x                                 37 1A
pulu  a,dp,x,pc ; (pul? pc=rts)              37 9A
pulu  a,dp,x,s                               37 5A
pulu  a,dp,x,s,pc ; (pul? pc=rts)            37 DA
pulu  a,dp,x,y                               37 3A
pulu  a,dp,x,y,pc ; (pul? pc=rts)            37 BA
pulu  a,dp,x,y,s                             37 7A
pulu  a,dp,x,y,s,pc ; (pul? pc=rts)          37 FA
pulu  a,dp,y                                 37 2A
pulu  a,dp,y,pc ; (pul? pc=rts)              37 AA
pulu  a,dp,y,s                               37 6A
pulu  a,dp,y,s,pc ; (pul? pc=rts)            37 EA
pulu  a,pc ; (pul? pc=rts)                   37 82
pulu  a,s                                    37 42
pulu  a,s,pc ; (pul? pc=rts)                 37 C2
pulu  a,x                                    37 12
pulu  a,x,pc ; (pul? pc=rts)                 37 92
pulu  a,x,s                                  37 52
pulu  a,x,s,pc ; (pul? pc=rts)               37 D2
pulu  a,x,y                                  37 32
pulu  a,x,y,pc ; (pul? pc=rts)               37 B2
pulu  a,x,y,s                                37 72
pulu  a,x,y,s,pc ; (pul? pc=rts)             37 F2
pulu  a,y                                    37 22
pulu  a,y,pc ; (pul? pc=rts)                 37 A2
pulu  a,y,s                                  37 62
pulu  a,y,s,pc ; (pul? pc=rts)               37 E2
pulu  b                                      37 04
pulu  b,dp                                   37 0C
pulu  b,dp,pc ; (pul? pc=rts)                37 8C
pulu  b,dp,s                                 37 4C
pulu  b,dp,s,pc ; (pul? pc=rts)              37 CC
pulu  b,dp,x                                 37 1C
pulu  b,dp,x,pc ; (pul? pc=rts)              37 9C
pulu  b,dp,x,s                               37 5C
pulu  b,dp,x,s,pc ; (pul? pc=rts)            37 DC
pulu  b,dp,x,y                               37 3C
pulu  b,dp,x,y,pc ; (pul? pc=rts)            37 BC
pulu  b,dp,x,y,s                             37 7C
pulu  b,dp,x,y,s,pc ; (pul? pc=rts)          37 FC
pulu  b,dp,y                                 37 2C
pulu  b,dp,y,pc ; (pul? pc=rts)              37 AC
pulu  b,dp,y,s                               37 6C
pulu  b,dp,y,s,pc ; (pul? pc=rts)            37 EC
pulu  b,pc ; (pul? pc=rts)                   37 84
pulu  b,s                                    37 44
pulu  b,s,pc ; (pul? pc=rts)                 37 C4
pulu  b,x                                    37 14
pulu  b,x,pc ; (pul? pc=rts)                 37 94
pulu  b,x,s                                  37 54
pulu  b,x,s,pc ; (pul? pc=rts)               37 D4
pulu  b,x,y                                  37 34
pulu  b,x,y,pc ; (pul? pc=rts)               37 B4
pulu  b,x,y,s                                37 74
pulu  b,x,y,s,pc ; (pul? pc=rts)             37 F4
pulu  b,y                                    37 24
pulu  b,y,pc ; (pul? pc=rts)                 37 A4
pulu  b,y,s                                  37 64
pulu  b,y,s,pc ; (pul? pc=rts)               37 E4
pulu  cc                                     37 01
pulu  cc,a                                   37 03
pulu  cc,a,b                                 37 07
pulu  cc,a,b,dp                              37 0F
pulu  cc,a,b,dp,pc ; (pul? pc=rts)           37 8F
pulu  cc,a,b,dp,s                            37 4F
pulu  cc,a,b,dp,s,pc ; (pul? pc=rts)         37 CF
pulu  cc,a,b,dp,x                            37 1F
pulu  cc,a,b,dp,x,pc ; (pul? pc=rts)         37 9F
pulu  cc,a,b,dp,x,s                          37 5F
pulu  cc,a,b,dp,x,s,pc ; (pul? pc=rts)       37 DF
pulu  cc,a,b,dp,x,y                          37 3F
pulu  cc,a,b,dp,x,y,pc ; (pul? pc=rts)       37 BF
pulu  cc,a,b,dp,x,y,s                        37 7F
pulu  cc,a,b,dp,x,y,s,pc ; (pul? pc=rts)     37 FF
pulu  cc,a,b,dp,y                            37 2F
pulu  cc,a,b,dp,y,pc ; (pul? pc=rts)         37 AF
pulu  cc,a,b,dp,y,s                          37 6F
pulu  cc,a,b,dp,y,s,pc ; (pul? pc=rts)       37 EF
pulu  cc,a,b,pc ; (pul? pc=rts)              37 87
pulu  cc,a,b,s                               37 47
pulu  cc,a,b,s,pc ; (pul? pc=rts)            37 C7
pulu  cc,a,b,x                               37 17
pulu  cc,a,b,x,pc ; (pul? pc=rts)            37 97
pulu  cc,a,b,x,s                             37 57
pulu  cc,a,b,x,s,pc ; (pul? pc=rts)          37 D7
pulu  cc,a,b,x,y                             37 37
pulu  cc,a,b,x,y,pc ; (pul? pc=rts)          37 B7
pulu  cc,a,b,x,y,s                           37 77
pulu  cc,a,b,x,y,s,pc ; (pul? pc=rts)        37 F7
pulu  cc,a,b,y                               37 27
pulu  cc,a,b,y,pc ; (pul? pc=rts)            37 A7
pulu  cc,a,b,y,s                             37 67
pulu  cc,a,b,y,s,pc ; (pul? pc=rts)          37 E7
pulu  cc,a,dp                                37 0B
pulu  cc,a,dp,pc ; (pul? pc=rts)             37 8B
pulu  cc,a,dp,s                              37 4B
pulu  cc,a,dp,s,pc ; (pul? pc=rts)           37 CB
pulu  cc,a,dp,x                              37 1B
pulu  cc,a,dp,x,pc ; (pul? pc=rts)           37 9B
pulu  cc,a,dp,x,s                            37 5B
pulu  cc,a,dp,x,s,pc ; (pul? pc=rts)         37 DB
pulu  cc,a,dp,x,y                            37 3B
pulu  cc,a,dp,x,y,pc ; (pul? pc=rts)         37 BB
pulu  cc,a,dp,x,y,s                          37 7B
pulu  cc,a,dp,x,y,s,pc ; (pul? pc=rts)       37 FB
pulu  cc,a,dp,y                              37 2B
pulu  cc,a,dp,y,pc ; (pul? pc=rts)           37 AB
pulu  cc,a,dp,y,s                            37 6B
pulu  cc,a,dp,y,s,pc ; (pul? pc=rts)         37 EB
pulu  cc,a,pc ; (pul? pc=rts)                37 83
pulu  cc,a,s                                 37 43
pulu  cc,a,s,pc ; (pul? pc=rts)              37 C3
pulu  cc,a,x                                 37 13
pulu  cc,a,x,pc ; (pul? pc=rts)              37 93
pulu  cc,a,x,s                               37 53
pulu  cc,a,x,s,pc ; (pul? pc=rts)            37 D3
pulu  cc,a,x,y                               37 33
pulu  cc,a,x,y,pc ; (pul? pc=rts)            37 B3
pulu  cc,a,x,y,s                             37 73
pulu  cc,a,x,y,s,pc ; (pul? pc=rts)          37 F3
pulu  cc,a,y                                 37 23
pulu  cc,a,y,pc ; (pul? pc=rts)              37 A3
pulu  cc,a,y,s                               37 63
pulu  cc,a,y,s,pc ; (pul? pc=rts)            37 E3
pulu  cc,b                                   37 05
pulu  cc,b,dp                                37 0D
pulu  cc,b,dp,pc ; (pul? pc=rts)             37 8D
pulu  cc,b,dp,s                              37 4D
pulu  cc,b,dp,s,pc ; (pul? pc=rts)           37 CD
pulu  cc,b,dp,x                              37 1D
pulu  cc,b,dp,x,pc ; (pul? pc=rts)           37 9D
pulu  cc,b,dp,x,s                            37 5D
pulu  cc,b,dp,x,s,pc ; (pul? pc=rts)         37 DD
pulu  cc,b,dp,x,y                            37 3D
pulu  cc,b,dp,x,y,pc ; (pul? pc=rts)         37 BD
pulu  cc,b,dp,x,y,s                          37 7D
pulu  cc,b,dp,x,y,s,pc ; (pul? pc=rts)       37 FD
pulu  cc,b,dp,y                              37 2D
pulu  cc,b,dp,y,pc ; (pul? pc=rts)           37 AD
pulu  cc,b,dp,y,s                            37 6D
pulu  cc,b,dp,y,s,pc ; (pul? pc=rts)         37 ED
pulu  cc,b,pc ; (pul? pc=rts)                37 85
pulu  cc,b,s                                 37 45
pulu  cc,b,s,pc ; (pul? pc=rts)              37 C5
pulu  cc,b,x                                 37 15
pulu  cc,b,x,pc ; (pul? pc=rts)              37 95
pulu  cc,b,x,s                               37 55
pulu  cc,b,x,s,pc ; (pul? pc=rts)            37 D5
pulu  cc,b,x,y                               37 35
pulu  cc,b,x,y,pc ; (pul? pc=rts)            37 B5
pulu  cc,b,x,y,s                             37 75
pulu  cc,b,x,y,s,pc ; (pul? pc=rts)          37 F5
pulu  cc,b,y                                 37 25
pulu  cc,b,y,pc ; (pul? pc=rts)              37 A5
pulu  cc,b,y,s                               37 65
pulu  cc,b,y,s,pc ; (pul? pc=rts)            37 E5
pulu  cc,dp                                  37 09
pulu  cc,dp,pc ; (pul? pc=rts)               37 89
pulu  cc,dp,s                                37 49
pulu  cc,dp,s,pc ; (pul? pc=rts)             37 C9
pulu  cc,dp,x                                37 19
pulu  cc,dp,x,pc ; (pul? pc=rts)             37 99
pulu  cc,dp,x,s                              37 59
pulu  cc,dp,x,s,pc ; (pul? pc=rts)           37 D9
pulu  cc,dp,x,y                              37 39
pulu  cc,dp,x,y,pc ; (pul? pc=rts)           37 B9
pulu  cc,dp,x,y,s                            37 79
pulu  cc,dp,x,y,s,pc ; (pul? pc=rts)         37 F9
pulu  cc,dp,y                                37 29
pulu  cc,dp,y,pc ; (pul? pc=rts)             37 A9
pulu  cc,dp,y,s                              37 69
pulu  cc,dp,y,s,pc ; (pul? pc=rts)           37 E9
pulu  cc,pc ; (pul? pc=rts)                  37 81
pulu  cc,s                                   37 41
pulu  cc,s,pc ; (pul? pc=rts)                37 C1
pulu  cc,x                                   37 11
pulu  cc,x,pc ; (pul? pc=rts)                37 91
pulu  cc,x,s                                 37 51
pulu  cc,x,s,pc ; (pul? pc=rts)              37 D1
pulu  cc,x,y                                 37 31
pulu  cc,x,y,pc ; (pul? pc=rts)              37 B1
pulu  cc,x,y,s                               37 71
pulu  cc,x,y,s,pc ; (pul? pc=rts)            37 F1
pulu  cc,y                                   37 21
pulu  cc,y,pc ; (pul? pc=rts)                37 A1
pulu  cc,y,s                                 37 61
pulu  cc,y,s,pc ; (pul? pc=rts)              37 E1
pulu  dp                                     37 08
pulu  dp,pc ; (pul? pc=rts)                  37 88
pulu  dp,s                                   37 48
pulu  dp,s,pc ; (pul? pc=rts)                37 C8
pulu  dp,x                                   37 18
pulu  dp,x,pc ; (pul? pc=rts)                37 98
pulu  dp,x,s                                 37 58
pulu  dp,x,s,pc ; (pul? pc=rts)              37 D8
pulu  dp,x,y                                 37 38
pulu  dp,x,y,pc ; (pul? pc=rts)              37 B8
pulu  dp,x,y,s                               37 78
pulu  dp,x,y,s,pc ; (pul? pc=rts)            37 F8
pulu  dp,y                                   37 28
pulu  dp,y,pc ; (pul? pc=rts)                37 A8
pulu  dp,y,s                                 37 68
pulu  dp,y,s,pc ; (pul? pc=rts)              37 E8
pulu  pc ; (pul? pc=rts)                     37 80
pulu  s                                      37 40
pulu  s,pc ; (pul? pc=rts)                   37 C0
pulu  x                                      37 10
pulu  x,pc ; (pul? pc=rts)                   37 90
pulu  x,s                                    37 50
pulu  x,s,pc ; (pul? pc=rts)                 37 D0
pulu  x,y                                    37 30
pulu  x,y,pc ; (pul? pc=rts)                 37 B0
pulu  x,y,s                                  37 70
pulu  x,y,s,pc ; (pul? pc=rts)               37 F0
pulu  y                                      37 20
pulu  y,pc ; (pul? pc=rts)                   37 A0
pulu  y,s                                    37 60
pulu  y,s,pc ; (pul? pc=rts)                 37 E0
rol   $0,s                                   69 60
rol   $0,u                                   69 40
rol   $0,x                                   69 00
rol   $0,y                                   69 20
rol   $01,pc                                 69 8C 01
rol   $01,pc                                 69 AC 01
rol   $01,pc                                 69 CC 01
rol   $01,pc                                 69 EC 01
rol   $01,s                                  69 E8 01
rol   $01,u                                  69 C8 01
rol   $01,x                                  69 88 01
rol   $01,y                                  69 A8 01
rol   $1,s                                   69 61
rol   $1,u                                   69 41
rol   $1,x                                   69 01
rol   $1,y                                   69 21
rol   $2,s                                   69 62
rol   $2,u                                   69 42
rol   $2,x                                   69 02
rol   $2,y                                   69 22
rol   $3,s                                   69 63
rol   $3,u                                   69 43
rol   $3,x                                   69 03
rol   $3,y                                   69 23
rol   $4,s                                   69 64
rol   $4,u                                   69 44
rol   $4,x                                   69 04
rol   $4,y                                   69 24
rol   $5,s                                   69 65
rol   $5,u                                   69 45
rol   $5,x                                   69 05
rol   $5,y                                   69 25
rol   $6,s                                   69 66
rol   $6,u                                   69 46
rol   $6,x                                   69 06
rol   $6,y                                   69 26
rol   $7,s                                   69 67
rol   $7,u                                   69 47
rol   $7,x                                   69 07
rol   $7,y                                   69 27
rol   $8,s                                   69 68
rol   $8,u                                   69 48
rol   $8,x                                   69 08
rol   $8,y                                   69 28
rol   $9,s                                   69 69
rol   $9,u                                   69 49
rol   $9,x                                   69 09
rol   $9,y                                   69 29
rol   $a,s                                   69 6A
rol   $a,u                                   69 4A
rol   $a,x                                   69 0A
rol   $a,y                                   69 2A
rol   $b,s                                   69 6B
rol   $b,u                                   69 4B
rol   $b,x                                   69 0B
rol   $b,y                                   69 2B
rol   $beef                                  69 8F BE EF
rol   $beef                                  69 AF BE EF
rol   $beef                                  69 CF BE EF
rol   $beef                                  69 EF BE EF
rol   $beef                                  79 BE EF
rol   $beef,pc                               69 8D BE EF
rol   $beef,pc                               69 AD BE EF
rol   $beef,pc                               69 CD BE EF
rol   $beef,pc                               69 ED BE EF
rol   $beef,s                                69 E9 BE EF
rol   $beef,u                                69 C9 BE EF
rol   $beef,x                                69 89 BE EF
rol   $beef,y                                69 A9 BE EF
rol   $c,s                                   69 6C
rol   $c,u                                   69 4C
rol   $c,x                                   69 0C
rol   $c,y                                   69 2C
rol   $d,s                                   69 6D
rol   $d,u                                   69 4D
rol   $d,x                                   69 0D
rol   $d,y                                   69 2D
rol   $e,s                                   69 6E
rol   $e,u                                   69 4E
rol   $e,x                                   69 0E
rol   $e,y                                   69 2E
rol   $f,s                                   69 6F
rol   $f,u                                   69 4F
rol   $f,x                                   69 0F
rol   $f,y                                   69 2F
rol   $ff                                    09 FF
rol   ,--s                                   69 E3
rol   ,--u                                   69 C3
rol   ,--x                                   69 83
rol   ,--y                                   69 A3
rol   ,-s                                    69 E2
rol   ,-u                                    69 C2
rol   ,-x                                    69 82
rol   ,-y                                    69 A2
rol   ,s                                     69 E4
rol   ,s+                                    69 E0
rol   ,s++                                   69 E1
rol   ,u                                     69 C4
rol   ,u+                                    69 C0
rol   ,u++                                   69 C1
rol   ,x                                     69 84
rol   ,x+                                    69 80
rol   ,x++                                   69 81
rol   ,y                                     69 A4
rol   ,y+                                    69 A0
rol   ,y++                                   69 A1
rol   -$1,s                                  69 7F
rol   -$1,u                                  69 5F
rol   -$1,x                                  69 1F
rol   -$1,y                                  69 3F
rol   -$10,s                                 69 70
rol   -$10,u                                 69 50
rol   -$10,x                                 69 10
rol   -$10,y                                 69 30
rol   -$2,s                                  69 7E
rol   -$2,u                                  69 5E
rol   -$2,x                                  69 1E
rol   -$2,y                                  69 3E
rol   -$3,s                                  69 7D
rol   -$3,u                                  69 5D
rol   -$3,x                                  69 1D
rol   -$3,y                                  69 3D
rol   -$4,s                                  69 7C
rol   -$4,u                                  69 5C
rol   -$4,x                                  69 1C
rol   -$4,y                                  69 3C
rol   -$5,s                                  69 7B
rol   -$5,u                                  69 5B
rol   -$5,x                                  69 1B
rol   -$5,y                                  69 3B
rol   -$6,s                                  69 7A
rol   -$6,u                                  69 5A
rol   -$6,x                                  69 1A
rol   -$6,y                                  69 3A
rol   -$7,s                                  69 79
rol   -$7,u                                  69 59
rol   -$7,x                                  69 19
rol   -$7,y                                  69 39
rol   -$8,s                                  69 78
rol   -$8,u                                  69 58
rol   -$8,x                                  69 18
rol   -$8,y                                  69 38
rol   -$9,s                                  69 77
rol   -$9,u                                  69 57
rol   -$9,x                                  69 17
rol   -$9,y                                  69 37
rol   -$a,s                                  69 76
rol   -$a,u                                  69 56
rol   -$a,x                                  69 16
rol   -$a,y                                  69 36
rol   -$b,s                                  69 75
rol   -$b,u                                  69 55
rol   -$b,x                                  69 15
rol   -$b,y                                  69 35
rol   -$c,s                                  69 74
rol   -$c,u                                  69 54
rol   -$c,x                                  69 14
rol   -$c,y                                  69 34
rol   -$d,s                                  69 73
rol   -$d,u                                  69 53
rol   -$d,x                                  69 13
rol   -$d,y                                  69 33
rol   -$e,s                                  69 72
rol   -$e,u                                  69 52
rol   -$e,x                                  69 12
rol   -$e,y                                  69 32
rol   -$f,s                                  69 71
rol   -$f,u                                  69 51
rol   -$f,x                                  69 11
rol   -$f,y                                  69 31
rol   a,s                                    69 E6
rol   a,u                                    69 C6
rol   a,x                                    69 86
rol   a,y                                    69 A6
rol   b,s                                    69 E5
rol   b,u                                    69 C5
rol   b,x                                    69 85
rol   b,y                                    69 A5
rol   d,s                                    69 EB
rol   d,u                                    69 CB
rol   d,x                                    69 8B
rol   d,y                                    69 AB
rol   [$01,pc]                               69 9C 01
rol   [$01,pc]                               69 BC 01
rol   [$01,pc]                               69 DC 01
rol   [$01,pc]                               69 FC 01
rol   [$01,s]                                69 F8 01
rol   [$01,u]                                69 D8 01
rol   [$01,x]                                69 98 01
rol   [$01,y]                                69 B8 01
rol   [$beef,pc]                             69 9D BE EF
rol   [$beef,pc]                             69 BD BE EF
rol   [$beef,pc]                             69 DD BE EF
rol   [$beef,pc]                             69 FD BE EF
rol   [$beef,s]                              69 F9 BE EF
rol   [$beef,u]                              69 D9 BE EF
rol   [$beef,x]                              69 99 BE EF
rol   [$beef,y]                              69 B9 BE EF
rol   [$beef]                                69 9F BE EF
rol   [$beef]                                69 BF BE EF
rol   [$beef]                                69 DF BE EF
rol   [$beef]                                69 FF BE EF
rol   [,--s]                                 69 F3
rol   [,--u]                                 69 D3
rol   [,--x]                                 69 93
rol   [,--y]                                 69 B3
rol   [,s++]                                 69 F1
rol   [,s]                                   69 F4
rol   [,u++]                                 69 D1
rol   [,u]                                   69 D4
rol   [,x++]                                 69 91
rol   [,x]                                   69 94
rol   [,y++]                                 69 B1
rol   [,y]                                   69 B4
rol   [a,s]                                  69 F6
rol   [a,u]                                  69 D6
rol   [a,x]                                  69 96
rol   [a,y]                                  69 B6
rol   [b,s]                                  69 F5
rol   [b,u]                                  69 D5
rol   [b,x]                                  69 95
rol   [b,y]                                  69 B5
rol   [d,s]                                  69 FB
rol   [d,u]                                  69 DB
rol   [d,x]                                  69 9B
rol   [d,y]                                  69 BB
rol   []                                     69 97
rol   []                                     69 9A
rol   []                                     69 9E
rol   []                                     69 B7
rol   []                                     69 BA
rol   []                                     69 BE
rol   []                                     69 D7
rol   []                                     69 DA
rol   []                                     69 DE
rol   []                                     69 F7
rol   []                                     69 FA
rol   []                                     69 FE
rola                                         49
rolb                                         59
ror   $0,s                                   66 60
ror   $0,u                                   66 40
ror   $0,x                                   66 00
ror   $0,y                                   66 20
ror   $01,pc                                 66 8C 01
ror   $01,pc                                 66 AC 01
ror   $01,pc                                 66 CC 01
ror   $01,pc                                 66 EC 01
ror   $01,s                                  66 E8 01
ror   $01,u                                  66 C8 01
ror   $01,x                                  66 88 01
ror   $01,y                                  66 A8 01
ror   $1,s                                   66 61
ror   $1,u                                   66 41
ror   $1,x                                   66 01
ror   $1,y                                   66 21
ror   $2,s                                   66 62
ror   $2,u                                   66 42
ror   $2,x                                   66 02
ror   $2,y                                   66 22
ror   $3,s                                   66 63
ror   $3,u                                   66 43
ror   $3,x                                   66 03
ror   $3,y                                   66 23
ror   $4,s                                   66 64
ror   $4,u                                   66 44
ror   $4,x                                   66 04
ror   $4,y                                   66 24
ror   $5,s                                   66 65
ror   $5,u                                   66 45
ror   $5,x                                   66 05
ror   $5,y                                   66 25
ror   $6,s                                   66 66
ror   $6,u                                   66 46
ror   $6,x                                   66 06
ror   $6,y                                   66 26
ror   $7,s                                   66 67
ror   $7,u                                   66 47
ror   $7,x                                   66 07
ror   $7,y                                   66 27
ror   $8,s                                   66 68
ror   $8,u                                   66 48
ror   $8,x                                   66 08
ror   $8,y                                   66 28
ror   $9,s                                   66 69
ror   $9,u                                   66 49
ror   $9,x                                   66 09
ror   $9,y                                   66 29
ror   $a,s                                   66 6A
ror   $a,u                                   66 4A
ror   $a,x                                   66 0A
ror   $a,y                                   66 2A
ror   $b,s                                   66 6B
ror   $b,u                                   66 4B
ror   $b,x                                   66 0B
ror   $b,y                                   66 2B
ror   $beef                                  66 8F BE EF
ror   $beef                                  66 AF BE EF
ror   $beef                                  66 CF BE EF
ror   $beef                                  66 EF BE EF
ror   $beef                                  76 BE EF
ror   $beef,pc                               66 8D BE EF
ror   $beef,pc                               66 AD BE EF
ror   $beef,pc                               66 CD BE EF
ror   $beef,pc                               66 ED BE EF
ror   $beef,s                                66 E9 BE EF
ror   $beef,u                                66 C9 BE EF
ror   $beef,x                                66 89 BE EF
ror   $beef,y                                66 A9 BE EF
ror   $c,s                                   66 6C
ror   $c,u                                   66 4C
ror   $c,x                                   66 0C
ror   $c,y                                   66 2C
ror   $d,s                                   66 6D
ror   $d,u                                   66 4D
ror   $d,x                                   66 0D
ror   $d,y                                   66 2D
ror   $e,s                                   66 6E
ror   $e,u                                   66 4E
ror   $e,x                                   66 0E
ror   $e,y                                   66 2E
ror   $f,s                                   66 6F
ror   $f,u                                   66 4F
ror   $f,x                                   66 0F
ror   $f,y                                   66 2F
ror   $ff                                    06 FF
ror   ,--s                                   66 E3
ror   ,--u                                   66 C3
ror   ,--x                                   66 83
ror   ,--y                                   66 A3
ror   ,-s                                    66 E2
ror   ,-u                                    66 C2
ror   ,-x                                    66 82
ror   ,-y                                    66 A2
ror   ,s                                     66 E4
ror   ,s+                                    66 E0
ror   ,s++                                   66 E1
ror   ,u                                     66 C4
ror   ,u+                                    66 C0
ror   ,u++                                   66 C1
ror   ,x                                     66 84
ror   ,x+                                    66 80
ror   ,x++                                   66 81
ror   ,y                                     66 A4
ror   ,y+                                    66 A0
ror   ,y++                                   66 A1
ror   -$1,s                                  66 7F
ror   -$1,u                                  66 5F
ror   -$1,x                                  66 1F
ror   -$1,y                                  66 3F
ror   -$10,s                                 66 70
ror   -$10,u                                 66 50
ror   -$10,x                                 66 10
ror   -$10,y                                 66 30
ror   -$2,s                                  66 7E
ror   -$2,u                                  66 5E
ror   -$2,x                                  66 1E
ror   -$2,y                                  66 3E
ror   -$3,s                                  66 7D
ror   -$3,u                                  66 5D
ror   -$3,x                                  66 1D
ror   -$3,y                                  66 3D
ror   -$4,s                                  66 7C
ror   -$4,u                                  66 5C
ror   -$4,x                                  66 1C
ror   -$4,y                                  66 3C
ror   -$5,s                                  66 7B
ror   -$5,u                                  66 5B
ror   -$5,x                                  66 1B
ror   -$5,y                                  66 3B
ror   -$6,s                                  66 7A
ror   -$6,u                                  66 5A
ror   -$6,x                                  66 1A
ror   -$6,y                                  66 3A
ror   -$7,s                                  66 79
ror   -$7,u                                  66 59
ror   -$7,x                                  66 19
ror   -$7,y                                  66 39
ror   -$8,s                                  66 78
ror   -$8,u                                  66 58
ror   -$8,x                                  66 18
ror   -$8,y                                  66 38
ror   -$9,s                                  66 77
ror   -$9,u                                  66 57
ror   -$9,x                                  66 17
ror   -$9,y                                  66 37
ror   -$a,s                                  66 76
ror   -$a,u                                  66 56
ror   -$a,x                                  66 16
ror   -$a,y                                  66 36
ror   -$b,s                                  66 75
ror   -$b,u                                  66 55
ror   -$b,x                                  66 15
ror   -$b,y                                  66 35
ror   -$c,s                                  66 74
ror   -$c,u                                  66 54
ror   -$c,x                                  66 14
ror   -$c,y                                  66 34
ror   -$d,s                                  66 73
ror   -$d,u                                  66 53
ror   -$d,x                                  66 13
ror   -$d,y                                  66 33
ror   -$e,s                                  66 72
ror   -$e,u                                  66 52
ror   -$e,x                                  66 12
ror   -$e,y                                  66 32
ror   -$f,s                                  66 71
ror   -$f,u                                  66 51
ror   -$f,x                                  66 11
ror   -$f,y                                  66 31
ror   a,s                                    66 E6
ror   a,u                                    66 C6
ror   a,x                                    66 86
ror   a,y                                    66 A6
ror   b,s                                    66 E5
ror   b,u                                    66 C5
ror   b,x                                    66 85
ror   b,y                                    66 A5
ror   d,s                                    66 EB
ror   d,u                                    66 CB
ror   d,x                                    66 8B
ror   d,y                                    66 AB
ror   [$01,pc]                               66 9C 01
ror   [$01,pc]                               66 BC 01
ror   [$01,pc]                               66 DC 01
ror   [$01,pc]                               66 FC 01
ror   [$01,s]                                66 F8 01
ror   [$01,u]                                66 D8 01
ror   [$01,x]                                66 98 01
ror   [$01,y]                                66 B8 01
ror   [$beef,pc]                             66 9D BE EF
ror   [$beef,pc]                             66 BD BE EF
ror   [$beef,pc]                             66 DD BE EF
ror   [$beef,pc]                             66 FD BE EF
ror   [$beef,s]                              66 F9 BE EF
ror   [$beef,u]                              66 D9 BE EF
ror   [$beef,x]                              66 99 BE EF
ror   [$beef,y]                              66 B9 BE EF
ror   [$beef]                                66 9F BE EF
ror   [$beef]                                66 BF BE EF
ror   [$beef]                                66 DF BE EF
ror   [$beef]                                66 FF BE EF
ror   [,--s]                                 66 F3
ror   [,--u]                                 66 D3
ror   [,--x]                                 66 93
ror   [,--y]                                 66 B3
ror   [,s++]                                 66 F1
ror   [,s]                                   66 F4
ror   [,u++]                                 66 D1
ror   [,u]                                   66 D4
ror   [,x++]                                 66 91
ror   [,x]                                   66 94
ror   [,y++]                                 66 B1
ror   [,y]                                   66 B4
ror   [a,s]                                  66 F6
ror   [a,u]                                  66 D6
ror   [a,x]                                  66 96
ror   [a,y]                                  66 B6
ror   [b,s]                                  66 F5
ror   [b,u]                                  66 D5
ror   [b,x]                                  66 95
ror   [b,y]                                  66 B5
ror   [d,s]                                  66 FB
ror   [d,u]                                  66 DB
ror   [d,x]                                  66 9B
ror   [d,y]                                  66 BB
ror   []                                     66 97
ror   []                                     66 9A
ror   []                                     66 9E
ror   []                                     66 B7
ror   []                                     66 BA
ror   []                                     66 BE
ror   []                                     66 D7
ror   []                                     66 DA
ror   []                                     66 DE
ror   []                                     66 F7
ror   []                                     66 FA
ror   []                                     66 FE
rora                                         46
rorb                                         56
rti                                          3B
rts                                          39
sbca  #$ff                                   82 FF
sbca  $0,s                                   A2 60
sbca  $0,u                                   A2 40
sbca  $0,x                                   A2 00
sbca  $0,y                                   A2 20
sbca  $01,pc                                 A2 8C 01
sbca  $01,pc                                 A2 AC 01
sbca  $01,pc                                 A2 CC 01
sbca  $01,pc                                 A2 EC 01
sbca  $01,s                                  A2 E8 01
sbca  $01,u                                  A2 C8 01
sbca  $01,x                                  A2 88 01
sbca  $01,y                                  A2 A8 01
sbca  $1,s                                   A2 61
sbca  $1,u                                   A2 41
sbca  $1,x                                   A2 01
sbca  $1,y                                   A2 21
sbca  $2,s                                   A2 62
sbca  $2,u                                   A2 42
sbca  $2,x                                   A2 02
sbca  $2,y                                   A2 22
sbca  $3,s                                   A2 63
sbca  $3,u                                   A2 43
sbca  $3,x                                   A2 03
sbca  $3,y                                   A2 23
sbca  $4,s                                   A2 64
sbca  $4,u                                   A2 44
sbca  $4,x                                   A2 04
sbca  $4,y                                   A2 24
sbca  $5,s                                   A2 65
sbca  $5,u                                   A2 45
sbca  $5,x                                   A2 05
sbca  $5,y                                   A2 25
sbca  $6,s                                   A2 66
sbca  $6,u                                   A2 46
sbca  $6,x                                   A2 06
sbca  $6,y                                   A2 26
sbca  $7,s                                   A2 67
sbca  $7,u                                   A2 47
sbca  $7,x                                   A2 07
sbca  $7,y                                   A2 27
sbca  $8,s                                   A2 68
sbca  $8,u                                   A2 48
sbca  $8,x                                   A2 08
sbca  $8,y                                   A2 28
sbca  $9,s                                   A2 69
sbca  $9,u                                   A2 49
sbca  $9,x                                   A2 09
sbca  $9,y                                   A2 29
sbca  $a,s                                   A2 6A
sbca  $a,u                                   A2 4A
sbca  $a,x                                   A2 0A
sbca  $a,y                                   A2 2A
sbca  $b,s                                   A2 6B
sbca  $b,u                                   A2 4B
sbca  $b,x                                   A2 0B
sbca  $b,y                                   A2 2B
sbca  $beef                                  A2 8F BE EF
sbca  $beef                                  A2 AF BE EF
sbca  $beef                                  A2 CF BE EF
sbca  $beef                                  A2 EF BE EF
sbca  $beef                                  B2 BE EF
sbca  $beef,pc                               A2 8D BE EF
sbca  $beef,pc                               A2 AD BE EF
sbca  $beef,pc                               A2 CD BE EF
sbca  $beef,pc                               A2 ED BE EF
sbca  $beef,s                                A2 E9 BE EF
sbca  $beef,u                                A2 C9 BE EF
sbca  $beef,x                                A2 89 BE EF
sbca  $beef,y                                A2 A9 BE EF
sbca  $c,s                                   A2 6C
sbca  $c,u                                   A2 4C
sbca  $c,x                                   A2 0C
sbca  $c,y                                   A2 2C
sbca  $d,s                                   A2 6D
sbca  $d,u                                   A2 4D
sbca  $d,x                                   A2 0D
sbca  $d,y                                   A2 2D
sbca  $e,s                                   A2 6E
sbca  $e,u                                   A2 4E
sbca  $e,x                                   A2 0E
sbca  $e,y                                   A2 2E
sbca  $f,s                                   A2 6F
sbca  $f,u                                   A2 4F
sbca  $f,x                                   A2 0F
sbca  $f,y                                   A2 2F
sbca  $ff                                    92 FF
sbca  ,--s                                   A2 E3
sbca  ,--u                                   A2 C3
sbca  ,--x                                   A2 83
sbca  ,--y                                   A2 A3
sbca  ,-s                                    A2 E2
sbca  ,-u                                    A2 C2
sbca  ,-x                                    A2 82
sbca  ,-y                                    A2 A2
sbca  ,s                                     A2 E4
sbca  ,s+                                    A2 E0
sbca  ,s++                                   A2 E1
sbca  ,u                                     A2 C4
sbca  ,u+                                    A2 C0
sbca  ,u++                                   A2 C1
sbca  ,x                                     A2 84
sbca  ,x+                                    A2 80
sbca  ,x++                                   A2 81
sbca  ,y                                     A2 A4
sbca  ,y+                                    A2 A0
sbca  ,y++                                   A2 A1
sbca  -$1,s                                  A2 7F
sbca  -$1,u                                  A2 5F
sbca  -$1,x                                  A2 1F
sbca  -$1,y                                  A2 3F
sbca  -$10,s                                 A2 70
sbca  -$10,u                                 A2 50
sbca  -$10,x                                 A2 10
sbca  -$10,y                                 A2 30
sbca  -$2,s                                  A2 7E
sbca  -$2,u                                  A2 5E
sbca  -$2,x                                  A2 1E
sbca  -$2,y                                  A2 3E
sbca  -$3,s                                  A2 7D
sbca  -$3,u                                  A2 5D
sbca  -$3,x                                  A2 1D
sbca  -$3,y                                  A2 3D
sbca  -$4,s                                  A2 7C
sbca  -$4,u                                  A2 5C
sbca  -$4,x                                  A2 1C
sbca  -$4,y                                  A2 3C
sbca  -$5,s                                  A2 7B
sbca  -$5,u                                  A2 5B
sbca  -$5,x                                  A2 1B
sbca  -$5,y                                  A2 3B
sbca  -$6,s                                  A2 7A
sbca  -$6,u                                  A2 5A
sbca  -$6,x                                  A2 1A
sbca  -$6,y                                  A2 3A
sbca  -$7,s                                  A2 79
sbca  -$7,u                                  A2 59
sbca  -$7,x                                  A2 19
sbca  -$7,y                                  A2 39
sbca  -$8,s                                  A2 78
sbca  -$8,u                                  A2 58
sbca  -$8,x                                  A2 18
sbca  -$8,y                                  A2 38
sbca  -$9,s                                  A2 77
sbca  -$9,u                                  A2 57
sbca  -$9,x                                  A2 17
sbca  -$9,y                                  A2 37
sbca  -$a,s                                  A2 76
sbca  -$a,u                                  A2 56
sbca  -$a,x                                  A2 16
sbca  -$a,y                                  A2 36
sbca  -$b,s                                  A2 75
sbca  -$b,u                                  A2 55
sbca  -$b,x                                  A2 15
sbca  -$b,y                                  A2 35
sbca  -$c,s                                  A2 74
sbca  -$c,u                                  A2 54
sbca  -$c,x                                  A2 14
sbca  -$c,y                                  A2 34
sbca  -$d,s                                  A2 73
sbca  -$d,u                                  A2 53
sbca  -$d,x                                  A2 13
sbca  -$d,y                                  A2 33
sbca  -$e,s                                  A2 72
sbca  -$e,u                                  A2 52
sbca  -$e,x                                  A2 12
sbca  -$e,y                                  A2 32
sbca  -$f,s                                  A2 71
sbca  -$f,u                                  A2 51
sbca  -$f,x                                  A2 11
sbca  -$f,y                                  A2 31
sbca  a,s                                    A2 E6
sbca  a,u                                    A2 C6
sbca  a,x                                    A2 86
sbca  a,y                                    A2 A6
sbca  b,s                                    A2 E5
sbca  b,u                                    A2 C5
sbca  b,x                                    A2 85
sbca  b,y                                    A2 A5
sbca  d,s                                    A2 EB
sbca  d,u                                    A2 CB
sbca  d,x                                    A2 8B
sbca  d,y                                    A2 AB
sbca  [$01,pc]                               A2 9C 01
sbca  [$01,pc]                               A2 BC 01
sbca  [$01,pc]                               A2 DC 01
sbca  [$01,pc]                               A2 FC 01
sbca  [$01,s]                                A2 F8 01
sbca  [$01,u]                                A2 D8 01
sbca  [$01,x]                                A2 98 01
sbca  [$01,y]                                A2 B8 01
sbca  [$beef,pc]                             A2 9D BE EF
sbca  [$beef,pc]                             A2 BD BE EF
sbca  [$beef,pc]                             A2 DD BE EF
sbca  [$beef,pc]                             A2 FD BE EF
sbca  [$beef,s]                              A2 F9 BE EF
sbca  [$beef,u]                              A2 D9 BE EF
sbca  [$beef,x]                              A2 99 BE EF
sbca  [$beef,y]                              A2 B9 BE EF
sbca  [$beef]                                A2 9F BE EF
sbca  [$beef]                                A2 BF BE EF
sbca  [$beef]                                A2 DF BE EF
sbca  [$beef]                                A2 FF BE EF
sbca  [,--s]                                 A2 F3
sbca  [,--u]                                 A2 D3
sbca  [,--x]                                 A2 93
sbca  [,--y]                                 A2 B3
sbca  [,s++]                                 A2 F1
sbca  [,s]                                   A2 F4
sbca  [,u++]                                 A2 D1
sbca  [,u]                                   A2 D4
sbca  [,x++]                                 A2 91
sbca  [,x]                                   A2 94
sbca  [,y++]                                 A2 B1
sbca  [,y]                                   A2 B4
sbca  [a,s]                                  A2 F6
sbca  [a,u]                                  A2 D6
sbca  [a,x]                                  A2 96
sbca  [a,y]                                  A2 B6
sbca  [b,s]                                  A2 F5
sbca  [b,u]                                  A2 D5
sbca  [b,x]                                  A2 95
sbca  [b,y]                                  A2 B5
sbca  [d,s]                                  A2 FB
sbca  [d,u]                                  A2 DB
sbca  [d,x]                                  A2 9B
sbca  [d,y]                                  A2 BB
sbca  []                                     A2 97
sbca  []                                     A2 9A
sbca  []                                     A2 9E
sbca  []                                     A2 B7
sbca  []                                     A2 BA
sbca  []                                     A2 BE
sbca  []                                     A2 D7
sbca  []                                     A2 DA
sbca  []                                     A2 DE
sbca  []                                     A2 F7
sbca  []                                     A2 FA
sbca  []                                     A2 FE
sbcb  #$ff                                   C2 FF
sbcb  $0,s                                   E2 60
sbcb  $0,u                                   E2 40
sbcb  $0,x                                   E2 00
sbcb  $0,y                                   E2 20
sbcb  $01,pc                                 E2 8C 01
sbcb  $01,pc                                 E2 AC 01
sbcb  $01,pc                                 E2 CC 01
sbcb  $01,pc                                 E2 EC 01
sbcb  $01,s                                  E2 E8 01
sbcb  $01,u                                  E2 C8 01
sbcb  $01,x                                  E2 88 01
sbcb  $01,y                                  E2 A8 01
sbcb  $1,s                                   E2 61
sbcb  $1,u                                   E2 41
sbcb  $1,x                                   E2 01
sbcb  $1,y                                   E2 21
sbcb  $2,s                                   E2 62
sbcb  $2,u                                   E2 42
sbcb  $2,x                                   E2 02
sbcb  $2,y                                   E2 22
sbcb  $3,s                                   E2 63
sbcb  $3,u                                   E2 43
sbcb  $3,x                                   E2 03
sbcb  $3,y                                   E2 23
sbcb  $4,s                                   E2 64
sbcb  $4,u                                   E2 44
sbcb  $4,x                                   E2 04
sbcb  $4,y                                   E2 24
sbcb  $5,s                                   E2 65
sbcb  $5,u                                   E2 45
sbcb  $5,x                                   E2 05
sbcb  $5,y                                   E2 25
sbcb  $6,s                                   E2 66
sbcb  $6,u                                   E2 46
sbcb  $6,x                                   E2 06
sbcb  $6,y                                   E2 26
sbcb  $7,s                                   E2 67
sbcb  $7,u                                   E2 47
sbcb  $7,x                                   E2 07
sbcb  $7,y                                   E2 27
sbcb  $8,s                                   E2 68
sbcb  $8,u                                   E2 48
sbcb  $8,x                                   E2 08
sbcb  $8,y                                   E2 28
sbcb  $9,s                                   E2 69
sbcb  $9,u                                   E2 49
sbcb  $9,x                                   E2 09
sbcb  $9,y                                   E2 29
sbcb  $a,s                                   E2 6A
sbcb  $a,u                                   E2 4A
sbcb  $a,x                                   E2 0A
sbcb  $a,y                                   E2 2A
sbcb  $b,s                                   E2 6B
sbcb  $b,u                                   E2 4B
sbcb  $b,x                                   E2 0B
sbcb  $b,y                                   E2 2B
sbcb  $beef                                  E2 8F BE EF
sbcb  $beef                                  E2 AF BE EF
sbcb  $beef                                  E2 CF BE EF
sbcb  $beef                                  E2 EF BE EF
sbcb  $beef                                  F2 BE EF
sbcb  $beef,pc                               E2 8D BE EF
sbcb  $beef,pc                               E2 AD BE EF
sbcb  $beef,pc                               E2 CD BE EF
sbcb  $beef,pc                               E2 ED BE EF
sbcb  $beef,s                                E2 E9 BE EF
sbcb  $beef,u                                E2 C9 BE EF
sbcb  $beef,x                                E2 89 BE EF
sbcb  $beef,y                                E2 A9 BE EF
sbcb  $c,s                                   E2 6C
sbcb  $c,u                                   E2 4C
sbcb  $c,x                                   E2 0C
sbcb  $c,y                                   E2 2C
sbcb  $d,s                                   E2 6D
sbcb  $d,u                                   E2 4D
sbcb  $d,x                                   E2 0D
sbcb  $d,y                                   E2 2D
sbcb  $e,s                                   E2 6E
sbcb  $e,u                                   E2 4E
sbcb  $e,x                                   E2 0E
sbcb  $e,y                                   E2 2E
sbcb  $f,s                                   E2 6F
sbcb  $f,u                                   E2 4F
sbcb  $f,x                                   E2 0F
sbcb  $f,y                                   E2 2F
sbcb  $ff                                    D2 FF
sbcb  ,--s                                   E2 E3
sbcb  ,--u                                   E2 C3
sbcb  ,--x                                   E2 83
sbcb  ,--y                                   E2 A3
sbcb  ,-s                                    E2 E2
sbcb  ,-u                                    E2 C2
sbcb  ,-x                                    E2 82
sbcb  ,-y                                    E2 A2
sbcb  ,s                                     E2 E4
sbcb  ,s+                                    E2 E0
sbcb  ,s++                                   E2 E1
sbcb  ,u                                     E2 C4
sbcb  ,u+                                    E2 C0
sbcb  ,u++                                   E2 C1
sbcb  ,x                                     E2 84
sbcb  ,x+                                    E2 80
sbcb  ,x++                                   E2 81
sbcb  ,y                                     E2 A4
sbcb  ,y+                                    E2 A0
sbcb  ,y++                                   E2 A1
sbcb  -$1,s                                  E2 7F
sbcb  -$1,u                                  E2 5F
sbcb  -$1,x                                  E2 1F
sbcb  -$1,y                                  E2 3F
sbcb  -$10,s                                 E2 70
sbcb  -$10,u                                 E2 50
sbcb  -$10,x                                 E2 10
sbcb  -$10,y                                 E2 30
sbcb  -$2,s                                  E2 7E
sbcb  -$2,u                                  E2 5E
sbcb  -$2,x                                  E2 1E
sbcb  -$2,y                                  E2 3E
sbcb  -$3,s                                  E2 7D
sbcb  -$3,u                                  E2 5D
sbcb  -$3,x                                  E2 1D
sbcb  -$3,y                                  E2 3D
sbcb  -$4,s                                  E2 7C
sbcb  -$4,u                                  E2 5C
sbcb  -$4,x                                  E2 1C
sbcb  -$4,y                                  E2 3C
sbcb  -$5,s                                  E2 7B
sbcb  -$5,u                                  E2 5B
sbcb  -$5,x                                  E2 1B
sbcb  -$5,y                                  E2 3B
sbcb  -$6,s                                  E2 7A
sbcb  -$6,u                                  E2 5A
sbcb  -$6,x                                  E2 1A
sbcb  -$6,y                                  E2 3A
sbcb  -$7,s                                  E2 79
sbcb  -$7,u                                  E2 59
sbcb  -$7,x                                  E2 19
sbcb  -$7,y                                  E2 39
sbcb  -$8,s                                  E2 78
sbcb  -$8,u                                  E2 58
sbcb  -$8,x                                  E2 18
sbcb  -$8,y                                  E2 38
sbcb  -$9,s                                  E2 77
sbcb  -$9,u                                  E2 57
sbcb  -$9,x                                  E2 17
sbcb  -$9,y                                  E2 37
sbcb  -$a,s                                  E2 76
sbcb  -$a,u                                  E2 56
sbcb  -$a,x                                  E2 16
sbcb  -$a,y                                  E2 36
sbcb  -$b,s                                  E2 75
sbcb  -$b,u                                  E2 55
sbcb  -$b,x                                  E2 15
sbcb  -$b,y                                  E2 35
sbcb  -$c,s                                  E2 74
sbcb  -$c,u                                  E2 54
sbcb  -$c,x                                  E2 14
sbcb  -$c,y                                  E2 34
sbcb  -$d,s                                  E2 73
sbcb  -$d,u                                  E2 53
sbcb  -$d,x                                  E2 13
sbcb  -$d,y                                  E2 33
sbcb  -$e,s                                  E2 72
sbcb  -$e,u                                  E2 52
sbcb  -$e,x                                  E2 12
sbcb  -$e,y                                  E2 32
sbcb  -$f,s                                  E2 71
sbcb  -$f,u                                  E2 51
sbcb  -$f,x                                  E2 11
sbcb  -$f,y                                  E2 31
sbcb  a,s                                    E2 E6
sbcb  a,u                                    E2 C6
sbcb  a,x                                    E2 86
sbcb  a,y                                    E2 A6
sbcb  b,s                                    E2 E5
sbcb  b,u                                    E2 C5
sbcb  b,x                                    E2 85
sbcb  b,y                                    E2 A5
sbcb  d,s                                    E2 EB
sbcb  d,u                                    E2 CB
sbcb  d,x                                    E2 8B
sbcb  d,y                                    E2 AB
sbcb  [$01,pc]                               E2 9C 01
sbcb  [$01,pc]                               E2 BC 01
sbcb  [$01,pc]                               E2 DC 01
sbcb  [$01,pc]                               E2 FC 01
sbcb  [$01,s]                                E2 F8 01
sbcb  [$01,u]                                E2 D8 01
sbcb  [$01,x]                                E2 98 01
sbcb  [$01,y]                                E2 B8 01
sbcb  [$beef,pc]                             E2 9D BE EF
sbcb  [$beef,pc]                             E2 BD BE EF
sbcb  [$beef,pc]                             E2 DD BE EF
sbcb  [$beef,pc]                             E2 FD BE EF
sbcb  [$beef,s]                              E2 F9 BE EF
sbcb  [$beef,u]                              E2 D9 BE EF
sbcb  [$beef,x]                              E2 99 BE EF
sbcb  [$beef,y]                              E2 B9 BE EF
sbcb  [$beef]                                E2 9F BE EF
sbcb  [$beef]                                E2 BF BE EF
sbcb  [$beef]                                E2 DF BE EF
sbcb  [$beef]                                E2 FF BE EF
sbcb  [,--s]                                 E2 F3
sbcb  [,--u]                                 E2 D3
sbcb  [,--x]                                 E2 93
sbcb  [,--y]                                 E2 B3
sbcb  [,s++]                                 E2 F1
sbcb  [,s]                                   E2 F4
sbcb  [,u++]                                 E2 D1
sbcb  [,u]                                   E2 D4
sbcb  [,x++]                                 E2 91
sbcb  [,x]                                   E2 94
sbcb  [,y++]                                 E2 B1
sbcb  [,y]                                   E2 B4
sbcb  [a,s]                                  E2 F6
sbcb  [a,u]                                  E2 D6
sbcb  [a,x]                                  E2 96
sbcb  [a,y]                                  E2 B6
sbcb  [b,s]                                  E2 F5
sbcb  [b,u]                                  E2 D5
sbcb  [b,x]                                  E2 95
sbcb  [b,y]                                  E2 B5
sbcb  [d,s]                                  E2 FB
sbcb  [d,u]                                  E2 DB
sbcb  [d,x]                                  E2 9B
sbcb  [d,y]                                  E2 BB
sbcb  []                                     E2 97
sbcb  []                                     E2 9A
sbcb  []                                     E2 9E
sbcb  []                                     E2 B7
sbcb  []                                     E2 BA
sbcb  []                                     E2 BE
sbcb  []                                     E2 D7
sbcb  []                                     E2 DA
sbcb  []                                     E2 DE
sbcb  []                                     E2 F7
sbcb  []                                     E2 FA
sbcb  []                                     E2 FE
sex                                          1D
sta   $0,s                                   A7 60
sta   $0,u                                   A7 40
sta   $0,x                                   A7 00
sta   $0,y                                   A7 20
sta   $01,pc                                 A7 8C 01
sta   $01,pc                                 A7 AC 01
sta   $01,pc                                 A7 CC 01
sta   $01,pc                                 A7 EC 01
sta   $01,s                                  A7 E8 01
sta   $01,u                                  A7 C8 01
sta   $01,x                                  A7 88 01
sta   $01,y                                  A7 A8 01
sta   $1,s                                   A7 61
sta   $1,u                                   A7 41
sta   $1,x                                   A7 01
sta   $1,y                                   A7 21
sta   $2,s                                   A7 62
sta   $2,u                                   A7 42
sta   $2,x                                   A7 02
sta   $2,y                                   A7 22
sta   $3,s                                   A7 63
sta   $3,u                                   A7 43
sta   $3,x                                   A7 03
sta   $3,y                                   A7 23
sta   $4,s                                   A7 64
sta   $4,u                                   A7 44
sta   $4,x                                   A7 04
sta   $4,y                                   A7 24
sta   $5,s                                   A7 65
sta   $5,u                                   A7 45
sta   $5,x                                   A7 05
sta   $5,y                                   A7 25
sta   $6,s                                   A7 66
sta   $6,u                                   A7 46
sta   $6,x                                   A7 06
sta   $6,y                                   A7 26
sta   $7,s                                   A7 67
sta   $7,u                                   A7 47
sta   $7,x                                   A7 07
sta   $7,y                                   A7 27
sta   $8,s                                   A7 68
sta   $8,u                                   A7 48
sta   $8,x                                   A7 08
sta   $8,y                                   A7 28
sta   $9,s                                   A7 69
sta   $9,u                                   A7 49
sta   $9,x                                   A7 09
sta   $9,y                                   A7 29
sta   $a,s                                   A7 6A
sta   $a,u                                   A7 4A
sta   $a,x                                   A7 0A
sta   $a,y                                   A7 2A
sta   $b,s                                   A7 6B
sta   $b,u                                   A7 4B
sta   $b,x                                   A7 0B
sta   $b,y                                   A7 2B
sta   $beef                                  A7 8F BE EF
sta   $beef                                  A7 AF BE EF
sta   $beef                                  A7 CF BE EF
sta   $beef                                  A7 EF BE EF
sta   $beef                                  B7 BE EF
sta   $beef,pc                               A7 8D BE EF
sta   $beef,pc                               A7 AD BE EF
sta   $beef,pc                               A7 CD BE EF
sta   $beef,pc                               A7 ED BE EF
sta   $beef,s                                A7 E9 BE EF
sta   $beef,u                                A7 C9 BE EF
sta   $beef,x                                A7 89 BE EF
sta   $beef,y                                A7 A9 BE EF
sta   $c,s                                   A7 6C
sta   $c,u                                   A7 4C
sta   $c,x                                   A7 0C
sta   $c,y                                   A7 2C
sta   $d,s                                   A7 6D
sta   $d,u                                   A7 4D
sta   $d,x                                   A7 0D
sta   $d,y                                   A7 2D
sta   $e,s                                   A7 6E
sta   $e,u                                   A7 4E
sta   $e,x                                   A7 0E
sta   $e,y                                   A7 2E
sta   $f,s                                   A7 6F
sta   $f,u                                   A7 4F
sta   $f,x                                   A7 0F
sta   $f,y                                   A7 2F
sta   $ff                                    97 FF
sta   ,--s                                   A7 E3
sta   ,--u                                   A7 C3
sta   ,--x                                   A7 83
sta   ,--y                                   A7 A3
sta   ,-s                                    A7 E2
sta   ,-u                                    A7 C2
sta   ,-x                                    A7 82
sta   ,-y                                    A7 A2
sta   ,s                                     A7 E4
sta   ,s+                                    A7 E0
sta   ,s++                                   A7 E1
sta   ,u                                     A7 C4
sta   ,u+                                    A7 C0
sta   ,u++                                   A7 C1
sta   ,x                                     A7 84
sta   ,x+                                    A7 80
sta   ,x++                                   A7 81
sta   ,y                                     A7 A4
sta   ,y+                                    A7 A0
sta   ,y++                                   A7 A1
sta   -$1,s                                  A7 7F
sta   -$1,u                                  A7 5F
sta   -$1,x                                  A7 1F
sta   -$1,y                                  A7 3F
sta   -$10,s                                 A7 70
sta   -$10,u                                 A7 50
sta   -$10,x                                 A7 10
sta   -$10,y                                 A7 30
sta   -$2,s                                  A7 7E
sta   -$2,u                                  A7 5E
sta   -$2,x                                  A7 1E
sta   -$2,y                                  A7 3E
sta   -$3,s                                  A7 7D
sta   -$3,u                                  A7 5D
sta   -$3,x                                  A7 1D
sta   -$3,y                                  A7 3D
sta   -$4,s                                  A7 7C
sta   -$4,u                                  A7 5C
sta   -$4,x                                  A7 1C
sta   -$4,y                                  A7 3C
sta   -$5,s                                  A7 7B
sta   -$5,u                                  A7 5B
sta   -$5,x                                  A7 1B
sta   -$5,y                                  A7 3B
sta   -$6,s                                  A7 7A
sta   -$6,u                                  A7 5A
sta   -$6,x                                  A7 1A
sta   -$6,y                                  A7 3A
sta   -$7,s                                  A7 79
sta   -$7,u                                  A7 59
sta   -$7,x                                  A7 19
sta   -$7,y                                  A7 39
sta   -$8,s                                  A7 78
sta   -$8,u                                  A7 58
sta   -$8,x                                  A7 18
sta   -$8,y                                  A7 38
sta   -$9,s                                  A7 77
sta   -$9,u                                  A7 57
sta   -$9,x                                  A7 17
sta   -$9,y                                  A7 37
sta   -$a,s                                  A7 76
sta   -$a,u                                  A7 56
sta   -$a,x                                  A7 16
sta   -$a,y                                  A7 36
sta   -$b,s                                  A7 75
sta   -$b,u                                  A7 55
sta   -$b,x                                  A7 15
sta   -$b,y                                  A7 35
sta   -$c,s                                  A7 74
sta   -$c,u                                  A7 54
sta   -$c,x                                  A7 14
sta   -$c,y                                  A7 34
sta   -$d,s                                  A7 73
sta   -$d,u                                  A7 53
sta   -$d,x                                  A7 13
sta   -$d,y                                  A7 33
sta   -$e,s                                  A7 72
sta   -$e,u                                  A7 52
sta   -$e,x                                  A7 12
sta   -$e,y                                  A7 32
sta   -$f,s                                  A7 71
sta   -$f,u                                  A7 51
sta   -$f,x                                  A7 11
sta   -$f,y                                  A7 31
sta   a,s                                    A7 E6
sta   a,u                                    A7 C6
sta   a,x                                    A7 86
sta   a,y                                    A7 A6
sta   b,s                                    A7 E5
sta   b,u                                    A7 C5
sta   b,x                                    A7 85
sta   b,y                                    A7 A5
sta   d,s                                    A7 EB
sta   d,u                                    A7 CB
sta   d,x                                    A7 8B
sta   d,y                                    A7 AB
sta   [$01,pc]                               A7 9C 01
sta   [$01,pc]                               A7 BC 01
sta   [$01,pc]                               A7 DC 01
sta   [$01,pc]                               A7 FC 01
sta   [$01,s]                                A7 F8 01
sta   [$01,u]                                A7 D8 01
sta   [$01,x]                                A7 98 01
sta   [$01,y]                                A7 B8 01
sta   [$beef,pc]                             A7 9D BE EF
sta   [$beef,pc]                             A7 BD BE EF
sta   [$beef,pc]                             A7 DD BE EF
sta   [$beef,pc]                             A7 FD BE EF
sta   [$beef,s]                              A7 F9 BE EF
sta   [$beef,u]                              A7 D9 BE EF
sta   [$beef,x]                              A7 99 BE EF
sta   [$beef,y]                              A7 B9 BE EF
sta   [$beef]                                A7 9F BE EF
sta   [$beef]                                A7 BF BE EF
sta   [$beef]                                A7 DF BE EF
sta   [$beef]                                A7 FF BE EF
sta   [,--s]                                 A7 F3
sta   [,--u]                                 A7 D3
sta   [,--x]                                 A7 93
sta   [,--y]                                 A7 B3
sta   [,s++]                                 A7 F1
sta   [,s]                                   A7 F4
sta   [,u++]                                 A7 D1
sta   [,u]                                   A7 D4
sta   [,x++]                                 A7 91
sta   [,x]                                   A7 94
sta   [,y++]                                 A7 B1
sta   [,y]                                   A7 B4
sta   [a,s]                                  A7 F6
sta   [a,u]                                  A7 D6
sta   [a,x]                                  A7 96
sta   [a,y]                                  A7 B6
sta   [b,s]                                  A7 F5
sta   [b,u]                                  A7 D5
sta   [b,x]                                  A7 95
sta   [b,y]                                  A7 B5
sta   [d,s]                                  A7 FB
sta   [d,u]                                  A7 DB
sta   [d,x]                                  A7 9B
sta   [d,y]                                  A7 BB
sta   []                                     A7 97
sta   []                                     A7 9A
sta   []                                     A7 9E
sta   []                                     A7 B7
sta   []                                     A7 BA
sta   []                                     A7 BE
sta   []                                     A7 D7
sta   []                                     A7 DA
sta   []                                     A7 DE
sta   []                                     A7 F7
sta   []                                     A7 FA
sta   []                                     A7 FE
stb   $0,s                                   E7 60
stb   $0,u                                   E7 40
stb   $0,x                                   E7 00
stb   $0,y                                   E7 20
stb   $01,pc                                 E7 8C 01
stb   $01,pc                                 E7 AC 01
stb   $01,pc                                 E7 CC 01
stb   $01,pc                                 E7 EC 01
stb   $01,s                                  E7 E8 01
stb   $01,u                                  E7 C8 01
stb   $01,x                                  E7 88 01
stb   $01,y                                  E7 A8 01
stb   $1,s                                   E7 61
stb   $1,u                                   E7 41
stb   $1,x                                   E7 01
stb   $1,y                                   E7 21
stb   $2,s                                   E7 62
stb   $2,u                                   E7 42
stb   $2,x                                   E7 02
stb   $2,y                                   E7 22
stb   $3,s                                   E7 63
stb   $3,u                                   E7 43
stb   $3,x                                   E7 03
stb   $3,y                                   E7 23
stb   $4,s                                   E7 64
stb   $4,u                                   E7 44
stb   $4,x                                   E7 04
stb   $4,y                                   E7 24
stb   $5,s                                   E7 65
stb   $5,u                                   E7 45
stb   $5,x                                   E7 05
stb   $5,y                                   E7 25
stb   $6,s                                   E7 66
stb   $6,u                                   E7 46
stb   $6,x                                   E7 06
stb   $6,y                                   E7 26
stb   $7,s                                   E7 67
stb   $7,u                                   E7 47
stb   $7,x                                   E7 07
stb   $7,y                                   E7 27
stb   $8,s                                   E7 68
stb   $8,u                                   E7 48
stb   $8,x                                   E7 08
stb   $8,y                                   E7 28
stb   $9,s                                   E7 69
stb   $9,u                                   E7 49
stb   $9,x                                   E7 09
stb   $9,y                                   E7 29
stb   $a,s                                   E7 6A
stb   $a,u                                   E7 4A
stb   $a,x                                   E7 0A
stb   $a,y                                   E7 2A
stb   $b,s                                   E7 6B
stb   $b,u                                   E7 4B
stb   $b,x                                   E7 0B
stb   $b,y                                   E7 2B
stb   $beef                                  E7 8F BE EF
stb   $beef                                  E7 AF BE EF
stb   $beef                                  E7 CF BE EF
stb   $beef                                  E7 EF BE EF
stb   $beef                                  F7 BE EF
stb   $beef,pc                               E7 8D BE EF
stb   $beef,pc                               E7 AD BE EF
stb   $beef,pc                               E7 CD BE EF
stb   $beef,pc                               E7 ED BE EF
stb   $beef,s                                E7 E9 BE EF
stb   $beef,u                                E7 C9 BE EF
stb   $beef,x                                E7 89 BE EF
stb   $beef,y                                E7 A9 BE EF
stb   $c,s                                   E7 6C
stb   $c,u                                   E7 4C
stb   $c,x                                   E7 0C
stb   $c,y                                   E7 2C
stb   $d,s                                   E7 6D
stb   $d,u                                   E7 4D
stb   $d,x                                   E7 0D
stb   $d,y                                   E7 2D
stb   $e,s                                   E7 6E
stb   $e,u                                   E7 4E
stb   $e,x                                   E7 0E
stb   $e,y                                   E7 2E
stb   $f,s                                   E7 6F
stb   $f,u                                   E7 4F
stb   $f,x                                   E7 0F
stb   $f,y                                   E7 2F
stb   $ff                                    D7 FF
stb   ,--s                                   E7 E3
stb   ,--u                                   E7 C3
stb   ,--x                                   E7 83
stb   ,--y                                   E7 A3
stb   ,-s                                    E7 E2
stb   ,-u                                    E7 C2
stb   ,-x                                    E7 82
stb   ,-y                                    E7 A2
stb   ,s                                     E7 E4
stb   ,s+                                    E7 E0
stb   ,s++                                   E7 E1
stb   ,u                                     E7 C4
stb   ,u+                                    E7 C0
stb   ,u++                                   E7 C1
stb   ,x                                     E7 84
stb   ,x+                                    E7 80
stb   ,x++                                   E7 81
stb   ,y                                     E7 A4
stb   ,y+                                    E7 A0
stb   ,y++                                   E7 A1
stb   -$1,s                                  E7 7F
stb   -$1,u                                  E7 5F
stb   -$1,x                                  E7 1F
stb   -$1,y                                  E7 3F
stb   -$10,s                                 E7 70
stb   -$10,u                                 E7 50
stb   -$10,x                                 E7 10
stb   -$10,y                                 E7 30
stb   -$2,s                                  E7 7E
stb   -$2,u                                  E7 5E
stb   -$2,x                                  E7 1E
stb   -$2,y                                  E7 3E
stb   -$3,s                                  E7 7D
stb   -$3,u                                  E7 5D
stb   -$3,x                                  E7 1D
stb   -$3,y                                  E7 3D
stb   -$4,s                                  E7 7C
stb   -$4,u                                  E7 5C
stb   -$4,x                                  E7 1C
stb   -$4,y                                  E7 3C
stb   -$5,s                                  E7 7B
stb   -$5,u                                  E7 5B
stb   -$5,x                                  E7 1B
stb   -$5,y                                  E7 3B
stb   -$6,s                                  E7 7A
stb   -$6,u                                  E7 5A
stb   -$6,x                                  E7 1A
stb   -$6,y                                  E7 3A
stb   -$7,s                                  E7 79
stb   -$7,u                                  E7 59
stb   -$7,x                                  E7 19
stb   -$7,y                                  E7 39
stb   -$8,s                                  E7 78
stb   -$8,u                                  E7 58
stb   -$8,x                                  E7 18
stb   -$8,y                                  E7 38
stb   -$9,s                                  E7 77
stb   -$9,u                                  E7 57
stb   -$9,x                                  E7 17
stb   -$9,y                                  E7 37
stb   -$a,s                                  E7 76
stb   -$a,u                                  E7 56
stb   -$a,x                                  E7 16
stb   -$a,y                                  E7 36
stb   -$b,s                                  E7 75
stb   -$b,u                                  E7 55
stb   -$b,x                                  E7 15
stb   -$b,y                                  E7 35
stb   -$c,s                                  E7 74
stb   -$c,u                                  E7 54
stb   -$c,x                                  E7 14
stb   -$c,y                                  E7 34
stb   -$d,s                                  E7 73
stb   -$d,u                                  E7 53
stb   -$d,x                                  E7 13
stb   -$d,y                                  E7 33
stb   -$e,s                                  E7 72
stb   -$e,u                                  E7 52
stb   -$e,x                                  E7 12
stb   -$e,y                                  E7 32
stb   -$f,s                                  E7 71
stb   -$f,u                                  E7 51
stb   -$f,x                                  E7 11
stb   -$f,y                                  E7 31
stb   a,s                                    E7 E6
stb   a,u                                    E7 C6
stb   a,x                                    E7 86
stb   a,y                                    E7 A6
stb   b,s                                    E7 E5
stb   b,u                                    E7 C5
stb   b,x                                    E7 85
stb   b,y                                    E7 A5
stb   d,s                                    E7 EB
stb   d,u                                    E7 CB
stb   d,x                                    E7 8B
stb   d,y                                    E7 AB
stb   [$01,pc]                               E7 9C 01
stb   [$01,pc]                               E7 BC 01
stb   [$01,pc]                               E7 DC 01
stb   [$01,pc]                               E7 FC 01
stb   [$01,s]                                E7 F8 01
stb   [$01,u]                                E7 D8 01
stb   [$01,x]                                E7 98 01
stb   [$01,y]                                E7 B8 01
stb   [$beef,pc]                             E7 9D BE EF
stb   [$beef,pc]                             E7 BD BE EF
stb   [$beef,pc]                             E7 DD BE EF
stb   [$beef,pc]                             E7 FD BE EF
stb   [$beef,s]                              E7 F9 BE EF
stb   [$beef,u]                              E7 D9 BE EF
stb   [$beef,x]                              E7 99 BE EF
stb   [$beef,y]                              E7 B9 BE EF
stb   [$beef]                                E7 9F BE EF
stb   [$beef]                                E7 BF BE EF
stb   [$beef]                                E7 DF BE EF
stb   [$beef]                                E7 FF BE EF
stb   [,--s]                                 E7 F3
stb   [,--u]                                 E7 D3
stb   [,--x]                                 E7 93
stb   [,--y]                                 E7 B3
stb   [,s++]                                 E7 F1
stb   [,s]                                   E7 F4
stb   [,u++]                                 E7 D1
stb   [,u]                                   E7 D4
stb   [,x++]                                 E7 91
stb   [,x]                                   E7 94
stb   [,y++]                                 E7 B1
stb   [,y]                                   E7 B4
stb   [a,s]                                  E7 F6
stb   [a,u]                                  E7 D6
stb   [a,x]                                  E7 96
stb   [a,y]                                  E7 B6
stb   [b,s]                                  E7 F5
stb   [b,u]                                  E7 D5
stb   [b,x]                                  E7 95
stb   [b,y]                                  E7 B5
stb   [d,s]                                  E7 FB
stb   [d,u]                                  E7 DB
stb   [d,x]                                  E7 9B
stb   [d,y]                                  E7 BB
stb   []                                     E7 97
stb   []                                     E7 9A
stb   []                                     E7 9E
stb   []                                     E7 B7
stb   []                                     E7 BA
stb   []                                     E7 BE
stb   []                                     E7 D7
stb   []                                     E7 DA
stb   []                                     E7 DE
stb   []                                     E7 F7
stb   []                                     E7 FA
stb   []                                     E7 FE
std   $0,s                                   ED 60
std   $0,u                                   ED 40
std   $0,x                                   ED 00
std   $0,y                                   ED 20
std   $01,pc                                 ED 8C 01
std   $01,pc                                 ED AC 01
std   $01,pc                                 ED CC 01
std   $01,pc                                 ED EC 01
std   $01,s                                  ED E8 01
std   $01,u                                  ED C8 01
std   $01,x                                  ED 88 01
std   $01,y                                  ED A8 01
std   $1,s                                   ED 61
std   $1,u                                   ED 41
std   $1,x                                   ED 01
std   $1,y                                   ED 21
std   $2,s                                   ED 62
std   $2,u                                   ED 42
std   $2,x                                   ED 02
std   $2,y                                   ED 22
std   $3,s                                   ED 63
std   $3,u                                   ED 43
std   $3,x                                   ED 03
std   $3,y                                   ED 23
std   $4,s                                   ED 64
std   $4,u                                   ED 44
std   $4,x                                   ED 04
std   $4,y                                   ED 24
std   $5,s                                   ED 65
std   $5,u                                   ED 45
std   $5,x                                   ED 05
std   $5,y                                   ED 25
std   $6,s                                   ED 66
std   $6,u                                   ED 46
std   $6,x                                   ED 06
std   $6,y                                   ED 26
std   $7,s                                   ED 67
std   $7,u                                   ED 47
std   $7,x                                   ED 07
std   $7,y                                   ED 27
std   $8,s                                   ED 68
std   $8,u                                   ED 48
std   $8,x                                   ED 08
std   $8,y                                   ED 28
std   $9,s                                   ED 69
std   $9,u                                   ED 49
std   $9,x                                   ED 09
std   $9,y                                   ED 29
std   $a,s                                   ED 6A
std   $a,u                                   ED 4A
std   $a,x                                   ED 0A
std   $a,y                                   ED 2A
std   $b,s                                   ED 6B
std   $b,u                                   ED 4B
std   $b,x                                   ED 0B
std   $b,y                                   ED 2B
std   $beef                                  ED 8F BE EF
std   $beef                                  ED AF BE EF
std   $beef                                  ED CF BE EF
std   $beef                                  ED EF BE EF
std   $beef                                  FD BE EF
std   $beef,pc                               ED 8D BE EF
std   $beef,pc                               ED AD BE EF
std   $beef,pc                               ED CD BE EF
std   $beef,pc                               ED ED BE EF
std   $beef,s                                ED E9 BE EF
std   $beef,u                                ED C9 BE EF
std   $beef,x                                ED 89 BE EF
std   $beef,y                                ED A9 BE EF
std   $c,s                                   ED 6C
std   $c,u                                   ED 4C
std   $c,x                                   ED 0C
std   $c,y                                   ED 2C
std   $d,s                                   ED 6D
std   $d,u                                   ED 4D
std   $d,x                                   ED 0D
std   $d,y                                   ED 2D
std   $e,s                                   ED 6E
std   $e,u                                   ED 4E
std   $e,x                                   ED 0E
std   $e,y                                   ED 2E
std   $f,s                                   ED 6F
std   $f,u                                   ED 4F
std   $f,x                                   ED 0F
std   $f,y                                   ED 2F
std   $ff                                    DD FF
std   ,--s                                   ED E3
std   ,--u                                   ED C3
std   ,--x                                   ED 83
std   ,--y                                   ED A3
std   ,-s                                    ED E2
std   ,-u                                    ED C2
std   ,-x                                    ED 82
std   ,-y                                    ED A2
std   ,s                                     ED E4
std   ,s+                                    ED E0
std   ,s++                                   ED E1
std   ,u                                     ED C4
std   ,u+                                    ED C0
std   ,u++                                   ED C1
std   ,x                                     ED 84
std   ,x+                                    ED 80
std   ,x++                                   ED 81
std   ,y                                     ED A4
std   ,y+                                    ED A0
std   ,y++                                   ED A1
std   -$1,s                                  ED 7F
std   -$1,u                                  ED 5F
std   -$1,x                                  ED 1F
std   -$1,y                                  ED 3F
std   -$10,s                                 ED 70
std   -$10,u                                 ED 50
std   -$10,x                                 ED 10
std   -$10,y                                 ED 30
std   -$2,s                                  ED 7E
std   -$2,u                                  ED 5E
std   -$2,x                                  ED 1E
std   -$2,y                                  ED 3E
std   -$3,s                                  ED 7D
std   -$3,u                                  ED 5D
std   -$3,x                                  ED 1D
std   -$3,y                                  ED 3D
std   -$4,s                                  ED 7C
std   -$4,u                                  ED 5C
std   -$4,x                                  ED 1C
std   -$4,y                                  ED 3C
std   -$5,s                                  ED 7B
std   -$5,u                                  ED 5B
std   -$5,x                                  ED 1B
std   -$5,y                                  ED 3B
std   -$6,s                                  ED 7A
std   -$6,u                                  ED 5A
std   -$6,x                                  ED 1A
std   -$6,y                                  ED 3A
std   -$7,s                                  ED 79
std   -$7,u                                  ED 59
std   -$7,x                                  ED 19
std   -$7,y                                  ED 39
std   -$8,s                                  ED 78
std   -$8,u                                  ED 58
std   -$8,x                                  ED 18
std   -$8,y                                  ED 38
std   -$9,s                                  ED 77
std   -$9,u                                  ED 57
std   -$9,x                                  ED 17
std   -$9,y                                  ED 37
std   -$a,s                                  ED 76
std   -$a,u                                  ED 56
std   -$a,x                                  ED 16
std   -$a,y                                  ED 36
std   -$b,s                                  ED 75
std   -$b,u                                  ED 55
std   -$b,x                                  ED 15
std   -$b,y                                  ED 35
std   -$c,s                                  ED 74
std   -$c,u                                  ED 54
std   -$c,x                                  ED 14
std   -$c,y                                  ED 34
std   -$d,s                                  ED 73
std   -$d,u                                  ED 53
std   -$d,x                                  ED 13
std   -$d,y                                  ED 33
std   -$e,s                                  ED 72
std   -$e,u                                  ED 52
std   -$e,x                                  ED 12
std   -$e,y                                  ED 32
std   -$f,s                                  ED 71
std   -$f,u                                  ED 51
std   -$f,x                                  ED 11
std   -$f,y                                  ED 31
std   a,s                                    ED E6
std   a,u                                    ED C6
std   a,x                                    ED 86
std   a,y                                    ED A6
std   b,s                                    ED E5
std   b,u                                    ED C5
std   b,x                                    ED 85
std   b,y                                    ED A5
std   d,s                                    ED EB
std   d,u                                    ED CB
std   d,x                                    ED 8B
std   d,y                                    ED AB
std   [$01,pc]                               ED 9C 01
std   [$01,pc]                               ED BC 01
std   [$01,pc]                               ED DC 01
std   [$01,pc]                               ED FC 01
std   [$01,s]                                ED F8 01
std   [$01,u]                                ED D8 01
std   [$01,x]                                ED 98 01
std   [$01,y]                                ED B8 01
std   [$beef,pc]                             ED 9D BE EF
std   [$beef,pc]                             ED BD BE EF
std   [$beef,pc]                             ED DD BE EF
std   [$beef,pc]                             ED FD BE EF
std   [$beef,s]                              ED F9 BE EF
std   [$beef,u]                              ED D9 BE EF
std   [$beef,x]                              ED 99 BE EF
std   [$beef,y]                              ED B9 BE EF
std   [$beef]                                ED 9F BE EF
std   [$beef]                                ED BF BE EF
std   [$beef]                                ED DF BE EF
std   [$beef]                                ED FF BE EF
std   [,--s]                                 ED F3
std   [,--u]                                 ED D3
std   [,--x]                                 ED 93
std   [,--y]                                 ED B3
std   [,s++]                                 ED F1
std   [,s]                                   ED F4
std   [,u++]                                 ED D1
std   [,u]                                   ED D4
std   [,x++]                                 ED 91
std   [,x]                                   ED 94
std   [,y++]                                 ED B1
std   [,y]                                   ED B4
std   [a,s]                                  ED F6
std   [a,u]                                  ED D6
std   [a,x]                                  ED 96
std   [a,y]                                  ED B6
std   [b,s]                                  ED F5
std   [b,u]                                  ED D5
std   [b,x]                                  ED 95
std   [b,y]                                  ED B5
std   [d,s]                                  ED FB
std   [d,u]                                  ED DB
std   [d,x]                                  ED 9B
std   [d,y]                                  ED BB
std   []                                     ED 97
std   []                                     ED 9A
std   []                                     ED 9E
std   []                                     ED B7
std   []                                     ED BA
std   []                                     ED BE
std   []                                     ED D7
std   []                                     ED DA
std   []                                     ED DE
std   []                                     ED F7
std   []                                     ED FA
std   []                                     ED FE
sts   $01                                    10 DF 01
sts   $1,x                                   10 EF 01
sts   $beef                                  10 FF BE EF
stu   $0,s                                   EF 60
stu   $0,u                                   EF 40
stu   $0,x                                   EF 00
stu   $0,y                                   EF 20
stu   $01,pc                                 EF 8C 01
stu   $01,pc                                 EF AC 01
stu   $01,pc                                 EF CC 01
stu   $01,pc                                 EF EC 01
stu   $01,s                                  EF E8 01
stu   $01,u                                  EF C8 01
stu   $01,x                                  EF 88 01
stu   $01,y                                  EF A8 01
stu   $1,s                                   EF 61
stu   $1,u                                   EF 41
stu   $1,x                                   EF 01
stu   $1,y                                   EF 21
stu   $2,s                                   EF 62
stu   $2,u                                   EF 42
stu   $2,x                                   EF 02
stu   $2,y                                   EF 22
stu   $3,s                                   EF 63
stu   $3,u                                   EF 43
stu   $3,x                                   EF 03
stu   $3,y                                   EF 23
stu   $4,s                                   EF 64
stu   $4,u                                   EF 44
stu   $4,x                                   EF 04
stu   $4,y                                   EF 24
stu   $5,s                                   EF 65
stu   $5,u                                   EF 45
stu   $5,x                                   EF 05
stu   $5,y                                   EF 25
stu   $6,s                                   EF 66
stu   $6,u                                   EF 46
stu   $6,x                                   EF 06
stu   $6,y                                   EF 26
stu   $7,s                                   EF 67
stu   $7,u                                   EF 47
stu   $7,x                                   EF 07
stu   $7,y                                   EF 27
stu   $8,s                                   EF 68
stu   $8,u                                   EF 48
stu   $8,x                                   EF 08
stu   $8,y                                   EF 28
stu   $9,s                                   EF 69
stu   $9,u                                   EF 49
stu   $9,x                                   EF 09
stu   $9,y                                   EF 29
stu   $a,s                                   EF 6A
stu   $a,u                                   EF 4A
stu   $a,x                                   EF 0A
stu   $a,y                                   EF 2A
stu   $b,s                                   EF 6B
stu   $b,u                                   EF 4B
stu   $b,x                                   EF 0B
stu   $b,y                                   EF 2B
stu   $beef                                  EF 8F BE EF
stu   $beef                                  EF AF BE EF
stu   $beef                                  EF CF BE EF
stu   $beef                                  EF EF BE EF
stu   $beef                                  FF BE EF
stu   $beef,pc                               EF 8D BE EF
stu   $beef,pc                               EF AD BE EF
stu   $beef,pc                               EF CD BE EF
stu   $beef,pc                               EF ED BE EF
stu   $beef,s                                EF E9 BE EF
stu   $beef,u                                EF C9 BE EF
stu   $beef,x                                EF 89 BE EF
stu   $beef,y                                EF A9 BE EF
stu   $c,s                                   EF 6C
stu   $c,u                                   EF 4C
stu   $c,x                                   EF 0C
stu   $c,y                                   EF 2C
stu   $d,s                                   EF 6D
stu   $d,u                                   EF 4D
stu   $d,x                                   EF 0D
stu   $d,y                                   EF 2D
stu   $e,s                                   EF 6E
stu   $e,u                                   EF 4E
stu   $e,x                                   EF 0E
stu   $e,y                                   EF 2E
stu   $f,s                                   EF 6F
stu   $f,u                                   EF 4F
stu   $f,x                                   EF 0F
stu   $f,y                                   EF 2F
stu   $ff                                    DF FF
stu   ,--s                                   EF E3
stu   ,--u                                   EF C3
stu   ,--x                                   EF 83
stu   ,--y                                   EF A3
stu   ,-s                                    EF E2
stu   ,-u                                    EF C2
stu   ,-x                                    EF 82
stu   ,-y                                    EF A2
stu   ,s                                     EF E4
stu   ,s+                                    EF E0
stu   ,s++                                   EF E1
stu   ,u                                     EF C4
stu   ,u+                                    EF C0
stu   ,u++                                   EF C1
stu   ,x                                     EF 84
stu   ,x+                                    EF 80
stu   ,x++                                   EF 81
stu   ,y                                     EF A4
stu   ,y+                                    EF A0
stu   ,y++                                   EF A1
stu   -$1,s                                  EF 7F
stu   -$1,u                                  EF 5F
stu   -$1,x                                  EF 1F
stu   -$1,y                                  EF 3F
stu   -$10,s                                 EF 70
stu   -$10,u                                 EF 50
stu   -$10,x                                 EF 10
stu   -$10,y                                 EF 30
stu   -$2,s                                  EF 7E
stu   -$2,u                                  EF 5E
stu   -$2,x                                  EF 1E
stu   -$2,y                                  EF 3E
stu   -$3,s                                  EF 7D
stu   -$3,u                                  EF 5D
stu   -$3,x                                  EF 1D
stu   -$3,y                                  EF 3D
stu   -$4,s                                  EF 7C
stu   -$4,u                                  EF 5C
stu   -$4,x                                  EF 1C
stu   -$4,y                                  EF 3C
stu   -$5,s                                  EF 7B
stu   -$5,u                                  EF 5B
stu   -$5,x                                  EF 1B
stu   -$5,y                                  EF 3B
stu   -$6,s                                  EF 7A
stu   -$6,u                                  EF 5A
stu   -$6,x                                  EF 1A
stu   -$6,y                                  EF 3A
stu   -$7,s                                  EF 79
stu   -$7,u                                  EF 59
stu   -$7,x                                  EF 19
stu   -$7,y                                  EF 39
stu   -$8,s                                  EF 78
stu   -$8,u                                  EF 58
stu   -$8,x                                  EF 18
stu   -$8,y                                  EF 38
stu   -$9,s                                  EF 77
stu   -$9,u                                  EF 57
stu   -$9,x                                  EF 17
stu   -$9,y                                  EF 37
stu   -$a,s                                  EF 76
stu   -$a,u                                  EF 56
stu   -$a,x                                  EF 16
stu   -$a,y                                  EF 36
stu   -$b,s                                  EF 75
stu   -$b,u                                  EF 55
stu   -$b,x                                  EF 15
stu   -$b,y                                  EF 35
stu   -$c,s                                  EF 74
stu   -$c,u                                  EF 54
stu   -$c,x                                  EF 14
stu   -$c,y                                  EF 34
stu   -$d,s                                  EF 73
stu   -$d,u                                  EF 53
stu   -$d,x                                  EF 13
stu   -$d,y                                  EF 33
stu   -$e,s                                  EF 72
stu   -$e,u                                  EF 52
stu   -$e,x                                  EF 12
stu   -$e,y                                  EF 32
stu   -$f,s                                  EF 71
stu   -$f,u                                  EF 51
stu   -$f,x                                  EF 11
stu   -$f,y                                  EF 31
stu   a,s                                    EF E6
stu   a,u                                    EF C6
stu   a,x                                    EF 86
stu   a,y                                    EF A6
stu   b,s                                    EF E5
stu   b,u                                    EF C5
stu   b,x                                    EF 85
stu   b,y                                    EF A5
stu   d,s                                    EF EB
stu   d,u                                    EF CB
stu   d,x                                    EF 8B
stu   d,y                                    EF AB
stu   [$01,pc]                               EF 9C 01
stu   [$01,pc]                               EF BC 01
stu   [$01,pc]                               EF DC 01
stu   [$01,pc]                               EF FC 01
stu   [$01,s]                                EF F8 01
stu   [$01,u]                                EF D8 01
stu   [$01,x]                                EF 98 01
stu   [$01,y]                                EF B8 01
stu   [$beef,pc]                             EF 9D BE EF
stu   [$beef,pc]                             EF BD BE EF
stu   [$beef,pc]                             EF DD BE EF
stu   [$beef,pc]                             EF FD BE EF
stu   [$beef,s]                              EF F9 BE EF
stu   [$beef,u]                              EF D9 BE EF
stu   [$beef,x]                              EF 99 BE EF
stu   [$beef,y]                              EF B9 BE EF
stu   [$beef]                                EF 9F BE EF
stu   [$beef]                                EF BF BE EF
stu   [$beef]                                EF DF BE EF
stu   [$beef]                                EF FF BE EF
stu   [,--s]                                 EF F3
stu   [,--u]                                 EF D3
stu   [,--x]                                 EF 93
stu   [,--y]                                 EF B3
stu   [,s++]                                 EF F1
stu   [,s]                                   EF F4
stu   [,u++]                                 EF D1
stu   [,u]                                   EF D4
stu   [,x++]                                 EF 91
stu   [,x]                                   EF 94
stu   [,y++]                                 EF B1
stu   [,y]                                   EF B4
stu   [a,s]                                  EF F6
stu   [a,u]                                  EF D6
stu   [a,x]                                  EF 96
stu   [a,y]                                  EF B6
stu   [b,s]                                  EF F5
stu   [b,u]                                  EF D5
stu   [b,x]                                  EF 95
stu   [b,y]                                  EF B5
stu   [d,s]                                  EF FB
stu   [d,u]                                  EF DB
stu   [d,x]                                  EF 9B
stu   [d,y]                                  EF BB
stu   []                                     EF 97
stu   []                                     EF 9A
stu   []                                     EF 9E
stu   []                                     EF B7
stu   []                                     EF BA
stu   []                                     EF BE
stu   []                                     EF D7
stu   []                                     EF DA
stu   []                                     EF DE
stu   []                                     EF F7
stu   []                                     EF FA
stu   []                                     EF FE
stx   $0,s                                   AF 60
stx   $0,u                                   AF 40
stx   $0,x                                   AF 00
stx   $0,y                                   AF 20
stx   $01,pc                                 AF 8C 01
stx   $01,pc                                 AF AC 01
stx   $01,pc                                 AF CC 01
stx   $01,pc                                 AF EC 01
stx   $01,s                                  AF E8 01
stx   $01,u                                  AF C8 01
stx   $01,x                                  AF 88 01
stx   $01,y                                  AF A8 01
stx   $1,s                                   AF 61
stx   $1,u                                   AF 41
stx   $1,x                                   AF 01
stx   $1,y                                   AF 21
stx   $2,s                                   AF 62
stx   $2,u                                   AF 42
stx   $2,x                                   AF 02
stx   $2,y                                   AF 22
stx   $3,s                                   AF 63
stx   $3,u                                   AF 43
stx   $3,x                                   AF 03
stx   $3,y                                   AF 23
stx   $4,s                                   AF 64
stx   $4,u                                   AF 44
stx   $4,x                                   AF 04
stx   $4,y                                   AF 24
stx   $5,s                                   AF 65
stx   $5,u                                   AF 45
stx   $5,x                                   AF 05
stx   $5,y                                   AF 25
stx   $6,s                                   AF 66
stx   $6,u                                   AF 46
stx   $6,x                                   AF 06
stx   $6,y                                   AF 26
stx   $7,s                                   AF 67
stx   $7,u                                   AF 47
stx   $7,x                                   AF 07
stx   $7,y                                   AF 27
stx   $8,s                                   AF 68
stx   $8,u                                   AF 48
stx   $8,x                                   AF 08
stx   $8,y                                   AF 28
stx   $9,s                                   AF 69
stx   $9,u                                   AF 49
stx   $9,x                                   AF 09
stx   $9,y                                   AF 29
stx   $a,s                                   AF 6A
stx   $a,u                                   AF 4A
stx   $a,x                                   AF 0A
stx   $a,y                                   AF 2A
stx   $b,s                                   AF 6B
stx   $b,u                                   AF 4B
stx   $b,x                                   AF 0B
stx   $b,y                                   AF 2B
stx   $beef                                  AF 8F BE EF
stx   $beef                                  AF AF BE EF
stx   $beef                                  AF CF BE EF
stx   $beef                                  AF EF BE EF
stx   $beef                                  BF BE EF
stx   $beef,pc                               AF 8D BE EF
stx   $beef,pc                               AF AD BE EF
stx   $beef,pc                               AF CD BE EF
stx   $beef,pc                               AF ED BE EF
stx   $beef,s                                AF E9 BE EF
stx   $beef,u                                AF C9 BE EF
stx   $beef,x                                AF 89 BE EF
stx   $beef,y                                AF A9 BE EF
stx   $c,s                                   AF 6C
stx   $c,u                                   AF 4C
stx   $c,x                                   AF 0C
stx   $c,y                                   AF 2C
stx   $d,s                                   AF 6D
stx   $d,u                                   AF 4D
stx   $d,x                                   AF 0D
stx   $d,y                                   AF 2D
stx   $e,s                                   AF 6E
stx   $e,u                                   AF 4E
stx   $e,x                                   AF 0E
stx   $e,y                                   AF 2E
stx   $f,s                                   AF 6F
stx   $f,u                                   AF 4F
stx   $f,x                                   AF 0F
stx   $f,y                                   AF 2F
stx   $ff                                    9F FF
stx   ,--s                                   AF E3
stx   ,--u                                   AF C3
stx   ,--x                                   AF 83
stx   ,--y                                   AF A3
stx   ,-s                                    AF E2
stx   ,-u                                    AF C2
stx   ,-x                                    AF 82
stx   ,-y                                    AF A2
stx   ,s                                     AF E4
stx   ,s+                                    AF E0
stx   ,s++                                   AF E1
stx   ,u                                     AF C4
stx   ,u+                                    AF C0
stx   ,u++                                   AF C1
stx   ,x                                     AF 84
stx   ,x+                                    AF 80
stx   ,x++                                   AF 81
stx   ,y                                     AF A4
stx   ,y+                                    AF A0
stx   ,y++                                   AF A1
stx   -$1,s                                  AF 7F
stx   -$1,u                                  AF 5F
stx   -$1,x                                  AF 1F
stx   -$1,y                                  AF 3F
stx   -$10,s                                 AF 70
stx   -$10,u                                 AF 50
stx   -$10,x                                 AF 10
stx   -$10,y                                 AF 30
stx   -$2,s                                  AF 7E
stx   -$2,u                                  AF 5E
stx   -$2,x                                  AF 1E
stx   -$2,y                                  AF 3E
stx   -$3,s                                  AF 7D
stx   -$3,u                                  AF 5D
stx   -$3,x                                  AF 1D
stx   -$3,y                                  AF 3D
stx   -$4,s                                  AF 7C
stx   -$4,u                                  AF 5C
stx   -$4,x                                  AF 1C
stx   -$4,y                                  AF 3C
stx   -$5,s                                  AF 7B
stx   -$5,u                                  AF 5B
stx   -$5,x                                  AF 1B
stx   -$5,y                                  AF 3B
stx   -$6,s                                  AF 7A
stx   -$6,u                                  AF 5A
stx   -$6,x                                  AF 1A
stx   -$6,y                                  AF 3A
stx   -$7,s                                  AF 79
stx   -$7,u                                  AF 59
stx   -$7,x                                  AF 19
stx   -$7,y                                  AF 39
stx   -$8,s                                  AF 78
stx   -$8,u                                  AF 58
stx   -$8,x                                  AF 18
stx   -$8,y                                  AF 38
stx   -$9,s                                  AF 77
stx   -$9,u                                  AF 57
stx   -$9,x                                  AF 17
stx   -$9,y                                  AF 37
stx   -$a,s                                  AF 76
stx   -$a,u                                  AF 56
stx   -$a,x                                  AF 16
stx   -$a,y                                  AF 36
stx   -$b,s                                  AF 75
stx   -$b,u                                  AF 55
stx   -$b,x                                  AF 15
stx   -$b,y                                  AF 35
stx   -$c,s                                  AF 74
stx   -$c,u                                  AF 54
stx   -$c,x                                  AF 14
stx   -$c,y                                  AF 34
stx   -$d,s                                  AF 73
stx   -$d,u                                  AF 53
stx   -$d,x                                  AF 13
stx   -$d,y                                  AF 33
stx   -$e,s                                  AF 72
stx   -$e,u                                  AF 52
stx   -$e,x                                  AF 12
stx   -$e,y                                  AF 32
stx   -$f,s                                  AF 71
stx   -$f,u                                  AF 51
stx   -$f,x                                  AF 11
stx   -$f,y                                  AF 31
stx   a,s                                    AF E6
stx   a,u                                    AF C6
stx   a,x                                    AF 86
stx   a,y                                    AF A6
stx   b,s                                    AF E5
stx   b,u                                    AF C5
stx   b,x                                    AF 85
stx   b,y                                    AF A5
stx   d,s                                    AF EB
stx   d,u                                    AF CB
stx   d,x                                    AF 8B
stx   d,y                                    AF AB
stx   [$01,pc]                               AF 9C 01
stx   [$01,pc]                               AF BC 01
stx   [$01,pc]                               AF DC 01
stx   [$01,pc]                               AF FC 01
stx   [$01,s]                                AF F8 01
stx   [$01,u]                                AF D8 01
stx   [$01,x]                                AF 98 01
stx   [$01,y]                                AF B8 01
stx   [$beef,pc]                             AF 9D BE EF
stx   [$beef,pc]                             AF BD BE EF
stx   [$beef,pc]                             AF DD BE EF
stx   [$beef,pc]                             AF FD BE EF
stx   [$beef,s]                              AF F9 BE EF
stx   [$beef,u]                              AF D9 BE EF
stx   [$beef,x]                              AF 99 BE EF
stx   [$beef,y]                              AF B9 BE EF
stx   [$beef]                                AF 9F BE EF
stx   [$beef]                                AF BF BE EF
stx   [$beef]                                AF DF BE EF
stx   [$beef]                                AF FF BE EF
stx   [,--s]                                 AF F3
stx   [,--u]                                 AF D3
stx   [,--x]                                 AF 93
stx   [,--y]                                 AF B3
stx   [,s++]                                 AF F1
stx   [,s]                                   AF F4
stx   [,u++]                                 AF D1
stx   [,u]                                   AF D4
stx   [,x++]                                 AF 91
stx   [,x]                                   AF 94
stx   [,y++]                                 AF B1
stx   [,y]                                   AF B4
stx   [a,s]                                  AF F6
stx   [a,u]                                  AF D6
stx   [a,x]                                  AF 96
stx   [a,y]                                  AF B6
stx   [b,s]                                  AF F5
stx   [b,u]                                  AF D5
stx   [b,x]                                  AF 95
stx   [b,y]                                  AF B5
stx   [d,s]                                  AF FB
stx   [d,u]                                  AF DB
stx   [d,x]                                  AF 9B
stx   [d,y]                                  AF BB
stx   []                                     AF 97
stx   []                                     AF 9A
stx   []                                     AF 9E
stx   []                                     AF B7
stx   []                                     AF BA
stx   []                                     AF BE
stx   []                                     AF D7
stx   []                                     AF DA
stx   []                                     AF DE
stx   []                                     AF F7
stx   []                                     AF FA
stx   []                                     AF FE
sty   $01                                    10 9F 01
sty   $1,x                                   10 AF 01
sty   $beef                                  10 BF BE EF
suba  #$ff                                   80 FF
suba  $0,s                                   A0 60
suba  $0,u                                   A0 40
suba  $0,x                                   A0 00
suba  $0,y                                   A0 20
suba  $01,pc                                 A0 8C 01
suba  $01,pc                                 A0 AC 01
suba  $01,pc                                 A0 CC 01
suba  $01,pc                                 A0 EC 01
suba  $01,s                                  A0 E8 01
suba  $01,u                                  A0 C8 01
suba  $01,x                                  A0 88 01
suba  $01,y                                  A0 A8 01
suba  $1,s                                   A0 61
suba  $1,u                                   A0 41
suba  $1,x                                   A0 01
suba  $1,y                                   A0 21
suba  $2,s                                   A0 62
suba  $2,u                                   A0 42
suba  $2,x                                   A0 02
suba  $2,y                                   A0 22
suba  $3,s                                   A0 63
suba  $3,u                                   A0 43
suba  $3,x                                   A0 03
suba  $3,y                                   A0 23
suba  $4,s                                   A0 64
suba  $4,u                                   A0 44
suba  $4,x                                   A0 04
suba  $4,y                                   A0 24
suba  $5,s                                   A0 65
suba  $5,u                                   A0 45
suba  $5,x                                   A0 05
suba  $5,y                                   A0 25
suba  $6,s                                   A0 66
suba  $6,u                                   A0 46
suba  $6,x                                   A0 06
suba  $6,y                                   A0 26
suba  $7,s                                   A0 67
suba  $7,u                                   A0 47
suba  $7,x                                   A0 07
suba  $7,y                                   A0 27
suba  $8,s                                   A0 68
suba  $8,u                                   A0 48
suba  $8,x                                   A0 08
suba  $8,y                                   A0 28
suba  $9,s                                   A0 69
suba  $9,u                                   A0 49
suba  $9,x                                   A0 09
suba  $9,y                                   A0 29
suba  $a,s                                   A0 6A
suba  $a,u                                   A0 4A
suba  $a,x                                   A0 0A
suba  $a,y                                   A0 2A
suba  $b,s                                   A0 6B
suba  $b,u                                   A0 4B
suba  $b,x                                   A0 0B
suba  $b,y                                   A0 2B
suba  $beef                                  A0 8F BE EF
suba  $beef                                  A0 AF BE EF
suba  $beef                                  A0 CF BE EF
suba  $beef                                  A0 EF BE EF
suba  $beef                                  B0 BE EF
suba  $beef,pc                               A0 8D BE EF
suba  $beef,pc                               A0 AD BE EF
suba  $beef,pc                               A0 CD BE EF
suba  $beef,pc                               A0 ED BE EF
suba  $beef,s                                A0 E9 BE EF
suba  $beef,u                                A0 C9 BE EF
suba  $beef,x                                A0 89 BE EF
suba  $beef,y                                A0 A9 BE EF
suba  $c,s                                   A0 6C
suba  $c,u                                   A0 4C
suba  $c,x                                   A0 0C
suba  $c,y                                   A0 2C
suba  $d,s                                   A0 6D
suba  $d,u                                   A0 4D
suba  $d,x                                   A0 0D
suba  $d,y                                   A0 2D
suba  $e,s                                   A0 6E
suba  $e,u                                   A0 4E
suba  $e,x                                   A0 0E
suba  $e,y                                   A0 2E
suba  $f,s                                   A0 6F
suba  $f,u                                   A0 4F
suba  $f,x                                   A0 0F
suba  $f,y                                   A0 2F
suba  $ff                                    90 FF
suba  ,--s                                   A0 E3
suba  ,--u                                   A0 C3
suba  ,--x                                   A0 83
suba  ,--y                                   A0 A3
suba  ,-s                                    A0 E2
suba  ,-u                                    A0 C2
suba  ,-x                                    A0 82
suba  ,-y                                    A0 A2
suba  ,s                                     A0 E4
suba  ,s+                                    A0 E0
suba  ,s++                                   A0 E1
suba  ,u                                     A0 C4
suba  ,u+                                    A0 C0
suba  ,u++                                   A0 C1
suba  ,x                                     A0 84
suba  ,x+                                    A0 80
suba  ,x++                                   A0 81
suba  ,y                                     A0 A4
suba  ,y+                                    A0 A0
suba  ,y++                                   A0 A1
suba  -$1,s                                  A0 7F
suba  -$1,u                                  A0 5F
suba  -$1,x                                  A0 1F
suba  -$1,y                                  A0 3F
suba  -$10,s                                 A0 70
suba  -$10,u                                 A0 50
suba  -$10,x                                 A0 10
suba  -$10,y                                 A0 30
suba  -$2,s                                  A0 7E
suba  -$2,u                                  A0 5E
suba  -$2,x                                  A0 1E
suba  -$2,y                                  A0 3E
suba  -$3,s                                  A0 7D
suba  -$3,u                                  A0 5D
suba  -$3,x                                  A0 1D
suba  -$3,y                                  A0 3D
suba  -$4,s                                  A0 7C
suba  -$4,u                                  A0 5C
suba  -$4,x                                  A0 1C
suba  -$4,y                                  A0 3C
suba  -$5,s                                  A0 7B
suba  -$5,u                                  A0 5B
suba  -$5,x                                  A0 1B
suba  -$5,y                                  A0 3B
suba  -$6,s                                  A0 7A
suba  -$6,u                                  A0 5A
suba  -$6,x                                  A0 1A
suba  -$6,y                                  A0 3A
suba  -$7,s                                  A0 79
suba  -$7,u                                  A0 59
suba  -$7,x                                  A0 19
suba  -$7,y                                  A0 39
suba  -$8,s                                  A0 78
suba  -$8,u                                  A0 58
suba  -$8,x                                  A0 18
suba  -$8,y                                  A0 38
suba  -$9,s                                  A0 77
suba  -$9,u                                  A0 57
suba  -$9,x                                  A0 17
suba  -$9,y                                  A0 37
suba  -$a,s                                  A0 76
suba  -$a,u                                  A0 56
suba  -$a,x                                  A0 16
suba  -$a,y                                  A0 36
suba  -$b,s                                  A0 75
suba  -$b,u                                  A0 55
suba  -$b,x                                  A0 15
suba  -$b,y                                  A0 35
suba  -$c,s                                  A0 74
suba  -$c,u                                  A0 54
suba  -$c,x                                  A0 14
suba  -$c,y                                  A0 34
suba  -$d,s                                  A0 73
suba  -$d,u                                  A0 53
suba  -$d,x                                  A0 13
suba  -$d,y                                  A0 33
suba  -$e,s                                  A0 72
suba  -$e,u                                  A0 52
suba  -$e,x                                  A0 12
suba  -$e,y                                  A0 32
suba  -$f,s                                  A0 71
suba  -$f,u                                  A0 51
suba  -$f,x                                  A0 11
suba  -$f,y                                  A0 31
suba  a,s                                    A0 E6
suba  a,u                                    A0 C6
suba  a,x                                    A0 86
suba  a,y                                    A0 A6
suba  b,s                                    A0 E5
suba  b,u                                    A0 C5
suba  b,x                                    A0 85
suba  b,y                                    A0 A5
suba  d,s                                    A0 EB
suba  d,u                                    A0 CB
suba  d,x                                    A0 8B
suba  d,y                                    A0 AB
suba  [$01,pc]                               A0 9C 01
suba  [$01,pc]                               A0 BC 01
suba  [$01,pc]                               A0 DC 01
suba  [$01,pc]                               A0 FC 01
suba  [$01,s]                                A0 F8 01
suba  [$01,u]                                A0 D8 01
suba  [$01,x]                                A0 98 01
suba  [$01,y]                                A0 B8 01
suba  [$beef,pc]                             A0 9D BE EF
suba  [$beef,pc]                             A0 BD BE EF
suba  [$beef,pc]                             A0 DD BE EF
suba  [$beef,pc]                             A0 FD BE EF
suba  [$beef,s]                              A0 F9 BE EF
suba  [$beef,u]                              A0 D9 BE EF
suba  [$beef,x]                              A0 99 BE EF
suba  [$beef,y]                              A0 B9 BE EF
suba  [$beef]                                A0 9F BE EF
suba  [$beef]                                A0 BF BE EF
suba  [$beef]                                A0 DF BE EF
suba  [$beef]                                A0 FF BE EF
suba  [,--s]                                 A0 F3
suba  [,--u]                                 A0 D3
suba  [,--x]                                 A0 93
suba  [,--y]                                 A0 B3
suba  [,s++]                                 A0 F1
suba  [,s]                                   A0 F4
suba  [,u++]                                 A0 D1
suba  [,u]                                   A0 D4
suba  [,x++]                                 A0 91
suba  [,x]                                   A0 94
suba  [,y++]                                 A0 B1
suba  [,y]                                   A0 B4
suba  [a,s]                                  A0 F6
suba  [a,u]                                  A0 D6
suba  [a,x]                                  A0 96
suba  [a,y]                                  A0 B6
suba  [b,s]                                  A0 F5
suba  [b,u]                                  A0 D5
suba  [b,x]                                  A0 95
suba  [b,y]                                  A0 B5
suba  [d,s]                                  A0 FB
suba  [d,u]                                  A0 DB
suba  [d,x]                                  A0 9B
suba  [d,y]                                  A0 BB
suba  []                                     A0 97
suba  []                                     A0 9A
suba  []                                     A0 9E
suba  []                                     A0 B7
suba  []                                     A0 BA
suba  []                                     A0 BE
suba  []                                     A0 D7
suba  []                                     A0 DA
suba  []                                     A0 DE
suba  []                                     A0 F7
suba  []                                     A0 FA
suba  []                                     A0 FE
subb  #$ff                                   C0 FF
subb  $0,s                                   E0 60
subb  $0,u                                   E0 40
subb  $0,x                                   E0 00
subb  $0,y                                   E0 20
subb  $01,pc                                 E0 8C 01
subb  $01,pc                                 E0 AC 01
subb  $01,pc                                 E0 CC 01
subb  $01,pc                                 E0 EC 01
subb  $01,s                                  E0 E8 01
subb  $01,u                                  E0 C8 01
subb  $01,x                                  E0 88 01
subb  $01,y                                  E0 A8 01
subb  $1,s                                   E0 61
subb  $1,u                                   E0 41
subb  $1,x                                   E0 01
subb  $1,y                                   E0 21
subb  $2,s                                   E0 62
subb  $2,u                                   E0 42
subb  $2,x                                   E0 02
subb  $2,y                                   E0 22
subb  $3,s                                   E0 63
subb  $3,u                                   E0 43
subb  $3,x                                   E0 03
subb  $3,y                                   E0 23
subb  $4,s                                   E0 64
subb  $4,u                                   E0 44
subb  $4,x                                   E0 04
subb  $4,y                                   E0 24
subb  $5,s                                   E0 65
subb  $5,u                                   E0 45
subb  $5,x                                   E0 05
subb  $5,y                                   E0 25
subb  $6,s                                   E0 66
subb  $6,u                                   E0 46
subb  $6,x                                   E0 06
subb  $6,y                                   E0 26
subb  $7,s                                   E0 67
subb  $7,u                                   E0 47
subb  $7,x                                   E0 07
subb  $7,y                                   E0 27
subb  $8,s                                   E0 68
subb  $8,u                                   E0 48
subb  $8,x                                   E0 08
subb  $8,y                                   E0 28
subb  $9,s                                   E0 69
subb  $9,u                                   E0 49
subb  $9,x                                   E0 09
subb  $9,y                                   E0 29
subb  $a,s                                   E0 6A
subb  $a,u                                   E0 4A
subb  $a,x                                   E0 0A
subb  $a,y                                   E0 2A
subb  $b,s                                   E0 6B
subb  $b,u                                   E0 4B
subb  $b,x                                   E0 0B
subb  $b,y                                   E0 2B
subb  $beef                                  E0 8F BE EF
subb  $beef                                  E0 AF BE EF
subb  $beef                                  E0 CF BE EF
subb  $beef                                  E0 EF BE EF
subb  $beef                                  F0 BE EF
subb  $beef,pc                               E0 8D BE EF
subb  $beef,pc                               E0 AD BE EF
subb  $beef,pc                               E0 CD BE EF
subb  $beef,pc                               E0 ED BE EF
subb  $beef,s                                E0 E9 BE EF
subb  $beef,u                                E0 C9 BE EF
subb  $beef,x                                E0 89 BE EF
subb  $beef,y                                E0 A9 BE EF
subb  $c,s                                   E0 6C
subb  $c,u                                   E0 4C
subb  $c,x                                   E0 0C
subb  $c,y                                   E0 2C
subb  $d,s                                   E0 6D
subb  $d,u                                   E0 4D
subb  $d,x                                   E0 0D
subb  $d,y                                   E0 2D
subb  $e,s                                   E0 6E
subb  $e,u                                   E0 4E
subb  $e,x                                   E0 0E
subb  $e,y                                   E0 2E
subb  $f,s                                   E0 6F
subb  $f,u                                   E0 4F
subb  $f,x                                   E0 0F
subb  $f,y                                   E0 2F
subb  $ff                                    D0 FF
subb  ,--s                                   E0 E3
subb  ,--u                                   E0 C3
subb  ,--x                                   E0 83
subb  ,--y                                   E0 A3
subb  ,-s                                    E0 E2
subb  ,-u                                    E0 C2
subb  ,-x                                    E0 82
subb  ,-y                                    E0 A2
subb  ,s                                     E0 E4
subb  ,s+                                    E0 E0
subb  ,s++                                   E0 E1
subb  ,u                                     E0 C4
subb  ,u+                                    E0 C0
subb  ,u++                                   E0 C1
subb  ,x                                     E0 84
subb  ,x+                                    E0 80
subb  ,x++                                   E0 81
subb  ,y                                     E0 A4
subb  ,y+                                    E0 A0
subb  ,y++                                   E0 A1
subb  -$1,s                                  E0 7F
subb  -$1,u                                  E0 5F
subb  -$1,x                                  E0 1F
subb  -$1,y                                  E0 3F
subb  -$10,s                                 E0 70
subb  -$10,u                                 E0 50
subb  -$10,x                                 E0 10
subb  -$10,y                                 E0 30
subb  -$2,s                                  E0 7E
subb  -$2,u                                  E0 5E
subb  -$2,x                                  E0 1E
subb  -$2,y                                  E0 3E
subb  -$3,s                                  E0 7D
subb  -$3,u                                  E0 5D
subb  -$3,x                                  E0 1D
subb  -$3,y                                  E0 3D
subb  -$4,s                                  E0 7C
subb  -$4,u                                  E0 5C
subb  -$4,x                                  E0 1C
subb  -$4,y                                  E0 3C
subb  -$5,s                                  E0 7B
subb  -$5,u                                  E0 5B
subb  -$5,x                                  E0 1B
subb  -$5,y                                  E0 3B
subb  -$6,s                                  E0 7A
subb  -$6,u                                  E0 5A
subb  -$6,x                                  E0 1A
subb  -$6,y                                  E0 3A
subb  -$7,s                                  E0 79
subb  -$7,u                                  E0 59
subb  -$7,x                                  E0 19
subb  -$7,y                                  E0 39
subb  -$8,s                                  E0 78
subb  -$8,u                                  E0 58
subb  -$8,x                                  E0 18
subb  -$8,y                                  E0 38
subb  -$9,s                                  E0 77
subb  -$9,u                                  E0 57
subb  -$9,x                                  E0 17
subb  -$9,y                                  E0 37
subb  -$a,s                                  E0 76
subb  -$a,u                                  E0 56
subb  -$a,x                                  E0 16
subb  -$a,y                                  E0 36
subb  -$b,s                                  E0 75
subb  -$b,u                                  E0 55
subb  -$b,x                                  E0 15
subb  -$b,y                                  E0 35
subb  -$c,s                                  E0 74
subb  -$c,u                                  E0 54
subb  -$c,x                                  E0 14
subb  -$c,y                                  E0 34
subb  -$d,s                                  E0 73
subb  -$d,u                                  E0 53
subb  -$d,x                                  E0 13
subb  -$d,y                                  E0 33
subb  -$e,s                                  E0 72
subb  -$e,u                                  E0 52
subb  -$e,x                                  E0 12
subb  -$e,y                                  E0 32
subb  -$f,s                                  E0 71
subb  -$f,u                                  E0 51
subb  -$f,x                                  E0 11
subb  -$f,y                                  E0 31
subb  a,s                                    E0 E6
subb  a,u                                    E0 C6
subb  a,x                                    E0 86
subb  a,y                                    E0 A6
subb  b,s                                    E0 E5
subb  b,u                                    E0 C5
subb  b,x                                    E0 85
subb  b,y                                    E0 A5
subb  d,s                                    E0 EB
subb  d,u                                    E0 CB
subb  d,x                                    E0 8B
subb  d,y                                    E0 AB
subb  [$01,pc]                               E0 9C 01
subb  [$01,pc]                               E0 BC 01
subb  [$01,pc]                               E0 DC 01
subb  [$01,pc]                               E0 FC 01
subb  [$01,s]                                E0 F8 01
subb  [$01,u]                                E0 D8 01
subb  [$01,x]                                E0 98 01
subb  [$01,y]                                E0 B8 01
subb  [$beef,pc]                             E0 9D BE EF
subb  [$beef,pc]                             E0 BD BE EF
subb  [$beef,pc]                             E0 DD BE EF
subb  [$beef,pc]                             E0 FD BE EF
subb  [$beef,s]                              E0 F9 BE EF
subb  [$beef,u]                              E0 D9 BE EF
subb  [$beef,x]                              E0 99 BE EF
subb  [$beef,y]                              E0 B9 BE EF
subb  [$beef]                                E0 9F BE EF
subb  [$beef]                                E0 BF BE EF
subb  [$beef]                                E0 DF BE EF
subb  [$beef]                                E0 FF BE EF
subb  [,--s]                                 E0 F3
subb  [,--u]                                 E0 D3
subb  [,--x]                                 E0 93
subb  [,--y]                                 E0 B3
subb  [,s++]                                 E0 F1
subb  [,s]                                   E0 F4
subb  [,u++]                                 E0 D1
subb  [,u]                                   E0 D4
subb  [,x++]                                 E0 91
subb  [,x]                                   E0 94
subb  [,y++]                                 E0 B1
subb  [,y]                                   E0 B4
subb  [a,s]                                  E0 F6
subb  [a,u]                                  E0 D6
subb  [a,x]                                  E0 96
subb  [a,y]                                  E0 B6
subb  [b,s]                                  E0 F5
subb  [b,u]                                  E0 D5
subb  [b,x]                                  E0 95
subb  [b,y]                                  E0 B5
subb  [d,s]                                  E0 FB
subb  [d,u]                                  E0 DB
subb  [d,x]                                  E0 9B
subb  [d,y]                                  E0 BB
subb  []                                     E0 97
subb  []                                     E0 9A
subb  []                                     E0 9E
subb  []                                     E0 B7
subb  []                                     E0 BA
subb  []                                     E0 BE
subb  []                                     E0 D7
subb  []                                     E0 DA
subb  []                                     E0 DE
subb  []                                     E0 F7
subb  []                                     E0 FA
subb  []                                     E0 FE
subd  #$beef                                 83 BE EF
subd  $0,s                                   A3 60
subd  $0,u                                   A3 40
subd  $0,x                                   A3 00
subd  $0,y                                   A3 20
subd  $01,pc                                 A3 8C 01
subd  $01,pc                                 A3 AC 01
subd  $01,pc                                 A3 CC 01
subd  $01,pc                                 A3 EC 01
subd  $01,s                                  A3 E8 01
subd  $01,u                                  A3 C8 01
subd  $01,x                                  A3 88 01
subd  $01,y                                  A3 A8 01
subd  $1,s                                   A3 61
subd  $1,u                                   A3 41
subd  $1,x                                   A3 01
subd  $1,y                                   A3 21
subd  $2,s                                   A3 62
subd  $2,u                                   A3 42
subd  $2,x                                   A3 02
subd  $2,y                                   A3 22
subd  $3,s                                   A3 63
subd  $3,u                                   A3 43
subd  $3,x                                   A3 03
subd  $3,y                                   A3 23
subd  $4,s                                   A3 64
subd  $4,u                                   A3 44
subd  $4,x                                   A3 04
subd  $4,y                                   A3 24
subd  $5,s                                   A3 65
subd  $5,u                                   A3 45
subd  $5,x                                   A3 05
subd  $5,y                                   A3 25
subd  $6,s                                   A3 66
subd  $6,u                                   A3 46
subd  $6,x                                   A3 06
subd  $6,y                                   A3 26
subd  $7,s                                   A3 67
subd  $7,u                                   A3 47
subd  $7,x                                   A3 07
subd  $7,y                                   A3 27
subd  $8,s                                   A3 68
subd  $8,u                                   A3 48
subd  $8,x                                   A3 08
subd  $8,y                                   A3 28
subd  $9,s                                   A3 69
subd  $9,u                                   A3 49
subd  $9,x                                   A3 09
subd  $9,y                                   A3 29
subd  $a,s                                   A3 6A
subd  $a,u                                   A3 4A
subd  $a,x                                   A3 0A
subd  $a,y                                   A3 2A
subd  $b,s                                   A3 6B
subd  $b,u                                   A3 4B
subd  $b,x                                   A3 0B
subd  $b,y                                   A3 2B
subd  $beef                                  A3 8F BE EF
subd  $beef                                  A3 AF BE EF
subd  $beef                                  A3 CF BE EF
subd  $beef                                  A3 EF BE EF
subd  $beef                                  B3 BE EF
subd  $beef,pc                               A3 8D BE EF
subd  $beef,pc                               A3 AD BE EF
subd  $beef,pc                               A3 CD BE EF
subd  $beef,pc                               A3 ED BE EF
subd  $beef,s                                A3 E9 BE EF
subd  $beef,u                                A3 C9 BE EF
subd  $beef,x                                A3 89 BE EF
subd  $beef,y                                A3 A9 BE EF
subd  $c,s                                   A3 6C
subd  $c,u                                   A3 4C
subd  $c,x                                   A3 0C
subd  $c,y                                   A3 2C
subd  $d,s                                   A3 6D
subd  $d,u                                   A3 4D
subd  $d,x                                   A3 0D
subd  $d,y                                   A3 2D
subd  $e,s                                   A3 6E
subd  $e,u                                   A3 4E
subd  $e,x                                   A3 0E
subd  $e,y                                   A3 2E
subd  $f,s                                   A3 6F
subd  $f,u                                   A3 4F
subd  $f,x                                   A3 0F
subd  $f,y                                   A3 2F
subd  $ff                                    93 FF
subd  ,--s                                   A3 E3
subd  ,--u                                   A3 C3
subd  ,--x                                   A3 83
subd  ,--y                                   A3 A3
subd  ,-s                                    A3 E2
subd  ,-u                                    A3 C2
subd  ,-x                                    A3 82
subd  ,-y                                    A3 A2
subd  ,s                                     A3 E4
subd  ,s+                                    A3 E0
subd  ,s++                                   A3 E1
subd  ,u                                     A3 C4
subd  ,u+                                    A3 C0
subd  ,u++                                   A3 C1
subd  ,x                                     A3 84
subd  ,x+                                    A3 80
subd  ,x++                                   A3 81
subd  ,y                                     A3 A4
subd  ,y+                                    A3 A0
subd  ,y++                                   A3 A1
subd  -$1,s                                  A3 7F
subd  -$1,u                                  A3 5F
subd  -$1,x                                  A3 1F
subd  -$1,y                                  A3 3F
subd  -$10,s                                 A3 70
subd  -$10,u                                 A3 50
subd  -$10,x                                 A3 10
subd  -$10,y                                 A3 30
subd  -$2,s                                  A3 7E
subd  -$2,u                                  A3 5E
subd  -$2,x                                  A3 1E
subd  -$2,y                                  A3 3E
subd  -$3,s                                  A3 7D
subd  -$3,u                                  A3 5D
subd  -$3,x                                  A3 1D
subd  -$3,y                                  A3 3D
subd  -$4,s                                  A3 7C
subd  -$4,u                                  A3 5C
subd  -$4,x                                  A3 1C
subd  -$4,y                                  A3 3C
subd  -$5,s                                  A3 7B
subd  -$5,u                                  A3 5B
subd  -$5,x                                  A3 1B
subd  -$5,y                                  A3 3B
subd  -$6,s                                  A3 7A
subd  -$6,u                                  A3 5A
subd  -$6,x                                  A3 1A
subd  -$6,y                                  A3 3A
subd  -$7,s                                  A3 79
subd  -$7,u                                  A3 59
subd  -$7,x                                  A3 19
subd  -$7,y                                  A3 39
subd  -$8,s                                  A3 78
subd  -$8,u                                  A3 58
subd  -$8,x                                  A3 18
subd  -$8,y                                  A3 38
subd  -$9,s                                  A3 77
subd  -$9,u                                  A3 57
subd  -$9,x                                  A3 17
subd  -$9,y                                  A3 37
subd  -$a,s                                  A3 76
subd  -$a,u                                  A3 56
subd  -$a,x                                  A3 16
subd  -$a,y                                  A3 36
subd  -$b,s                                  A3 75
subd  -$b,u                                  A3 55
subd  -$b,x                                  A3 15
subd  -$b,y                                  A3 35
subd  -$c,s                                  A3 74
subd  -$c,u                                  A3 54
subd  -$c,x                                  A3 14
subd  -$c,y                                  A3 34
subd  -$d,s                                  A3 73
subd  -$d,u                                  A3 53
subd  -$d,x                                  A3 13
subd  -$d,y                                  A3 33
subd  -$e,s                                  A3 72
subd  -$e,u                                  A3 52
subd  -$e,x                                  A3 12
subd  -$e,y                                  A3 32
subd  -$f,s                                  A3 71
subd  -$f,u                                  A3 51
subd  -$f,x                                  A3 11
subd  -$f,y                                  A3 31
subd  a,s                                    A3 E6
subd  a,u                                    A3 C6
subd  a,x                                    A3 86
subd  a,y                                    A3 A6
subd  b,s                                    A3 E5
subd  b,u                                    A3 C5
subd  b,x                                    A3 85
subd  b,y                                    A3 A5
subd  d,s                                    A3 EB
subd  d,u                                    A3 CB
subd  d,x                                    A3 8B
subd  d,y                                    A3 AB
subd  [$01,pc]                               A3 9C 01
subd  [$01,pc]                               A3 BC 01
subd  [$01,pc]                               A3 DC 01
subd  [$01,pc]                               A3 FC 01
subd  [$01,s]                                A3 F8 01
subd  [$01,u]                                A3 D8 01
subd  [$01,x]                                A3 98 01
subd  [$01,y]                                A3 B8 01
subd  [$beef,pc]                             A3 9D BE EF
subd  [$beef,pc]                             A3 BD BE EF
subd  [$beef,pc]                             A3 DD BE EF
subd  [$beef,pc]                             A3 FD BE EF
subd  [$beef,s]                              A3 F9 BE EF
subd  [$beef,u]                              A3 D9 BE EF
subd  [$beef,x]                              A3 99 BE EF
subd  [$beef,y]                              A3 B9 BE EF
subd  [$beef]                                A3 9F BE EF
subd  [$beef]                                A3 BF BE EF
subd  [$beef]                                A3 DF BE EF
subd  [$beef]                                A3 FF BE EF
subd  [,--s]                                 A3 F3
subd  [,--u]                                 A3 D3
subd  [,--x]                                 A3 93
subd  [,--y]                                 A3 B3
subd  [,s++]                                 A3 F1
subd  [,s]                                   A3 F4
subd  [,u++]                                 A3 D1
subd  [,u]                                   A3 D4
subd  [,x++]                                 A3 91
subd  [,x]                                   A3 94
subd  [,y++]                                 A3 B1
subd  [,y]                                   A3 B4
subd  [a,s]                                  A3 F6
subd  [a,u]                                  A3 D6
subd  [a,x]                                  A3 96
subd  [a,y]                                  A3 B6
subd  [b,s]                                  A3 F5
subd  [b,u]                                  A3 D5
subd  [b,x]                                  A3 95
subd  [b,y]                                  A3 B5
subd  [d,s]                                  A3 FB
subd  [d,u]                                  A3 DB
subd  [d,x]                                  A3 9B
subd  [d,y]                                  A3 BB
subd  []                                     A3 97
subd  []                                     A3 9A
subd  []                                     A3 9E
subd  []                                     A3 B7
subd  []                                     A3 BA
subd  []                                     A3 BE
subd  []                                     A3 D7
subd  []                                     A3 DA
subd  []                                     A3 DE
subd  []                                     A3 F7
subd  []                                     A3 FA
subd  []                                     A3 FE
swi                                          3F
swi2                                         10 3F
swi3                                         11 3F
sync                                         13
tfr   a,a                                    1F 88
tfr   a,b                                    1F 89
tfr   a,cc                                   1F 8A
tfr   a,d                                    1F 80
tfr   a,dp                                   1F 8B
tfr   a,inv                                  1F 86
tfr   a,inv                                  1F 87
tfr   a,inv                                  1F 8C
tfr   a,inv                                  1F 8D
tfr   a,inv                                  1F 8E
tfr   a,inv                                  1F 8F
tfr   a,pc                                   1F 85
tfr   a,s                                    1F 84
tfr   a,u                                    1F 83
tfr   a,x                                    1F 81
tfr   a,y                                    1F 82
tfr   b,a                                    1F 98
tfr   b,b                                    1F 99
tfr   b,cc                                   1F 9A
tfr   b,d                                    1F 90
tfr   b,dp                                   1F 9B
tfr   b,inv                                  1F 96
tfr   b,inv                                  1F 97
tfr   b,inv                                  1F 9C
tfr   b,inv                                  1F 9D
tfr   b,inv                                  1F 9E
tfr   b,inv                                  1F 9F
tfr   b,pc                                   1F 95
tfr   b,s                                    1F 94
tfr   b,u                                    1F 93
tfr   b,x                                    1F 91
tfr   b,y                                    1F 92
tfr   cc,a                                   1F A8
tfr   cc,b                                   1F A9
tfr   cc,cc                                  1F AA
tfr   cc,d                                   1F A0
tfr   cc,dp                                  1F AB
tfr   cc,inv                                 1F A6
tfr   cc,inv                                 1F A7
tfr   cc,inv                                 1F AC
tfr   cc,inv                                 1F AD
tfr   cc,inv                                 1F AE
tfr   cc,inv                                 1F AF
tfr   cc,pc                                  1F A5
tfr   cc,s                                   1F A4
tfr   cc,u                                   1F A3
tfr   cc,x                                   1F A1
tfr   cc,y                                   1F A2
tfr   d,a                                    1F 08
tfr   d,b                                    1F 09
tfr   d,cc                                   1F 0A
tfr   d,d                                    1F 00
tfr   d,dp                                   1F 0B
tfr   d,inv                                  1F 06
tfr   d,inv                                  1F 07
tfr   d,inv                                  1F 0C
tfr   d,inv                                  1F 0D
tfr   d,inv                                  1F 0E
tfr   d,inv                                  1F 0F
tfr   d,pc                                   1F 05
tfr   d,s                                    1F 04
tfr   d,u                                    1F 03
tfr   d,x                                    1F 01
tfr   d,y                                    1F 02
tfr   dp,a                                   1F B8
tfr   dp,b                                   1F B9
tfr   dp,cc                                  1F BA
tfr   dp,d                                   1F B0
tfr   dp,dp                                  1F BB
tfr   dp,inv                                 1F B6
tfr   dp,inv                                 1F B7
tfr   dp,inv                                 1F BC
tfr   dp,inv                                 1F BD
tfr   dp,inv                                 1F BE
tfr   dp,inv                                 1F BF
tfr   dp,pc                                  1F B5
tfr   dp,s                                   1F B4
tfr   dp,u                                   1F B3
tfr   dp,x                                   1F B1
tfr   dp,y                                   1F B2
tfr   inv,a                                  1F 68
tfr   inv,a                                  1F 78
tfr   inv,a                                  1F C8
tfr   inv,a                                  1F D8
tfr   inv,a                                  1F E8
tfr   inv,a                                  1F F8
tfr   inv,b                                  1F 69
tfr   inv,b                                  1F 79
tfr   inv,b                                  1F C9
tfr   inv,b                                  1F D9
tfr   inv,b                                  1F E9
tfr   inv,b                                  1F F9
tfr   inv,cc                                 1F 6A
tfr   inv,cc                                 1F 7A
tfr   inv,cc                                 1F CA
tfr   inv,cc                                 1F DA
tfr   inv,cc                                 1F EA
tfr   inv,cc                                 1F FA
tfr   inv,d                                  1F 60
tfr   inv,d                                  1F 70
tfr   inv,d                                  1F C0
tfr   inv,d                                  1F D0
tfr   inv,d                                  1F E0
tfr   inv,d                                  1F F0
tfr   inv,dp                                 1F 6B
tfr   inv,dp                                 1F 7B
tfr   inv,dp                                 1F CB
tfr   inv,dp                                 1F DB
tfr   inv,dp                                 1F EB
tfr   inv,dp                                 1F FB
tfr   inv,inv                                1F 66
tfr   inv,inv                                1F 67
tfr   inv,inv                                1F 6C
tfr   inv,inv                                1F 6D
tfr   inv,inv                                1F 6E
tfr   inv,inv                                1F 6F
tfr   inv,inv                                1F 76
tfr   inv,inv                                1F 77
tfr   inv,inv                                1F 7C
tfr   inv,inv                                1F 7D
tfr   inv,inv                                1F 7E
tfr   inv,inv                                1F 7F
tfr   inv,inv                                1F C6
tfr   inv,inv                                1F C7
tfr   inv,inv                                1F CC
tfr   inv,inv                                1F CD
tfr   inv,inv                                1F CE
tfr   inv,inv                                1F CF
tfr   inv,inv                                1F D6
tfr   inv,inv                                1F D7
tfr   inv,inv                                1F DC
tfr   inv,inv                                1F DD
tfr   inv,inv                                1F DE
tfr   inv,inv                                1F DF
tfr   inv,inv                                1F E6
tfr   inv,inv                                1F E7
tfr   inv,inv                                1F EC
tfr   inv,inv                                1F ED
tfr   inv,inv                                1F EE
tfr   inv,inv                                1F EF
tfr   inv,inv                                1F F6
tfr   inv,inv                                1F F7
tfr   inv,inv                                1F FC
tfr   inv,inv                                1F FD
tfr   inv,inv                                1F FE
tfr   inv,inv                                1F FF
tfr   inv,pc                                 1F 65
tfr   inv,pc                                 1F 75
tfr   inv,pc                                 1F C5
tfr   inv,pc                                 1F D5
tfr   inv,pc                                 1F E5
tfr   inv,pc                                 1F F5
tfr   inv,s                                  1F 64
tfr   inv,s                                  1F 74
tfr   inv,s                                  1F C4
tfr   inv,s                                  1F D4
tfr   inv,s                                  1F E4
tfr   inv,s                                  1F F4
tfr   inv,u                                  1F 63
tfr   inv,u                                  1F 73
tfr   inv,u                                  1F C3
tfr   inv,u                                  1F D3
tfr   inv,u                                  1F E3
tfr   inv,u                                  1F F3
tfr   inv,x                                  1F 61
tfr   inv,x                                  1F 71
tfr   inv,x                                  1F C1
tfr   inv,x                                  1F D1
tfr   inv,x                                  1F E1
tfr   inv,x                                  1F F1
tfr   inv,y                                  1F 62
tfr   inv,y                                  1F 72
tfr   inv,y                                  1F C2
tfr   inv,y                                  1F D2
tfr   inv,y                                  1F E2
tfr   inv,y                                  1F F2
tfr   pc,a                                   1F 58
tfr   pc,b                                   1F 59
tfr   pc,cc                                  1F 5A
tfr   pc,d                                   1F 50
tfr   pc,dp                                  1F 5B
tfr   pc,inv                                 1F 56
tfr   pc,inv                                 1F 57
tfr   pc,inv                                 1F 5C
tfr   pc,inv                                 1F 5D
tfr   pc,inv                                 1F 5E
tfr   pc,inv                                 1F 5F
tfr   pc,pc                                  1F 55
tfr   pc,s                                   1F 54
tfr   pc,u                                   1F 53
tfr   pc,x                                   1F 51
tfr   pc,y                                   1F 52
tfr   s,a                                    1F 48
tfr   s,b                                    1F 49
tfr   s,cc                                   1F 4A
tfr   s,d                                    1F 40
tfr   s,dp                                   1F 4B
tfr   s,inv                                  1F 46
tfr   s,inv                                  1F 47
tfr   s,inv                                  1F 4C
tfr   s,inv                                  1F 4D
tfr   s,inv                                  1F 4E
tfr   s,inv                                  1F 4F
tfr   s,pc                                   1F 45
tfr   s,s                                    1F 44
tfr   s,u                                    1F 43
tfr   s,x                                    1F 41
tfr   s,y                                    1F 42
tfr   u,a                                    1F 38
tfr   u,b                                    1F 39
tfr   u,cc                                   1F 3A
tfr   u,d                                    1F 30
tfr   u,dp                                   1F 3B
tfr   u,inv                                  1F 36
tfr   u,inv                                  1F 37
tfr   u,inv                                  1F 3C
tfr   u,inv                                  1F 3D
tfr   u,inv                                  1F 3E
tfr   u,inv                                  1F 3F
tfr   u,pc                                   1F 35
tfr   u,s                                    1F 34
tfr   u,u                                    1F 33
tfr   u,x                                    1F 31
tfr   u,y                                    1F 32
tfr   x,a                                    1F 18
tfr   x,b                                    1F 19
tfr   x,cc                                   1F 1A
tfr   x,d                                    1F 10
tfr   x,dp                                   1F 1B
tfr   x,inv                                  1F 16
tfr   x,inv                                  1F 17
tfr   x,inv                                  1F 1C
tfr   x,inv                                  1F 1D
tfr   x,inv                                  1F 1E
tfr   x,inv                                  1F 1F
tfr   x,pc                                   1F 15
tfr   x,s                                    1F 14
tfr   x,u                                    1F 13
tfr   x,x                                    1F 11
tfr   x,y                                    1F 12
tfr   y,a                                    1F 28
tfr   y,b                                    1F 29
tfr   y,cc                                   1F 2A
tfr   y,d                                    1F 20
tfr   y,dp                                   1F 2B
tfr   y,inv                                  1F 26
tfr   y,inv                                  1F 27
tfr   y,inv                                  1F 2C
tfr   y,inv                                  1F 2D
tfr   y,inv                                  1F 2E
tfr   y,inv                                  1F 2F
tfr   y,pc                                   1F 25
tfr   y,s                                    1F 24
tfr   y,u                                    1F 23
tfr   y,x                                    1F 21
tfr   y,y                                    1F 22
tst   $0,s                                   6D 60
tst   $0,u                                   6D 40
tst   $0,x                                   6D 00
tst   $0,y                                   6D 20
tst   $01,pc                                 6D 8C 01
tst   $01,pc                                 6D AC 01
tst   $01,pc                                 6D CC 01
tst   $01,pc                                 6D EC 01
tst   $01,s                                  6D E8 01
tst   $01,u                                  6D C8 01
tst   $01,x                                  6D 88 01
tst   $01,y                                  6D A8 01
tst   $1,s                                   6D 61
tst   $1,u                                   6D 41
tst   $1,x                                   6D 01
tst   $1,y                                   6D 21
tst   $2,s                                   6D 62
tst   $2,u                                   6D 42
tst   $2,x                                   6D 02
tst   $2,y                                   6D 22
tst   $3,s                                   6D 63
tst   $3,u                                   6D 43
tst   $3,x                                   6D 03
tst   $3,y                                   6D 23
tst   $4,s                                   6D 64
tst   $4,u                                   6D 44
tst   $4,x                                   6D 04
tst   $4,y                                   6D 24
tst   $5,s                                   6D 65
tst   $5,u                                   6D 45
tst   $5,x                                   6D 05
tst   $5,y                                   6D 25
tst   $6,s                                   6D 66
tst   $6,u                                   6D 46
tst   $6,x                                   6D 06
tst   $6,y                                   6D 26
tst   $7,s                                   6D 67
tst   $7,u                                   6D 47
tst   $7,x                                   6D 07
tst   $7,y                                   6D 27
tst   $8,s                                   6D 68
tst   $8,u                                   6D 48
tst   $8,x                                   6D 08
tst   $8,y                                   6D 28
tst   $9,s                                   6D 69
tst   $9,u                                   6D 49
tst   $9,x                                   6D 09
tst   $9,y                                   6D 29
tst   $a,s                                   6D 6A
tst   $a,u                                   6D 4A
tst   $a,x                                   6D 0A
tst   $a,y                                   6D 2A
tst   $b,s                                   6D 6B
tst   $b,u                                   6D 4B
tst   $b,x                                   6D 0B
tst   $b,y                                   6D 2B
tst   $beef                                  6D 8F BE EF
tst   $beef                                  6D AF BE EF
tst   $beef                                  6D CF BE EF
tst   $beef                                  6D EF BE EF
tst   $beef                                  7D BE EF
tst   $beef,pc                               6D 8D BE EF
tst   $beef,pc                               6D AD BE EF
tst   $beef,pc                               6D CD BE EF
tst   $beef,pc                               6D ED BE EF
tst   $beef,s                                6D E9 BE EF
tst   $beef,u                                6D C9 BE EF
tst   $beef,x                                6D 89 BE EF
tst   $beef,y                                6D A9 BE EF
tst   $c,s                                   6D 6C
tst   $c,u                                   6D 4C
tst   $c,x                                   6D 0C
tst   $c,y                                   6D 2C
tst   $d,s                                   6D 6D
tst   $d,u                                   6D 4D
tst   $d,x                                   6D 0D
tst   $d,y                                   6D 2D
tst   $e,s                                   6D 6E
tst   $e,u                                   6D 4E
tst   $e,x                                   6D 0E
tst   $e,y                                   6D 2E
tst   $f,s                                   6D 6F
tst   $f,u                                   6D 4F
tst   $f,x                                   6D 0F
tst   $f,y                                   6D 2F
tst   $ff                                    0D FF
tst   ,--s                                   6D E3
tst   ,--u                                   6D C3
tst   ,--x                                   6D 83
tst   ,--y                                   6D A3
tst   ,-s                                    6D E2
tst   ,-u                                    6D C2
tst   ,-x                                    6D 82
tst   ,-y                                    6D A2
tst   ,s                                     6D E4
tst   ,s+                                    6D E0
tst   ,s++                                   6D E1
tst   ,u                                     6D C4
tst   ,u+                                    6D C0
tst   ,u++                                   6D C1
tst   ,x                                     6D 84
tst   ,x+                                    6D 80
tst   ,x++                                   6D 81
tst   ,y                                     6D A4
tst   ,y+                                    6D A0
tst   ,y++                                   6D A1
tst   -$1,s                                  6D 7F
tst   -$1,u                                  6D 5F
tst   -$1,x                                  6D 1F
tst   -$1,y                                  6D 3F
tst   -$10,s                                 6D 70
tst   -$10,u                                 6D 50
tst   -$10,x                                 6D 10
tst   -$10,y                                 6D 30
tst   -$2,s                                  6D 7E
tst   -$2,u                                  6D 5E
tst   -$2,x                                  6D 1E
tst   -$2,y                                  6D 3E
tst   -$3,s                                  6D 7D
tst   -$3,u                                  6D 5D
tst   -$3,x                                  6D 1D
tst   -$3,y                                  6D 3D
tst   -$4,s                                  6D 7C
tst   -$4,u                                  6D 5C
tst   -$4,x                                  6D 1C
tst   -$4,y                                  6D 3C
tst   -$5,s                                  6D 7B
tst   -$5,u                                  6D 5B
tst   -$5,x                                  6D 1B
tst   -$5,y                                  6D 3B
tst   -$6,s                                  6D 7A
tst   -$6,u                                  6D 5A
tst   -$6,x                                  6D 1A
tst   -$6,y                                  6D 3A
tst   -$7,s                                  6D 79
tst   -$7,u                                  6D 59
tst   -$7,x                                  6D 19
tst   -$7,y                                  6D 39
tst   -$8,s                                  6D 78
tst   -$8,u                                  6D 58
tst   -$8,x                                  6D 18
tst   -$8,y                                  6D 38
tst   -$9,s                                  6D 77
tst   -$9,u                                  6D 57
tst   -$9,x                                  6D 17
tst   -$9,y                                  6D 37
tst   -$a,s                                  6D 76
tst   -$a,u                                  6D 56
tst   -$a,x                                  6D 16
tst   -$a,y                                  6D 36
tst   -$b,s                                  6D 75
tst   -$b,u                                  6D 55
tst   -$b,x                                  6D 15
tst   -$b,y                                  6D 35
tst   -$c,s                                  6D 74
tst   -$c,u                                  6D 54
tst   -$c,x                                  6D 14
tst   -$c,y                                  6D 34
tst   -$d,s                                  6D 73
tst   -$d,u                                  6D 53
tst   -$d,x                                  6D 13
tst   -$d,y                                  6D 33
tst   -$e,s                                  6D 72
tst   -$e,u                                  6D 52
tst   -$e,x                                  6D 12
tst   -$e,y                                  6D 32
tst   -$f,s                                  6D 71
tst   -$f,u                                  6D 51
tst   -$f,x                                  6D 11
tst   -$f,y                                  6D 31
tst   a,s                                    6D E6
tst   a,u                                    6D C6
tst   a,x                                    6D 86
tst   a,y                                    6D A6
tst   b,s                                    6D E5
tst   b,u                                    6D C5
tst   b,x                                    6D 85
tst   b,y                                    6D A5
tst   d,s                                    6D EB
tst   d,u                                    6D CB
tst   d,x                                    6D 8B
tst   d,y                                    6D AB
tst   [$01,pc]                               6D 9C 01
tst   [$01,pc]                               6D BC 01
tst   [$01,pc]                               6D DC 01
tst   [$01,pc]                               6D FC 01
tst   [$01,s]                                6D F8 01
tst   [$01,u]                                6D D8 01
tst   [$01,x]                                6D 98 01
tst   [$01,y]                                6D B8 01
tst   [$beef,pc]                             6D 9D BE EF
tst   [$beef,pc]                             6D BD BE EF
tst   [$beef,pc]                             6D DD BE EF
tst   [$beef,pc]                             6D FD BE EF
tst   [$beef,s]                              6D F9 BE EF
tst   [$beef,u]                              6D D9 BE EF
tst   [$beef,x]                              6D 99 BE EF
tst   [$beef,y]                              6D B9 BE EF
tst   [$beef]                                6D 9F BE EF
tst   [$beef]                                6D BF BE EF
tst   [$beef]                                6D DF BE EF
tst   [$beef]                                6D FF BE EF
tst   [,--s]                                 6D F3
tst   [,--u]                                 6D D3
tst   [,--x]                                 6D 93
tst   [,--y]                                 6D B3
tst   [,s++]                                 6D F1
tst   [,s]                                   6D F4
tst   [,u++]                                 6D D1
tst   [,u]                                   6D D4
tst   [,x++]                                 6D 91
tst   [,x]                                   6D 94
tst   [,y++]                                 6D B1
tst   [,y]                                   6D B4
tst   [a,s]                                  6D F6
tst   [a,u]                                  6D D6
tst   [a,x]                                  6D 96
tst   [a,y]                                  6D B6
tst   [b,s]                                  6D F5
tst   [b,u]                                  6D D5
tst   [b,x]                                  6D 95
tst   [b,y]                                  6D B5
tst   [d,s]                                  6D FB
tst   [d,u]                                  6D DB
tst   [d,x]                                  6D 9B
tst   [d,y]                                  6D BB
tst   []                                     6D 97
tst   []                                     6D 9A
tst   []                                     6D 9E
tst   []                                     6D B7
tst   []                                     6D BA
tst   []                                     6D BE
tst   []                                     6D D7
tst   []                                     6D DA
tst   []                                     6D DE
tst   []                                     6D F7
tst   []                                     6D FA
tst   []                                     6D FE
tsta                                         4D
tstb                                         5D
