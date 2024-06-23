
## 1-Porque e tão difícil consertar as fontes Sony?

Bem as fontes dos tvs Sony são difíceis de consertar porque os técnicos utilizão o conceito errado. 
**As fontes Sony NÃO SÃO FONTES CHAVEADAS, são na verdade INVERSORES DE ALTA POTENCIA isto é são osciladores sonoidais ( do tipo LC) de alta potencia.**


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

## Circuitos de proteção das tvs Sony 

Circuitos de proteção das tvs Sony (que dão mais defeito do que protegem), porém vou me deter nos modelos KV2970T/3470T que ao invés de dar lucro aos técnicos (por serem 29 ou 34) acabam dando dor de cabeça e prejuízos por causa dos problemas como: liga funciona um tempo e desliga ou nem liga etc..

Mais primeiro vamos a uma breve descrição do acionamento deste TV. Quando ligamos o TV na tomada surge as tensões de 135V(+B), 22V(áudio), 5V(reset), 5V(stad by) e 9v(+B do IC301). As de 5V alimentam o micro. o micro controla o on-off do TV através do seu pino 7(relay) chaveando o pino 2 do IC 641da fonte que fornece os 9V nos pinos 3 e 4 que alimenta o IC 301 da placa principal.

Este chassis (AA-2B) tem nada menos que seis(6) circuitos de proteções que são:

1-proteção de sobrecorrente na fonte.
2-circuito regulador da fonte
3-ABL
4-proteção de falta de deflexão vertical
5-proteção de sobrecorrente na placa principal
6-proteção de sobre tensão na placa principal


### 1-PROTEÇÃO DE SOBRECORRENTE DA FONTE:

É composta por R655(220K),R650(0,47R),Q641,Q643.
A tensão de +B (135V) passa pelo R650 que e de 0,47R e vai para a placa principal para alimentar o fly-back, se a corrente que passa pôr R650 ultrapassar a 2 A á tensão encima do R650 será igual ou superior a 0,7v o que fará Q641 conduzir que por sua vez fará Q643 também conduzir que ira aterrar a tensão de relay (stand by da fonte) e conseqüentemente o tv ira desligar.

### 2- PROTEÇÃO DO CIRCUITO REGULADOR DA FONTE

É composta por IC643(DM58) e R648(220K)
O IC 643 recebe em seu pino 1 uma amostra da tensão de 135v via R661(470R) esta tensão e comparada internamente com uma referencia e o erro e aplicado ao pino 4 em forma de corrente para controlar a tensão da fonte.


### 3-ABL

Composto por R547(33k),R546(30K),R549(4K7).
Os resistores R547, R546 estão ligados em serie e ligados na fonte de 135V e na linha de ABL o R549 vai à linha de ABL e para terra, desta forma temos uma tensão de ABL pré-determinada e monitorada pelo pina 26 do IC301(CXA1871S)se a tensão de ABL ultrapassar a pré determinada o IC301 ira ativar a proteção de x-ray (composta por Q591 e Q592)e fará o TV desligar.


### 4-PROTEÇÃO POR FALTA DE DEFLEXAO VERTICAL.

O micro processador IC 001recebe em seu pino2(vpin) uma amostra do pulso de deflexão vertical, se houver algum problema na saída vertical que provocar a falta deste pulso o micro processador ira colocar o tv em stand by.


### 5-PROTEÇÃO DE SOBRECORRENTE DA PLACA PRINCIPAL.

O circuito e composto pelos componentes R539(0.47R),R540(2.2K),R541(330K),R543(470K),R544(27K),R545(100K),D542,D533 e Q515.
Os resistores R540 e R541 estão ligados em serie formando um divisor de tensão que fornece uma tensão de referencia para o emissor de Q515 .A tensão de 115V que alimenta o fly-back passa pelo resistor R539, se a corrente de consumo do fly ultrapassar os 2 A, a tensão encima do R539 será maior que 0.7v que fará Q515 conduzir levando a tensão de referencia do emissor para o coletor onde temos um outro divisor formado pelos resistores R544 e R545.a tensão resultante deste divisor vai par o anodo do diodo D533 que por sua vez vai para a base de Q592 que e o x-ray protector.


