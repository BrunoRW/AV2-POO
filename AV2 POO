// 1 a 3 

class Ninja {
    #ninja;
    #shurikens;
    #inimigo;

    constructor(){
        this.#ninja = "joao";
        this.#shurikens = 10;
        this.#inimigo = {
            nome: "Enemy",
            vivo: true
        };
    }

    // MENSAGEM 

    #msg(e) {
        console.log(e)
    }

    // matar inimigo 

    #matar() {
        this.#shurikens -= 1;
        if(this.#inimigo.vivo){
            this.#inimigo.vivo = false;
            this.#msg("Matou o inimigo");
            return;
        } 
        this.#msg("Inimigo já não está vivo");
    }

    atirarShuriken() {
        this.#shurikens > 0 ? this.#matar() : this.#msg("Acabou as shurikens :(");
        this.#msg(this.#shurikens)
    }

    
}

let x = new Ninja();

x.atirarShuriken()

// 4
// VERIFICAR INTANCIA 

function instancia(){
    (x instanceof Object) ? console.log("É instância de objeto") : console.log("Não é instância")
}

instancia()


// 5

let g = "asd";
let h = 'uhfg'
const obj = {g, h}

console.log(obj)


// 6

const caminhao = {
    marca: "mercedes",
    altura: 3.5
}

let {marca, altura} = caminhao;

console.log(marca, altura)

// 7 

class Conta {
    #id;
    #saldo;
    #nome;

    constructor(){
        this.#id = 0;
        this.#nome = "";
        this.#saldo = 0;
    }

    mostrarConta(){
        console.log(`\nID: ${this.#id}, SALDO: R$${this.#saldo}, NOME: ${this.#nome}\n`);
    }

    criarConta(nome, deposito){
        if(this.#id == 0 && nome){
            this.#id = Math.floor(Math.random() * 100 + 1);
            this.#nome = nome;
            if(deposito){
                this.#saldo = deposito;
            }
            this.mostrarConta();
            return;
        } 
        this.#id == 0 ? console.log("Coloque um nome para começar") : console.log("Conta ja criada")
    }

    alterarNome(newName){
        if(newName){
            let k = this.#nome;
            this.#nome = newName;
            console.log(`ALterado ${k} -> ${this.#nome}`)
            this.mostrarConta()
            return;
        }
        console.log("Erro ao alterar")
    }

    sacar(val){
        if(this.#saldo > val + 5 && val && val != 0){
            this.#saldo -= val + 5;
            console.log(`Valor de saque R$${val} + taxa R$5`)
            this.mostrarConta();
            return;
        }
        console.log(`Saldo insuficiente ou valor de saque não informado\n`)
    }

    depositar(val){
        if(val && val != 0){
            this.#saldo += val;
            console.log(`Valor de depósito R$${val}`)
            this.mostrarConta();
            return;
        }
        console.log(`Valor de depósito não informado`);
    }
}

let y = new Conta();

y.criarConta("Joao")

y.alterarNome("Carlos")

y.sacar(50);

y.depositar(100);

y.sacar(100);

y.sacar(50)
