---
title: Sobre o suporte do InfoPath para tecnologias XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: O Microsoft InfoPath é uma ferramenta híbrida que combina o melhor de uma experiência tradicional de edição de documentos, como um processador de palavras ou aplicativo de email, com os rigorosos recursos de captura de dados de um pacote de formulários. Este artigo descreve os problemas que o InfoPath foi projetado para resolver e explica os princípios de design e os padrões do setor XML usados para resolver esses problemas.
ms.openlocfilehash: 20831635fba8d76b9d6b45f42a5308ab7236db20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407225"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Sobre o suporte do InfoPath para tecnologias XML

O Microsoft InfoPath é uma ferramenta híbrida que combina o melhor de uma experiência tradicional de edição de documentos, como um processador de palavras ou aplicativo de email, com os rigorosos recursos de captura de dados de um pacote de formulários. Este artigo descreve os problemas que o InfoPath foi projetado para resolver e explica os princípios de design e os padrões do setor XML usados para resolver esses problemas.
  
## <a name="introduction"></a>Introdução

O InfoPath é uma ferramenta de criação de XML de alto nível que permite aos usuários finais comuns criar documentos XML que pertencem a um esquema XML definido de forma personalizada. Quando o usuário edita um documento XML, as modificações no documento são controladas pelo esquema XML.
  
O usuário interage com o documento XML por meio de uma exibição rica e formatada exibida aplicando uma folha de estilos XSLT ao documento. Um nó folha ou um valor de atributo do documento XML é exibido como um campo, como uma caixa de texto ou uma caixa de seleção, enquanto uma hierarquia de nós é renderizada como um grupo de campos.
  
O InfoPath permite a edição validada e estruturada de dados XML mostrando as ações de edição válidas para o campo ou grupo de campos atualmente selecionado. Essa edição estruturada permite que o usuário adicione e remova atributos e elementos XML válidos trabalhando com grupos de campos exibidos em exibições dinâmicas, sem ver os elementos e atributos.
  
O InfoPath resolve um problema na área de coleta de dados que não pôde ser resolvido antes do advento do XML: fornecendo formulários que podem crescer adicionando grupos de campos que usam o modelo de dados hierárquico de XML, o InfoPath adiciona a flexibilidade dos documentos do processador de palavras aos rigorosos recursos de validação de um aplicativo de formulários. Transformações XSLT complexas são uma parte integral dessa solução que fornece exibições dinâmicas e fáceis de usar dos dados XML.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Limitações de formulários e documentos tradicionais para coleta de dados

Ao coletar dados corporativos, os usuários geralmente querem mais flexibilidade do que os formulários estáticos fornecem, mas a edição e validação são mais estruturadas do que os documentos do processador do Word fornecem.
  
Os formulários tradicionais são estáticos e limitados em comprimento. Eles têm um número fixo de linhas repetitivas e não podem ser estendidos quando o formulário está sendo preenchido. Formulários tradicionais são difíceis de usar porque não têm recursos avançados de edição. Muitas vezes, o usuário deve fornecer todas as informações em uma única passagem.
  
Por outro lado, documentos tradicionais criados usando um processador de palavras permitem que o usuário adicione e remova conteúdo livremente, mas fornece pouca orientação sobre como inserir informações completas, estruturadas e válidas; quaisquer campos definidos no documento têm validação mínima ou não de valores de dados e tipos de dados. Os dados nos campos não são rotulados corretamente para habilitar a referência fácil e a reutilização automática. Os dados são de forma livre em vez de estruturados; você não pode agrupar informações, como a aplicação de um rótulo "Address" a um grupo de campos "Street", "City" e "State".
  
Portanto, há uma necessidade de edição tão flexível, mas estruturada, mas como esse tipo de tecnologia não estava disponível antes do advento do XML, os desenvolvedores precisaram criar aplicativos personalizados, que exigem codificação extensiva. Aplicativos personalizados são caros e difíceis de modificar e exigem codificação personalizada para validação. Os aplicativos personalizados geralmente exigem treinamento do usuário final e é difícil reutilizar os dados resultantes de outros processos empresariais.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Fornecendo edição estruturada exibindo dados XML como grupos de campos