### 6-PROTEÇAO DE SOBRETENSÃO DA PLACA PRINCIPAL.

E composto pelos componentes D548,R532(120K)R533(10K)o IC comparador IC541(duplo comparador- Upc393)D546,D547(zener 8.2V) R534(680R) D545.
O diodo D548 retifica a tensão que vem do pino 7 do fly-back, a tensão resultante alimenta o divisor formado pelos resistores R532 e R533. A tensão resultante do divisor vai para o pino 3 do IC 541(entrada + do comparador).no pino 2 do IC541 (- do comparador) temos uma tensão de referencia fornecida por D546 e D547.se por algum motivo a tensão retificada (do fly-back) por D548 for superior a do pino 2 (v de referencia ) o pino 1(saída do comparador) ficara com nível alto e polarizara a base de Q592(x-ray protector)e o tv entrara em stand by.


Como já deve ter percebido as proteções da placa principal atuam no Q592. os trasistores Q591 e Q592 atum no pino relay (stand-by) do micro fazendo o tv entrar em stand-by.

Bem estas foram as descrições de funcionamento dos circuitos de proteção, porem sem o esquema elétrico fica difícil entender algumas coisas mas recomendo que imprimam este documento para quando tiverem um tv destes vocês verifiquem na placa a posição dos componentes descritos isto ajudara na manutenção.


#### Agora vamos ver como identificar qual proteção esta sendo ativada.

Vamos considerar os seguintes sintomas:

1-tv parte e logo em seguida desliga (nem chega a aparecer imagem ou som)

2-tv desliga-se após alguns minutos de funcionamento.

A primeira coisa que devemos fazer e verificar e a proteção de falta de deflexão vertical, para isto basta acessar o modo de serviço, pois todos os tvs Sony desativa esta proteção quando entramos no modo de serviço para tanto com o tv em stand-by digite DISPLAY, CANAL 5, VOLUME + e POWER se for defeito de vertical o tv ira ligar com um traço horizontal na tela indicando defeito de vertical,verifique as alimentações do IC 561 +12V e -15V o pulso v drive no pino 27 no IC 301 etc...
Caso feito o descrito e não adiantar devemos agora definir se e proteção da fonte ou da placa principal para isto verifique o seguinte:

a)Primeiro coloque uma antena no aparelho e execute a auto programação. Se o TV se desligar durante a procura de canais verifique a proteção do circuito regulador da fonte ,comece medindo o resistor R648 de 220K que e de precisão e o capacitor C651.

b)Quando o TV desliga só conseguimos ligalo novamente se retirarmos da tomada e ligamos denovo.

c)Quando o TV desliga basta pressionai power no controle remoto para ligar novamente.

Se for o primeiro é a proteção de sobrecorrente da fonte. verifique o R650(0,47R) e R655(220K) utilize multímetro digital "nem pense utilizar aquele seu velho analógico que já esta com o ponteiro que e um gancho de tanto bater no fundo da escala". O resistor R655 de 220K e de precisão se você medir (com o digital e claro!)e der 221k por exemplo, considere-o alterado. os transistores Q641 e Q643 apresentam um defeito interessante,com o tempo alteram o seu ganho portanto devem ser substituídos.

