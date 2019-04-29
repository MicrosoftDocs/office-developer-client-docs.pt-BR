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
  
> no Uma bitmask de sinalizadores que controla como as informações são retornadas na tabela. Os seguintes sinalizadores podem ser definidos:
    
CONVENIENT_DEPTH 
  
> Preenche a tabela de hierarquia com contêineres de vários níveis. Se CONVENIENT_DEPTH não for definido, a tabela de hierarquia conterá apenas os contêineres filhos imediatos do contêiner.
    
MAPI_DEFERRED_ERRORS 
  
> **** GetHierarchyTable pode retornar com êxito, possivelmente antes de a tabela ser disponibilizada para o chamador. Se a tabela não estiver disponível, fazer uma chamada de tabela subsequente poderá gerar um erro. 
    
MAPI_UNICODE 
  
> Solicita que as colunas que contêm dados de cadeia de caracteres sejam retornadas no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres deverão ser retornadas no formato ANSI. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens atualmente marcados como excluídos por software, ou seja, estão na fase de tempo de retenção de item excluído.
    
 _lppTable_
  
> bota Um ponteiro para um ponteiro para a tabela de hierarquia.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A tabela de hierarquia foi recuperada com êxito.
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação oferece suporte somente a Unicode.
    
MAPI_E_NO_SUPPORT 
  
> O contêiner não tem contêineres filho e não pode fornecer uma tabela de hierarquia.
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::** GetHierarchyTable retorna um ponteiro para a tabela de hierarquia de um contêiner. Uma tabela de hierarquia contém informações de resumo sobre os contêineres filhos no contêiner. Tabelas de hierarquia de pastas armazenam informações sobre subpastas; As tabelas de hierarquia de catálogo de endereços armazenam informações sobre contêineres e listas de distribuição de catálogo de endereços filho. 
  
É possível que alguns contêineres não tenham contêineres filhos. Esses contêineres retornam MAPI_E_NO_SUPPORT de suas **** implementações de GetHierarchyTable.
  
Quando o sinalizador CONVENIENT_DEPTH é definido, cada linha na tabela de hierarquia também inclui a propriedade **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) como uma coluna. **PR_DEPTH** indica o nível de cada contêiner em relação ao contêiner que implementa a tabela. Os contêineres filhos imediatos de implementação do contêiner estão em profundidade zero, os contêineres filho nos contêineres de profundidade zero estão em profundidade um e assim por diante. Os valores de **PR_DEPTH** aumentam de forma seqüencial à medida que a hierarquia dos níveis aprofunda. 
  
Para obter uma lista completa de colunas obrigatórias e opcionais em tabelas de hierarquia, consulte [tabelas de hierarquia](hierarchy-tables.md).
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Se você oferecer suporte a uma tabela de hierarquia para seu contêiner, você também deve fazer o seguinte:
  
- Suporte a uma chamada para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).
    
- Retornar **PR_CONTAINER_HIERARCHY** de uma chamada para os métodos [IMAPIProp::](imapiprop-getproplist.md) getproplist ou [IMAPIProp::](imapiprop-getprops.md) GetProps do contêiner. 
    
## <a name="notes-to-callers"></a>Notas para chamadores

As colunas da tabela de conteúdo binário e cadeia de caracteres podem ser truncadas. Normalmente, os provedores retornam 255 caracteres. Como você não pode saber antecipadamente se uma tabela inclui colunas truncadas, suponha que uma coluna será truncada se o comprimento da coluna for 255 ou 510 bytes. Você sempre pode recuperar o valor completo de uma coluna truncada, se necessário, diretamente do objeto usando seu identificador de entrada para abri-lo e, em seguida, chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps. 
  
Dependendo da implementação do provedor, as operações de classificação e restrições podem ser aplicadas à cadeia de caracteres inteira ou à versão truncada dessa cadeia de caracteres. Além disso, os provedores de repositório não são garantidos para honrar a ordem de classificação definida [SSortOrderSet](ssortorderset.md) especificada para tabelas de hierarquia. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|HierarchyTableTreeCtrl. cpp  <br/> |CHierarchyTableTreeCtrl:: getHierarchytable  <br/> |A classe CHierarchyTableTreeCtrl usa **** GetHierarchyTable para obter tabelas de hierarquia a serem exibidas em um controle de modo de exibição de árvore.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Propriedade canônica PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