Um importante problema de design técnico que precisava ser resolvido era como fornecer uma interface de usuário fácil para adicionar e remover atributos e elementos XML, sem mostrar os elementos e atributos, mas manter a árvore DOM válida de acordo com o esquema XML definido de forma personalizada. A interface do usuário precisava fornecer uma maneira natural de editar a árvore dom que inclui a inserção de subárvore opcionais, substituição de escolhas de subárvores e extensão de subárvores existentes.
  
Para fornecer essa interface de usuário fácil, uma subárvore DOM é exibida como um grupo de campos ou seção. Um grupo de campos é um grupo de controles de interface do usuário, como caixas de texto e listas de lista, e serve como uma interface de usuário fácil que permite ao usuário visualizar e editar dados XML hierárquicos. Um grupo de campos pode conter outros grupos de campos e pode ser opcional ou repetido, assim como uma subárvore DOM pode conter outras subárvores e pode ser opcional ou repetido. Uma subárvore é adicionada à árvore DOM quando o usuário coloca o ponteiro do mouse sobre um grupo de **\< \>** campos, clica no menu suspenso que aparece no grupo de campos e seleciona Inserir nome do grupo de campos.
  
O InfoPath fornece essa edição estruturada de dados XML usando o esquema XML especificado para restringir e orientar a edição. O esquema controla se os comandos **Inserir** e **Remover** aparecem no menu suspenso de um grupo de campos. O esquema também é usado para validação. Para habilitar a edição de um documento XML para o qual não há esquema XML, o InfoPath pode gerar um esquema a partir do documento XML. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Fornecendo exibições fáceis de usar de dados XML usando transformações XSLT

Outro desafio de design técnico que precisava ser resolvido era como permitir que o conteúdo das exibições da interface do usuário fosse organizado de maneira muito diferente da estrutura dos dados XML. Para apresentar os dados de uma maneira que faça mais sentido para o usuário e permite que o usuário leia e edite facilmente os dados, o designer deve ser capaz de exibir dados em uma sequência diferente da da árvore de dados DOM, omitir alguns dados de um modo de exibição, reorganizar nós de árvore de dados adjacentes em exibições separadas e coletar dados de diferentes partes da árvore de dados em um único modo de exibição.
  
Portanto, a ordem e a estrutura do conteúdo dos modo de exibição devem ser independentes da ordem e da estrutura dos nós de árvore DOM. Essa independência estrutural da apresentação e dos dados requer uma associação ou mapeamento complexo e dinâmico entre os campos agrupados nos modo de exibição e os nós na árvore DOM.
  
Para fornecer esse mapeamento complexo entre exibições e dados, o InfoPath usa extensivamente xSL Transformations (XSLT). O XSLT é uma linguagem de folha de estilos poderosa que oferece suporte a transformações XSLT complexas e oferece suporte a exibições rich com apresentação dinâmica e flexível de conteúdo. Um arquivo XSLT é usado para cada exibição. O uso de uma folha de estilos é uma abordagem de design comum e bem estabelecida em ferramentas de criação de SGML e XML, e o XSLT é o padrão W3C para folhas de estilo que são usadas para esse tipo de transformação complexa.
  
Para evitar a execução de toda a transformação XSLT sempre que o usuário modifica a estrutura de uma subárvore no DOM, os algoritmos são usados para determinar qual parte da exibição deve ser atualizada. Em seguida, apenas a parte relevante da folha de estilos XSLT é aplicada, e a parte afetada do exibição é atualizada.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Como os padrões XML são usados ao editar um formulário

O InfoPath foi criado desde o zero em padrões XML que incluem o seguinte:
  
- Extensible Markup Language (XML) 1.0 Second Edition
    
- Namespaces em XML
    
- Xml Path Language (XPath) 1.0
    
