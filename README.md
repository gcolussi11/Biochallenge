# **Classificador de sons ambientes**

## **Sobre mim e a proposta do projeto**
Oi! Meu nome é Gabriella Colussi e quando desenvolvi esse projeto estava no meu quinto semestre de Engenharia Biomédica.
O projeto foi desenvolvido para uma competição nacional chamada Biochallenge, organizada pelo Inatel, de Santa Rita do Sapucaí - MG.

A proposta deles foi o desenvolvimento de um aplicativo que pudesse classificar sons ambientes. Visando essa funcionalidade, desenvolvi um pipeline simplificado de machine learning que pudesse fazer a extração de áudios do youtube, caso necessário,
toda a etapa de pré-processamento requerida para que o modelo pudesse ser treinado, treino, validação e teste. 

## **O Projeto**
Este repositório lista os seguintes arquivos:
`Audios.ipynb`
`Modelos.ipynb`
`balanced_train_segments.csv`
`dic_labels_negadas2.json`

O dataset foi formado a partir da complementação de dois bancos de dados diferentes, [ESC-50](https://github.com/karolpiczak/ESC-50) e o [Audioset](https://research.google.com/audioset/). 
Considerando que o Audioset apenas referencia os segmentos de audios de links do YouTube, diferentemente do ESC-50 que já provê os áudios em formato .wav, o primeiro arquivo `Audios.ipynb` é um notebook destinado a filtragem de 
labels e download dos áudios no mesmo formato que o .wav.

O próximo noteboook, `Modelos.ipynb`, é o código que traz um pipeline simplificado dividio em: 
- Banco de dados;
- Pré-Processamento dos dados;
- Modelos

De forma resumida, o banco de dados traz a leitura e filtragem dos dados provenientes de ambos datasets, ESC-50 e Audioset, como também junta o conteúdo dos dois para melhor acesso posteriormente e cria um df para melhor mapeamento dos áudios e labels disponíveis.
O pré-processamento faz a extração de features dos áudios como MFCCs e Zero-Crossing Rate que vão servir como entradas para os modelos. Por fim, a seção "Modelos" traz o treinamento e avaliação de dois modelos diferentes, Random Forest.

Já os arquivos `balanced_train_segments.csv`e `dic_labels_negadas2.json` foram arquivos auxiliares ao meu propósito de desenvolvimento, o primeiro podendo ser encontrado no próprio site do audioset e o segundo um dicionário de labels filtradas por mim.

## **Conclusões**
Com este repositório, meu objetivo é contribuir para a comunidade de desenvolvedores e entusiastas que compartilham interesses semelhantes. Embora este seja um trabalho amador, ele reflete minha dedicação e aprendizado contínuo no campo. Estou sempre buscando aprimorar minhas habilidades e conhecimento, e espero que este projeto possa ser útil para aqueles que estão nessa mesma jornada!

Agradeço por explorar meu repositório! Estou aberta a feedbacks e sugestões.

Sinta-se à vontade para me contatar através do meu [LinkedIn](https://www.linkedin.com/in/gabriella-colussi-ferreira-314190165/), até a próxima!
