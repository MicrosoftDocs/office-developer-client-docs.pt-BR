---
title: Sobre o suporte do InfoPath para tecnologias XML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 074181a2-3a75-824c-049d-549aabff0f9f
description: Microsoft InfoPath é uma ferramenta de híbrido que combina o melhor de um documento tradicional experiência, como um processador ou aplicativo de email, com os recursos de rigoroso de captura de dados de um pacote de formulários de edição. Este artigo descreve os problemas do InfoPath foi projetado para endereços e explica os princípios de design e padrões do setor de XML usados para resolver esses problemas.
ms.openlocfilehash: 5d7b0bd0de045bdb9ada6946b7142993cd80df0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765600"
---
# <a name="about-infopath-support-for-xml-technologies"></a>Sobre o suporte do InfoPath para tecnologias XML

Microsoft InfoPath é uma ferramenta de híbrido que combina o melhor de um documento tradicional experiência, como um processador ou aplicativo de email, com os recursos de rigoroso de captura de dados de um pacote de formulários de edição. Este artigo descreve os problemas do InfoPath foi projetado para endereços e explica os princípios de design e padrões do setor de XML usados para resolver esses problemas.
  
## <a name="introduction"></a>Introdução

O InfoPath é uma ferramenta de criação de XML alto nível que permite que os usuários finais comuns criar documentos XML que pertencem a um esquema XML personalizadas. Quando o usuário edita um documento XML, as modificações no documento são controladas pelo esquema XML.
  
O usuário interage com o documento XML através de uma exibição rica e formatada que é exibido, aplicando uma folha de estilo XSLT ao documento. Um valor de nó ou atributo de folha do documento XML é exibido como um campo, como uma caixa de texto ou caixa de seleção, enquanto uma hierarquia de nós é processada como um grupo de campos.
  
InfoPath permite validada, estruturados edição de dados XML, mostrando as ações de edição que são válidas para o campo ou grupo de campo que está selecionado no momento. Esta edição estruturado habilita o usuário adicionar e remover os atributos e elementos XML válidos trabalhando com grupos de campos exibidos em modos de exibição dinâmicos avançados, sem ver os elementos e atributos.
  
InfoPath resolve um problema na área de coleta de dados que não pode ser resolvida antes do advento do XML: fornecendo formulários que podem crescer com a adição de grupos de campos que usam o modelo de dados hierárquicos de XML, o InfoPath adiciona a flexibilidade de documentos do word processador para os recursos de validação rigoroso de um aplicativo de formulários. Transformações do XSLT complexas são uma parte integrante dessa solução que fornece dinâmicos e fácil de usar modos de exibição dos dados XML.
  
## <a name="limitations-of-traditional-forms-and-documents-for-gathering-data"></a>Limitações das formas tradicionais e documentos para coleta de dados

Quando a coleta de dados corporativos, os usuários desejam mais flexibilidade do que fornecem de formulários estáticos, mas edição mais estruturada e validação que os documentos do word processador fornecem frequentemente.
  
Formulários tradicionais são estático e limitado de comprimento. Eles têm um número fixo de linhas de repetição e não pode ser estendido quando o formulário está sendo preenchido. Formulários tradicionais são difíceis de usar porque não têm recursos avançados de edição. Muitas vezes, o usuário deve fornecer todas as informações em uma única passagem.
  
Por outro lado, o tradicionais documentos criados usando-se um processador de texto habilitar o usuário livremente adicionar e remover o conteúdo, mas oferecem pouca orientação sobre como inserir completa, estruturado e informações válidas; todos os campos que são definidos no documento tiverem um mínimo ou nenhuma validação de valores de dados e tipos de dados. Dados nos campos não estão rotulados corretamente para permitir a reutilização de fácil referência e automática. Os dados são livres ao invés estruturado; Você não pode agrupar informações, como a aplicação de um rótulo "Address" a um grupo de campos "Street", "City" e "Estado".
  
Assim, há uma necessidade para tais edição flexível ainda estruturado, mas porque esse tipo de tecnologia não estava disponível antes do advento do XML, os desenvolvedores tiveram que criar aplicativos personalizados, que requer códigos extensos. Aplicativos personalizados são caros e difíceis de modificar e exigem a codificação personalizada para validação. Aplicativos personalizados normalmente exigem o treinamento do usuário final, e é difícil reutilizar os dados resultantes para outros processos de negócios.
  
