# Guessing.md

# Guessing Game – Flowchart

This version of the guessing game includes:
- A random number between 1–100
- Exit option by typing `'exit'`
- A maximum of 5 attempts before the game ends

```mermaid
flowchart TD
    Start([Start])
    A[Generate random number 1–100]
    B[Set attempts = 0]
    C[Prompt user: Enter number or 'exit']
    D{Input is 'exit'?}
    E[End game early]
    F{Is input valid number?}
    G[Display: Invalid input]
    H[attempts += 1]
    I{Attempts >= 5?}
    J[Display: Out of attempts. Reveal number.]
    K{Is guess = number?}
    L[Display: Correct!]
    M{Play again?}
    N[Generate new number and reset attempts]
    End([End])

    Start --> A --> B --> C
    C --> D
    D -- Yes --> E --> End
    D -- No --> F
    F -- No --> G --> C
    F -- Yes --> H --> I
    I -- Yes --> J --> M
    I -- No --> K
    K -- Yes --> L --> M
    K -- No --> C
    M -- Yes --> N --> B
    M -- No --> End
```

---

# Description of Flow

- **Start**: The game initializes.
- **A & B**: Random number is generated; attempts counter set to 0.
- **C**: The user is prompted to guess or exit.
- **D**: If they type “exit”, game ends immediately.
- **F**: Validates the input.
- **H**: Increments attempts.
- **I**: If attempts ≥ 5, user loses.
- **K**: If guess is correct, show success message.
- **M**: User chooses whether to play again.

---
