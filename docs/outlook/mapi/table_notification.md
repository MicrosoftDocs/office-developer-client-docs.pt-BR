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
ms.openlocfilehash: fd77473ce728a51220a4c039f1d12d03d90e7f36
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770586"
---
# <a name="tablenotification"></a>TABLE_NOTIFICATION

**Aplica-se a**: Outlook 
  
Descreve uma linha em uma tabela que foi afetada por algum tipo de evento, como uma alteração ou um erro. Isso faz com que uma notificação de tabela a ser gerado. 
  
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
  
> Bitmask dos sinalizadores usado para representar o tipo de evento de tabela. Sinalizadores a seguir podem ser definidos:
    
TABLE_CHANGED 
  
> Indica nitidamente que algo sobre a tabela foi alterado. Estado da tabela é como era antes do evento. Isso significa que todas as propriedades de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), indicadores, posicionamento atual e seleções de interface do usuário são ainda válidas. Manipule esse evento, releitura a tabela. Provedores de serviços que não deseja implementar notificações de tabela rich enviam eventos TABLE_CHANGED em vez de eventos mais detalhados para indicar um tipo específico de alteração. 
    
TABLE_ERROR 
  
> Ocorreu um erro, geralmente durante o processamento de uma operação assíncrona. Erros durante o processamento dos métodos a seguir podem gerar esse evento: 
    
   - [IMAPITable::SortTable](imapitable-sorttable.md)
    
   - [IMAPITable::SetColumns](imapitable-setcolumns.md)
    
   - [IMAPITable::Restrict](imapitable-restrict.md)
    
   Após receber um evento TABLE_ERROR, um cliente não pode depender a precisão do conteúdo da tabela. Além disso, notificações sobre outras alterações pendentes podem ser perdidas. O método [IMAPITable::GetLastError](imapitable-getlasterror.md) não pode fornecer informações adicionais sobre o erro porque ela foi gerada em algum momento anterior, não necessariamente da última chamada de método. 
    
TABLE_RELOAD 
  
> Os dados na tabela devem ser recarregados. Provedores de serviços enviam TABLE_RELOAD quando, por exemplo, os dados subjacentes são armazenados em um banco de dados e o banco de dados foi substituído. Manipule esse evento por supondo que nada sobre a tabela ainda é válido e por releitura a tabela. Todos os indicadores, chaves da instância, status e informações de posicionamento são inválidos.
    
TABLE_RESTRICT_DONE 
  
> Uma operação de restrição iniciada com uma chamada de método **IMAPITable:: Restrict** foi concluída. 
    
TABLE_ROW_ADDED 
  
> Foi adicionada uma nova linha à tabela de e o objeto correspondente salvo. Eventos TABLE_ROW_ADDED são gerados após uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . 
    
TABLE_ROW_DELETED 
  
> Uma linha foi removida da tabela. O membro **propPrior** é definido como NULL. 
    
TABLE_ROW_MODIFIED 
  
> Uma linha foi alterada. O membro de **linha** contém as propriedades afetadas para a linha. Vários eventos TABLE_ROW_MODIFIED são enviados na ordem em que eles aparecem no modo de exibição de tabela. 
    
  Eventos TABLE_ROW_MODIFIED são enviados depois que forem confirmadas com uma chamada ao método **IMAPIProp::SaveChanges** alterações ao objeto correspondente. Se a linha modificada agora for a primeira linha da tabela, o valor da propriedade marca no membro **propPrior** é **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).
    
TABLE_SETCOL_DONE 
  
> Uma operação de configuração de coluna iniciada com uma chamada de método **IMAPITable::SetColumns** foi concluída. 
    
TABLE_SORT_DONE 
  
> Uma operação iniciada com uma chamada de método **IMAPITable:: SortTable** de classificação de tabela foi concluída. 
    
**hResult**
  
> Valor HRESULT para o erro que ocorreu, se o membro **ulTableEvent** for definido como TABLE_ERROR. 
    
**propIndex**
  
> Estrutura de [SPropValue](spropvalue.md) para a propriedade **PR_INSTANCE_KEY** da linha afetada. 
    
**propPrior**
  
> Estrutura de **SPropValue** para a propriedade **PR_INSTANCE_KEY** da linha antes daquela afetado. Se a linha afetada for a primeira linha na tabela, **propPrior** deve ser definida para **PR_NULL** e não a zero. Zero não é uma marca de propriedade válido. 
    
**row**
  
> Estrutura de [SRow](srow.md) descrevendo na linha afetada. Essa estrutura é preenchida para todos os eventos de notificação de tabela. Para eventos de notificação de tabela que não transmitir dados de linha, o membro **cValues** da estrutura **SRow** está definido como zero e o membro **lpProps** é definido como NULL. Como essa estrutura **SRow** é somente leitura; os clientes devem fazer uma cópia dela se desejam fazer modificações. A função de [ScDupPropset](scduppropset.md) pode ser usada para fazer a cópia. 
    
## <a name="remarks"></a>Comentários

O **tabela\_notificação** estrutura é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) . O membro **info** inclui um **tabela\_notificação** estruturar quando o membro **ulEventType** da estrutura é definido como _fnevTableModified_.
  
A ordem e o tipo das colunas no membro da linha refletem a ordem e o tipo que estava em vigor no momento em que a notificação foi gerada. A ordem e o tipo no momento em que a notificação foi gerada não é necessariamente o mesmo quando a notificação foi entregue. 
  
Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.
  
|**Tópico**|**Descrição**|
|:-----|:-----|
|[Notificações de eventos no MAPI](event-notification-in-mapi.md) <br/> |Visão geral de notificação e eventos de notificação.  <br/> |
|[Lidar com notificações](handling-notifications.md) <br/> |Discussão sobre como os clientes devem manipular notificações.  <br/> |
|[Suporte à notificação de eventos](supporting-event-notification.md) <br/> |Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.  <br/> |
   
Como notificações de tabela são assíncronas, os clientes podem receber notificações de uma linha adicionada depois de conhecer a adição por outros meios. É possível receber um evento TABLE_ERROR quando houver um erro em um método de **IMAPITable::Sort**, **IMAPITable:: Restrict**ou **IMAPITable::SetColumns** ou quando uma base de processo tenta atualizar uma tabela com, por exemplo, a nova funcionalidade ou linhas modificadas. 
  
## <a name="see-also"></a>Confira também

- [NOTIFICAÇÃO](notification.md) 
- [ScDupPropset](scduppropset.md)
- [SRow](srow.md)
- [SPropValue](spropvalue.md)
- [Estruturas MAPI](mapi-structures.md)

