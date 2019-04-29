---
title: Sobre o suporte do InfoPath para tecnologias XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: O Microsoft InfoPath é uma ferramenta híbrida que combina o melhor de uma experiência de edição de documentos tradicional, como um processador de texto ou um aplicativo de email, com os recursos de captura de dados rigorosos de um pacote de formulários. Este artigo descreve os problemas que o InfoPath foi projetado para tratar e explica os princípios de design e os padrões do setor XML usados para resolver esses problemas.
ms.openlocfilehash: 20831635fba8d76b9d6b45f42a5308ab7236db20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407225"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Sobre o suporte do InfoPath para tecnologias XML

O Microsoft InfoPath é uma ferramenta híbrida que combina o melhor de uma experiência de edição de documentos tradicional, como um processador de texto ou um aplicativo de email, com os recursos de captura de dados rigorosos de um pacote de formulários. Este artigo descreve os problemas que o InfoPath foi projetado para tratar e explica os princípios de design e os padrões do setor XML usados para resolver esses problemas.
  
## <a name="introduction"></a>Introdução

O InfoPath é uma ferramenta de criação de XML de alto nível que permite que usuários finais comuns criem documentos XML que pertencem a um esquema XML definido por personalizado. Quando o usuário edita um documento XML, as modificações no documento são controladas pelo esquema XML.
  
O usuário interage com o documento XML por meio de uma exibição formatada e rica que é exibida aplicando uma folha de estilos XSLT ao documento. Um nó folha ou um valor de atributo do documento XML é exibido como um campo, como uma caixa de texto ou uma caixa de seleção, enquanto uma hierarquia de nós é renderizada como um grupo de campos.
  
O InfoPath permite a edição de dados XML validada e estruturada, mostrando as ações de edição que são válidas para o campo ou grupo de campos atualmente selecionado. Essa edição estruturada permite que o usuário adicione e remova atributos e elementos XML válidos, trabalhando com grupos de campos exibidos em exibições dinâmicas sofisticadas, sem ver os elementos e atributos.
  
O InfoPath resolve um problema na área de coleta de dados que não pôde ser resolvida antes do surgimento de XML: ao fornecer formulários que podem crescer adicionando-se grupos de campos que usam o modelo de dados hierárquicos XML, o InfoPath adiciona a flexibilidade dos documentos do processador de texto para os recursos de validação rigorosos de um aplicativo de formulários. Transformações XSLT complexas são parte integrante dessa solução que oferece exibições dinâmicas e fáceis de usar dos dados XML.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Limitações de formulários e documentos tradicionais para coletar dados

Ao coletar dados corporativos, os usuários sempre querem mais flexibilidade do que os formulários estáticos fornecem, mas mais edição e validação estruturadas do que os documentos do processador de texto fornecem.
  
Os formulários tradicionais são estáticos e limitados por comprimento. Eles têm um número fixo de linhas repetidas e não podem ser estendidos quando o formulário está sendo preenchido. Os formulários tradicionais são difíceis de usar porque não têm recursos de edição avançados. Com frequência, o usuário deve fornecer todas as informações em uma passagem.
  
Por outro lado, os documentos tradicionais criados usando um processador de texto permitem que o usuário adicione e remova conteúdo livremente, mas forneça poucas orientações sobre como inserir informações completas, estruturadas e válidas; quaisquer campos definidos no documento têm validação mínima ou inexistente de valores de dados e tipos de dados. Os dados nos campos não são rotulados corretamente para habilitar a referência fácil e a reutilização automática. Os dados são de forma livre, e não estruturados; Você não pode agrupar informações, como aplicar um rótulo "endereço" a um grupo de campos "rua", "cidade" e "estado".
  
Portanto, há uma necessidade de edição flexível, mas estruturada, mas como esse tipo de tecnologia não estava disponível antes do surgimento de XML, os desenvolvedores precisaram criar aplicativos personalizados, que exigem uma codificação extensiva. Os aplicativos personalizados são caros e difíceis de modificar e exigem codificação personalizada para validação. Os aplicativos personalizados geralmente exigem treinamento do usuário final, e é difícil reutilizar os dados resultantes para outros processos de negócios.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Fornecendo edição estruturada exibindo dados XML como grupos de campos