- Esquema XML (XSD) 1.0 Parte 1: estruturas e parte 2: tipos de dados
    
- Extensible Stylesheet Language Transformations (XSLT) 1.0
    
- Extensible Hypertext Markup Language (XHTML) 1.0
    
- CSS (Folhas de Estilos em Cascata)
    
- Dom (Modelo de Objeto do Documento) 1.0
    
- XML Digital Signatures (XML DSig)
    
- Simple Object Access Protocol (SOAP) 1.1
    
- Web Services Description Language (WSDL) 1.1
    
- Descrição Universal, Descoberta e Integração (UDDI) 1.0
    
Por exemplo, o InfoPath usa e gera arquivos XML, XSLT e XSD padrão que podem ser reutilizados em vários processos empresariais. O InfoPath usa o MSXML, o SOAP Toolkit e o namespace .NET System.XML para dar suporte a esses padrões e fornece suporte integrado completo para serviços Web XML.
  
A Figura 1 mostra o menu suspenso sensível ao contexto de um grupo  de campo do  cliente, que permite que o usuário adicione outro grupo de campo  do cliente, remova esse grupo de campos de cliente, insira uma linha de **item** na tabela de itens de compra neste grupo de campo ou insira um grupo de campo de ações opcionais dentro desse grupo de campo.  O **link Clique aqui** fornece outra maneira de inserir o grupo de **campos** de ações. Um menu suspenso mais curto aparece em cada linha de item de compra. 
  
1. No InfoPath, o usuário cria um novo documento XML com base em um modelo de formulário do InfoPath ou abre um documento XML existente baseado em um modelo de formulário. O documento XML é um arquivo de dados XML que contém uma referência ao modelo de formulário e pode usar namespaces XML. 
    
    Um modelo de formulário é o conjunto de arquivos que fornecem edição estruturada de documentos XML que estão em conformidade com um esquema XML específico definido de forma personalizada. Os arquivos que formam o modelo de formulário podem ser empacotados como arquivos individuais dentro de uma pasta comum ou como arquivos residindo em uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão e arquivos de suporte opcionais, como assemblies de código gerenciado.
    
2. Se o documento XML for assinado digitalmente usando assinatura XML, o InfoPath confirmará que o arquivo XML é consistente antes de ser aberto.
    
3. O InfoPath cria uma árvore de dados DOM do documento XML na memória.
    
4. Transformações XSLT são aplicadas à árvore DOM, produzindo exibições que mostram uma apresentação apropriada do documento ao usuário. Elementos no início do documento XML podem ser exibidos na parte inferior do modo de exibição e também em uma organização diferente em outro modo de exibição. As exibições consistem em contêineres de interface do usuário, como seções que contêm texto e controles, como caixas de texto, caixas rich text, setores de data e listas de lista. Os contêineres também podem conter outros contêineres.
    
5. A transformação XSLT produz XHTML como saída e, em seguida, um CSS é usado para controlar a apresentação do XHTML.
    
6. Se o esquema XML permitir a adição de nós a um nó da árvore de dados, o campo ou grupo de campos mapeado para o nó terá um menu suspenso que permite ao usuário adicionar ou remover grupos de campos. O usuário edita o documento adicionando um grupo de campos repetitivo ou opcional, inserindo um valor, selecionando uma opção ou inserindo rich text. Se um nó de esquema XML estiver associado ao esquema para XHTML, o InfoPath apresentará uma interface do usuário para criar rich text. Quando o usuário inser rich text, o conteúdo XHTML é criado como uma subárvore no DOM.
    
7. A árvore DOM é sempre mantida válida. Conforme o usuário edita o documento XML, as edições são validadas em relação ao esquema XML associado. As tentativas de alterações na estrutura DOM e nos valores do nó folha são validadas em relação ao esquema XML para garantir que seus tipos de dados e valores sejam válidos. Se as tentativas de alterações são inválidas, uma caixa de diálogo de validação é aberta e as alterações não são aplicadas à árvore DOM. Se as alterações são válidas, a árvore DOM é atualizada.
    
