# my-library-libft

*This project created by `<mohalaou>`.*

# Libft

## Description

Libft is the first project of the 42 curriculum. The goal is to build your own C library by re-implementing a set of functions from the C standard library, along with additional utility functions that will be reused in every future project.

The project helps you understand how these functions work internally, practice memory management and pointer manipulation, and learn how to build and maintain a static library.

The result is a static library, `libft.a`, written in C and compiled with `-Wall -Wextra -Werror`.

## Instructions

### Requirements

- A C compiler (`cc` or `gcc`)
- `make`

### Compilation

```bash
# Build the library
make

# Build the library with the bonus functions
make bonus

# Remove object files
make clean

# Remove object files and libft.a
make fclean

# Rebuild everything
make re
```

### Usage

Include the header in your code:

```c
#include "libft.h"
```

Then compile your program with the library:

```bash
cc -Wall -Wextra -Werror main.c -L. -lft -o program
```

## Functions

### Part 1 — Libc functions

| Category | Functions |
|----------|-----------|
| Character checks | `ft_isalpha`, `ft_isdigit`, `ft_isalnum`, `ft_isascii`, `ft_isprint` |
| Character conversion | `ft_toupper`, `ft_tolower` |
| String | `ft_strlen`, `ft_strlcpy`, `ft_strlcat`, `ft_strchr`, `ft_strrchr`, `ft_strncmp`, `ft_strnstr`, `ft_strdup` |
| Memory | `ft_memset`, `ft_bzero`, `ft_memcpy`, `ft_memmove`, `ft_memchr`, `ft_memcmp`, `ft_calloc` |
| Conversion | `ft_atoi` |

### Part 2 — Additional functions

| Function | Description |
|----------|-------------|
| `ft_substr` | Extracts a substring from a string |
| `ft_strjoin` | Concatenates two strings into a new one |
| `ft_strtrim` | Trims a set of characters from both ends of a string |
| `ft_split` | Splits a string using a delimiter character |
| `ft_itoa` | Converts an integer to a string |
| `ft_strmapi` | Applies a function to each character, returning a new string |
| `ft_striteri` | Applies a function to each character, using its index |
| `ft_putchar_fd` | Writes a character to a file descriptor |
| `ft_putstr_fd` | Writes a string to a file descriptor |
| `ft_putendl_fd` | Writes a string followed by a newline to a file descriptor |
| `ft_putnbr_fd` | Writes an integer to a file descriptor |

### Bonus — Linked lists

Uses the following structure:

```c
typedef struct s_list
{
    void            *content;
    struct s_list   *next;
}   t_list;
```

| Function | Description |
|----------|-------------|
| `ft_lstnew` | Creates a new node |
| `ft_lstadd_front` | Adds a node at the beginning of the list |
| `ft_lstsize` | Counts the nodes in the list |
| `ft_lstlast` | Returns the last node |
| `ft_lstadd_back` | Adds a node at the end of the list |
| `ft_lstdelone` | Deletes one node using a given function |
| `ft_lstclear` | Deletes and frees a node and all that follow |
| `ft_lstiter` | Applies a function to the content of each node |
| `ft_lstmap` | Creates a new list by applying a function to each node |

## Project Structure

```
.
├── Makefile
├── libft.h
├── ft_*.c
└── ft_lst*_bonus.c
```

## Resources

- [Linux man pages](https://man7.org/linux/man-pages/)
- [GNU C Library documentation](https://www.gnu.org/software/libc/manual/)
- [GNU Make manual](https://www.gnu.org/software/make/manual/)
- *The C Programming Language* — Brian W. Kernighan & Dennis M. Ritchie