Um problema de design técnico importante que precisa ser resolvido era como fornecer uma interface do usuário fácil para adicionar e remover atributos e elementos XML, sem mostrar os elementos e atributos, mas manter a árvore DOM válida de acordo com o XML definido por personalizado esquemas. A interface de usuário necessária para oferecer uma maneira natural de editar a árvore DOM que inclui a inserção de subárvores opcionais, a substituição de opções de subárvores e a extensão de subárvores existentes.
  
Para fornecer essa interface de usuário fácil, uma subárvore DOM é exibida como um grupo de campos ou seção. Um grupo de campos é um grupo de controles de interface do usuário, como caixas de texto e listas suspensas, e funciona como uma interface de usuário fácil que permite ao usuário visualizar e editar dados XML hierárquicos. Um grupo de campos pode conter outros grupos de campos e pode ser opcional ou repetido, da mesma forma que uma sub-árvore DOM pode conter outras subárvores e pode ser opcional ou repetitiva. Uma subárvore é adicionada à árvore DOM quando o usuário posiciona o ponteiro do mouse sobre um grupo de campos, clica no menu suspenso exibido no grupo de campos e seleciona o **nome \<\>do grupo de campos de inserção**.
  
O InfoPath fornece essa edição estruturada de dados XML usando o esquema XML especificado para restringir e orientar a edição. O esquema controla se os comandos **Inserir** e **remover** são exibidos no menu suspenso de um grupo de campos. O esquema também é usado para validação. Para habilitar a edição de um documento XML para o qual não há nenhum esquema XML, o InfoPath pode gerar um esquema do documento XML. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Fornecendo modos de exibição fáceis de usar de dados XML usando transformações XSLT

Outro desafio de design técnico que precisava ser resolvido foi como habilitar o conteúdo dos modos de exibição da interface do usuário para ser organizado de forma muito diferente da estrutura dos dados XML. Para apresentar os dados de uma maneira que faz mais sentido para o usuário e permite que o usuário leia e edite os dados facilmente, o designer deve ser capaz de exibir dados em uma sequência diferente da árvore de dados DOM, omitir alguns dados de um modo de exibição , reorganizar os nós da árvore de dados adjacentes em modos de exibição separados e coletar dados de diferentes partes da árvore de dados em um único modo de exibição.
  
A ordem e a estrutura do conteúdo dos modos de exibição devem, portanto, ser independentes da ordem e da estrutura dos nós de árvore DOM. Essa independência estrutural de apresentação e dados requer uma associação dinâmica, ou mapeamento, complexo entre os campos agrupados nos modos de exibição e os nós na árvore DOM.
  
Para fornecer esse mapeamento complexo entre modos de exibição e dados, o InfoPath usa extensivamente transformações de XSL (XSLT). O XSLT é uma linguagem de folha de estilos poderosa que oferece suporte a transformações de XSLT complexas e suporta visualizações ricas com apresentação dinâmica e flexível de conteúdo. Um arquivo XSLT é usado para cada modo de exibição. O uso de uma folha de estilos é uma abordagem de design comum e bem estabelecida em ferramentas de criação de XML, e XSLT é o padrão W3C para folhas de estilo usadas para esse tipo de transformação complexa.
  
Para evitar a execução de toda a transformação XSLT toda vez que o usuário modifica a estrutura de uma subárvore no DOM, os algoritmos são usados para determinar qual parte do modo de exibição deve ser atualizada. Em seguida, somente a parte relevante da folha de estilos XSLT é aplicada e a parte afetada do modo de exibição é atualizada.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Como os padrões XML são usados durante a edição de um formulário

O InfoPath é construído a partir do zero em relação aos padrões XML que inclui o seguinte:
  
- Extensible Markup Language (XML) 1,0 segunda edição
    
- Namespaces em XML
    
- Linguagem de caminho XML (XPath) 1,0
    
- Esquema XML (XSD) 1,0 parte 1: estruturas e parte 2: tipos de datatypes
    
