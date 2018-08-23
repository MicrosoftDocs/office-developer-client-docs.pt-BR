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
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579960"
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
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _lppRestriction_
  
> [out] Um ponteiro para um ponteiro para uma estrutura [SRestriction](srestriction.md) que define os critérios de pesquisa. Se um aplicativo cliente transmite NULL no parâmetro _lppRestriction_ , **obter GetSearchCriteria** não retorna uma estrutura **SRestriction** . 
    
 _lppContainerList_
  
> [out] Um ponteiro para um ponteiro para uma matriz de identificadores de entrada que representam os contêineres a serem incluídos na pesquisa. Se um cliente transmite NULL no parâmetro _lppContainerList_ , **obter GetSearchCriteria** não retorna uma matriz de identificadores de entrada. 
    
 _lpulSearchState_
  
> [out] Um ponteiro para uma bitmask dos sinalizadores usados para indicar o estado atual da pesquisa. Se um cliente transmite NULL no parâmetro _lpulSearchState_ , **obter GetSearchCriteria** não retorna nenhuma sinalizadores. Sinalizadores a seguir podem ser definidos: 
    
SEARCH_FOREGROUND 
  
> A pesquisa deve ser executado em alta prioridade em relação a outras pesquisas. Se esse sinalizador não estiver definida, a pesquisa é executado com prioridade normal em relação a outras pesquisas.
    
SEARCH_REBUILD 
  
> A pesquisa está no modo intensivo da CPU de sua operação, tentar localizar mensagens que correspondem aos critérios. Se esse sinalizador não estiver definida, a parte de intensivo da CPU da operação de pesquisa é sobre. Esse sinalizador tem significado apenas se a pesquisa estiver ativa (ou seja, se o sinalizador SEARCH_RUNNING está definido).
    
SEARCH_RECURSIVE 
  
> A pesquisa está procurando nos contêineres especificados e todos os seus contêineres filho para entradas correspondentes. Se esse sinalizador não estiver definida, somente os contêineres explicitamente incluídos na última chamada para o método [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) estão sendo pesquisados. 
    
SEARCH_RUNNING 
  
> A pesquisa está ativa e a tabela de conteúdo do contêiner está sendo atualizada para refletir as alterações no repositório de mensagem ou o catálogo de endereços. Se esse sinalizador não estiver definida, a pesquisa está inativa e a tabela de conteúdo é estática.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os critérios de pesquisa foi obtida com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_NOT_INITIALIZED 
  
> Critérios de pesquisa nunca estabelecidos para o contêiner.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::GetSearchCriteria** obtém os critérios de pesquisa para um contêiner que suporta pesquisas, geralmente, uma pasta de resultados de pesquisa. Você pode criar critérios de pesquisa chamando o método de **IMAPIContainer::SetSearchCriteria** de um contêiner. 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Contêineres de catálogo de endereços, talvez seja necessário dar suporte ao **obter GetSearchCriteria** somente se eles oferecem as capacidades de pesquisa avançada associadas com a propriedade **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)). Para obter mais informações sobre como implementar o recurso de pesquisa avançada para contêineres do catálogo de endereços, consulte [Implementando a pesquisa avançada](implementing-advanced-searching.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando tiver terminado com as estruturas de dados apontadas pelos parâmetros _lppRestriction_ e _lppContainerList_ , chame [MAPIFreeBuffer](mapifreebuffer.md) uma vez para cada estrutura ser liberada. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableDlg.cpp  <br/> |CHierarchyTableDlg::OnEditSearchCriteria  <br/> |MFCMAPI usa o método **IMAPIContainer::GetSearchCriteria** para obter os critérios de pesquisa de uma pasta para exibir.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)
  
[IMAPIFolder::CreateFolder](imapifolder-createfolder.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propriedade canônica PidTagSearch](pidtagsearch-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