Se for o segundo caso , e devido ao acionamento de uma das proteções da placa principal ,para descobrir qual faça o seguinte:
No momento que o tv desliga verifique se há tensão no catodo dos diodos D533 e D545.
Se tiver tensão no D533 e a proteção de sobrecorrente da placa principal que esta sendo acionada. Verifique os resistores R539(0,47R) e R541(330k). O R541 costuma abrir com freqüência.
Se tiver tensão no D545 e a proteção de sobre tensão que esta sendo acionada verifique as tensões nos pinos 1,2,3 do IC 541
1= 0.1v
2= 10.5V(tensão de referência)
3= 9,4v
A tensão no pino 3 tem que ser inferior a do pino 2.
Se tiver superior verifique os resistores R533(10K) R532(120K).
A cola que prende o resistor (aquela vermeliha) R532 com o tempo começa a dar fuga, para corrigir isto retire o resistor do lugar e raspe a cola e recoloque o resistor.
As vazes quando trocamos o fly e não colocamos o original, por pequenas diferenças de construção do fly o mesmo fornece uma tensão um pouquinho amais (1v já e suficiente) e faz a proteção ser acionada.para contornar isto altere o valor de R533 de 10K para 8K2.
Se não tiver tensão em nem um dos diodos quando o TV desliga verifique a tensão no pino 33 do IC 301 se tiver, e a proteção de ABL que esta sendo acionada. Verifique os resistores R547,546,549 TODOS DE PRECISAO.
obs.
O descrito ate aqui foi para defeitos nos propios circuito de proteção, porem pode realmente ser um defeito de um estagio fazendo o TV se desligar, portanto cuidado, não desligue nem uma das proteções, pois poderá ocorrer dano ao aparelho.
Verifique também se a fonte principal esta com 135V se tiver um pouco alta o TV também se desliga. a tensão de +B das fontes sony podem ser ajustadas pelo modo de serviço no item PADJ ,portanto monitore o +B e vá ajustando ate chegar na tensão correta e memorize pressionando MUTE e após ENTER.
O emissor do transistor de saída horizontal e ligado a terra pelo dissipador do transistor, na junção da trilha com o dissipador costuma dar solda-fria o que faz o TV se desligar.
Verifique também se não há solda-fria no IC 641 da fonte, pois ele e que fornece os 9V para o IC 301.
Bem como já deve Ter dado para perceber este TV tem vários itens para verificar o que exige do técnico paciência e raciocínio lógico portanto antes de sair trocando componentes como louco, análise os estágios anotando tudo e então tire uma conclusão de qual o estágio com defeito ou componente defeituoso.
Espero que com o que passo aqui posa estar ajudando os amigos a resolverem com mais agilidade (e menos prejuízos) os defeitos destes modelos de TV. O meu muito obrigado a todos e ate mais.


Part 3

explicar algumas coisas sobre os TVs KV-29T75(CHASSI AA2F) e KV-29T80 (CHASSI BA4B). As explicações são básicas e me detive mais nos circuitos de proteção pôr darem mais defeito.
Os TVS em questão têm poucas diferenças nos seus circuitos, devido a isto as explicações que se sequem são baseadas no KV-29T80(BA4B).

este Tv possui 5 circuitos de proteção:

- PROTEÇÃO DE SOBRECORRENTE DA LINHA DE 135V.
- PROTEÇÃODE SOBRETENCAO DO FLY-BACK
- PROTEÇÃO DE SOBRECORRENTE DA FONTE PRINCIPAL
- PROTEÇÃO DA FONTE DE 9V DE STAND-BY
- PROTEÇÃO DE FALTA DE DEFLEXAO VERTICAL

## PROTEÇÃO DE SOBRECORRENTE DA LINHA DE 135V

E composta pôr Q571,R571,RR574,R575,R572,R573,R576,D581,D571.
Se a corrente ultrapassar os 2 A, a tensão encima de R 571 fará Q 571 conduzir enviando uma tensão para a base de Q 300 que pôr sua vez ira aterrar o pulso H DRIVE do pino 18 do ic 301 fazendo o TV desligar e ao mesmo tempo polarizara a base de Q 613 que pôr sua vez ira aterrar o pino RELAY(STAND-BY) colocando a fonte em OFF.

## PROTEÇÃO DE SOBRETENSÃO DO FLY-BACK

A segunda e compota pôr D574,R582,R583,R584. O diodo D574 retifica a tensão vinda do pino7 do fly, e passa pelo divisor resistivo composto pôr R582, R583, R584 e vai para o pino 5 do ic 521.no pino 6 do ic521 temos uma tensão de referencia fornecida pôr D572, D573 e R579. Se a tensão do pino 5 ultrapassar a do pino 6 o pino 7 ficará com nível alto polarizando a base de Q300 e Q613 fazendo o TV se desligar.

## PROTEÇÃO DE SOBRECORRENTE DA FONTE PRINCIPAL

