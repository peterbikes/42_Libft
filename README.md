# libft

*C programming can be very tedious when one doesn’t have access to the highly useful
standard functions. This project is about understanding the way these functions work,
implementing and learning to use them. You will create your own library. It will be
helpful since you will use it in your next C school assignments.*

In this project, students were challenged to recreate a set of functions that already exist within the Standard C Library, among some custom ones.

## libft functions

`LIBC functions:`

|                |                |                |                |               |
|----------------|----------------|----------------|----------------|---------------|
| **ft_isalpha** | **ft_strlen**  | **ft_strlcpy** | **ft_strrchr** | **ft_atoi**   |
| **ft_isdigit** | **ft_memset**  | **ft_strlcat** | **ft_strncmp** | **ft_calloc** |
| **ft_isalnum** | **ft_bzero**   | **ft_toupper** | **ft_memchr**  | **ft_strdup** |
| **ft_isascii** | **ft_memcpy**  | **ft_tolower** | **ft_memcmp**  |               |
| **ft_isprint** | **ft_memmove** | **ft_strchr**  | **ft_strnstr** |               |


`Custom functions:`

<details>
<summary> ft_substr </summary>

char *ft_substr(char const *s, unsigned int start,
size_t len);

Allocates with malloc and returns a substring
from the string ’s’.
The substring begins at index ’start’ and is of
maximum size ’len’.

</details>
<br>

<details>
<summary> ft_strjoin </summary>

char *ft_strjoin(char const *s1, char const *s2);

Allocates with malloc and returns a new
string, which is the result of the concatenation
of ’s1’ and ’s2’.

</details>
<br>

<details>
<summary> ft_strtrim </summary>

char *ft_strtrim(char const *s1, char const *set);

Allocates malloc and returns a copy of
’s1’ with the characters specified in ’set’ removed
from the beginning and the end of the string.

</details>
<br>

<details>
<summary> ft_split </summary>

char **ft_split(char const *s, char c);

Allocates malloc and returns an array
of strings obtained by splitting ’s’ using the
character ’c’ as a delimiter. The array must end
with a NULL pointer.

</details>
<br>

<details>
<summary> ft_itoa </summary>

char *ft_itoa(int n);

Allocates malloc and returns a string
representing the integer received as an argument.
Negative numbers must be handled.

</details>
<br>

<details>
<summary> ft_strmapi </summary>

char *ft_strmapi(char const *s, char (*f)(unsigned
int, char));

Applies the function ’f’ to each character of the
string ’s’, and passing its index as first argument
to create a new string (with malloc(3)) resulting
from successive applications of ’f’.

</details>
<br>

<details>
<summary> ft_striteri </summary>

void ft_striteri(char *s, void (*f)(unsigned int, char*));

Applies the function ’f’ on each character of
the string passed as argument, passing its index
as first argument. Each character is passed by
address to ’f’ to be modified if necessary.

</details>
<br>

<details>
<summary> ft_putchar_fd </summary>

void ft_putchar_fd(char c, int fd);

Outputs the character ’c’ to the given file
descriptor.

</details>
<br>

<details>
<summary> ft_putstr_fd </summary>

void ft_putstr_fd(char *s, int fd);

Outputs the string ’s’ to the given file
descriptor.

</details>
<br>

<details>
<summary> ft_putendl_fd </summary>

void ft_putendl_fd(char *s, int fd);

Outputs the string ’s’ to the given file descriptor
followed by a newline.

</details>
<br>

<details>
<summary> ft_putnbr_fd </summary>

void ft_putnbr_fd(int n, int fd);

Outputs the integer ’n’ to the given file
descriptor.

</details>
<br>

`Custom functions - List manipulation:`

<details>
<summary> ft_lstnew </summary>

t_list *ft_lstnew(void *content);

Allocates (with malloc(3)) and returns a new node.
The member variable ’content’ is initialized with
the value of the parameter ’content’. The variable
’next’ is initialized to NULL.

</details>
<br>

<details>
<summary> ft_lstadd_front </summary>

void ft_lstadd_front(t_list **lst, t_list *new);

Adds the node ’new’ at the beginning of the list.

</details>
<br>

<details>
<summary> ft_lstsize </summary>

int ft_lstsize(t_list *lst);

Counts the number of nodes in a list.

</details>
<br>

<details>
<summary> ft_lstlast </summary>

t_list *ft_lstlast(t_list *lst);

Returns the last node of the list.

</details>
<br>

<details>
<summary> ft_lstadd_back </summary>

void ft_lstadd_back(t_list **lst, t_list *new);

Adds the node ’new’ at the end of the list.

</details>
<br>

<details>
<summary> ft_lstdelone </summary>

void ft_lstdelone(t_list *lst, void (*del)(void*));

Takes as a parameter a node and frees the memory of
the node’s content using the function ’del’ given
as a parameter and free the node. The memory of
’next’ must not be freed.

</details>
<br>

<details>
<summary> ft_lstclear </summary>

void ft_lstclear(t_list **lst, void (*del)(void*));

Deletes and frees the given node and every
successor of that node, using the function ’del’
and free(3).
Finally, the pointer to the list must be set to
NULL.

</details>
<br>

<details>
<summary> ft_lstiter </summary>

void ft_lstiter(t_list *lst, void (*f)(void *));

Iterates the list ’lst’ and applies the function
’f’ on the content of each node.

</details>
<br>

<details>
<summary> ft_lstmap </summary>

t_list *ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));

Iterates the list ’lst’ and applies the function
’f’ on the content of each node. Creates a new
list resulting of the successive applications of
the function ’f’. The ’del’ function is used to
delete the content of a node if needed.

</details>
<br>

--------
LinkedIn: https://www.linkedin.com/in/pedrosmpm