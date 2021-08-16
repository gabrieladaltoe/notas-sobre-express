# PRIMER VIEW #

Para visualizar uma view, é preciso passar pelo controlador qual view será renderizada ao cliente de acordo com a funcionalidade. 


~~~javascript

const controller = {
    mostrarProdutos : (req,res) => {
        res.render('produtos')
    }
}

~~~

Para isso, não é necessário passar o nome da pasta, nem a extensão do arquivo, apenas o nome do arquivo. No caso acima: "produtos"