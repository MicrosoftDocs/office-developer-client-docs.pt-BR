---
title: Enumerações (referência do desenvolvedor do OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: Este tópico descreve as enumerações no modelo de objeto do OneNote 2013.
ms.openlocfilehash: 3338e444e5b0bfd0239e363c3161aeb1914b2d53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410333"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumerações (referência do desenvolvedor do OneNote)

Este tópico descreve as enumerações no modelo de objeto do OneNote 2013.
  
## <a name="createfiletype"></a>CreateFiletype
<a name="odc_CreateFileType"> </a>

Quando passado para o método **OpenHierarchy** , especifica o tipo de objeto a ser criado, se houver, se o caminho passado para o método ainda não existir. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**cftNone** <br/> |,0  <br/> |Não cria nenhum objeto novo.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Cria um bloco de anotações usando o nome e o local especificados.  <br/> |
|**cftFolder** <br/> |duas  <br/> |Cria um grupo de seção usando o nome e o local especificados.  <br/> |
|**cftSection** <br/> |3D  <br/> |Cria uma seção usando o nome e o local especificados.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica o local encaixado de uma janela do OneNote 2013 usando a interface de [janela](window-interfaces-onenote.md) . Quando definido como a propriedade **DockedLocation** , especifica o local no qual uma janela do OneNote será encaixada. Essa enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |A janela do OneNote é encaixada no local padrão na área de trabalho.  <br/> |
|**dlLeft** <br/> |1  <br/> |A janela do OneNote é encaixada no lado esquerdo da área de trabalho.  <br/> |
|**dlRight** <br/> |duas  <br/> |A janela do OneNote é encaixada no lado direito da área de trabalho.  <br/> |
|**dlTop** <br/> |3D  <br/> |A janela do OneNote é encaixada na parte superior da área de trabalho.  <br/> |
|**dlBottom** <br/> |4   <br/> |A janela do OneNote é encaixada na parte inferior da área de trabalho.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Quando passado para o método **SetFilingLocation** , especifica qual tipo de conteúdo o local de arquivamento é definido quando o tipo de conteúdo é enviado para o OneNote. Essa enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**flEMail** <br/> |,0  <br/> |Define onde as mensagens de email do Outlook serão arquivadas.  <br/> |
|**flContacts** <br/> |1  <br/> |Define onde os contatos do Outlook serão arquivados.  <br/> |
|**flTasks** <br/> |duas  <br/> |Define onde as tarefas do Outlook serão arquivadas.  <br/> |
|**flMeetings** <br/> |3D  <br/> |Define onde as reuniões do Outlook serão arquivadas.  <br/> |
|**flWebContent** <br/> |4   <br/> |Define onde o conteúdo do Internet Explorer será arquivado.  <br/> |
|**flPrintOuts** <br/> |5   <br/> |Define onde as impressões da impressora do OneNote serão arquivadas.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Quando passado para o método **SetFilingLocation** , especifica onde o conteúdo enviado para o OneNote é arquivado. Essa enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |,0  <br/> |Define o conteúdo a ser arquivado em uma nova página em uma seção especificada.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Define o conteúdo a ser arquivado em uma nova página na seção atual.  <br/> |
|**fltCurrentPage** <br/> |duas  <br/> |Define o conteúdo a ser arquivado na página atual.  <br/> |
|**fltNamedPage** <br/> |4   <br/> |Define o conteúdo a ser arquivado em uma página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>Hierarchyelement
<a name="odc_CreateFileType"> </a>

Quando atribuído à propriedade **TreeDepth** da interface [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , especifica a profundidade da árvore do OneNote a ser exibida quando a caixa de diálogo de arquivamento rápido é renderizada. Quando passado para o método **AddButton** do objeto **IQuickFilingDialog** , faz referência a determinados elementos na hierarquia do OneNote. Essa enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**heNone** <br/> |,0  <br/> |Refere-se a nenhum elemento.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Refere-se aos elementos do bloco de anotações.  <br/> |
|**heSectionGroups** <br/> |duas  <br/> |Refere-se aos elementos do grupo de seções.  <br/> |
|**heSections** <br/> |4   <br/> |Refere-se aos elementos da seção.  <br/> |
|**hePages** <br/> |8   <br/> |Refere-se aos elementos da página.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Quando passado para o **** método GetHierarchy, especifica o nível mais baixo para obter na hierarquia do nó do bloco de anotações. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |,0  <br/> |Obtém apenas o nó inicial especificado e nenhum descendente.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtém os nós filho imediatos do nó inicial e nenhum descendente em grupos de subseções superiores ou inferiores.  <br/> |
|**hsNotebooks** <br/> |duas  <br/> |Obtém todos os blocos de anotações abaixo do nó inicial ou raiz.  <br/> |
|**hsSections** <br/> |3D  <br/> |Obtém todas as seções abaixo do nó inicial, incluindo seções em grupos de seções e grupos de subseções.  <br/> |
|**hsPages** <br/> |4   <br/> |Obtém todas as páginas abaixo do nó inicial, incluindo todas as páginas em grupos de seções e grupos de subseções.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Quando passado para o método **CreateNewPage** , especifica o estilo da nova página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |,0  <br/> |Cria uma página com o estilo de página padrão.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Cria uma página em branco que tem um título.  <br/> |
|**npsBlankPageNoTitle** <br/> |duas  <br/> |Cria uma página em branco sem título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Quando passado para o método **NotebookFilterOut** do objeto **QFD** , especifica quais blocos de anotações serão exibidos quando a caixa de QFD for renderizada. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Permitir somente blocos de anotações locais.  <br/> |
|**nfoNetwork** <br/> |duas  <br/> |Permite blocos de anotações UNC ou do SharePoint.  <br/> |
|**nfoWeb** <br/> |4   <br/> |Permite blocos de anotações do OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8   <br/> |Quaisquer blocos de anotações em locais que não tenham um cliente da Web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (atualizado para o OneNote 2013)
<a name="odc_PageInfo"> </a>

Quando passado para o método **GetPageContent** , especifica o tipo de informação a ser retornado com o conteúdo da página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**piBasic** <br/> |,0  <br/> |Retorna somente o conteúdo básico da página, sem marcação de seleção, tipos de arquivo para objetos de dados binários e objetos de dados binários. Este é o valor padrão a ser passado.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Retorna o conteúdo da página sem marcação de seleção, mas com todos os dados binários.  <br/> |
|**piSelection** <br/> |duas  <br/> |Retorna o conteúdo da página com marcação de seleção, mas não dados binários.  <br/> |
|**piBinaryDataSelection** <br/> |3D  <br/> |Retorna o conteúdo da página com marcação de seleção e todos os dados binários.  <br/> |
|**piFileType** <br/> |4   <br/> |Retorna o conteúdo da página com informações de tipo de arquivo para objetos de dados binários.  <br/> |
|**piBinaryDataFileType** <br/> |5   <br/> |Retorna o conteúdo da página com informações de tipo de arquivo para objetos de dados binários e objetos de dados binários  <br/> |
|**piSelectionFileType** <br/> |6   <br/> |Retorna o conteúdo da página com marcação de seleção e informações de tipo de arquivo para dados binários.  <br/> |
|**piAll** <br/> |7   <br/> |Retorna todo o conteúdo da página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Quando passado para o método **Publish** , especifica o formato no qual a página publicada será exibida. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |,0  <br/> |A página publicada está no formato. One.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |A página publicada está no formato. ONEPKG.  <br/> |
|**pfMHTML** <br/> |duas  <br/> |A página publicada está no formato. mht.  <br/> |
|**pfPDF** <br/> |3D  <br/> |A página publicada está no formato. pdf.  <br/> |
|**pfXPS** <br/> |4   <br/> |A página publicada está no formato. XPS.  <br/> |
|**pfWord** <br/> |5   <br/> |A página publicada está no formato. doc ou. docx.  <br/> |
|**pfEMF** <br/> |6   <br/> |A página publicada está no formato metarquivo avançado (. EMF).  <br/> |
|**pfHTML** <br/> |7   <br/> |A página publicada está no formato. html. Este membro é novo no OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8   <br/> |A página publicada está no formato 2007. One. Este membro é novo no OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Quando passado para o método **SetRecentResults** do objeto **IQuickFilingDialog** , especifica a lista de resultados recentes a ser exibida quando a caixa de diálogo de arquivamento rápido é renderizada. Listas de resultados recentes são usadas para controlar o conjunto de locais do OneNote que o usuário seleciona na caixa de diálogo de arquivamento rápido. Há três listas de resultados recentes no OneNote 2013 que controlam o arquivamento, a pesquisa e a vinculação de ações. Essa enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |,0  <br/> |Define que nenhuma lista de resultados recentes seja renderizada.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Define a lista de resultados recentes de "arquivamento" a ser renderizada.  <br/> |
|**rrtSearch** <br/> |duas  <br/> |Define a lista de resultados recentes de "pesquisa" a ser renderizada.  <br/> |
|**rrtLinks** <br/> |3D  <br/> |Define a lista de resultados recentes de "links" a ser renderizada.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Quando passado para o método **GetSpecialLocation** , especifica o caminho de local especial a ser obtido. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |,0  <br/> |Obtém o caminho para o local da pasta de pastas de backup.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtém o caminho para o local da pasta de anotações não arquivadas.  <br/> |
|**slDefaultNotebookFolder** <br/> |duas  <br/> |Obtém o caminho para o local da pasta de bloco de anotações padrão.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Quando passado para o método **TreeCollapsedState** do objeto **QFD** , especifica se a árvore hierárquica deve ser expandida ou recolhida. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |,0  <br/> |Define a árvore de hierarquia como expandida.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Define a árvore de hierarquia como recolhida.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (atualizado para o OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Quando passadas para um dos métodos a seguir, especifica a versão do esquema XML do OneNote a ser usada:
  
- **OneNote15. Application. GetPageContent**
    
- **OneNote15. Application. FindMeta**
    
- **OneNote15. Application. FindPages**
    
- **OneNote15. Application. getHierarchy**
    
- **OneNote15. Application. GetPageContent**
    
- **OneNote15. Application. UpdateHierarchy**
    
- **OneNote15. Application. UpdatePageContent**
    
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**xs2007** <br/> |,0  <br/> |Faz referência ao esquema do OneNote 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Faz referência ao esquema do OneNote 2010.  <br/> |
|**xs2013** <br/> |duas  <br/> |Faz referência ao esquema do OneNote 2013.  <br/> |
|**xsCurrent** <br/> |duas  <br/> |Faz referência ao esquema da versão atual do OneNote.  <br/> <br/>**Observação**: não é recomendável usar **xsCurrent** na maioria dos casos, pois isso pode causar problemas de compatibilidade com versões futuras do OneNote. Em vez disso, especifique a versão do esquema que seu aplicativo foi criado para lidar, como xs2013.           |
   
## <a name="see-also"></a>Confira também

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

