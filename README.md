# computacaoGrafica
destinado a trabalhos de computação grafica

Aluno: Leonardo Kunz Tramontina

E ai professor, não consegui criar pasta para os algoritmos de reconhecimento de objetos, dai eu zipei eles e fiz um commit, só fazer o download que da pra ver! Abraço!

Tutorial de como treinar uma rede para ser usada no python

1. Primeiramente é necessário um set de imagens negativas, ou seja varias imagens que não contenham o objeto que você deseja realizar o reconhecimento, normalmente voce vai precisar o dobro de imagens positivas, por exemplo se eu quero reconhecer um cachorro, eu preciso de um set que contenha 500 imagens negativas e um set que contenha 250 imagens positivas(as imagens positivas, são as que contem o objeto a ser reconhecido, por exemplo um cachorro)

2. Após ter as imagens negativas, é preciso também um set com imagens positivas, ja explicadas no passo anterior.

3. é necessario também algumas imagens para analise, que irão servir para validar o reconhecimento do objeto, essas imagens devem conter o objeto e outras não conter!

4.Após ter todas imagens em mãos, é necessario criar uma lista de imagens negativas(é possivel usar um algoritmo que crie um arquivo .txt que é facilmente implementado, que gera uma lista com o nome de todos os arquivos na pasta em questão)

5. É necessario ter o OPENCV nativo no computador(pode ser encontrado no site do opencv.org)

6. Após ter descompactado o opencv, iremos utilizar a ferramenta opencv anotation, usado para treinar a inteligencia artificial, onde iremos selecionar em todas as imagens positivas o objeto que deseja reconhecer.

7. Após treinado a IA com todas as imagens positivas, o opencv annotation gera um arquivo chamado saida(nome pode ser alterado, não precisa ser obrigatoriamente saida), esse arquivo contem uma lista com todas imagens positivas e as respectivas coordenadas do objeto circulado

8. Agora tendo o arquivo positivas e saida, o proximo passo é usar a ferramenta create_samples, que utiliza a tecnica de grirar em todos os graus e angulos possiveis para detectar o objeto, é gerado um arquivo de vetor(o create_samples vai criar exemplos das imagens positivas, ele que vai ser utilizado para treinar a IA)

9.Feito isso, o ultimo comando é o Opencv traincascade, que vai criar dados em uma pasta desejada, passando alguns parametros, como o nivel de aceitação... (esse comando costuma ser demorado dependendo o numero de imagens a serem analisadas)

10. Após a IA treinada, é facilmente implementado um algoritmo que pode ser em python, para fazer um retangulo que faz a analise, utilizando os metodos do opencv!


PESQUISA SOBRE OS METODOS DO OPENCV:
OPENCV_ANNOTATION
A ferramenta do opencv irá abrir a primeira imagem da pasta. No entanto, como a listagem de arquivos dentro de uma pasta é específica do sistema, pode ser possível que não seja a primeira imagem que você vê. Como precisamos processar todas as imagens da pasta, isso não é problema algum. A função é "anotar" as coordenadas de um objeto selecionado para posteriormente realizar a analise. Essa ferramenta gera um arquivo TXT, contento o nome das imagens, a quantidade de itens selecionados e as respectivas coordenadas.

OPENCV_CREATESAMPLES
 Ferramenta utilizada para geração de imagens positivas, ela ira girar as imagens em todos os angulos e graus para criar exemplos de imagens positivas.
 
 OPENCV_TRAINCASCADE
 A ferramenta traincascade, é uma das mais importantes que vai usar os dados das duas ferramentas mencionadas anteriormente para treinar o detector e poder fazer a analise de uma imagem posteriormente.
