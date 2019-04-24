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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349291"
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
  
> no Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _lppRestriction_
  
> bota Um ponteiro para um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa. Se um aplicativo cliente passar nulo no parâmetro _lppRestriction_ , **GetSearchCriteria** não retornará uma estrutura **SRestriction** . 
    
 _lppContainerList_
  
> bota Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam contêineres a serem incluídos na pesquisa. Se um cliente passar nulo no parâmetro _lppContainerList_ , **GetSearchCriteria** não retornará uma matriz de identificadores de entrada. 
    
 _lpulSearchState_
  
> bota Um ponteiro para uma bitmask de sinalizadores usados para indicar o estado atual da pesquisa. Se um cliente passar nulo no parâmetro _lpulSearchState_ , **GetSearchCriteria** não retornará nenhum sinalizador. Os seguintes sinalizadores podem ser definidos: 
    
SEARCH_FOREGROUND 
  
> A pesquisa deve ser executada com prioridade alta em relação a outras pesquisas. Se esse sinalizador não for definido, a pesquisa será executada em prioridade normal em relação a outras pesquisas.
    
SEARCH_REBUILD 
  
> A pesquisa está no modo de CPU intensa de sua operação, tentando localizar mensagens que correspondam aos critérios. Se esse sinalizador não for definido, a parte intensiva da CPU da operação da pesquisa será sobre. Esse sinalizador tem significado somente se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING estiver definido).
    
SEARCH_RECURSIVE 
  
> A pesquisa está procurando por contêineres especificados e todos os seus contêineres filhos para entradas correspondentes. Se esse sinalizador não estiver definido, somente os contêineres incluídos explicitamente na última chamada para o método [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) estão sendo pesquisados. 
    
SEARCH_RUNNING 
  
> A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no repositório de mensagens ou no catálogo de endereços. Se esse sinalizador não for definido, a pesquisa estará inativa e a tabela de conteúdo será estática.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os critérios de pesquisa foram obtidos com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Os critérios de pesquisa nunca foram estabelecidos para o contêiner.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer:: GetSearchCriteria** Obtém os critérios de pesquisa para um contêiner que oferece suporte a pesquisas, normalmente uma pasta de resultados de pesquisa. Você cria critérios de pesquisa chamando o método **IMAPIContainer:: SetSearchCriteria** do contêiner. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os contêineres do catálogo de endereços podem precisar de suporte para o **GetSearchCriteria** somente se eles fornecerem os recursos de pesquisa avançada associados à propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Para obter mais informações sobre como implementar o recurso de pesquisa avançada para contêineres do catálogo de endereços, consulte [implementação de pesquisa avançada](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você tiver concluído as estruturas de dados apontadas pelos parâmetros _lppRestriction_ e _LppContainerList_ , chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura a ser liberada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableDlg. cpp  <br/> |CHierarchyTableDlg:: OnEditSearchCriteria  <br/> |MFCMAPI usa o método **IMAPIContainer:: GetSearchCriteria** para obter critérios de pesquisa de uma pasta a ser exibida.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

