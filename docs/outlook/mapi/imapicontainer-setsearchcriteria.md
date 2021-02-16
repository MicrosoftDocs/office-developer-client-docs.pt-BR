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
  
> [in] Um ponteiro para uma [estrutura SRestriction](srestriction.md) que define os critérios de pesquisa. Se NULL for passado no  _parâmetro lpRestriction,_ os critérios de pesquisa usados mais recentemente para esse contêiner serão usados novamente. NULL não deve ser passado  _em lpRestriction_ para a primeira pesquisa em um contêiner. 
    
 _lpContainerList_
  
> [in] Um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa. Se um cliente passar NULL no parâmetro  _lpContainerList,_ os identificadores de entrada usados mais recentemente para pesquisar esse contêiner serão usados para a nova pesquisa. Um cliente não deve passar NULL em  _lpContainerList_ para a primeira pesquisa em um contêiner. 
    
 _ulSearchFlags_
  
> [in] Uma máscara de bits de sinalizadores que controlam como a pesquisa é realizada. Os sinalizadores a seguir podem ser definidos:
    
BACKGROUND_SEARCH 
  
> A pesquisa deve ser executado com prioridade normal em relação a outras pesquisas. Esse sinalizador não pode ser definido ao mesmo tempo que o FOREGROUND_SEARCH sinalizador.
    
FOREGROUND_SEARCH 
  
> A pesquisa deve ser executado com alta prioridade em relação a outras pesquisas. Esse sinalizador não pode ser definido ao mesmo tempo que o BACKGROUND_SEARCH sinalizador.
    
NON_CONTENT_INDEXED_SEARCH
  
> A pesquisa não deve usar a indexação de conteúdo para encontrar entradas correspondentes. Esse sinalizador só é válido para armazenamentos do Exchange.
    
RECURSIVE_SEARCH 
  
> A pesquisa deve incluir os contêineres especificados no parâmetro  _lpContainerList_ e todos os contêineres filho. Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador SHALLOW_SEARCH linha. 
    
RESTART_SEARCH 
  
> A pesquisa deve ser iniciada se esta for a primeira chamada para **SetSearchCriteria** ou reiniciada se a pesquisa estiver inativa. Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador STOP_SEARCH linha.
    
SHALLOW_SEARCH 
  
> A pesquisa deve procurar apenas nos contêineres especificados no parâmetro  _lpContainerList_ para entradas correspondentes. Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador RECURSIVE_SEARCH linha. 
    
STOP_SEARCH 
  
> A pesquisa deve ser interrompida. Esse sinalizador não pode ser definido ao mesmo tempo que o sinalizador RESTART_SEARCH linha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os critérios de pesquisa foram definidos com êxito.
    
MAPI_E_TOO_COMPLEX 
  
> O provedor de serviços não suporta os critérios de pesquisa especificados.
    
## <a name="remarks"></a>Comentários

O **método IMAPIContainer::SetSearchCriteria** estabelece critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa. Uma pasta de resultados de pesquisa contém links para as mensagens que atendem aos critérios de pesquisa; as mensagens reais ainda são armazenadas em seus locais originais. Os únicos dados exclusivos contidos em uma pasta de resultados de pesquisa são sua tabela de conteúdo. O índice de conteúdo de uma pasta de resultados de pesquisa tem o conteúdo mesclado do armazenamento de mensagens após a restrição de pesquisa ter sido aplicada. 
  
Uma operação de pesquisa funciona somente nesta tabela de conteúdo mesclado; ele não pesquisa por outras pastas de resultados de pesquisa. Os resultados da pesquisa retornam apenas as mensagens que corresponderem aos critérios de pesquisa; a hierarquia de pastas não é retornada.
  
O controle é retornado ao cliente quando a pesquisa tiver sido concluída.
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os contêineres de agendas estabelecem critérios de pesquisa aplicando restrições a seus índices de conteúdo. Para obter mais informações sobre critérios de pesquisa e contêineres de livro de endereços, consulte [Implementando Pesquisa Avançada.](implementing-advanced-searching.md)
  
Você deve dar suporte a operações de abrir, copiar, mover e excluir mensagens nas mensagens dentro de pastas de resultados de pesquisa, não na própria pasta de resultados de pesquisa. Não permita que mensagens sejam criadas dentro ou copiadas em uma pasta de resultados de pesquisa. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para procurar destinatários de mensagem, de definida  _lpRestriction_ para apontar para uma restrição de subobjeto com o membro **ulSubObject** na [estrutura SSubRestriction](ssubrestriction.md) definida como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Para procurar anexos, de definir o **membro ulSubObject** como **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)). Definir o **membro lpRes** para apontar para uma restrição de propriedade que descreve os critérios de pesquisa para os destinatários ou anexos. 
  
Por exemplo, para procurar anexos de arquivo que tenham a extensão .mss, de definir **ulSubObject** como **PR_MESSAGE_ATTACHMENTS** e **lpRes** como uma restrição de propriedade que corresponde a **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) com .mss.
  
Definir o FOREGROUND_SEARCH sinalizador no  _parâmetro ulSearchFlags_ pode causar uma diminuição no desempenho do sistema. 
  
Você pode usar **SetSearchCriteria para** alterar os critérios de pesquisa de uma pesquisa já em andamento. Você pode especificar novas restrições, novas listas de pastas a pesquisar e uma nova prioridade de pesquisa, como atualizar uma pesquisa para uma prioridade mais alta. As alterações na prioridade da pesquisa não fazem com que uma pesquisa existente seja reiniciada, mas outras alterações nos critérios de pesquisa podem. 
  
Quando você estiver usando uma pasta de resultados de pesquisa, poderá excluí-la ou deixá-la aberta para uso posterior. Se você excluir a pasta de resultados de pesquisa, somente os links de mensagens serão excluídos. As mensagens reais permanecem em suas pastas pai. 
  
Para obter mais informações sobre pastas de resultados de pesquisa, consulte [MapI Search Folders](mapi-search-folders.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa o **método IMAPIContainer::SetSearchCriteria** para gravar critérios de pesquisa para uma pasta após um usuário editá-la.  <br/> |
   
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

