---
title: Enumerações (referência de desenvolvedor do OneNote)
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
# <a name="enumerations-onenote-developer-reference"></a>Enumerações (referência de desenvolvedor do OneNote)

Este tópico descreve as enumerações no modelo de objeto do OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Quando passado para o **método OpenHierarchy,** especifica o tipo de objeto a ser criado, se existir, se o caminho passado para o método ainda não existir. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |Não cria um novo objeto.  <br/> |
|**cftNotebook** <br/> |1   <br/> |Cria um bloco de anotações usando o nome e o local especificados.  <br/> |
|**cftFolder** <br/> |2   <br/> |Cria um grupo de seções usando o nome e o local especificados.  <br/> |
|**cftSection** <br/> |3   <br/> |Cria uma seção usando o nome e o local especificados.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica o local encaixado de uma janela do OneNote 2013 usando a interface [window.](window-interfaces-onenote.md) Quando definido para a **propriedade DockedLocation,** especifica o local no qual encaixar uma janela do OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |A janela do OneNote está encaixada no local padrão na área de trabalho.  <br/> |
|**dlLeft** <br/> |1   <br/> |A janela do OneNote é encaixada no lado esquerdo da área de trabalho.  <br/> |
|**dlRight** <br/> |2   <br/> |A janela do OneNote é encaixada no lado direito da área de trabalho.  <br/> |
|**dlTop** <br/> |3   <br/> |A janela do OneNote é encaixada na parte superior da área de trabalho.  <br/> |
|**dlBottom** <br/> |4   <br/> |A janela do OneNote é encaixada na parte inferior da área de trabalho.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Quando passado para o **método SetFilingLocation,** especifica para qual tipo de conteúdo o local de arquivamento é definido quando o tipo de conteúdo é enviado para o OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Define onde as mensagens de email do Outlook serão arquivadas.  <br/> |
|**flContacts** <br/> |1   <br/> |Define onde os contatos do Outlook serão arquivados.  <br/> |
|**flTasks** <br/> |2   <br/> |Define onde as tarefas do Outlook serão arquivadas.  <br/> |
|**flMeetings** <br/> |3   <br/> |Define onde as reuniões do Outlook serão arquivadas.  <br/> |
|**flWebContent** <br/> |4   <br/> |Define onde o conteúdo do Internet Explorer será arquivado.  <br/> |
|**flPrintOuts** <br/> |5   <br/> |Define onde as impressão da impressora do OneNote serão arquivadas.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Quando passado para o **método SetFilingLocation,** especifica para onde o conteúdo enviado para o OneNote é arquivado. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Define o conteúdo a ser arquivado em uma nova página em uma seção especificada.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1   <br/> |Define o conteúdo a ser arquivado em uma nova página na seção atual.  <br/> |
|**fltCurrentPage** <br/> |2   <br/> |Define o conteúdo a ser arquivado na página atual.  <br/> |
|**fltNamedPage** <br/> |4   <br/> |Define o conteúdo a ser arquivado em uma página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Quando atribuído à propriedade **TreeDepth** da interface [IQuickFilingDialog,](quick-filing-dialog-box-interfaces-onenote.md) especifica a profundidade da árvore do OneNote a ser exibida quando a caixa de diálogo de arquivamento rápido é renderizada. Quando passada para o **método AddButton** do objeto **IQuickFilingDialog,** faz referência a determinados elementos na hierarquia do OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Refere-se a nenhum elemento.  <br/> |
|**heNotebooks** <br/> |1   <br/> |Refere-se aos elementos do Bloco de Anotações.  <br/> |
|**heSectionGroups** <br/> |2   <br/> |Refere-se aos elementos do Grupo de Seções.  <br/> |
|**heSections** <br/> |4   <br/> |Refere-se aos elementos Section.  <br/> |
|**hePages** <br/> |8   <br/> |Refere-se aos elementos Page.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Quando passado para o **método GetHierarchy,** especifica o nível mais baixo para obter na hierarquia de nós do bloco de anotações. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtém apenas o nó inicial especificado e nenhum descendente.  <br/> |
|**hsChildren** <br/> |1   <br/> |Obtém os nós filho imediatos do nó inicial e nenhum descendente em grupos de subseção mais altos ou inferiores.  <br/> |
|**hsNotebooks** <br/> |2   <br/> |Obtém todos os blocos de anotações abaixo do nó inicial ou raiz.  <br/> |
|**hsSections** <br/> |3   <br/> |Obtém todas as seções abaixo do nó inicial, incluindo seções em grupos de seções e grupos de subseção.  <br/> |
|**hsPages** <br/> |4   <br/> |Obtém todas as páginas abaixo do nó inicial, incluindo todas as páginas em grupos de seções e grupos de subseção.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Quando passado para o **método CreateNewPage,** especifica o estilo da nova página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Cria uma página que tem o estilo de página padrão.  <br/> |
|**npsBlankPageWithTitle** <br/> |1   <br/> |Cria uma página em branco que tem um título.  <br/> |
|**npsBlankPageNoTitle** <br/> |2   <br/> |Cria uma página em branco que não tem título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Quando passado para o método **NotebookFilterOut** do objeto **QFD,** especifica quais blocos de anotações serão exibidos quando a caixa QFD for renderizada. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1   <br/> |Permitir somente Blocos de Anotações Locais.  <br/> |
|**nfoNetwork** <br/> |2   <br/> |Permite blocos de anotações UNC ou SharePoint.  <br/> |
|**nfoWeb** <br/> |4   <br/> |Permite blocos de anotações do OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8   <br/> |Todos os blocos de anotações em locais que não tenham um cliente Web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (Atualizado para o OneNote 2013)
<a name="odc_PageInfo"> </a>

