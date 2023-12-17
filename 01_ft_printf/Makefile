# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: momrane <momrane@student.42.fr>            +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/11/17 15:35:19 by momrane           #+#    #+#              #
#    Updated: 2023/12/17 14:33:06 by momrane          ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

AR = ar rcs
CC = cc -Wall -Werror -Wextra
NAME = libftprintf.a
SRCDIR = ./src
BINDIR = ./bin
INCDIR = ./inc
HEADER = $(INCDIR)/ft_printf.h
SRCS = 	$(SRCDIR)/ft_print_integer.c $(SRCDIR)/ft_print_ptr.c \
		$(SRCDIR)/ft_print_uinteger.c $(SRCDIR)/ft_printf.c \
		$(SRCDIR)/ft_putchar.c $(SRCDIR)/ft_putnbr_hexa.c \
		$(SRCDIR)/ft_print_string.c $(SRCDIR)/ft_strchr.c 
OBJS = $(patsubst $(SRCDIR)/%.c,$(BINDIR)/%.o,$(SRCS))

all: $(NAME)

$(NAME): $(OBJS)
	$(AR) $(NAME) $^

$(BINDIR)/%.o: $(SRCDIR)/%.c $(HEADER)
	$(CC) -c $< -o $@

setup:
	mkdir -p $(SRCDIR) $(BINDIR) $(INCDIR)

clean:
	rm -rf $(OBJS)

fclean: clean
	rm -rf $(NAME)

re: fclean all

.PHONY: all clean fclean re