## <a name="providing-structured-editing-by-displaying-xml-data-as-field-groups"></a>Fornecimento de edição estruturado exibindo dados XML como grupos de campo

Um problema de design técnico importantes que tiveram de ser resolvidos era como fornecer uma interface de usuário fácil para adicionar e remover os elementos e atributos, XML sem mostrando os elementos e atributos, mas manter a árvore DOM válido de acordo com o XML personalizadas esquema. A interface de usuário necessária para oferecer uma maneira natural para editar a árvore DOM que inclui inserindo subárvores opcionais, substituindo escolhas de subárvores e estendendo subárvores existentes.
  
Para fornecer essa interface de usuário fácil, uma subárvore DOM é exibida como um grupo de campo ou seção. Um grupo de campo é um grupo de controles de interface do usuário, como caixas de texto e listas suspensas e serve como uma interface de usuário fácil que permite ao usuário visualizar e editar dados XML hierárquicos. Um grupo de campo pode conter outros grupos de campo e pode ser opcional ou repetitivo, assim como uma subárvore DOM pode conter outros subárvores e pode ser opcional ou repetição. Uma subárvore é adicionada à árvore DOM quando o usuário posiciona o ponteiro do mouse sobre um grupo de campo, clicar no menu suspenso que aparece no grupo de campo e, em seguida, seleciona **Inserir \<nome do grupo de campo\>**.
  
O InfoPath fornece essa edição estruturado de dados XML usando o esquema XML especificado para restringir e guia de edição. O esquema controla se os comandos **Inserir** e **Remover** serão exibidos no menu suspenso para um grupo de campo. O esquema também é usado para validação. Para habilitar a edição de um documento XML para o qual não há um esquema XML, o InfoPath pode gerar um esquema do documento XML. 
  
## <a name="providing-easy-to-use-views-of-xml-data-by-using-xslt-transformations"></a>Fornecendo fácil de usar exibições de dados XML usando XSLT Transformations

Outro desafio de design técnico que precisam ser resolvidos era como habilitar o conteúdo dos modos de exibição da interface do usuário seja organizado muito diferente a estrutura dos dados XML. Para apresentar os dados de uma forma que faz mais sentido para o usuário e permite ao usuário ler facilmente e editar os dados, o designer deve ser capaz de exibir dados em uma sequência diferente vez na árvore de dados de DOM, omita alguns dados a partir de um modo de exibição , reorganizar nós da árvore de dados adjacentes em modos de exibição separados e coletar dados de diferentes partes da árvore de dados em um modo de exibição único.
  
A ordem e a estrutura do conteúdo dos modos de exibição, portanto, devem ser independentes da ordem e da estrutura de nós da árvore DOM. Essa independência estrutural de apresentação e dados requer um complexo dinâmico associando ou o mapeamento entre os campos agrupados nos modos de exibição e os nós em árvore DOM.
  
Para fornecer esse mapeamento complexo entre modos de exibição e de dados, o InfoPath usa extensivamente transformações XSLT (XSL). XSLT é uma linguagem de folha de estilo poderosa que suporta XSLT transformations complexas e suporta ricos modos de exibição com a apresentação dinâmica e flexível de conteúdo. Um arquivo XSLT é usado para cada modo de exibição. Usando um estilo folha é uma aproximação de design comum e bem estabelecidas no SGML e ferramentas de criação de XML e XSLT é o padrão de W3C para folhas de estilo que são usadas para esse tipo de transformação complexa.
  
Para evitar que executa a transformação XSLT toda toda vez que o usuário modifica a estrutura de uma subárvore no DOM, algoritmos são usados para determinar qual parte do modo de exibição deve ser atualizada. Em seguida, somente a parte relevante da folha de estilo XSLT será aplicada e a parte afetada do modo de exibição for atualizada.
  
## <a name="how-xml-standards-are-used-when-editing-a-form"></a>Como os padrões XML são usados durante a edição de um formulário

InfoPath é criado com base em padrões XML que inclui o seguinte:
  
- Extensible Markup Language (XML) 1.0 Second Edition
    
