# 1-projeto
software para armazenar e consultar usuários


var  entrada  =  require ( 'readline-sync' )

var  nomes  =  [ ]
varidades  = [ ] _  
var  sexos  =  [ ]
var  contador  =  0
var  opcao  =  - 1


while  ( opcao  !==  0 )  {
    consola . log ( "0, 1, 2 ou 3: " )
    opcao  =  parseInt ( entrada . question ( "Opcao: " ) )
    if  ( opcao  !==  "" )  {
        if  ( opcao  ===  0 )  {
            consola . log ( "Encerrou..." )
        }  else  if  ( opcao  ===  1 )  {
            var  nome  =  entrada . pergunta ( "Nome?" )
            //...dados completos
            if  ( nome  !==  "" )  {
                nomes [ contador ]  =  nome
                contador ++
            }  senão  {
                consola . log ( "O nome é obrigatório" )
            }
        }  else  if  ( opcao  ===  2 )  {
            if  ( nomes . comprimento  >  0 )  {
                var  nomeConsulta  =  entrada . pergunta ( "Consulta: " )
                if  ( nomeConsulta  !==  "" )  {
                    var  índice  =  - 1
                    var  achou  =  false
                    for  ( var  i  =  0 ;  i  <  nomes . comprimento ;  i ++ )  {
                        if  ( nomeConsulta  ===  nomes [ i ] )  {
                            índice  =  eu
                            achou  =  verdadeiro
                        }
                    }
                    if  ( achou  ===  true )  {
                        consola . log ( nomes [ índice ] )
                    }  senão  {
                        consola . log ( "Usuário não encontrado" )
                    }
                }  senão  {
                    consola . log ( "Informe um nome para consulta" )
                }
            }  senão  {
                consola . log ( "Nao ha usuarios" )
            }
        }  else  if  ( opcao  ===  3 )  {
            if  ( nomes . comprimento  >  0 )  {
                for  ( var  i  =  0 ;  i  <  nomes . comprimento ;  i ++ )  {
                    consola . log ( nomes [ i ] )
                }
            }  senão  {
                consola . log ( "Não há usuários cadastrados" )
            }
        }  senão  {
            consola . log ( "opcao invalida..." )
        }
    }  senão  {
        consola . log ( "A opcao nao pode ser vazia..." )
    }
}