A terceira e na propia fonte de alimentação e é obtida monitorando a tensão encima de R641 e R640 ,se a corrente aumentar muito a tensão encima destes resistores ira aumentar e o ic601 ira cortar o pulso de chaveamento da fonte.

## PROTEÇÃO DA FONTE DE 9V DE STAND-BY.

É composta basicamente pelo transistor Q604 e pelo diodo zener D619.
Se pôr algum motivo a fonte de 9v subir acima de 10v o diodo D619 ira conduzir polarizando a base de Q604 que nesta
Condição ira aterrar a tensão de relay fazendo o TV desligar.

## PROTEÇÃO DE FALTA DE DEFLEXAO VERTICAL

O micro processador recebe em seu pino 17(i-prot) uma amostra do pulso da saída vertical ,se pôr algum motivo faltar este pulso no pino 17 o micro coloca o TV em stand-by pelo pino relay e faz o led do painel piscar 4 vezes.

## ROTINA DE REPARO.

A rotina de reparo empregada para este chassi e a mesma do KV-2970.

-Verificar se não a falha de deflexão vertical (entrando no modo de serviço)
-Verificar proteção de sobrecorrente do fly
-Verificar proteção de sobretensao do fly
-Verificar circuito de IK (saída de vídeo)

## Agora vamos a algumas dicas.


Em 95% dos casos em que este TV fica de desligando intermitente ou não e pôr solda fria nos pinos do trafo driver horizontal (T501) não da para ver a olho nu só com uma lupa e pressionando o trofo pôr cima.


Se o fly-back não for original e a proteção de sobre tensão ficar sendo acionada freqüentemente devemos alterar o valor do R582 de 10k para 8k2.
Às vezes o TV esta se desligando e pelas piscadas do led concluímos que e defeito de vertical, porem quando acessamos o modo de serviço o TV sege funcionando com deflexão normal.nestes casos não e defeito na saída vertical, mas na linha que envia a informação para o pino i-prot (17) do micro, geralmente o diodo zener D001 costuma a dar fuga ou estar em curto ou ainda com fuga intermitente o que deixa o técnico louco que troca tudo no vertical e é o diodo com problemas, fiquem atentos a isto.


Este TV possui auto diagnostico (que quando o TV foi lançado era chamado de'IA'.. ? inteligência artificial, imagina só.) que pode ser identificado pelo numero de piscadas do led.


2 vezes - proteção de sobrecorrente do fly.
4 vezes - falta de deflexão vertical
5 vezes - falha na linha de ik (a corrente dos cátodos e muito pequena.)


se você pegar este TV com defeitos estranhos como, geometria desajustada (vertical, largura ,pin...) sem som
ou outro sintoma estranho execute o recet da memória para isto faça o seguinte.

Entre no modo de serviço: com o TV em stand-by digite pelo remoto DISPLAY, CANAL 5, VOLUME + E POWER.
Deste modo aparecera a tela de serviço então DIDITE 8 E APARECERA NA TELA RECET EM VERMELHO
E AGORA PRECIONE ENTER, o TV ira desligar e ligar novamente. geralmente resolve estes casos.


A ELTEC publica este esquema elétrico, com tudo você pode adquiri-lo e utilizar para os dois modelos.
Procure descobrir qual circuito está falhando e/ou qual proteção esta sendo acionada ou se não e defeito no próprio circuito de proteção,não saia trocando peças como louco tente seguir uma logica de reparo.


# Part 4

## circuito de IK das tvs Sony 

### Para que serve o circuito IK?

Bem sabemos que com o passar do tempo os tubos de imagem vão se desgastado o que provoca um desbalanceamento das cores RGB e consequentemente uma má escala de cinza prejudicando a qualidade final da imagem. Os televisores Sony utilizam o circuito de IK para monitorar a corrente nos cátodos e assim modificar o ganho dos amplificadores de RGB interno ao processador de vídeo para compensar o desgaste do tubo mantendo assim a qualidade final da imagem.

### Como funciona?

Quando ligamos o tv o circuito integrado processador de vídeo envia para a placa de saída de vídeo (C) um trem de pulsos de diferente períodos através dos pinos de RGB. Tais pulsos são enviados para os cátodos e retornam pelo pino de IK. O processador de vídeo então compara a amplitude do pulso de retorno com uma tensão de referencia interna e compensa o ganho dos amplificadores para que todos estejam no mesmo nível para então liberar a imagem.

