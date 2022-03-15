#Library
NAME = 				libft.a

#Compiler 
CC = 				gcc

#Flags
CFLAGS = 			-Wall -Wextra -Werror

#Headers
HEA_PATH = 			.
HEA_NAME = 			libft.h
HEA =				${addprefix ${HEA_PATH}/,${HEA_NAME}}


#Sources
SRC_NAME = 			ft_atoi.c ft_bzero.c ft_calloc.c ft_isalnum.c ft_isalpha.c ft_isascii.c ft_isdigit.c ft_isprint.c ft_itoa.c ft_lstadd_back.c\
					ft_lstadd_front.c ft_lstclear.c ft_lstdelone.c ft_lstiter.c ft_lstlast.c ft_lstmap.c ft_lstnew.c ft_lstsize.c ft_memccpy.c\
					ft_memchr.c ft_memcmp.c ft_memcpy.c ft_memmove.c ft_memset.c ft_putchar_fd.c ft_putendl_fd.c ft_putnbr_fd.c\
					ft_putstr_fd.c ft_split.c ft_strchr.c ft_strdup.c ft_strjoin.c ft_strlcat.c ft_strlcpy.c ft_strlen.c ft_strmapi.c\
					ft_strncmp.c ft_strnstr.c ft_strrchr.c ft_strtrim.c ft_substr.c ft_tolower.c ft_toupper.c

#Bonus
BONUS_NAME = 		ft_atoi.c ft_bzero.c ft_calloc.c ft_isalnum.c ft_isalpha.c ft_isascii.c ft_isdigit.c ft_isprint.c ft_itoa.c ft_lstadd_back.c\
					ft_lstadd_front.c ft_lstclear.c ft_lstdelone.c ft_lstiter.c ft_lstlast.c ft_lstmap.c ft_lstnew.c ft_lstsize.c ft_memccpy.c\
					ft_memchr.c ft_memcmp.c ft_memcpy.c ft_memmove.c ft_memset.c ft_putchar_fd.c ft_putendl_fd.c ft_putnbr_fd.c\
					ft_putstr_fd.c ft_split.c ft_strchr.c ft_strdup.c ft_strjoin.c ft_strlcat.c ft_strlcpy.c ft_strlen.c ft_strmapi.c\
					ft_strncmp.c ft_strnstr.c ft_strrchr.c ft_strtrim.c ft_substr.c ft_tolower.c ft_toupper.c\
					get_next_line.c

#Objects
OBJ_PATH = 			.
OBJ_NAME = 			${SRC_NAME:.c=.o}
OBJ_BONUS_NAME =	${BONUS_NAME:.c=.o}
OBJ = 				${addprefix ${OBJ_PATH}/,${OBJ_NAME}}
OBJ_BONUS =			${addprefix ${OBJ_PATH}/,${OBJ_BONUS_NAME}}

${NAME}: 			${OBJ} ${HEA}
					@ar rc ${NAME} ${OBJ}

%.o: 				%.c ${HEA}
					${CC} ${CFLAGS} -c $< -o $@


all: 				${NAME}

bonus:				${OBJ} ${OBJ_BONUS}
					@ar rc ${NAME} ${OBJ} ${OBJ_BONUS}

clean:
					@rm -rf ${OBJ} ${OBJ_BONUS}

fclean: 			clean
					@rm -rf ${NAME} 

re: 				fclean all

.PHONY: 			all clean fclean re bonus