- XSLT (Extensible Stylesheet Language Transformations) 1,0
    
- Extensible Hypertext Markup Language (XHTML) 1,0
    
- Folhas de estilo em cascata (CSS)
    
- Modelo de objeto de documento (DOM) 1,0
    
- Assinaturas digitais XML (XML DSig)
    
- Protocolo SOAP (Simple Object Access Protocol) 1,1
    
- Linguagem de descrição de serviços Web (WSDL) 1,1
    
- Descrição universal, descoberta e integração (UDDI) 1,0
    
Por exemplo, o InfoPath usa e gera arquivos XML, XSLT e XSD padrão que podem ser reutilizados em vários processos de negócios. O InfoPath usa o MSXML, o kit de ferramentas SOAP e o namespace .NET System. XML para dar suporte a esses padrões e fornece suporte completo integrado para XML Web Services.
  
A Figura 1 mostra o menu suspenso sensível ao contexto para um grupo de campos do **cliente** , que permite ao usuário adicionar outro grupo de campos de **cliente** , remover esse grupo de campos do **cliente** , inserir uma linha de **Item** na tabela de itens de compra no Este grupo de campos ou inserir um grupo de campos de **ações** opcionais dentro desse grupo de campos. O link **clique aqui** oferece outra maneira de inserir o grupo de campos **ações** . Um menu suspenso mais curto aparece em cada linha de item de compra. 
  
1. No InfoPath, o usuário cria um novo documento XML com base em um modelo de formulário do InfoPath ou abre um documento XML existente baseado em um modelo de formulário. O documento XML é um arquivo de dados XML que contém uma referência ao modelo de formulário e pode usar namespaces XML. 
    
    Um modelo de formulário é o conjunto de arquivos que fornecem a edição estruturada de documentos XML que estão em conformidade com um esquema XML definido por um determinado personalizado. Os arquivos que compõem o modelo de formulário podem ser empacotados como arquivos individuais dentro de uma pasta comum ou como arquivos que residem em uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão e arquivos de suporte opcionais, como assemblies de código gerenciado.
    
2. Se o documento XML for assinado digitalmente usando a assinatura XML, o InfoPath confirmará que o arquivo XML é consistente antes de abri-lo.
    
3. O InfoPath cria uma árvore de dados DOM do documento XML na memória.
    
4. Transformações de XSLT são aplicadas à árvore DOM, produzindo modos de exibição que mostram uma apresentação apropriada do documento para o usuário. Os elementos no início do documento XML podem ser exibidos na parte inferior do modo de exibição e também em uma organização diferente em outro modo de exibição. Os modos de exibição consistem em contêineres de interface do usuário, como seções que contêm texto e controles, como caixas de texto, caixas de Rich Text, selecionadores de datas e listas suspensas. Os contêineres também podem conter outros contêineres.
    
5. A transformação XSLT produz XHTML como saída e, em seguida, um CSS é usado para controlar a apresentação do XHTML.
    
6. Se o esquema XML permitir a adição de nós a um nó da árvore de dados, o campo ou grupo de campos que é mapeado para o nó tem um menu suspenso que permite ao usuário adicionar ou remover grupos de campos. O usuário edita o documento adicionando um grupo de campos de repetição ou opcional, inserindo um valor, selecionando uma opção ou digitando Rich Text. Se um nó de esquema XML estiver associado ao esquema para XHTML, o InfoPath apresentará uma interface do usuário para a criação de Rich Text. Quando o usuário insere Rich Text, o conteúdo XHTML é criado como uma subárvore no DOM.
    
7. A árvore DOM é sempre mantida válida. À medida que o usuário edita o documento XML, as edições são validadas em relação ao esquema XML associado. As alterações tentadas na estrutura DOM e nos valores do nó folha são validadas em relação ao esquema XML para garantir que seus valores e tipos de dados sejam válidos. Se as alterações tentadas forem inválidas, uma caixa de diálogo de validação será aberta, e as alterações não serão aplicadas à árvore DOM. Se as alterações forem válidas, a árvore DOM será atualizada.
    
