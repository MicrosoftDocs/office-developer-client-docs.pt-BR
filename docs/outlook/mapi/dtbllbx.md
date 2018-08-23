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
ms.openlocfilehash: 35e19a4281c46ae7c2b5cbd76c1ecea35bf87665
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569761"
---
# <a name="dtbllbx"></a>DTBLLBX

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma lista que será usada em uma caixa de diálogo que é construída a partir de uma tabela de exibição.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _DTBLLBX
{
  ULONG ulFlags;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLLBX, FAR *LPDTBLLBX

```

## <a name="members"></a>Members

 **ulFlags**
  
> Bitmask dos sinalizadores usados para eliminar uma barra de rolagem horizontal ou vertical da lista. Sinalizadores a seguir podem ser definidos:
    
MAPI_NO_HBAR 
  
> Nenhuma barra de rolagem horizontal deve ser exibida com a lista.
    
MAPI_NO_VBAR 
  
> Nenhuma barra de rolagem vertical deve ser exibida com a lista.
    
 **ulPRSetProperty**
  
> Marca de propriedade para uma propriedade de qualquer tipo. Essa propriedade é uma das colunas na tabela identificado pelo membro **ulPRTableTable** . 
    
 **ulPRTableName**
  
> Marca de propriedade para uma propriedade de tabela do tipo PT_OBJECT que podem ser abertos usando uma **OpenProperty** chamar. O número de colunas que a tabela deve ter depende se a lista é uma lista de seleção única ou múltipla. Se o membro **ulPRSetProperty** é definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)), a lista permite a seleção múltipla.
    
## <a name="remarks"></a>Comentários

Uma estrutura **DTBLLBX** descreve uma um controle que é usado para mostrar vários itens e permitir que o usuário selecione um ou mais dos itens de lista. 
  
O membro **ulPRSetProperty** e o membro **ulPRTableName** trabalhar juntos; Quando um valor for escolhido da tabela, ele será gravado novamente **ulPRSetProperty** quando a caixa de diálogo é descartada. 
  
O valor de flags indica se uma barra de rolagem horizontal ou vertical deve ser exibida com a lista. O padrão é a ter tipos de barra de rolagem aparece se for necessário. Provedores de serviços podem definir MAPI_NO_HBAR para suprimir a uma barra de rolagem horizontal e MAPI_NO_VBAR para suprimir a uma barra de rolagem vertical. 
  
Os membros da marca de dois propriedade funcionam juntos para exibir valores na lista e definir propriedades correspondentes, quando um item na lista é selecionado. Quando o MAPI primeiro exibe a lista, ele chama o método de **OpenProperty** da implementação **IMAPIProp** para recuperar a tabela identificada no membro **ulPRTableName** . O número de colunas na tabela depende do valor do membro **ulPRSetProperty** . Se **ulPRSetProperty** for definido como **PR_NULL**, a lista é uma lista de seleção de vários com base em um objeto que contém os destinatários, como um contêiner de catálogo de endereços, uma tabela de destinatários de uma mensagem ou uma tabela de conteúdo de lista de distribuição. 
  
Um objeto table para uma lista de seleção de vários deve incluir as seguintes colunas:
  
 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
  
 **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
  
 **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) e um máximo de cinco outras propriedades de cadeia de caracteres de valores múltiplos também pode ser exibido com as três colunas obrigatórias. 
  
Se o membro **ulPRSetProperty** não estiver definido como **PR_NULL**, a lista é uma lista de seleção única. O valor inicial de **ulPRSetProperty** determina a primeira linha selecionada. Quando um usuário seleciona uma das linhas, o membro **ulPRSetProperty** for definido como o valor selecionado e esse valor será gravado novamente a implementação de interface de propriedade com uma chamada para [IMAPIProp::SetProps](imapiprop-setprops.md). 
  
Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md). Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).
  
## <a name="see-also"></a>Confira também



[DTCTL](dtctl.md)


[Estruturas MAPI](mapi-structures.md)

