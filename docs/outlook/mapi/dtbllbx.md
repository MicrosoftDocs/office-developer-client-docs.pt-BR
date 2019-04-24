---
title: DTBLLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLLBX
api_type:
- COM
ms.assetid: 971b4837-6823-4f28-9803-3c22b2ec091f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2bff20af2b3e9ea4e203e38ae38a8bc19074a727
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321229"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Membros

 **ulFlags**
  
> Bitmask dos sinalizadores usados para eliminar uma barra de rolagem horizontal ou vertical da lista. Os seguintes sinalizadores podem ser definidos:
    
MAPI_NO_HBAR 
  
> Nenhuma barra de rolagem horizontal deve ser mostrada com a lista.
    
MAPI_NO_VBAR 
  
> Nenhuma barra de rolagem vertical deve ser exibida com a lista.
    
 **ulPRSetProperty**
  
> Marca de propriedade de uma propriedade de qualquer tipo. Essa propriedade é uma das colunas na tabela identificadas pelo membro **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Marca de propriedade de uma propriedade de tabela do tipo PT_OBJECT que pode ser aberta usando **** uma chamada OpenProperty. O número de colunas que a tabela deve ter depende se a lista é uma única ou múltipla lista de seleção. Se o membro **ulPRSetProperty** estiver definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), a lista permitirá a seleção múltipla.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLLBX** descreve uma lista um controle que é usado para mostrar vários itens e permitir que um usuário selecione um ou mais itens. 
  
O membro **ulPRSetProperty** e o membro **ulPRTableName** funcionam juntos; Quando um valor é escolhido na tabela, ele é gravado novamente no **ulPRSetProperty** quando a caixa de diálogo é descartada. 
  
O valor flags indica se uma barra de rolagem horizontal ou vertical deve ser exibida com a lista. O padrão é que os tipos de barras de rolagem apareçam se necessário. Os provedores de serviços podem definir MAPI_NO_HBAR para suprimir uma barra de rolagem horizontal e MAPI_NO_VBAR para suprimir uma barra de rolagem vertical. 
  
Os dois membros da marca de propriedade trabalham juntos para exibir valores na lista e definir as propriedades correspondentes quando um item da lista é selecionado. Quando MAPI exibe primeiro a lista, ele chama o método OpenProperty **** da implementação do **IMAPIProp** para recuperar a tabela identificada no membro **ulPRTableName** . O número de colunas na tabela depende do valor do membro **ulPRSetProperty** . Se **ulPRSetProperty** estiver definido como **PR_NULL**, a lista é uma lista de seleção múltipla com base em um objeto que contém destinatários, como um contêiner de catálogo de endereços, uma tabela de destinatários para uma mensagem ou uma tabela de conteúdo da lista de distribuição. 
  
Uma tabela para uma lista de seleção múltipla deve incluir as seguintes colunas:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) e um máximo de cinco outras propriedades de cadeia de caracteres com valores múltiplos também podem ser exibidos com as três colunas obrigatórias. 
  
Se o membro **ulPRSetProperty** não estiver definido como **PR_NULL**, a lista será uma única lista de seleção. O valor inicial de **ulPRSetProperty** determina a primeira linha selecionada. Quando um usuário seleciona uma das linhas, o membro **ulPRSetProperty** é definido para o valor selecionado e esse valor é gravado novamente na implementação da interface de propriedade com uma chamada para [IMAPIProp::](imapiprop-setprops.md)SetProps. 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