8. A parte alterada do modo de exibição é atualizada, aplicando apenas as partes necessárias da folha de estilos XSLT à árvore DOM.
    
9. O usuário pode salvar o documento XML ou enviar o documento XML usando HTTP ou SOAP simples. O usuário não tem permissão para enviar o documento, a menos que seja válido de acordo com o esquema XML.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Como os padrões XML são usados durante a criação de um formulário

Você pode criar um formulário começando com um esquema XML existente, conectando-se a um serviço Web ou banco de dados XML e obtendo seu esquema XML, ou gerando automaticamente um esquema de um novo formulário ou de um arquivo de dados XML. Esses cenários são descritos nos procedimentos a seguir. A Figura 3 mostra a interface do usuário básica para a criação de um modelo de formulário.
  
1. Crie um novo formulário no designer do InfoPath selecionando o modelo de formulário **XML ou de esquema** e selecione um arquivo de esquema XML existente como a fonte de dados. O esquema XML é carregado no painel de tarefas e mostrado como um controle de árvore. 
    
2. Use as ferramentas de layout de design para definir os controles da interface do usuário, como linhas e o design de plano de fundo, em um ou mais modos de exibição. Isso gera alguns dos elementos XSLT. Os modos de exibição XSLT e o esquema XML são associados automaticamente ao modelo de formulário.
    
3. Mapeie os elementos do esquema XML para os controles da interface do usuário nos modos de exibição usando o recurso de arrastar e soltar. O InfoPath ajuda você a escolher controles apropriados para os elementos do esquema XML, com base no tipo dos elementos do esquema. Por exemplo, se o tipo de dados XML for Data, o InfoPath sugere um controle de seletor de data. Com base nas opções do esquema XML, o InfoPath pode inserir grupos de campos opcionais ou de repetição. O mapeamento dos elementos do esquema XML para os controles da interface do usuário gera a estrutura XSLT.
    
4. Salve o modelo de formulário. Você pode salvar os arquivos que compõem o modelo de formulário como arquivos individuais em uma pasta regular ou como arquivos dentro de uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão. O modelo de formulário agora está pronto para uso do usuário.
    
Um modelo de formulário contém todas as informações de semântica necessárias para fornecer edição estruturada quando um formulário é aberto no InfoPath. Um modelo de formulário inclui um arquivo de manifesto, os arquivos XSLT que definem as exibições, as informações necessárias para validar os dados e um identificador de recurso opcional para um serviço Web XML.
  
O manifesto, ou o arquivo de definição de formulário, é o hub comum e o ponto de entrada para todos os arquivos necessários para o modelo de formulário. O manifesto contém referências aos outros arquivos no modelo de formulário e contém as informações necessárias para validar os dados e fornecer edição estruturada. As informações de validação do esquema XML são personalizadas para a interface do usuário resultante e adicionadas ao arquivo de manifesto. Por exemplo, se o esquema permitir a inserção de vários elementos opcionais em uma sub-árvore específica, você pode projetar a interface do usuário para que vários elementos opcionais sejam adicionados quando o usuário executar uma única operação de interface do usuário. Essa personalização é importante para fornecer uma ótima experiência do usuário para o usuário comum. 
  
Você também pode criar um formulário usando um XML Web Service existente para fornecer o esquema XML. Para fazer isso:
  
1. Use o UDDI para localizar serviços Web relevantes.
    
2. Selecione o serviço Web a ser usado. O InfoPath lê o arquivo WSDL associado ao serviço Web e identifica o esquema XML a ser usado.
    
3. Abra o esquema XML para carregá-lo.
    
4. Crie um layout dos controles da interface do usuário e associe-os com elementos e atributos do esquema XML.
    
5. Definir como enviar o documento XML para o serviço Web que usa SOAP.
    
Se você deseja criar um formulário a partir do zero e gerar automaticamente o esquema XML:
  
1. Na guia **arquivo** , selecione o modelo formulário **em** branco ou formulário **em branco (InfoPath Filler)** e clique em formulário de **design**.
    
