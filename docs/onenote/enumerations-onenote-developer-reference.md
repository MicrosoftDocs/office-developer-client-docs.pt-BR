---
title: Enumerações (referência para desenvolvedores do OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 62912d6e-c39e-4f8b-8cdb-ae9b6376cbc0
description: Este tópico descreve as enumerações no modelo de objeto do OneNote 2013.
ms.openlocfilehash: ccd75843326ea5942aa80d02246e59e92331a7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765778"
---
# <a name="enumerations-onenote-developer-reference"></a>Enumerações (referência para desenvolvedores do OneNote)

Este tópico descreve as enumerações no modelo de objeto do OneNote 2013.
  
## <a name="createfiletype"></a>CreateFileType
<a name="odc_CreateFileType"> </a>

Quando passados ao método **OpenHierarchy** , especifica o tipo de objeto a ser criado, se houver, se o caminho é passado para o método ainda não existe. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**cftNone** <br/> |0  <br/> |Não cria nenhum novo objeto.  <br/> |
|**cftNotebook** <br/> |1  <br/> |Cria um bloco de anotações, usando o nome especificado e o local.  <br/> |
|**cftFolder** <br/> |2  <br/> |Cria um grupo de seção usando o nome especificado e o local.  <br/> |
|**cftSection** <br/> |3  <br/> |Cria uma seção usando o nome especificado e o local.  <br/> |
   
## <a name="docklocation"></a>DockLocation
<a name="odc_CreateFileType"> </a>

Indica a localização ancorada de uma janela do OneNote 2013 usando a interface de [janela](window-interfaces-onenote.md) . Quando definido como o **DockedLocation** a propriedade, especifica o local no qual se encaixa uma janela do OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**dlDefault** <br/> |-1  <br/> |A janela do OneNote é encaixada no local padrão da área de trabalho.  <br/> |
|**dlLeft** <br/> |1  <br/> |A janela do OneNote é encaixada no lado esquerdo da área de trabalho.  <br/> |
|**dlRight** <br/> |2  <br/> |A janela do OneNote é encaixada no lado direito da área de trabalho.  <br/> |
|**dlTop** <br/> |3  <br/> |A janela do OneNote é encaixada na parte superior da área de trabalho.  <br/> |
|**dlBottom** <br/> |4  <br/> |A janela do OneNote é encaixada na parte inferior da área de trabalho.  <br/> |
   
## <a name="filinglocation"></a>FilingLocation
<a name="odc_CreateFileType"> </a>

Quando passados ao método **SetFilingLocation** , especifica que tipo de conteúdo o local de arquivamento é definido para quando o tipo de conteúdo é enviado para o OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**flEMail** <br/> |0  <br/> |Define onde as mensagens de email do Outlook serão arquivadas.  <br/> |
|**flContacts** <br/> |1  <br/> |Define em que os contatos do Outlook serão arquivados.  <br/> |
|**flTasks** <br/> |2  <br/> |Conjuntos de onde serão arquivadas tarefas do Outlook.  <br/> |
|**flMeetings** <br/> |3  <br/> |Conjuntos de onde serão arquivadas reuniões no Outlook.  <br/> |
|**flWebContent** <br/> |4  <br/> |Define onde será arquivado conteúdo do Internet Explorer.  <br/> |
|**flPrintOuts** <br/> |5  <br/> |Define onde impressões da impressora OneNote serão arquivadas.  <br/> |
   
## <a name="filinglocationtype"></a>FilingLocationType
<a name="odc_CreateFileType"> </a>

Quando passados ao método **SetFilingLocation** , especifica onde o conteúdo que é enviado para o OneNote é arquivado. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**fltNamedSectionNewPage** <br/> |0  <br/> |Define o conteúdo arquivado em uma nova página em uma seção especificada.  <br/> |
|**fltCurrentSectionNewPage** <br/> |1  <br/> |Define o conteúdo arquivado em uma nova página da seção atual.  <br/> |
|**fltCurrentPage** <br/> |2  <br/> |Define o conteúdo arquivado na página atual.  <br/> |
|**fltNamedPage** <br/> |4  <br/> |Define o conteúdo arquivado em uma página especificada.  <br/> |
   
## <a name="hierarchyelement"></a>HierarchyElement
<a name="odc_CreateFileType"> </a>

Quando atribuído à propriedade **TreeDepth** da interface [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md) , especifique a profundidade da árvore do OneNote para exibir quando a caixa de diálogo arquivamento rápido é processada. Quando passados ao método **AddButton** do objeto **IQuickFilingDialog** , referencia determinados elementos na hierarquia do OneNote. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**heNone** <br/> |0  <br/> |Refere-se a nenhum elemento.  <br/> |
|**heNotebooks** <br/> |1  <br/> |Refere-se aos elementos de bloco de anotações.  <br/> |
|**heSectionGroups** <br/> |2  <br/> |Refere-se aos elementos grupo da seção.  <br/> |
|**heSections** <br/> |4  <br/> |Refere-se aos elementos da seção.  <br/> |
|**hePages** <br/> |8  <br/> |Refere-se aos elementos da página.  <br/> |
   
## <a name="hierarchyscope"></a>HierarchyScope
<a name="odc_HierarchyScope"> </a>

Quando passados ao método **GetHierarchy** , especifica o nível mais baixo para obter na hierarquia de nó de bloco de anotações. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**hsSelf** <br/> |0  <br/> |Obtém apenas o nó de início especificado e nenhum descendentes.  <br/> |
|**hsChildren** <br/> |1  <br/> |Obtém o filho imediato nós de nó inicial e nenhum descendentes em grupos de subseção superior ou inferior.  <br/> |
|**hsNotebooks** <br/> |2  <br/> |Obtém todos os blocos de anotações abaixo do nó inicial ou raiz.  <br/> |
|**hsSections** <br/> |3  <br/> |Obtém todas as seções abaixo do nó de início, incluindo seções em grupos de seções e grupos de subseção.  <br/> |
|**hsPages** <br/> |4  <br/> |Obtém todas as páginas abaixo do nó de início, incluindo todas as páginas em grupos de seções e grupos de subseção.  <br/> |
   
## <a name="newpagestyle"></a>NewPageStyle
<a name="odc_HierarchyScope"> </a>

Quando passados ao método **CreateNewPage** , especifica o estilo da nova página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**npsDefault** <br/> |0  <br/> |Cria uma página que tem o estilo de página padrão.  <br/> |
|**npsBlankPageWithTitle** <br/> |1  <br/> |Cria uma página em branco que tem um título.  <br/> |
|**npsBlankPageNoTitle** <br/> |2  <br/> |Cria uma página em branco que não tem um título.  <br/> |
   
## <a name="notebookfilterouttype"></a>NotebookFilterOutType
<a name="odc_HierarchyScope"> </a>

Quando passados ao método **NotebookFilterOut** do objeto **QFD** , especifica quais blocos de anotações para exibir quando a caixa QFD é processada. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**nfoLocal** <br/> |1  <br/> |Permitir somente locais blocos de anotações.  <br/> |
|**nfoNetwork** <br/> |2  <br/> |Permite UNC ou blocos de anotações do SharePoint.  <br/> |
|**nfoWeb** <br/> |4  <br/> |Permite que os blocos de anotações do OneDrive.  <br/> |
|**nfoNoWacUrl** <br/> |8  <br/> |Qualquer blocos de anotações em locais que não têm um cliente web.  <br/> |
   
## <a name="pageinfo-updated-for-onenote-2013"></a>PageInfo (atualizado para o OneNote 2013)
<a name="odc_PageInfo"> </a>

Quando passado para o método **GetPageContent** , especifica o tipo de informação para retornar o conteúdo de página. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**piBasic** <br/> |0  <br/> |Retorna o conteúdo de página apenas básica, sem marcação de seleção, os tipos de arquivo para os objetos de dados binários e dados binários. Esse é o valor padrão para passar.  <br/> |
|**piBinaryData** <br/> |1  <br/> |Retorna o conteúdo com nenhuma marcação de seleção, mas com todos os dados binários de página.  <br/> |
|**piSelection** <br/> |2  <br/> |Retorna o conteúdo com marcação de seleção, mas nenhum dado binário de página.  <br/> |
|**piBinaryDataSelection** <br/> |3  <br/> |Retorna o conteúdo com marcação de seleção e todos os dados binários de página.  <br/> |
|**piFileType** <br/> |4  <br/> |Retorna o conteúdo com informação de tipo de arquivo para os objetos de dados binários de página.  <br/> |
|**piBinaryDataFileType** <br/> |5  <br/> |Retorna o conteúdo com informação de tipo de arquivo para os objetos de dados binários e dados binários de página  <br/> |
|**piSelectionFileType** <br/> |6  <br/> |Retorna o conteúdo com informação de tipo marcação e o arquivo de seleção para dados binários de página.  <br/> |
|**piAll** <br/> |7  <br/> |Retorna todo o conteúdo de página.  <br/> |
   
## <a name="publishformat"></a>PublishFormat
<a name="odc_PublishFormat"> </a>

Quando passado para o método **Publish** , especifica o formato no qual a página publicada será exibida. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**pfOneNote** <br/> |0  <br/> |Página publicada está no formato. one.  <br/> |
|**pfOneNotePackage** <br/> |1  <br/> |Página publicada está no formato. onepkg.  <br/> |
|**pfMHTML** <br/> |2  <br/> |Página publicada está no formato. mht.  <br/> |
|**pfPDF** <br/> |3  <br/> |Página publicada está no formato. PDF.  <br/> |
|**pfXPS** <br/> |4  <br/> |Página publicada está no formato. XPS.  <br/> |
|**pfWord** <br/> |5  <br/> |Página publicada está no formato. doc ou. docx.  <br/> |
|**pfEMF** <br/> |6  <br/> |Página publicada é no formato de metarquivo avançado (. emf).  <br/> |
|**pfHTML** <br/> |7  <br/> |Página publicada está no formato. HTML. Este membro é novo no OneNote 2013.  <br/> |
|**pfOneNote2007** <br/> |8  <br/> |Página publicada está no formato. one 2007. Este membro é novo no OneNote 2013.  <br/> |
   
## <a name="recentresulttype"></a>RecentResultType
<a name="odc_RecentResultType"> </a>

Quando passados ao método **SetRecentResults** do objeto **IQuickFilingDialog** , especifica qual recentes lista de resultados a ser exibido quando a caixa de diálogo Preenchimento rápido é processada. Listas de resultado recentes são usadas para controlar o conjunto de locais do OneNote que o usuário seleciona na caixa de diálogo arquivamento rápido. Há três listas de resultado recente no OneNote 2013 que controlam a vinculação de ações, pesquisa e arquivamento. Esta enumeração é nova no OneNote 2013. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**rrtNone** <br/> |0  <br/> |Não define a lista de nenhum resultado recente a ser renderizado.  <br/> |
|**rrtFiling** <br/> |1  <br/> |Define a lista de resultado recente "Arquivamento" a ser renderizado.  <br/> |
|**rrtSearch** <br/> |2  <br/> |Define a lista de resultado recente "Pesquisa" a ser renderizado.  <br/> |
|**rrtLinks** <br/> |3  <br/> |Define a lista de resultado recente "Links" a ser renderizado.  <br/> |
   
## <a name="speciallocation"></a>SpecialLocation
<a name="odc_SpecialLocation"> </a>

Quando passados ao método **o GetSpecialLocation** , especifica o caminho de local especial para obter. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**slBackupFolder** <br/> |0  <br/> |Obtém o caminho para o local da pasta de Backup de pastas.  <br/> |
|**slUnfiledNotesSection** <br/> |1  <br/> |Obtém o caminho para o local da pasta anotações não arquivadas.  <br/> |
|**slDefaultNotebookFolder** <br/> |2  <br/> |Obtém o caminho para o local da pasta de bloco de anotações padrão.  <br/> |
   
## <a name="treecollapsedstatetype"></a>TreeCollapsedStateType
<a name="odc_SpecialLocation"> </a>

Quando passados ao método **TreeCollapsedState** do objeto **QFD** , especifica se a árvore de hierarquia deve ser expandido ou recolhido. 
  
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**tcsExpanded** <br/> |0  <br/> |Define a árvore de hierarquia expandido.  <br/> |
|**tcsCollapsed** <br/> |1  <br/> |Define a árvore de hierarquia recolhida.  <br/> |
   
## <a name="xmlschema-updated-for-onenote-2013"></a>XMLSchema (atualizado para o OneNote 2013)
<a name="odc_SpecialLocation"> </a>

Quando passado para um dos métodos a seguir, especifica a versão do esquema XML do OneNote usar:
  
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.FindMeta**
    
- **OneNote15.Application.FindPages**
    
- **OneNote15.Application.GetHierarchy**
    
- **OneNote15.Application.GetPageContent**
    
- **OneNote15.Application.UpdateHierarchy**
    
- **OneNote15.Application.UpdatePageContent**
    
|**Membro**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|**xs2007** <br/> |0  <br/> |Referências o esquema do OneNote 2007.  <br/> |
|**xs2010** <br/> |1  <br/> |Referências o esquema do OneNote 2010.  <br/> |
|**xs2013** <br/> |2  <br/> |Referências o esquema do OneNote 2013.  <br/> |
|**xsCurrent** <br/> |2  <br/> |Referências o esquema da versão atual do OneNote.  <br/> <br/>**Observação**: não é recomendável usar **xsCurrent** na maioria dos casos, como ela pode causar problemas de compatibilidade com versões futuras do OneNote. Em vez disso, especifica a versão do esquema do seu aplicativo foi desenvolvido para lidar com, como xs2013.           |
   
## <a name="see-also"></a>Confira também

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

