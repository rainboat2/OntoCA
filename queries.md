# Queries

## Query1

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y
WHERE
{
    ?X rdf:type ub:GraduateStudent .
    ?X ub:takesCourse ?Y .
}
```

## Query2

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y ?Z
WHERE
{
	?X rdf:type ub:Student .
	?Y rdf:type ub:GraduateCourse .
	?X ub:takesCourse ?Y .
	?X ub:name ?Z .
}
```

## Query3

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y
WHERE
{
	?X rdf:type ub:GraduateStudent .
	?X ub:takesCourse ?Y .
}
```

## Query4

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y ?Z ?A
WHERE
{
	?X ub:memberOf ?Y .
	?Y ub:subOrganizationOf ?Z .
	?A ub:advisor ?X .
}

## Query5

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y ?Z
WHERE
{
	?Y rdf:type ub:Department .
	?X ub:worksFor ?Y .
	?Y ub:subOrganizationOf ?Z .
}
```

## Query6

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y1 ?Y2 ?Y3 ?Y4
WHERE
{
	?X ub:name ?Y1 .
	?X ub:emailAddress ?Y2 .
	?X ub:telephone ?Y3 .
	?X ub:memberOf ?Y4.
}
```

## Query7

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X
WHERE
{
	?X rdf:type ub:ResearchGroup .
	?X ub:subOrganizationOf <http://www.University0.edu> .
}
```

## Query8

```SPARQL
PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX ub: <tju:#>
SELECT ?X ?Y ?Z ?A ?B
WHERE
{
    ?X rdf:type ub:GraduateStudent .
    ?X ub:takesCourse ?Z .
    ?B ub:teacherOf ?Z .
    ?X ub:memberOf ?Y .
    ?Y ub:subOrganizationOf ?A .
}
```