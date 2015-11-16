# Teste remoto Sage One

 // Criar a aplicação
 
 mkdir projects 
 cd projects
 rails new railsmichele
 cd railsmichele
 rails s
 
 //Criar CRUD/Incluir/Excluir/Alterar dados
  
 $>rails new tabela_produto -d=SQlite
 $>cd tabela_produto/
 $>rails generate scaffold Produto categoria:string unidade:string descricao:string identificacao:string custo:decimal precodevenda1:decimal observacoes:string fornecedor:string estoque:string cod.barra:float precodevenda2:decimal precodevenda3:decimal estoqueminimo:float estoquemaximo:float estoquecompra:float fatorunidevenda:float NCM:float marca:string peso:decimal tamanho:decimal inativo:string tipo:string composicao:string materiaprima:string materialexpediente:string paravenda:string moeda:decimal
 $>rake db:create:all
 $>rake db:migrate
 $>rails new tabela_cliente -d=SQlite
 $>cd tabela_cliente/
 $>rails generate scaffold Cliente nome:string telefone:float cnpj:float endereço:string numero:integer email:string
 $>rake db:create:all
 $>rake db:migrate
 $ rails server

   // Importar (Upload) arquivo CSV
   
    /Gemfile
	gem install carrierwave
      gem 'carrierwave'
	 ./script/generate uploader cliente
	 add_column :user, :cliente, :string
	 class User
     mount_uploader :cliente, ProdutoUploader
	 
	 User.create(params[:user]) 
     rails generate controller files
	 
   $ rails g uploader file_csv
   $ rails g uploader file_txt
   
   // 
 
