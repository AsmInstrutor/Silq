# Silq Quantum Programming

_Silq é uma nova linguagem de programação de alto nível para computação quântica com um sistema de tipo estático forte, desenvolvida na ETH Zürich. Silq foi publicada originalmente na PLDI'20._


___Visão geral dos conceitos chaves:___
 
 - Fundo: Assumimos um conhecimento básico em computação quântica. Concretamente, o leitor deve estar familiarizado com os seguintes assuntos:
   - Super Posições
   - Algoritmo de Grover
   - Teorema de Bohr

___Recursos básicos:___

__Atribuição de variável__

_O fragmento a seguir aplica a transformação Hadamart ___H___ a um Qubit ___X___ e atribui o nome ___Y___ ao resultado:_

y:=H(x);

_Compilar este Snippet para um circuito produz:_

X [H] y

_Aqui, nomeamos o fio ___H___ como ___X___ e o fio resultante como ___Y___. Um possível estado antes de aplicar ___H___ é o ___|0>x___, onde subscrito ___X___ indica que a variável ___X___ é armazenada ___0___. A linha ___Y:=H(X)___ resultaria então em estado 1/√2.π(|0>y+|1>y)_

_Para enfatizar o resultado de ___H___ ainda se refere ao mesmo Qubit ___X___, podemos escrever:_

X:=H(X);

_Essa linha consome o original ___X___, mas nomeia a saída ___X___ novamente._
