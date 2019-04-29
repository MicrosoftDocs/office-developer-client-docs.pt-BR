---
title: TABLE_NOTIFICATION
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TABLE_NOTIFICATION
api_type:
- COM
ms.assetid: 48e478c4-6e9a-40ab-a7bb-e6219b743b08
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6c35220529fb88b470c563a0b004bfcf7e63ef76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415954"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma linha em uma tabela que foi afetada por algum tipo de evento, como uma alteração ou um erro. Isso faz com que uma notificação de tabela seja gerada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _TABLE_NOTIFICATION
{
  ULONG ulTableEvent;
  HRESULT hResult;
  SPropValue propIndex;
  SPropValue propPrior;
  SRow row;
} TABLE_NOTIFICATION;

```

## <a name="members"></a>Members

**ulTableEvent**
  
> Bitmask dos sinalizadores usados para representar o tipo de evento Table. Os seguintes sinalizadores podem ser definidos:
    
TABLE_CHANGED 
  
> Indica em um nível alto que algo sobre a tabela foi alterado. O estado da tabela é como era antes do evento. Isso significa que todas as propriedades de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), indicadores, posicionamento atual e seleções de interface do usuário ainda são válidas. Manipule esse evento relendo a tabela. Os provedores de serviços que não querem implementar notificações de tabela rica enviam eventos TABLE_CHANGED em vez de eventos mais detalhados para indicar um tipo específico de alteração. 
    
TABLE_ERROR 
  
> Ocorreu um erro, geralmente durante o processamento de uma operação assíncrona. Erros durante o processamento dos seguintes métodos podem gerar esse evento: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Após receber um evento TABLE_ERROR, um cliente não pode depender da precisão do conteúdo da tabela. Além disso, as notificações pendentes sobre outras alterações podem ser perdidas. O método imApitable [:: GetLastError](imapitable-getlasterror.md) pode não fornecer informações adicionais sobre o erro, pois ele foi gerado em algum ponto anterior, não necessariamente da última chamada do método. 
    
TABLE_RELOAD 
  
> Os dados da tabela devem ser recarregados. Os provedores de serviços enviam TABLE_RELOAD Quando, por exemplo, os dados subjacentes são armazenados em um banco de dados e o banco de dados é substituído. Manipule esse evento supondo que nada sobre a tabela ainda seja válido e releia a tabela. Todos os indicadores, as teclas de instância, o status e as informações de posicionamento são inválidos.
    
TABLE_RESTRICT_DONE 
  
> Uma operação de restrição iniciada com uma chamada de método imApitable **:: Restrict** foi concluída. 
    
TABLE_ROW_ADDED 
  
> Uma nova linha foi adicionada à tabela e o objeto correspondente foi salvo. Eventos TABLE_ROW_ADDED são gerados após uma chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Uma linha foi removida da tabela. O membro **propPrior** está definido como nulo. 
    
TABLE_ROW_MODIFIED 
  
> Uma linha foi alterada. O membro **Row** contém as propriedades afetadas para a linha. Vários eventos TABLE_ROW_MODIFIED são enviados na ordem em que aparecem no modo de exibição de tabela. 
    
  Os eventos TABLE_ROW_MODIFIED são enviados após as alterações no objeto correspondente terem sido confirmadas com uma chamada para o método **IMAPIProp:: SaveChanges** . Se a linha modificada agora for a primeira linha na tabela, o valor da marca de propriedade no membro **propPrior** será **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Uma operação de configuração de coluna iniciada com uma chamada de método imApitable **::** SetColumns foi concluída. 
    
TABLE_SORT_DONE 
  
> Uma operação de classificação de tabela iniciada com uma chamada de método imApitable **:: SortTable** foi concluída. 
    
**And**
  
> Valor HRESULT para o erro que ocorreu, se o membro **ulTableEvent** estiver definido como TABLE_ERROR. 
    
**propIndex**
  
> Estrutura [SPropValue](spropvalue.md) para a propriedade **PR_INSTANCE_KEY** da linha afetada. 
    
**propPrior**
  
> Estrutura **SPropValue** da propriedade **PR_INSTANCE_KEY** da linha antes da afetada. Se a linha afetada for a primeira linha na tabela, **propPrior** deverá ser definido como **PR_NULL** e não como zero. Zero não é uma marca de propriedade válida. 
    
**Row**
  
> Estrutura [SRow](srow.md) descrevendo a linha afetada. Essa estrutura é preenchida para todos os eventos de notificação de tabela. Para eventos de notificação de tabela que não passam dados de linha, o membro **cValues** da estrutura **SRow** é definido como zero e o membro **lpProps** é definido como nulo. Como essa estrutura **SRow** é somente leitura; Os clientes devem fazer uma cópia deles se desejarem fazer modificações. A função [ScDupPropset](scduppropset.md) pode ser usada para fazer a cópia. 
    
## <a name="remarks"></a>Comentários

A estrutura de **notificação de\_tabela** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) . O membro **info** inclui uma estrutura de **notificação de\_tabela** quando o membro **ulEventType** da estrutura é definido como _fnevTableModified_.
  
A ordem e o tipo de colunas no membro da linha refletem a ordem e o tipo que estava em vigor no momento em que a notificação foi gerada. A ordem e o tipo no momento em que a notificação foi gerada não é necessariamente o mesmo que quando a notificação foi entregue. 
  
Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento no MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos Notification e Notification.  <br/> |
|[Manipular notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Notificação de evento de suporte](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
Como as notificações de tabela são assíncronas, os clientes podem receber a notificação de uma linha adicionada após aprender sobre a adição por outro meio. É possível receber um evento TABLE_ERROR quando há um erro em um método imApitable: **: Sort**, IMAPITable: **: reStrict**ou imapitaBle:: SetColumns ou quando um processo subjacente tenta atualizar uma tabela com, por exemplo, novo ou **** linhas modificadas. 
  
## <a name="see-also"></a>Confira também

- [Notifica](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estruturas MAPI](mapi-structures.md)

