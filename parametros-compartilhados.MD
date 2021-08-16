# Parametros compartilhados #

Nos templates engines podemos passar dados dinamicos de um controlador para uma view.

~~~javascript

const controller = {
    mostrarProdutos : (req,res) => {
        res.render('produtos', {listadepessoas: pessoas})
    }
}

~~~

Dessa forma, na view.ejs, poderemos realizar um loop utilizando listadepessoas de forma dinâmica. 


Quando passamos um dado como a variável info abaixo, não é necessário chama-la na view como info.cursos, mas apenas cursos. 

~~~javascript

const HomeController = {
    index: (req,res) => {

        let info = {
            cursos: ['Full Stack', 'Android', 'React']
        }


        return res.render('index', info);
    }
}

module.exports = HomeController

~~~