Quando passado para o **método GetPageContent,** especifica o tipo de informação a ser retornada com o conteúdo da página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Retorna apenas o conteúdo de página básico, sem marcação de seleção, tipos de arquivo para objetos de dados binários e objetos de dados binários. Este é o valor padrão a ser aprovado.  <br/> |
|**piBinaryData** <br/> |1   <br/> |Retorna o conteúdo da página sem marcação de seleção, mas com todos os dados binários.  <br/> |
|**piSelection** <br/> |2   <br/> |Retorna o conteúdo da página com marcação de seleção, mas nenhum dado binário.  <br/> |
|**piBinaryDataSelection** <br/> |3   <br/> |Retorna o conteúdo da página com marcação de seleção e todos os dados binários.  <br/> |
|**piFileType** <br/> |4   <br/> |Retorna o conteúdo da página com informações de tipo de arquivo para objetos de dados binários.  <br/> |
|**piBinaryDataFileType** <br/> |5   <br/> |Retorna o conteúdo da página com informações de tipo de arquivo para objetos de dados binários e objetos de dados binários  <br/> |
|**piSelectionFileType** <br/> |6   <br/> |Retorna o conteúdo da página com marcação de seleção e informações de tipo de arquivo para dados binários.  <br/> |
|**piAll** <br/> |7   <br/> |Retorna todo o conteúdo da página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Quando passado para o **método Publish,** especifica o formato no qual a página publicada será exibida. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |A página publicada está no formato .one.  <br/> |
|**pfOneNotePackage** <br/> |1   <br/> |A página publicada está no formato .onepkg.  <br/> |
|**pfMHTML** <br/> |2   <br/> |A página publicada está no formato .mht.  <br/> |
|**pfPDF** <br/> |3   <br/> |A página publicada está no formato .pdf.  <br/> |
|**pfXPS** <br/> |4   <br/> |A página publicada está no formato .xps.  <br/> |
|**pfWord** <br/> |5   <br/> |A página publicada está no formato .doc ou .docx.  <br/> |
|**pfEMF** <br/> |6   <br/> |A página publicada está no formato de metarquivo avançado (.emf).  <br/> |
|**pfHTML** <br/> |7   <br/> |A página publicada está no formato .html. Este membro é novo no OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8   <br/> |A página publicada está no formato 2007 .one. Este membro é novo no OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Quando passada para o método **SetRecentResults** do objeto **IQuickFilingDialog,** especifica qual lista de resultados recentes será exibida quando a caixa de diálogo Arquivamento Rápido for renderizada. Listas de resultados recentes são usadas para controlar o conjunto de locais do OneNote que o usuário seleciona na caixa de diálogo Arquivamento Rápido. Há três listas de resultados recentes no OneNote 2013 que rastreia ações de arquivamento, pesquisa e vinculação. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |Não define nenhuma lista de resultados recentes a ser renderizada.  <br/> |
|**rrtFiling** <br/> |1   <br/> |Define a lista de resultados recentes "Arquivamento" a ser renderizada.  <br/> |
|**rrtSearch** <br/> |2   <br/> |Define a lista de resultados recentes "Pesquisa" a ser renderizada.  <br/> |
|**rrtLinks** <br/> |3   <br/> |Define a lista de resultados recentes "Links" a ser renderizada.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Quando passado para o **método GetSpecialLocation,** especifica o caminho de local especial a ser localizado. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtém o caminho para o local da pasta Pastas de Backup.  <br/> |
|**slUnfiledNotesSection** <br/> |1   <br/> |Obtém o caminho para o local da pasta Anotações NãoFiladas.  <br/> |
|**slDefaultNotebookFolder** <br/> |2   <br/> |Obtém o caminho para o local da pasta Bloco de Anotações Padrão.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Quando passada para **o método TreeCollapsedState** do objeto **QFD,** especifica se a árvore de hierarquia deve ser expandida ou recolhido. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Define a árvore de hierarquias a ser expandida.  <br/> |
|**tcsCollapsed** <br/> |1   <br/> |Define a árvore hierárquica como recolhido.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (Atualizado para o OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Quando passado para um dos seguintes métodos, especifica a versão do esquema XML do OneNote a ser usada:
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Faz referência ao esquema do OneNote 2007.  <br/> |
|**xs2010** <br/> |1   <br/> |Faz referência ao esquema do OneNote 2010.  <br/> |
|**xs2013** <br/> |2   <br/> |Faz referência ao esquema do OneNote 2013.  <br/> |
|**xsCurrent** <br/> |2   <br/> |Faz referência ao esquema da versão atual do OneNote.  <br/> <br/>**OBSERVAÇÃO:** não recomendamos o uso do **xsCurrent** na maioria dos casos, pois ele pode causar problemas de compatibilidade com versões futuras do OneNote. Em vez disso, especifique a versão do esquema que seu aplicativo foi criado para manipular, como xs2013.           |
   
## <a name="see-also"></a>Confira também

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