- Namespaces em XML
    
- XML Path Language (XPath) 1.0
    
- Esquema XML (XSD) 1.0 parte 1: estruturas e parte 2: tipos de dados
    
- Extensible Stylesheet Language Transformations (XSLT) 1.0
    
- Hypertext Extensible Markup Language (XHTML) 1.0
    
- Folhas de estilo em cascata (CSS)
    
- Modelo de objeto de documento (DOM) 1.0
    
- Assinaturas digitais de XML (XML DSig)
    
- Simple Object Access Protocol (SOAP) 1.1
    
- Web Services Description Language (WSDL) 1.1
    
- Descrição universal, descoberta e integração (UDDI) 1.0
    
Por exemplo, o InfoPath usa e gera arquivos XML, XSLT e XSD padrão que podem ser reutilizados em vários processos de negócios. InfoPath usa MSXML, o SOAP Toolkit e o namespace System. XML do .NET para dar suporte a esses padrões e fornece suporte integrado completo para serviços Web XML.
  
A Figura 1 mostra o menu suspenso sensível ao contexto para um grupo de campo do **cliente** , que permite que o usuário adicione outro grupo de campo do **cliente** , remover este grupo de campo do **cliente** , inserir uma linha do **item** na tabela de itens de compra em Este grupo de campo, ou inserir um grupo de campo opcional **ações** dentro desse grupo de campos. No link **clique aqui** oferece outra maneira de inserir grupo **ações** de campo. Um menu de menu suspenso mais curto aparece em cada linha de item de compra. 
  
1. No InfoPath, o usuário cria um novo documento XML com base em um modelo de formulário do InfoPath, ou abre um documento XML existente que se baseia em um modelo de formulário. O documento XML é um arquivo de dados XML que contém uma referência ao modelo de formulário e pode usar espaços para nome XML. 
    
    Um modelo de formulário é o conjunto de arquivos que fornecem estruturado a edição de documentos XML que estão em conformidade com um esquema específico de XML personalizadas. Os arquivos que compõem o modelo de formulário podem ser empacotados como arquivos individuais dentro de uma pasta comum ou como arquivos que residem em uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão e assemblies de código de arquivos, como gerenciado suporte opcional.
    
2. Se o documento XML é assinado digitalmente usando assinatura XML, o InfoPath confirma que o arquivo XML é consistente, antes que ele é aberto.
    
3. InfoPath cria uma árvore de dados DOM do XML documento na memória.
    
4. Transformações XSLT são aplicadas a árvore DOM, produzindo modos de exibição que mostram uma apresentação apropriada do documento para o usuário. Elementos no início do documento XML poderiam ser exibidos na parte inferior do modo de exibição e também em uma organização diferente em outro modo de exibição. Os modos de exibição consistem em contêineres de interface do usuário como seções que contêm texto e controles, como caixas de texto, caixas de rich text, escolha de data e listas suspensas. Contêineres também podem conter outros contêineres.
    
5. Transformação XSLT produz XHTML como saída e, em seguida, uma CSS é usada para controlar a apresentação do XHTML.
    
6. Se o esquema XML permite a adição de nós para um nó da árvore de dados, no campo ou grupo de campo que é mapeado para o nó tem um menu suspenso que permite ao usuário adicionar ou remover grupos de campo. O usuário edita o documento, adicionando um grupo de campos de repetição ou opcional, inserindo um valor, selecionando uma opção ou inserindo RTF. Se um nó de esquema XML está associado com o esquema para o XHTML, o InfoPath apresenta uma interface do usuário para a criação de rich text. Quando o usuário insere RTF, o conteúdo XHTML é criado como uma subárvore no DOM.
    
7. A árvore DOM sempre é mantida válida. À medida que o usuário edita o documento XML, as edições são validadas no esquema XML associado. A tentativa de alteração para os valores de nó de folha e a estrutura do DOM é validada no esquema XML para garantir que seus valores e tipos de dados são válidos. Se a tentativa de alteração forem inválida, abre uma caixa de diálogo de validação e as alterações não são aplicadas à árvore DOM. Se as alterações forem válidas, a árvore DOM será atualizada.
    
8. A parte alterada do modo de exibição é atualizada, aplicando apenas as partes necessárias da folha de estilo XSLT à árvore DOM.
    
