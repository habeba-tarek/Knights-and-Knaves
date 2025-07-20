# Knights-and-Knaves
This project implements a logic-based solver for the classic "Knights and Knaves" puzzles, where knights always tell the truth and knaves always lie. 
Project Description: Knights and Knaves Logic Puzzle Solver
Overview
This project implements a logic-based solver for the classic "Knights and Knaves" puzzles, where knights always tell the truth and knaves always lie. The solver uses propositional logic to model and solve a series of puzzles involving characters (A, B, C) who make statements about their identities as knights or knaves. The system determines which characters are knights or knaves based on their statements and logical consistency.
Files

logic.py: Defines the core logic engine with classes for logical sentences (Symbol, Not, And, Or, Implication, Biconditional) and a model-checking algorithm to evaluate whether a knowledge base entails a query. It supports constructing and evaluating complex logical expressions with proper handling of parentheses and symbols.
puzzle.py: Implements four specific Knights and Knaves puzzles using the logic engine. Each puzzle is represented as a knowledge base of logical sentences based on character statements and the rules that each character is either a knight or a knave (but not both). The main function checks which symbols (e.g., "A is a Knight") are entailed by the knowledge base and outputs the results.

Functionality

Logic Engine (logic.py):
Supports propositional logic operations: negation (Not), conjunction (And), disjunction (Or), implication (Implication), and biconditional (Biconditional).
Provides methods to evaluate logical sentences given a model (truth assignments) and extract symbols used in expressions.
Includes a model_check function to determine if a knowledge base entails a query by exhaustively checking all possible models.


Puzzle Solver (puzzle.py):
Defines symbols for each character's knight or knave status (e.g., AKnight, AKnave).
Models four puzzles (Puzzle 0 to Puzzle 3) with increasing complexity, encoding character statements as logical sentences.
Puzzle 0: A single character's self-referential statement.
Puzzle 1: A's statement about both being knaves, with B silent.
Puzzle 2: A and B make conflicting statements about their types.
Puzzle 3: Involves three characters (A, B, C) with interconnected statements.
Outputs the entailed truths for each puzzle (e.g., which characters are knights or knaves).



Usage

Run puzzle.py to execute the solver for all four puzzles.
The program prints each puzzle's name and the symbols (e.g., "A is a Knight") that are logically entailed by the knowledge base.
Requirements: Python 3.x with the itertools library (standard library, no external dependencies).

Purpose
The project demonstrates the application of propositional logic to solve constraint-based puzzles. It showcases how logical sentences can be programmatically constructed, evaluated, and used to deduce consistent truths in a reasoning system.
