# Microdigital TK-3000 IIe

<p align="center">
<img height="200" alt="TK3000_imagem_ilustracao" src="https://github.com/user-attachments/assets/234f9543-1e90-4b74-a59f-41a9bb4c1fef" />
</p>

A Microdigital Eletrônica Ltda foi uma das empresas pioneiras no mercado de microcomputadores no Brasil, tendo grande importância na popularização da informática durante a década de 1980. Fundada em 1979, a empresa se destacou por criar e distribuir uma série de microcomputadores compatíveis com modelos internacionais. A Microdigital se beneficiou da reserva de mercado imposta pelo governo brasileiro, o que levou a empresa a desenvolver produtos que atendessem à demanda interna por tecnologia, educação e entretenimento.

O TK-3000 IIe foi um computador pessoal brasileiro lançado em abril de 1986, inspirado no Apple IIe Enhanced, da Apple. Na época, ele chamou a atenção por oferecer boa compatibilidade com o sistema original, permitindo rodar diversos programas, jogos e ferramentas de programação. Equipado com processador de 1 MHz e 64 KB de memória RAM, o TK-3000 IIe também contava com recursos gráficos coloridos, teclado com acentuação em português e suporte a expansões e periféricos. Foi um dos computadores que marcaram a história da informática no Brasil durante os anos 1980, conquistando espaço entre usuários interessados em aprender programação, trabalhar e se divertir com a tecnologia da época.

## Sobre essa reprodução

<p align="center">
<img height="200" alt="image" src="https://github.com/user-attachments/assets/fbf6602f-097d-40d7-9908-30ba7401f2cb" />
</p>

A reprodução do projeto foi realizada sem acesso físico à placa original, com base em fotos da placa MA 104 sem componentes. Para isso, utilizou-se os software Sprint Layout e o KiCad para desenhar o esquema e a placa de circuito impresso. A réplica ainda não foi produzida, e seu funcionamento não foi validado. Agradecemos às pessoas que disponibilizaram as fotos e o esquema original, permitindo que esse trabalho fosse possível.

 ### Detalhes da placa
A placa é de dupla face e ficou com um tamanho final de 239 × 239 mm. Originalmente, os chips não têm uma identificação individual, sendo identificados apenas pela linha e coluna em que estão localizados. Para facilitar a montagem, adicionei o designador de cada circuito integrado diretamente na placa, dentro da área correspondente a ele.

<p align="center">
<img height="300" alt="TK3000 frente" src="https://github.com/user-attachments/assets/fe73e844-e351-410c-b1ba-75181dc5c0ea" hspace="20" />
<img height="300" alt="TK3000 verso" src="https://github.com/user-attachments/assets/525b184c-ddb6-4f6b-a064-215575a86778" hspace="20" />
</p>

### Comparação com a placa original
Como não tive acesso direto à placa original, fiz o que pude para que a recriação ficasse o mais fiel possível. Também recriei a fonte utilizada no projeto para deixar o resultado ainda mais parecido com o original.

<p align="center">
<img height="300" alt="comparação" src="https://github.com/user-attachments/assets/63457337-c67b-4c99-8110-a57300a06e56" />
</p>

O circuito de RF foi removido e, no lugar, foi adicionada uma saída de vídeo composto.

No TK-3000 original, a saída e a entrada de dados do cassete compartilham o mesmo circuito, o que pode causar incompatibilidades na leitura de dados a partir de algumas fontes de áudio. Para resolver esse problema, foi incluída uma entrada independente para leitura de dados, que pode ser ativada pelo jumper X6.

- Posição 1-2: mantém o funcionamento original do TK-3000.
- Posição 2-3: ativa a entrada independente de áudio para leitura de dados.

### Para confecção

Na seção de releases desta página, você encontrará todos os arquivos necessários para a fabricação da placa: o gerber em formato zip, o esquema em PDF e a lista interativa de materiais em HTML. Basta enviar o arquivo zip para a sua fabricante de PCB de preferência.

### Chips customizados

O TK-3000 possui três chips customizados: a MMU, a IOU e a GAL. Encontrar os chips originais MMU e IOU é bem difícil, mas é possível usar equivalentes do Apple IIe ou de clones asiáticos. Porém, é preciso ficar atento à disposição dos pinos, que pode ser diferente da original, exigindo o uso de adaptadores.

Outra alternativa mais moderna é utilizar versões desses chips recriadas em FPGA. Já a GAL é mais fácil de encontrar e está disponível para compra na internet.

As equações da GAL utilizadas no Apple IIe estão disponíveis na pasta PAL_G1 deste repositório e podem ser adaptadas para funcionar neste projeto.

## Créditos

### Recriação da Placa: 

Clemar Folly Jr.

https://x.com/clemarfolly/ - https://www.facebook.com/clemarjr

### Fotos 

Fotos da Placa sem componentes

William Barbacena, José Ferro

Post Facebook (indisponível no momento)

https://www.facebook.com/share/p/xtZCQikUJb32PADm/

Clube do TK - Logo Microdigital

http://www.tk90x.com.br/Download.html

Wikipedia

https://pt.wikipedia.org/wiki/Ficheiro:Microdigital_TK3000IIe_MoBo_MA104.jpg

### Esquema

Tabalabs - Esquema do TK 3000 e Diagrama de blocos

http://www.tabalabs.com.br/apple/esquemas_microdigital/index.htm

Esquemateca Tabalabs - Esquema do CCE Exato IIe

http://www.tabalabs.com.br/esquemateca/

### ROMs 

Datassette - Eduardo Luccas

https://datassette.org/pt-br/softwares/apple/apple-ii/firmwares/br-brasil/tk3000-roms-8kb

### Outras contribuições

Carlos Milek - Inclusão de alguns resistores, capacitores e transistor


