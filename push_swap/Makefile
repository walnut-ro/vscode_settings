NAME = push_swap
CC = cc -g
RM = rm -f
FLAGS = -Wall -Wextra -Werror
LIBFTDIR = libft/
OBJ_DIR = obj/

SRC_1 = srcs/push_swap.c

SRC_2 =	srcs/ft_print_list.c \
		srcs/ft_stackadd_back.c \
		srcs/ft_stacklast.c \
		srcs/ft_stacknew.c \

OBJ_1 = ${SRC_1:.c=.o}
OBJ_2 = ${SRC_2:.c=.o}

INCLUDE = -L ./libft -lft

.c.o:
	${CC} -c $< -o ${<:.c=.o}

${NAME}: ${OBJ_1} ${OBJ_2}
	make -C $(LIBFTDIR)
	${CC} ${FLAGS} ${OBJ_1} ${OBJ_2} -o ${NAME} ${INCLUDE}

all: ${NAME}

clean:
	${RM} ${OBJ_1} ${OBJ_2} ${NAME}
	@cd $(LIBFTDIR) && $(MAKE) clean

fclean: clean
	${RM} ${NAME}
	@cd $(LIBFTDIR) && $(MAKE) fclean

re: clean all

.PHONY: all clean fclean re
