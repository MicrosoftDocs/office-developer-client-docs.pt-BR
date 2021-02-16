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
# <a name="table_notification"></a>TABLE_NOTIFICATION

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve uma linha em uma tabela que foi afetada por algum tipo de evento, como uma alteração ou um erro. Isso faz com que uma notificação de tabela seja gerada. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
   
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
  
> Bitmask de sinalizadores usados para representar o tipo de evento de tabela. Os sinalizadores a seguir podem ser definidos:
    
TABLE_CHANGED 
  
> Indica em um nível alto que algo sobre a tabela foi alterado. O estado da tabela é como era antes do evento. Isso significa que **todas PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) , indicadores, posicionamento atual e seleções de interface do usuário ainda são válidas. Manipular esse evento relendo a tabela. Os provedores de serviços que não querem implementar notificações de tabelas detalhadas enviam TABLE_CHANGED eventos em vez de eventos mais detalhados para indicar um tipo específico de alteração. 
    
TABLE_ERROR 
  
> Ocorreu um erro, geralmente durante o processamento de uma operação assíncrona. Erros durante o processamento dos seguintes métodos podem gerar esse evento: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Depois de receber TABLE_ERROR evento, um cliente não pode confiar na precisão do conteúdo da tabela. Além disso, as notificações pendentes sobre outras alterações podem ser perdidas. O [método IMAPITable::GetLastError](imapitable-getlasterror.md) pode não fornecer informações adicionais sobre o erro porque ele foi gerado em algum ponto anterior, não necessariamente a partir da última chamada de método. 
    
TABLE_RELOAD 
  
> Os dados na tabela devem ser recarregados. Os provedores de serviços enviam TABLE_RELOAD quando, por exemplo, os dados subjacentes são armazenados em um banco de dados e o banco de dados é substituído. Manipular esse evento supondo que nada sobre a tabela ainda seja válido e relendo a tabela. Todos os indicadores, chaves de instância, informações de status e posicionamento são inválidos.
    
TABLE_RESTRICT_DONE 
  
> Uma operação de restrição iniciada com uma chamada de método **IMAPITable::Restrict** foi concluída. 
    
TABLE_ROW_ADDED 
  
> Uma nova linha foi adicionada à tabela e o objeto correspondente foi salvo. TABLE_ROW_ADDED eventos são gerados após uma chamada para o [método IMAPIProp::SaveChanges.](imapiprop-savechanges.md) 
    
TABLE_ROW_DELETED 
  
> Uma linha foi removida da tabela. O **membro propPrior** é definido como NULL. 
    
TABLE_ROW_MODIFIED 
  
> Uma linha foi alterada. O **membro** da linha contém as propriedades afetadas para a linha. Vários TABLE_ROW_MODIFIED eventos são enviados na ordem em que aparecem no modo de exibição de tabela. 
    
  TABLE_ROW_MODIFIED eventos são enviados depois que as alterações no objeto correspondente são comprometidas com uma chamada para o método **IMAPIProp::SaveChanges.** Se a linha modificada agora for a primeira linha na tabela, o valor da marca de propriedade no membro **propPrior** **será PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Uma operação de configuração de coluna iniciada com uma chamada do método **IMAPITable::SetColumns** foi concluída. 
    
TABLE_SORT_DONE 
  
> Uma operação de classificação de tabela iniciada com uma chamada de método **IMAPITable::SortTable** foi concluída. 
    
**hResult**
  
> Valor HRESULT do erro ocorrido, se o **membro ulTableEvent** estiver definido como TABLE_ERROR. 
    
**propIndex**
  
> [Estrutura SPropValue](spropvalue.md) para a **PR_INSTANCE_KEY** propriedade da linha afetada. 
    
**propPrior**
  
> **Estrutura SPropValue** para a **PR_INSTANCE_KEY** propriedade da linha antes da afetada. Se a linha afetada for a primeira linha na tabela, **propPrior** deverá ser definido como **PR_NULL** e não como zero. Zero não é uma marca de propriedade válida. 
    
**row**
  
> [Estrutura SRow](srow.md) que descreve a linha afetada. Essa estrutura é preenchida para todos os eventos de notificação de tabela. Para eventos de notificação de tabela que não passam dados de linha, o membro **cValues** da estrutura **SRow** é definido como zero e o membro **lpProps** é definido como NULL. Como essa **estrutura SRow** é somente leitura; os clientes devem fazer uma cópia se quiserem fazer modificações. A [função ScDupPropset](scduppropset.md) pode ser usada para fazer a cópia. 
    
## <a name="remarks"></a>Comentários

A **estrutura \_ DE NOTIFICAÇÃO** DE TABELA é um dos membros da união de estruturas incluídas no membro **de** informações da estrutura [NOTIFICATION.](notification.md) O **membro** de informações inclui uma estrutura **DE \_ NOTIFICAÇÃO DE** TABELA quando o membro **ulEventType** da estrutura é definido como  _fnevTableModified_.
  
A ordem e o tipo de colunas no membro da linha refletem a ordem e o tipo que estava em vigor no momento em que a notificação foi gerada. A ordem e o tipo no momento em que a notificação foi gerada não é necessariamente o mesmo de quando a notificação foi entregue. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificação de evento em MAPI](event-notification-in-mapi.md) <br/> |Visão geral dos eventos de notificação e notificação.  <br/> |
|[Manipulando notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem lidar com notificações.  <br/> |
|[Suporte à notificação de evento](supporting-event-notification.md) <br/> |Discussão sobre como os provedores de serviços podem usar o **método IMAPISupport** para gerar notificações.  <br/> |
   
Como as notificações de tabela são assíncronas, os clientes podem receber uma notificação de uma linha adicionada depois de aprender sobre a adição por meio de outro meio. É possível receber um evento TABLE_ERROR quando há um erro em um **método IMAPITable::Sort**, **IMAPITable::Restrict** ou **IMAPITable::SetColumns** ou quando um processo subjacente tenta atualizar uma tabela com, por exemplo, linhas novas ou modificadas. 
  
## <a name="see-also"></a>Confira também

- [NOTIFICAÇÃO](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estruturas MAPI](mapi-structures.md)

