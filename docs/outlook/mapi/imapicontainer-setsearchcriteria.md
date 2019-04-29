---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427196"
---
# <a name="imapicontainersetsearchcriteria"></a>IMAPIContainer::SetSearchCriteria

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece critérios de pesquisa para o contêiner.
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpRestriction_
  
> no Um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa. Se NULL for passado no parâmetro _lpRestriction_ , os critérios de pesquisa que foram usados mais recentemente para este contêiner serão usados novamente. NULL não deve ser passado no _lpRestriction_ para a primeira pesquisa em um contêiner. 
    
 _lpContainerList_
  
> no Um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa. Se um cliente passa nulo no parâmetro _lpContainerList_ , os identificadores de entrada usados mais recentemente para pesquisar esse contêiner são usados para a nova pesquisa. Um cliente não deve passar nulo no _lpContainerList_ para a primeira pesquisa em um contêiner. 
    
 _ulSearchFlags_
  
> no Uma bitmask de sinalizadores que controlam como a pesquisa é realizada. Os seguintes sinalizadores podem ser definidos:
    
BACKGROUND_SEARCH 
  
> A pesquisa deve ser executada em prioridade normal em relação a outras pesquisas. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador FOREGROUND_SEARCH.
    
FOREGROUND_SEARCH 
  
> A pesquisa deve ser executada com prioridade alta em relação a outras pesquisas. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador BACKGROUND_SEARCH.
    
NON_CONTENT_INDEXED_SEARCH
  
> A pesquisa não deve usar a indexação de conteúdo para localizar entradas correspondentes. Este sinalizador só é válido para repositórios do Exchange.
    
RECURSIVE_SEARCH 
  
> A pesquisa deve incluir os contêineres especificados no parâmetro _lpContainerList_ e todos os seus contêineres filhos. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador SHALLOW_SEARCH. 
    
RESTART_SEARCH 
  
> A pesquisa deve ser iniciada se esta for a primeira chamada para **SetSearchCriteria**ou reiniciada se a pesquisa estiver inativa. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador STOP_SEARCH.
    
SHALLOW_SEARCH 
  
> A pesquisa deve procurar somente nos contêineres especificados no parâmetro _lpContainerList_ para entradas correspondentes. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador RECURSIVE_SEARCH. 
    
STOP_SEARCH 
  
> A pesquisa deve ser interrompida. Este sinalizador não pode ser definido ao mesmo tempo que o sinalizador RESTART_SEARCH.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os critérios de pesquisa foram definidos com êxito.
    
MAPI_E_TOO_COMPLEX 
  
> O provedor de serviços não oferece suporte aos critérios de pesquisa especificados.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer:: SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa. Uma pasta de resultados de pesquisa contém links para as mensagens que atendem aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais. Os únicos dados exclusivos que estão contidos em uma pasta de resultados de pesquisa é sua tabela de conteúdo. A tabela de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado do repositório de mensagens após a restrição de pesquisa ter sido aplicada. 
  
Uma operação de pesquisa funciona somente nesta tabela de conteúdo mesclado; Ele não pesquisa por outras pastas de resultados de pesquisa. Os resultados da pesquisa retornam apenas as mensagens que correspondem aos critérios de pesquisa; a hierarquia de pastas não é retornada.
  
O controle é retornado ao cliente quando a pesquisa foi concluída.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os contêineres do catálogo de endereços estabelecem critérios de pesquisa aplicando restrições às tabelas de conteúdo. Para obter mais informações sobre critérios de pesquisa e contêineres do catálogo de endereços, consulte [implementaNdo pesquisa avançada](implementing-advanced-searching.md).
  
Você deve oferecer suporte a operações abrir, copiar, mover e excluir nas mensagens dentro das pastas de resultados de pesquisa, e não na própria pasta de resultados de pesquisa. Não permite que as mensagens sejam criadas dentro ou copiadas para uma pasta de resultados de pesquisa. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para procurar destinatários de mensagens, defina _lpRestriction_ para apontar para uma restrição de subobjeto com o membro **UlSubObject** na estrutura [SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Para procurar anexos, defina o membro **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Defina o membro **lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos. 
  
Por exemplo, para procurar anexos de arquivo com a extensão. MSS, defina **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** e **lpRes** como uma restrição de propriedade que corresponda a **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) ) com. MSS.
  
Definir o sinalizador FOREGROUND_SEARCH no parâmetro _ulSearchFlags_ pode causar uma redução no desempenho do sistema. 
  
Você pode usar o **SetSearchCriteria** para alterar os critérios de pesquisa de uma pesquisa já em andamento. Você pode especificar novas restrições, novas listas de pastas a serem pesquisadas e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta. As alterações na prioridade de pesquisa não fazem com que uma pesquisa existente seja reiniciada, mas outras alterações nos critérios de pesquisa podem. 
  
Quando você usa uma pasta de resultados de pesquisa, você pode excluir a pasta ou deixá-la permanecer aberta para uso posterior. Se você excluir a pasta de resultados de pesquisa, somente os links de mensagens serão excluídos. As mensagens reais permanecem em suas pastas pai. 
  
Para obter mais informações sobre pastas de resultados de pesquisa, consulte [pastas de pesquisa MAPI](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI usa o método **IMAPIContainer:: SetSearchCriteria** para gravar critérios de pesquisa para uma pasta após o usuário ter editado.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md)
  
[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[SPropertyRestriction](spropertyrestriction.md)
  
[SRestriction](srestriction.md)
  
[SSubRestriction](ssubrestriction.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

