---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412020"
---
# <a name="imapicontainergetsearchcriteria"></a>IMAPIContainer::GetSearchCriteria

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obtém os critérios de pesquisa para o contêiner.
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppRestriction_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura SRestriction](srestriction.md) que define os critérios de pesquisa. Se um aplicativo cliente passar NULL no parâmetro _lppRestriction,_ **GetSearchCriteria** não retornará uma **estrutura SRestriction.** 
    
 _lppContainerList_
  
> [out] Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa. Se um cliente passar NULL no parâmetro  _lppContainerList,_ **GetSearchCriteria** não retornará uma matriz de identificadores de entrada. 
    
 _lpulSearchState_
  
> [out] Um ponteiro para uma máscara de bits de sinalizadores usado para indicar o estado atual da pesquisa. Se um cliente passar NULL no parâmetro  _lpulSearchState,_ **GetSearchCriteria não** retornará sinalizadores. Os sinalizadores a seguir podem ser definidos: 
    
SEARCH_FOREGROUND 
  
> A pesquisa deve ser executado com alta prioridade em relação a outras pesquisas. Se esse sinalizador não estiver definido, a pesquisa será executado com prioridade normal em relação a outras pesquisas.
    
SEARCH_REBUILD 
  
> A pesquisa está no modo de uso intenso da CPU de sua operação, tentando localizar mensagens que corresponderem aos critérios. Se esse sinalizador não estiver definido, a parte de uso intensivo da CPU da operação da pesquisa terminou. Esse sinalizador só terá significado se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING estiver definido).
    
SEARCH_RECURSIVE 
  
> A pesquisa está procurando por entradas correspondentes em contêineres especificados e em todos os contêineres filho. Se esse sinalizador não estiver definido, somente os contêineres incluídos explicitamente na última chamada para o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) serão pesquisados. 
    
SEARCH_RUNNING 
  
> A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no armazenamento de mensagens ou no livro de endereços. Se esse sinalizador não estiver definido, a pesquisa será inativa e o índice de conteúdo será estático.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os critérios de pesquisa foram obtidos com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Os critérios de pesquisa nunca foram estabelecidos para o contêiner.
    
## <a name="remarks"></a>Comentários

O **método IMAPIContainer::GetSearchCriteria** obtém os critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa. Você cria critérios de pesquisa chamando o método **IMAPIContainer::SetSearchCriteria de** um contêiner. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os contêineres do livro de endereços talvez precisem dar suporte a **GetSearchCriteria** somente se eles fornecerem os recursos avançados de pesquisa associados à propriedade **PR_SEARCH** ([PidTagSearch).](pidtagsearch-canonical-property.md) For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando terminar as estruturas de dados apontadas pelos parâmetros  _lppRestriction_ e  _lppContainerList,_ chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura a ser liberada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa o **método IMAPIContainer::GetSearchCriteria** para obter critérios de pesquisa de uma pasta a ser exibida.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

