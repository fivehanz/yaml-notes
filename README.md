# YAML notes

## TOC
- Introduction
- Syntax
- Properties / Datatypes
- Tools

# Introduction

- YAML:- yaml ain't markup language.
- data format used to exchange data, similar to XML, JSON.
- serialization of Objects.
- human readable, strict syntax, convert to JSON. 
- ext: .yaml, .yml

# Syntax

- key value pair

```yaml
"key" : "value"
```

- lists

```yaml

- item1
- item2
- Item3

---

ListWithAName:
  - Item1
  - Item2

---
AnotherList: [Item1, Item2]
...
```

- datatypes

```yaml

name: string without qoutes
anotherName: "string with qoutes"

multipleLines: |
this is a line.
this is another line.

number: 1234
floatNumber: 34.43
boolValue: No # N, False, false, FALSE
anotherBool: Yes # y, Y, TRUE

## specific type
# int
zero: !!int 0
positiveNum: !!int 45
negativeNum: !!int -45
binaryNum: !!int 0b11001
octalNum: !!int 06574
hexaNum: !!int 0x45
commaNum: !!int +545_000

# float
floatVal: !!float 54.44
infinite: !!float .inf
notANum: .nan

exponentialNum: 6.023E56

# string
aString: !!str string

# bool
boolVal: !!bool No

# null / None
nullValue: !!null NULL # null, ~

# date and time
date: !!timestamp 2022-12-14
anotherExample: 2022-12-15-T02:59:43.10 # UTC
inAnotherTimeZone: 2022-12-15T02:59:43.10 +5:30
```

# advanced datatypes

- sequence type

```yaml

student: !!seq
  - name
  - grade
  - reg_no

# sparse sequence
sparseSeq: 
  - Item1
  - Item2
  -
  - NULL
  - 

```
- maps: key => value pairs

```yaml
!!map

```

- nested maps
```yaml
name: Name Name
role:
  age: 20
  job: Job
```

- pairs
```yaml
example: !!pairs
  - job: exampleJob1
  - job: exampleJob2

```

- sets: unique values
```yaml

names: !!set
  ? name1
  ? name2
  ? name3

```

# Tools

Datree - YAML validation checks.
Monocle by Kubeshop - largescale YAML visualization.
Lens - K8s IDE
