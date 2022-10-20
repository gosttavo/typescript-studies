//classes -> representações de objetos do mundo real 
//podem ter atributos e métodos
//define o que vai ter e como se comportar

//declaração de classe
class Spacecraft{
    //atributo da classe
    propulsor: string;

    //construtor -> utilizado para inicializar objetos criados     
    constructor (propulsor: string){
        //atributo que armazena o parâmetro
        //para acessar o atributo da classe é usado o "this"
        this.propulsor = propulsor;
    }

    //método -> ação
    jumpIntoHyperspace(){
        console.log('Entering hyperspace with ' + this.propulsor);
    } 
}

//criar objeto através da classe -> operador new
let falcon = new Spacecraft('falcon');

//falcon entrando no método
falcon.jumpIntoHyperspace();

//forma reduzida de escrever o código anterior
class Spaceship{
    //atributo público -> acessível diretamente por vários objetos
    constructor(public nave: string){}
}

//herança -> EXTENDS -> consigo herdar as características
class MilleniumFalcon extends Spacecraft{
    constructor(){
        //super -> invocar implementação da classe original
        super('hiperdrive');
    }

    jumpIntoHyperspace() {
        if(Math.random()>=0.5){
            super.jumpIntoHyperspace();
        } else{
            console.log('failed');
        }
    }
}