9. O usuário pode salvar o documento XML ou enviar o documento XML usando SOAP ou HTTP sem formatação. O usuário não é permitido para enviar o documento, a menos que ele seja válido de acordo com o esquema XML.
    
## <a name="how-xml-standards-are-used-when-designing-a-form"></a>Como os padrões XML são usados durante a criação de um formulário

Você pode criar um formulário, iniciando com um esquema XML existente, conectando a um banco de dados ou serviço Web XML e obtendo seu esquema XML ou gerando automaticamente um esquema, a partir de um novo formulário ou de um arquivo de dados XML. Esses cenários estão descritos nos procedimentos a seguir. A Figura 3 mostra a interface de usuário básica para projetar um modelo de formulário.
  
1. Criar um novo formulário no Designer do InfoPath, selecionando o modelo de formulário **XML ou esquema** e, em seguida, selecione um arquivo de esquema XML existente como a fonte de dados. O esquema XML é carregado no painel de tarefas e exibido como um controle de árvore. 
    
2. Use as ferramentas de design de layout para dispor os controles da interface do usuário, como linhas e o design de plano de fundo, em um ou mais modos de exibição. Isso gerará alguns dos elementos XSLT. Os modos de exibição do XSLT e o esquema XML são automaticamente associados com o modelo de formulário.
    
3. Mapear os elementos de esquema XML para os controles de interface do usuário nos modos de exibição usando o recurso de arrastar e soltar. InfoPath ajuda você a escolher os controles apropriados para os elementos de esquema XML, com base no tipo de elementos do esquema. Por exemplo, se o tipo de dados XML for Data, o InfoPath sugere um controle de selecionador de data. Com base em escolhas no esquema XML, o InfoPath pode inserir grupos de campos opcionais ou repetição. Mapeando os elementos de esquema XML para os controles de interface do usuário gera a estrutura do XSLT.
    
4. Salve o modelo de formulário. Você pode salvar os arquivos que compõem o modelo de formulário como arquivos individuais em uma pasta regular ou como arquivos dentro de uma pasta de gabinete. Em ambos os casos, os arquivos são arquivos XML padrão. O modelo de formulário agora está pronto para uso do usuário.
    
Um modelo de formulário contém todas as informações de semânticas que não é necessário para fornecer a edição estruturado quando um formulário é aberto no InfoPath. Um modelo de formulário inclui um arquivo de manifesto, os arquivos XSLT que definem os modos de exibição, as informações que é necessário para validar dados e um identificador de recurso opcional para um serviço Web XML.
  
O manifesto, ou arquivo de definição de formulário, é o ponto de entrada e de hub comuns para todos os arquivos que são exigidos pelo modelo de formulário. O manifesto contém referências aos outros arquivos no modelo de formulário e contém as informações que é necessário para validar dados e fornecer a edição estruturado. As informações de validação do esquema XML são personalizadas para a interface do usuário resultante e são adicionadas ao arquivo de manifesto. Por exemplo, se o esquema permitir inserindo vários elementos opcionais de uma subárvore específica, você pode projetar a interface do usuário para que os vários elementos opcionais são adicionados quando o usuário executa uma única operação de interface do usuário. Essa personalização é importante para fornecer uma experiência de usuário excelente para o usuário comum. 
  
Você também pode criar um formulário usando um serviço Web XML existente para fornecer o esquema XML. Para fazer isso:
  
1. Use UDDI para localizar serviços da Web relevantes.
    
2. Selecione o serviço Web para usar. InfoPath lê o arquivo WSDL associado ao serviço Web e identifica o esquema XML a ser usado.
    
3. Abra o esquema XML para carregá-la.
    
4. Dispor os controles da interface do usuário e associá-los com os atributos e elementos de esquema XML.
    
5. Defina como enviar o documento XML para o serviço Web que usa SOAP.
    
Se você deseja criar um formulário do zero e gerar automaticamente o esquema XML:
  
1. Na guia **arquivo** , selecione o **Formulário em branco** ou um **Formulário em branco (InfoPath Filler)** de modelo de formulário e clique em **Design do formulário**.
    
