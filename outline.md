<style>
body {
    counter-reset: h1
}

h1 {
    font-size: 1.5rem !important;
    counter-reset: h2
}

h2 {
    font-size: 1.25rem !important;
    counter-reset: h3
}

h3 {
    font-size: 1.0rem !important;
    counter-reset: h4
}

h4 {
  font-size: 1.0rem !important;
  font-weight: normal !important;
}

h1:before {
    counter-increment: h1;
    content: counter(h1) ". "
}

h2:before {
    counter-increment: h2;
    content: counter(h1) "." counter(h2) ". "
}

h3:before {
    counter-increment: h3;
    content: counter(h1) "." counter(h2) "." counter(h3) ". "
}

h4:before {
    counter-increment: h4;
    content: counter(h1) "." counter(h2) "." counter(h3) "." counter(h4) ". "
}
</style>

# Motivation

### Problem Statement

### Purpose of Study

### Research Questions

### Limitations


# Fundamentals
## Methodology

## CouchEdit

## ModelSyntax
### Petrinets

### Statecharts


# Related Workd
## Fondement & Baar

## ...




# Design Concept


## Abstraction
- Graph traversal
- hiding services through extension functions
- parser configures processor requirements


## Syntax Processing
- Fondement & Baar
### Recognition

### Syncing

#### Abstract processor


## Kinds

## plugins


# Prototype


# Evaluation


# Conclustion