2. Na guia **página inicial** , clique na seta no canto inferior direito do grupo **controles** para exibir o painel de tarefas **controles** e, em seguida, certifique-se de que a caixa de seleção **criar fonte de dados automaticamente** esteja marcada. (Por padrão, essa caixa de seleção está marcada.) 
    
3. Esquematizar os controles da interface do usuário. À medida que você os modela, o InfoPath cria automaticamente o esquema XML e mapeia seus elementos e atributos para os controles da interface do usuário.
    
Para criar um formulário começando com qualquer arquivo de dados XML válido:
  
1. Na guia **arquivo** , selecione o modelo de formulário **XML ou de esquema** e clique em **formulário de design**.
    
2. No **Assistente de fonte de dados**, selecione o arquivo XML que você deseja usar como a fonte de dados. Um esquema XML é criado automaticamente, com base no arquivo de dados XML.
    
3. Crie um layout dos controles da interface do usuário, conforme descrito anteriormente nesta seção.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Projetado como um cliente ideal para serviços Web

O amplo suporte do setor para serviços da Web está se tornando disponível. Muitos sistemas de back-end e de camada intermediária podem ser configurados para se comunicarem usando padrões de serviços Web, como SOAP, UDDI e WSDL. Estes sistemas habilitados para serviços da Web incluem bancos de dados, sistemas de fluxo de trabalho, planejamento de recursos empresariais (ERP), gerenciamento de relacionamento com clientes (CRM) e outros sistemas. Agora, o InfoPath fornece uma interface do usuário ideal para exibir e editar os dados XML que estão sendo enviados por meio de serviços Web. A Figura 4 mostra o suporte integrado para XML Web Services.
  
O InfoPath se ajusta bem ao modelo de serviços da Web menos rígido, no qual os dados são enviados entre computadores como documentos XML completos. Esse modelo de comunicação de alta granularidade se ajusta bem à natureza assíncrona da Web. Como uma ferramenta de criação de alto nível para documentos XML, o InfoPath oferece suporte à codificação SOAP de documento/literal em vez de a codificação SOAP RPC (chamada de procedimento remoto). O InfoPath é um cliente ideal para serviços Web, pois ele pode ler nativamente o esquema XML especificado em uma mensagem SOAP e, em seguida, criar uma interface do usuário com base no esquema, que permite aos usuários exibir e editar facilmente os documentos XML que são gerados ou recebidos pela Web correspondente serviço. O InfoPath também fornece suporte para conjuntos de ADO.NET que incluem controle de alterações.
  
## <a name="terminology"></a>Terminologia

|||
|:-----|:-----|
|**grupo de campos:** <br/> |Uma seção, seção de repetição, seção opcional ou tabela de repetição. Seções e tabelas de repetição são controles em um formulário que contêm outros controles e que se repetem conforme necessário. Os usuários podem inserir várias seções ou linhas ao preencher o formulário.  <br/> |
|**Árvore DOM:** <br/> |A estrutura da fonte de dados do formulário. Em particular, a coleção de campos e grupos que definem e armazenam os dados de um formulário do InfoPath.  <br/> |
   
## <a name="conclusion"></a>Conclusão

O InfoPath usa padrões Open XML para fornecer aos usuários uma edição XML flexível e estruturada para a coleta de dados. Para fornecer uma interface do usuário fácil para visualização e edição de dados XML hierárquicos, grupos de campos aninhados que contenham controles da interface do usuário são mapeados para a árvore DOM. As transformações XSLT permitem que o conteúdo dos modos de exibição da interface do usuário seja organizado de forma diferente da estrutura dos dados XML.
  
O InfoPath fornece mais flexibilidade do que formulários estáticos, com mais edição e validação estruturadas do que documentos do processador de texto. O resultado é uma ferramenta híbrida que combina o melhor de uma experiência de edição de documentos tradicional com os recursos rigorosos de captura de dados de um pacote de formulários, que permite que os usuários comuns criem documentos XML válidos que pertençam a um esquema XML definido por personalizado. O suporte integrado para serviços Web permite definir facilmente modos de exibição para a edição de documentos XML que estão em conformidade com um esquema de serviços Web.
  