2. Na guia **página inicial** , clique na seta no canto inferior direito do grupo de **controles** para exibir o painel de tarefas de **controles** e, em seguida, verifique se a caixa de seleção **criar automaticamente a fonte de dados** está selecionada. (Por padrão, essa caixa de seleção está selecionada.) 
    
3. Dispor os controles de interface do usuário. Conforme você posicioná-los, InfoPath automaticamente cria o esquema XML e mapeia seus elementos e atributos para os controles de interface do usuário.
    
Para criar um formulário, iniciando com qualquer arquivo de dados XML bem formado:
  
1. Na guia **arquivo** , selecione o modelo de formulário **XML ou esquema** e, em seguida, clique em **Design do formulário**.
    
2. No **Assistente de fonte de dados**, selecione o arquivo XML que você deseja usar como fonte de dados. Um esquema XML é criado automaticamente, com base no arquivo de dados XML.
    
3. Dispor os controles de interface do usuário, conforme descrito anteriormente nesta seção.
    
## <a name="designed-as-an-ideal-client-for-web-services"></a>Projetado como um cliente Ideal para serviços Web

Amplo suporte no setor para serviços Web está se tornando disponível. Muitos sistemas de back-end e de camada intermediária podem ser configurados para se comunicar usando padrões de serviços da Web como SOAP, WSDL e UDDI. Esses sistemas de habilitado para serviços da Web incluem bancos de dados, sistemas de fluxo de trabalho, (ERP) de planejamento de recursos corporativos, gerenciamento de relacionamento do cliente (CRM) e outros sistemas. Agora, o InfoPath fornece uma interface de usuário ideal para exibir e editar os dados XML que está sendo enviados pelos serviços da Web. Figura 4 mostra o suporte integrado para serviços Web XML.
  
InfoPath se encaixa bem com o modelo de menos rígido dos serviços da Web, no qual os dados são enviados entre computadores como documentos do XML concluídos. Este modelo de comunicações menos elaboradas se encaixa bem com a natureza assíncrona da Web. Como uma ferramenta de criação alto nível para documentos XML, o InfoPath oferece suporte a codificação de documento/literal SOAP em vez de codificação SOAP de chamada de procedimento remoto (RPC). InfoPath é um cliente ideal para serviços da Web, porque ele nativamente pode ler o esquema XML especificado em uma mensagem SOAP e, em seguida, criar uma interface do usuário com base no esquema, o que permite aos usuários exibir e editar documentos XML que são gerados ou recebidos por Web correspondente facilmente serviço. InfoPath também oferece suporte para conjuntos de dados ADO.NET que inclui o controle de alterações.
  
## <a name="terminology"></a>Terminologia

|||
|:-----|:-----|
|**grupo de campo:** <br/> |Uma seção, seção de repetição, seção opcional ou tabela de repetição. Seções e tabelas de repetição são controles em um formulário que contêm outros controles e que Repita conforme necessário. Os usuários podem inserir várias seções ou linhas durante o preenchimento do formulário.  <br/> |
|**Árvore DOM:** <br/> |A estrutura da fonte de dados do formulário. Em particular, a coleção de campos e grupos que definem e armazenam os dados de um formulário do InfoPath.  <br/> |
   
## <a name="conclusion"></a>Conclusão

Para fornecer aos usuários flexível ainda estruturado edição de XML para coleta de dados, o InfoPath usa os padrões do open XML. Para fornecer uma interface de usuário fácil para a visualização e edição de dados XML hierárquicos, grupos aninhados do campo que contém os controles da interface do usuário são mapeados para a árvore DOM. Transformações XSLT habilite o conteúdo dos modos de exibição da interface do usuário sejam organizados de forma diferente a estrutura dos dados XML.
  
O InfoPath fornece mais flexibilidade do que formulários estáticos, com mais estruturada edição e validação de que os documentos do processador de texto. O resultado é uma ferramenta de híbrido que combina o melhor de um documento tradicional experiência com os recursos de rigoroso de captura de dados de um pacote de formulários, que permite que os usuários comuns criar documentos XML válidos que pertencem a um esquema XML personalizadas de edição. Suporte integrado para serviços Web permite determinantes facilmente modos de exibição para edição de documentos XML que estão em conformidade com um esquema de serviços da Web.
  