8. A parte alterada do exibição é atualizada, aplicando apenas as partes necessárias da folha de estilos XSLT à árvore DOM.
    
9. O usuário pode salvar o documento XML ou enviar o documento XML usando HTTP ou SOAP simples. O usuário não tem permissão para enviar o documento, a menos que ele seja válido de acordo com o esquema XML.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Como os padrões XML são usados ao criar um formulário

You can design a form by starting with an existing XML schema, by connecting to an XML Web service or database and obtaining its XML schema, or by automatically generating a schema from a new form or from an XML data file. Esses cenários são descritos nos procedimentos a seguir. A Figura 3 mostra a interface do usuário básica para projetar um modelo de formulário.
  
1. Crie um novo formulário no InfoPath Designer selecionando o modelo de formulário **XML** ou esquema e selecione um arquivo de esquema XML existente como fonte de dados. O esquema XML é carregado no painel de tarefas e mostrado como um controle de árvore. 
    
2. Use as ferramentas de layout de design para estruturar os controles da interface do usuário, como linhas e o design de plano de fundo, em um ou mais exibições. Isso gera alguns dos elementos XSLT. Os exibições XSLT e o esquema XML são associados automaticamente ao modelo de formulário.
    
3. Mapeie os elementos de esquema XML para os controles da interface do usuário nos visualizações usando arrastar e soltar. O InfoPath ajuda você a escolher os controles apropriados para os elementos de esquema XML, com base no tipo de elementos de esquema. Por exemplo, se o tipo de dados XML for data, o InfoPath sugerirá um controle selador de data. Com base nas opções no esquema XML, o InfoPath pode inserir grupos de campos opcionais ou repetidos. Mapear os elementos de esquema XML para os controles da interface do usuário gera a estrutura XSLT.
    
4. Salve o modelo de formulário. Você pode salvar os arquivos que formam o modelo de formulário como arquivos individuais em uma pasta regular ou como arquivos dentro de uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão. O modelo de formulário agora está pronto para ser usado pelo usuário.
    
Um modelo de formulário contém todas as informações semânticas necessárias para fornecer edição estruturada quando um formulário é aberto no InfoPath. Um modelo de formulário inclui um arquivo de manifesto, os arquivos XSLT que definem as exibições, as informações necessárias para validar dados e um identificador de recurso opcional para um serviço Web XML.
  
O manifesto, ou arquivo de definição de formulário, é o hub e ponto de entrada comuns para todos os arquivos exigidos pelo modelo de formulário. O manifesto contém referências a outros arquivos no modelo de formulário e contém as informações necessárias para validar dados e fornecer edição estruturada. As informações de validação do esquema XML são personalizadas para a interface do usuário resultante e adicionadas ao arquivo de manifesto. Por exemplo, se o esquema permitir a inserção de vários elementos opcionais em uma subárvore específica, você poderá projetar a interface do usuário para que vários elementos opcionais sejam adicionados quando o usuário executar uma única operação de interface do usuário. Essa personalização é importante para proporcionar uma ótima experiência de usuário para o usuário comum. 
  
Você também pode criar um formulário usando um serviço Web XML existente para fornecer o esquema XML. Para fazer isso:
  
1. Use UDDI para localizar serviços Web relevantes.
    
2. Selecione o serviço Web a ser usado. O InfoPath lê o arquivo WSDL associado ao serviço Web e identifica o esquema XML a ser usado.
    
3. Abra o esquema XML para carregá-lo.
    
4. Associe os controles da interface do usuário a elementos e atributos do esquema XML.
    
5. Defina como enviar o documento XML para o serviço Web que usa SOAP.
    
Se você quiser criar um formulário do zero e gerar automaticamente o esquema XML:
  
1. Na guia **Arquivo,** selecione  o modelo de formulário Formulário em Branco ou Formulário em Branco **(InfoPath Filler)** e clique em **Design Form**.
    
