# Projetodjango
A mini Netflix simulation - Tenta simular a netflix
class Homepage(FormView):
    # The only page available for non-logged-in users
    # It contains an email form, and if the email exists, the user logs in
    # Redirects to the 'homefilmes' page; otherwise, redirects to 'Criarconta'

class Homefilmes(LoginRequiredMixin, ListView):
    # Displays movies in various ways, like most-watched or newest
    # Available only for logged-in users

class Detalhesfilme(LoginRequiredMixin, DetailView):
    # Displays detailed information about each movie available in the movie lists
    # Users can watch the movie video and see a list of similar films
    # Available only for logged-in users

class Pesquisarfilme(LoginRequiredMixin, ListView):
    # If the movie exists, it displays the video; otherwise, returns None
    # Available only for logged-in users

class Editarpagina(LoginRequiredMixin, UpdateView):
    # Users can edit their information in fields like 'first_name', 'last_name', 'email'
    # There's another class for changing the password
    # Available only for logged-in users

class Criarconta(FormView):
    # Users can create a new account


O projeto contém as seguintes rotas:
# class Homepage(FormView):
A unica página disponível para usuários não logados ela contém formulário de email 
se o email existir ele faz login e é redirecionado para a pagina homefilmes caso contrário 
ele será redirecionado para Criarconta.

# class Homefilmes(LoginRequiredMixin, ListView):
Essa página fará a exibição dos filmes em uma forma variada de lista de filmes
como por exemplo os filmes mais assistidos e os filmes mais novos.

# class Detalhesfilme(LoginRequiredMixin, DetailView):
Vai exibir o detalhe de cada filme disponível nas listas de filmes o usuário poderá ver o video do filme
e exibirá uma lista de filmes semelhantes.

# class Pesquisarfilme(LoginRequiredMixin, ListView):
Se o filme existir ele fará a exibição do video caso o filme não exista ele retornará None.

# class Editarpagina(LoginRequiredMixin, UpdateView):
O usuário poderá editar as informações dele nos campos = 'first_name', 'last_name', 'email'
existe uma outra classe para trocar de senha.

# class Criarconta(FormView):
O usuário poderá criar uma nova conta.
