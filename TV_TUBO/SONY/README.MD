
## 1-Porque e tão difícil consertar as fontes Sony?

Bem as fontes dos tvs Sony são difíceis de consertar porque os técnicos utilizão o conceito errado. as fontes Sony NÃO SÃO FONTES CHAVEADAS, são na verdade INVERSORES DE ALTA POTENCIA isto é são osciladores sonoidais ( do tipo LC) de alta potencia.


## 2- Porque troco os transistores o resistor da fonte e fica esquentando muito e queima tudo denovo?

Primeiro o resistor da fonte (aquele branquinho) não e um simples resistor e um fusistor e tem que ser original jamais coloque de fio, pois um resistor de fio é um indutor e alteraria a freqüência de trabalho de fonte queimando tudo de novo.

Os transistores 2SC4834 e 2SC4056 NÃO POSUEM EQUIVALENTES tem que serem originais, pois foram projetados especificamente para as fontes Sony ( já viu um destes em um outro aparelho de outra marca?)e um não serve no lugar do outro, para ter uma idéia de como são especiais chega haver mais de um tipo, por exemplo, o KV 140 MG utiliza o 2SC4834EMNP código Sony 87-290-39-09 já o KP41T15(telão)utiliza o
2SC4834MNP com o código Sony 87-290-19-49 aparentemente iguais porem diferentes e um não da no lugar do outro.

Outros componentes importantes são, os capacitores de base dos transistores (aqueles azulzinhos) observe que eles são no Maximo para 100V e se você seguir a trilha da base dos transistores (ou pelo esquema o que e raro quem tenha ) Vera que vai num terminal do capacitor e o outro terminal do capacitor naquele trafo pequenininho que vai para terra. então temos um capacitor em serie com a base e o trafo para terra.Normalmente o aparelho chega para o técnico com os transistores em curto total isto quer dizer que a tensão do coletor que e 300V(do circuito de retificação primaria) foi aplicado momentaneamente a base e ao capacitor que e de 100V ai eu pergunto será que ele se alterou? E lógico que sim e é a principal causa de queima dos transistores.

Concluindo: quando o tv chega com os transistores queimados devemos trocar os transistores e o resistor por originais,trocar os capacitores de base por novos .quanto aos transistores devem ser comprados no serviço autorizado Sony,pois o do comercio comum não são originais,não caiam na conversa do vendedor a Sony não fornece estes componentes se não for autorizado.

## 3-porque os tvs Sony ficam sem imagem?

Os televisores Sony possuem um controle automático de temperatura de cor que funciona monitorando a corrente dos catodos R G B do cinescópio (ou tubo para muitos). Se algum dos catodos estiverem com desgaste a imagem não será liberada, pois o circuito não consegue balancear os catodos.Este circuito e chamado de Ik e funciona da seguinte forma:

Quando o tv é ligado o ic de vídeo (CXA1877 por exemplo) libera um trem de pulsos de períodos diferentes na linha de RGB e monitora o retorno destes pulsos no pino IK ajustando internamente o ganho dos sinais RGB e desta maneira balanciando os catodos. Se algum dos catodos estiverer mais fracos o circuito não conseguirá ajustar o RGB no mesmo nível e consequentemnte não liberara a imagem. Quando o tv não libera imagem deve-se fazer o seguinte:

Na placa de saída de video no conector onde tem marcado R G B IK coloque um resistor de um k (1k) em cada pino de RGB e as outras extremidades dos resistores no pino IK deste modo estaremos desviando os trens de pulsos diretamente para IK e com mesmo nível então a tv ira liberar a imagem e o técnico pode fazer os testes necessários para solucionar o problema (se não for o cinescópio!).

* O artifício descrito acima e somente para teste e após resolvido o defeito o mesmo deve ser removido.

## 4-Porque os tvs Sony KV1450/2170/2172s2173s ficam sem som?

O que causa este defeito e que devido a um mau dimensionamento de componentes, o micro acaba recebendo no seu pino de MUTE uma tensão muito alta o que acaba danificando o IC e o MUTE fica permanentemente ativado.

Par solucionar este defeito deve-se trocar o micro e colocar no lugar do jumper JW110 um diodo zener de 12V com anodo voltado para o R040 isto evitará a queima do IC novamente. Outra opção é simplesmente somente retirar o JW110 porem o tv fica sem MUTE com a estação fora do ar.

## dicas e macetes:

### Tv com fonte pifada:

As fontes Sony utilizam em geral dois trafos um grande que chama PIT e um pequeno que chama DTC.
O PIT e como se fosse o chooper e o pequeno é responsável pelo oscilador da fonte.
Quando os transistores estão em curto devemos fazer como já foi escrito antes e verificar também se os trafos PIT e DTC não estão com o seu núcleo de ferrite trincado ou solto caso contrario ira queimar tudo de novo.

Macete: quando a fonte utilizar STR ligue o tv em 220Ve verifique ainda com os transistores em curto a tensão encima do fusistor ,se houver mais que 275V indica que o dobrador esta ativado o que não deveria acontecer ,fique atento a isto principalmente no KV2959. próximo ao STR tem um capacitor eletrolítico de baixo valor e alta tensão (400V) cuja a tensão encima dele serve de referencia para o dobrador ser ativado ou não portanto substitua-o neste caso.


### Fonte queima quando liga na tomada:

Subistituir um capacito eletrolítico geralmente de 10uf próximo ao DTC porem respeite a sua tensão de trabalho,não esqueça que um capacitor só alcança seu valor após alcançar 15% de sua tensão nominal (já notou que nas fontes de vídeo k7 tem capacitores de mesmo valor porem de tensões diferentes ,isto não é atoa)

### Já fiz tudo que foi dito e continua queimando:

Neste caso troque os capacitores de largura e só por ultimo o fly-back.

##



https://13norte.blogspot.com/2011/03/kv-21fs140-quema-transistor-de-salida.html

https://www.clubedohardware.com.br/forums/topic/1270768-tv-sony-29-modelo-kv-29fs140-com-imagem-avermelhada/


https://www.youtube.com/watch?v=lUe458SeCCw
