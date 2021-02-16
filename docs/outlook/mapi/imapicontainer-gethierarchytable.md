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
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426195"
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
  
> [in] Uma máscara de bits de sinalizadores que controla como as informações são retornadas na tabela. Os sinalizadores a seguir podem ser definidos:
    
CONVENIENT_DEPTH 
  
> Preenche a tabela de hierarquia com contêineres de vários níveis. Se CONVENIENT_DEPTH não estiver definida, a tabela de hierarquias conterá apenas os contêineres filho imediatos do contêiner.
    
MAPI_DEFERRED_ERRORS 
  
> **GetHierarchyTable** pode retornar com êxito, possivelmente antes da tabela ser disponibilizada para o chamador. Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá criar um erro. 
    
MAPI_UNICODE 
  
> Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Mostra itens que estão marcados como excluídos de forma suave, ou seja, eles estão na fase de tempo de retenção de itens excluídos.
    
 _lppTable_
  
> [out] Um ponteiro para um ponteiro para a tabela de hierarquia.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de hierarquias foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação dá suporte apenas a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O contêiner não tem contêineres filhos e não pode fornecer uma tabela de hierarquia.
    
## <a name="remarks"></a>Comentários

O **método IMAPIContainer::GetHierarchyTable** retorna um ponteiro para a tabela de hierarquia de um contêiner. Uma tabela de hierarquia contém informações resumidas sobre os contêineres filho no contêiner. As tabelas de hierarquia de pastas têm informações sobre subpastas; as tabelas de hierarquia do livro de endereços têm informações sobre contêineres do livro de endereços filho e listas de distribuição. 
  
É possível que alguns contêineres não tenham contêineres filhos. Esses contêineres retornam MAPI_E_NO_SUPPORT de suas implementações de **GetHierarchyTable**.
  
Quando o CONVENIENT_DEPTH de comando é definido, cada linha na tabela de hierarquia também inclui a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como uma coluna. **PR_DEPTH** indica o nível de cada contêiner em relação ao contêiner que implementa a tabela. Os contêineres filho imediatos do contêiner estão na profundidade zero, os contêineres filho nos contêineres de profundidade zero estão em profundidade um e assim por diante. Os valores de **PR_DEPTH** aumentam sequencialmente à medida que a hierarquia de níveis se aprofunda. 
  
Para uma lista completa de colunas necessárias e opcionais em tabelas de hierarquias, consulte [Tabelas de Hierarquia.](hierarchy-tables.md)
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você tiver suporte para uma tabela de hierarquia para seu contêiner, também deverá fazer o seguinte:
  
- Suporte a uma chamada para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Retorne **PR_CONTAINER_HIERARCHY** de uma chamada para os métodos [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) do contêiner. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

As colunas da tabela de cadeia de caracteres e conteúdo binário podem ser truncadas. Normalmente, os provedores retornam 255 caracteres. Como não é possível saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna seja truncada se o tamanho da coluna for de 255 ou 510 bytes. Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-la e, em seguida, chamando o método [IMAPIProp::GetProps.](imapiprop-getprops.md) 
  
Dependendo da implementação do provedor, as restrições e as operações de classificação podem ser aplicadas à cadeia de caracteres inteira ou à versão truncada dessa cadeia de caracteres. Além disso, os provedores de armazenamento não têm garantia de atender ao conjunto de ordem de classificação [SSortOrderSet](ssortorderset.md) especificado para tabelas de hierarquia. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl.cpp  <br/> |CHierarchyTableTreeCtrl::GetHierarchyTable  <br/> |A classe CHierarchyTableTreeCtrl usa **GetHierarchyTable** para obter tabelas de hierarquia para exibir em um controle de exibição de árvore.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

