---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563797"
---
# <a name="imapicontainergethierarchytable"></a>IMAPIContainer::GetHierarchyTable

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro para a tabela de hierarquia do contêiner.
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como as informações são retornadas na tabela. Sinalizadores a seguir podem ser definidos:
    
CONVENIENT_DEPTH 
  
> Preenche a tabela de hierarquia com contêineres de vários níveis. Se CONVENIENT_DEPTH não estiver definida, a tabela de hierarquia contém apenas os contêineres de filho imediato do contêiner.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** pode retornar com êxito, possivelmente antes que a tabela é disponibilizada para o chamador. Se a tabela não estiver disponível, fazendo uma chamada de tabela subsequentes pode gerar um erro. 
    
MAPI_UNICODE 
  
> Solicitações que as colunas que contêm dados de cadeia de caracteres a ser retornado em formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem ser retornadas no formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens que estão marcados como suaves excluídos — ou seja, eles estão na retenção de item excluído fase de tempo.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de hierarquia.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A tabela de hierarquia foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação suporta somente Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O contêiner tem sem contêineres filho e não pode fornecer uma tabela de hierarquia.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::GetHierarchyTable** retorna um ponteiro para a tabela de hierarquia de um contêiner. Uma tabela de hierarquia contém informações de resumo sobre os contêineres filho no contêiner. Tabelas de hierarquias de pasta mantêm informações sobre subpastas; tabelas de hierarquias de catálogo de endereços mantêm informações sobre filho contêineres do catálogo de endereços e listas de distribuição. 
  
É possível que alguns contêineres ter sem contêineres filho. Desses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetHierarchyTable**.
  
Quando o sinalizador CONVENIENT_DEPTH estiver definido, cada linha da tabela de hierarquia também inclui a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como uma coluna. **PR_DEPTH** indica o nível de cada contêiner em relação ao contêiner que implementa a tabela. Filho imediato de implementação do contêiner contêineres correm depth zero, recipientes filho nos contêineres de zero profundidade correm profundidade um e assim por diante. Os valores de **PR_DEPTH** aumentam sequencialmente à medida que aprofunda a hierarquia dos níveis. 
  
Para obter uma lista completa das colunas obrigatórios e opcionais em tabelas de hierarquias, consulte as [Tabelas de hierarquias](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Caso você ofereça suporte a uma tabela de hierarquia de seu contêiner, você deve também faça o seguinte:
  
- Suporte a uma chamada ao método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Retorne **PR_CONTAINER_HIERARCHY** de uma chamada para os métodos de [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

Cadeia de caracteres e binário colunas da tabela de conteúdo podem ser truncadas. Normalmente, provedores retornam 255 caracteres. Porque você não pode saber com antecedência se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna é 255 ou 510 bytes. Você sempre pode recuperar o valor completo de uma coluna truncado, se necessário, diretamente do objeto utilizando seu identificador de entrada para abri-lo e, em seguida, chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Dependendo da implementação do provedor, restrições e operações de classificação podem aplicar para a cadeia de caracteres inteira ou para a versão truncada da cadeia de caracteres. Além disso, provedores de armazenamento não há uma garantia honram o conjunto de ordem de classificação [que ssortorderset](ssortorderset.md) especificado para tabelas de hierarquias. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |A classe CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obter as tabelas de hierarquias para exibir em um controle de exibição de árvore.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