2. Na guia **Página** Base, clique na seta no canto inferior  direito do grupo Controles para  exibir o painel de tarefas Controles e verifique se a caixa de seleção Criar automaticamente a fonte de dados está marcada.  (Por padrão, essa caixa de seleção está marcada.) 
    
3. Desemita os controles da interface do usuário. Conforme você os cria, o InfoPath cria automaticamente o esquema XML e mapeia seus elementos e atributos para os controles da interface do usuário.
    
Para criar um formulário começando com qualquer arquivo de dados XML bem formado:
  
1. Na guia **Arquivo,** selecione o **modelo de formulário XML** ou esquema e clique em Design **Form**.
    
2. No Assistente **de Fonte de Dados,** selecione o arquivo XML que você deseja usar como fonte de dados. Um esquema XML é criado automaticamente, com base no arquivo de dados XML.
    
3. Descreva os controles de interface do usuário conforme descrito anteriormente nesta seção.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Projetado como um cliente ideal para serviços Web

O suporte amplo a todo o setor para serviços Web está se tornando disponível. Muitos sistemas back-end e de camada intermediária podem ser configurados para se comunicar usando padrões de serviços Web, como SOAP, UDDI e WSDL. Esses sistemas habilitados para serviços Web incluem bancos de dados, sistemas de fluxo de trabalho, ERP (planejamento de recursos empresariais), CRM (gerenciamento de relacionamento com o cliente) e outros sistemas. Agora, o InfoPath fornece uma interface do usuário ideal para exibir e editar os dados XML que estão sendo enviados por meio de serviços Web. A Figura 4 mostra o suporte integrado para serviços Web XML.
  
O InfoPath se encaixa bem com o modelo de serviços Web menos relacionados, no qual os dados são enviados entre computadores como documentos XML completos. Esse modelo de comunicação se ajusta bem à natureza assíncrona da Web. Como uma ferramenta de autoria de alto nível para documentos XML, o InfoPath dá suporte à codificação SOAP de documento/literal em vez da codificação SOAP RPC (Remote Procedure Call). O InfoPath é um cliente ideal para serviços Web, porque ele pode ler na verdade o esquema XML especificado em uma mensagem SOAP e criar uma interface do usuário com base no esquema, que permite aos usuários exibir e editar facilmente documentos XML gerados ou recebidos pelo serviço Web correspondente. O InfoPath também fornece suporte para ADO.NET DataSets que inclui o controle de alterações.
  
## <a name="terminology"></a>Terminologia

|||
|:-----|:-----|
|**grupo de campos:** <br/> |Uma seção, seção repetida, seção opcional ou tabela de repetição. Seções e tabelas de repetição são controles em um formulário que contêm outros controles e que se repetem conforme necessário. Os usuários podem inserir várias seções ou linhas ao preencher o formulário.  <br/> |
|**Árvore DOM:** <br/> |A estrutura da fonte de dados do formulário. Em particular, o conjunto de campos e grupos que definem e armazenam os dados de um formulário do InfoPath.  <br/> |
   
## <a name="conclusion"></a>Conclusão

O InfoPath usa padrões XML abertos para fornecer aos usuários edição XML flexível, mas estruturada, para coleta de dados. Para fornecer uma interface do usuário fácil para visualizar e editar dados XML hierárquicos, os grupos de campos aninhados que contêm controles de interface do usuário são mapeados para a árvore DOM. As transformações XSLT permitem que o conteúdo das exibições da interface do usuário seja organizado de forma diferente da estrutura dos dados XML.
  
O InfoPath oferece mais flexibilidade do que os formulários estáticos, com edição e validação mais estruturadas do que documentos do processador do Word. O resultado é uma ferramenta híbrida que combina o melhor de uma experiência tradicional de edição de documentos com os rigorosos recursos de captura de dados de um pacote de formulários, que permite que usuários comuns criem documentos XML válidos que pertencem a um esquema XML definido de forma personalizada. O suporte integrado para serviços Web permite definir facilmente exibições para edição de documentos XML que estão em conformidade com um esquema de serviços Web.
  

