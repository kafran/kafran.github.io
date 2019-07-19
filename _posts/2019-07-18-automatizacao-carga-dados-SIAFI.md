---
title: "Automatização de carga de dados no SIAFI"
header:
  video:
    id: 3p1XEpkm_ro
    provider: youtube
categories:
  - SIAFI
tags:
  - siafi
modified: 2019-07-18T23:47:16-03:00
---

Em 2016 eu estava trabalhando no financeiro do Instituto Federal da Paraíba (IFPB) e havia uma série de rotinas passíveis de automatização. O diretor financeiro me solicitou que estudasse os processos de cargas de dados no SIAFI e que desenvolvesse alguma forma de automatizar as tarefas de cadastramento de credores e de geração de listas de pagamentos. Era um processo extramente custoso em termos de recursos humanos e exigia que várias pessoas se dedicassem à tarefa.

Após estudar os mecanismos de carga _batch_ disponíveis no Sistema Integrado de Administração Financeira (SIAFI) eu desenvolvi uma série de _scripts_ _Python_ e _Shell_ que convertiam planilhas Excel no formato aceito pelo SIAFI. Entretanto, os _scripts_ eram pouco intuitivos, com um código porco e documentação ausente. Isso significava que ninguém era capaz de usá-los a não ser eu mesmo. O trabalho feito em 7 dias por 7 pessoas passou a ser feito por mim em uma manhã. O problema é que apesar de desonerar os meus colegas de trabalho eu acabei onerando a mim com a tarefa chata =/.

Não muito tempo depois o SERPRO atualizou o processo de carga _batch_ e migrou parte do processo para o "novo" SIAFI WEB. O formato de arquivo aceito pelo sistema deixou de ser um _Flat File_ de colunas fixas e passou a ser um XML. Graças a Deus [a STN se antecipou e forneceu uma solução](https://youtu.be/zqP4pnmtobg) para converter os dados para o novo formato XML aceito pelo sistema. A solução não é perfeita, mas estava mais bonita do que a minha.

A solução apresentada pela STN é uma planilha Excel que já traz consigo o "dicionário" do formato XML aceito pelo sistema, o que dá à planilha a capacidade de "se exportar" para o formato correto. Entretanto, com a implementação dos centro de custos nos sistemas de contabilidade aplicada ao setor público, a planilha disponibilizada pela STN não atendia a todas as necessidades do IFPB. Eu fiz algumas modificações no "dicionário" embarcado na planilha da STN de modo a possibilitar a exportação dos dados com os centros de custos utilizados pelo IFPB.

Com a mudança no processo, consegui sair da enrascada em que havia me metido (Rs.) e também passei a ficar desonarado da tarefa chata. Com a realocação do tempo, consegui evoluir também o processo de conversão dos dados dos credores para cadastro/alteração no SIAFI [o equivalente ao ATUCREDOR em processo _batch_]. Infelizmente, o processo de carga _batch_ para os dados dos credores continua sendo feito no SIAFI tela preta. No entanto, a planilha da STN me inspirou e eu convertir as rotinas em _Python_ e _Shell_ para Macros VBA em uma planilha no Excel.

Eu cheguei a gravar um vídeo explicando o funcionamento da planilha da STN com as modificações que eu fiz [foi quando eu descobri que não levo o menor jeito para YouTuber, Rs.], entretanto no final de 2018 apareceu uma oportunidade de ir para o Ministério do Planejamento, em Brasília, para trabalhar com dados - há algum tempo eu já estava querendo me desenvolver nessa área de ciência de dados e acabei aceitando a oportunidade - e por isso não cheguei a gravar o segundo vídeo mostrando o funcionamento da planilha que exporta os dados dos credores.

Muitas pessoas que viram o primeiro vídeo com a planilha da STN modificada têm me pedido para compartilhar os arquivos. Portanto, abaixo disponibilizo os arquivos para Download. Infelizmente eu não tenho a menor condição [tempo] de prestar suporte e apoio quanto ao funcionamento desses processos de carga de dados no SIAFI, por isso vocês irão precisar descobrir por conta própria.

**O caminho das pedras** A carga dos dados no SIAFI tela preta acontece através do portal do [Sistema de Transferência de Arquivos](https://sta.tesouro.fazenda.gov.br/pcasp/index.asp). Orientações quanto ao processo _batch_ no SIAFI tela preta podem ser encontradas no [manual da STN](https://www.tesouro.fazenda.gov.br/documents/10180/562554/PROCESSO_BT_SIAFI_INSTRUCOESv2.pdf).
{: .notice--info}

[Link para a planilha Batch da STN modificada](/assets/planilhas/Modelo_DOF-JP_IFPB.xlsx)

[Link para a planilha com a macro para exportar os dados dos credores](/assets/planilhas/Exportar_Batch_ATUCREDOR_DOF-JP_IFPB.xlsm) para serem importados/atualizados via _batch_ (ATUCREDOR) no SIAFI tela preta.

que o Excel ainda tem o seu espaço nesse enorme universo de ferramentas de Business Inteligence.

**Atenção** Infelizmente essas planilhas só funcionam com o Microsoft Excel, não funcionando com o LibreOffice e similares.
{: .notice--warning}