### Defeitos.

Se o processador não conseguir compensar a diferença de amplitude do pulso de retorno não será liberada a imagem. As causas podem ser o próprio tudo ou algum outro defeito de polarização do mesmo.

### Análise da defeito.


Para analisar o sintoma de LED do painel piscando e sem imagem ,devemos enganar o processador de vídeo colocando três resistores de 1K ligados entre os pinos de RGB e IK da placa do tubo (C). desta forma estaremos desviando os pulsos diretamente para o pino de IK. Então o tv ira liberar a imagem e o técnico poderá analisar o defeito.
#Para sabem quem é o culpado faça o seguinte, após a liberação de imagem coloque o nível de cor do tv em 0 e em um canal fora do ar ou entre com uma padrão de escala de cinza , veja como está a escala de cinza se estiver com uma determinada com mais forte, verifique as tensões nos pinos de KR, KG e KB no soquete do tubo. se estiverem em praticamente em mesmo nível o problema geralmente é o tubo , para comprovar ligue o tv na serie e aterre momentaneamente um de cada vês os pinos KR, KB, KG do tubo e compare o brilho das cores. se uma estiver mais fraca é o tubo que está esgotado.
Se o tubo estiver ok o problema é na placa do cinescopio. Em 90% dos defeitos da placa (c) são os transistores que estão com o seu ganho alterado, e sempre devem ser substituídos os três.
Outra causa deste tipo de defeito é o ajuste de screem e a tensão de 180V.
Porem se com o artificio dos resistores não ouve a liberação da imagem o problema é na placa principal. Na linha de IK temos um resistor em serie com um capacitor eletrolítico, verifique o resistor e troque o capacitor que pode estar com ESR elevada o que provocaria o defeito. Se o capacitor e o resistor estiver ok o provável defeito é o processador de vídeo (CXA).

### Rotina de reparo.


1- verifica se o filamento está aceso , caso não verifique toda a linha até o fly-back . alguns modelos tem um jumper na linha de harter que da solda fria e o filamento não acende.
2- Tente um ajuste de screem se a imagem aparecer troque os transistores da placa c.
3- verifique a tensão de 180V que é 180V para os de 14 polegadas e de 200V para os de 20 polegadas (veja sempre o que está escrito na placa c). se a tensão estiver mais alta verifique a tensão da fonte principal ,se esta estiver ok siga a linha dos 180V( ou 200V) e terá um resistor de 220K ou 330K para terra que deve estar aberto ou alterado.
4- Se a tensão de 180V (200V) estiver ok, o screen ok e filamento ok, coloque os resistores de 1K e faça os testes como já foi descrito(#).


Quanto aos tubos da Sony são de tecnologia exclusiva(Trinitron) da empresa o que quer dizer que não podemos colocar outro tubo de outro fabricante no lugar porem há a exceção do KV-200MG e do KV-140MG que utilizam tubos comuns que podem ser substituídos por tubos da Philips, sansung etc..


Quando o defeito é mesmo o tubo porem não está tão ruim o técnico logo pensa em deixar os resistores e entregar o tv para o cliente. Porem uma observação deve ser feita. Quando o tubo está desgastado a tendência é piorar mais e mais rápido e isto deve ser informado ao cliente. Se assim for, a melhor alternativa seria a seguinte:
Corte a trilha que vai no pino de IK na placa C.
Coloque ao invés de resistores ,diodos de sinal (1N4148) com os anodos em RGB e os cátodos em IK.
Bem pessoal estas são algumas informações sobre o circuito de IK, espero que ajude a facilitar a análise e solucionar os problemas que apresentam este estagio dos tvs sony.
Um abraço a todos e até mais


https://13norte.blogspot.com/2011/03/kv-21fs140-quema-transistor-de-salida.html

https://www.clubedohardware.com.br/forums/topic/1270768-tv-sony-29-modelo-kv-29fs140-com-imagem-avermelhada/


https://www.youtube.com/watch?v=lUe458SeCCw
