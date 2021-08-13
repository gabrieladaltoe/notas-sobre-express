*** Controllers ***

Faz a comunicação entre Modelos e Visualizações através de rotas específicas.

~~~javascript

const controlador = {
    index: (req,res) => {
        res.send("index do produto");
    },
    criarProduto: (req,res) => {
        res.send("Criando um produto") 
    },
    deletarProduto: (req,res) => {
        const{id}= req.params;
        res.send('Deletando o produto com id: ' + id)
    }
};

module.exports = controlador

~~~

Cada funcionalidade terá um Controller próprio para assim evitarmos conflitos. O Controller é chamado no arquivo de rotas. 


~~~javascript

const controladorController = require('./controllers/controlador')

router.get('/criar', controladorController.criarProduto)
router.get('/deletar', controladorController.deletarProduto)


~~~


Dessa forma, acessando o localhost/criar, acessaremos o retorno deste método. 


