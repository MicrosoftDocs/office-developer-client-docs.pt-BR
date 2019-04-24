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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345644"
---
# <a name="tablenotification"></a><span data-ttu-id="5ad66-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5ad66-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="5ad66-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ad66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ad66-105">Descreve uma linha em uma tabela que foi afetada por algum tipo de evento, como uma alteração ou um erro.</span><span class="sxs-lookup"><span data-stu-id="5ad66-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="5ad66-106">Isso faz com que uma notificação de tabela seja gerada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ad66-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5ad66-107">Header file:</span></span>  <br/> |<span data-ttu-id="5ad66-108">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5ad66-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="5ad66-109">Members</span><span class="sxs-lookup"><span data-stu-id="5ad66-109">Members</span></span>

<span data-ttu-id="5ad66-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="5ad66-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="5ad66-111">Bitmask dos sinalizadores usados para representar o tipo de evento Table.</span><span class="sxs-lookup"><span data-stu-id="5ad66-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="5ad66-112">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="5ad66-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5ad66-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="5ad66-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="5ad66-114">Indica em um nível alto que algo sobre a tabela foi alterado.</span><span class="sxs-lookup"><span data-stu-id="5ad66-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="5ad66-115">O estado da tabela é como era antes do evento.</span><span class="sxs-lookup"><span data-stu-id="5ad66-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="5ad66-116">Isso significa que todas as propriedades de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), indicadores, posicionamento atual e seleções de interface do usuário ainda são válidas.</span><span class="sxs-lookup"><span data-stu-id="5ad66-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="5ad66-117">Manipule esse evento relendo a tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="5ad66-118">Os provedores de serviços que não querem implementar notificações de tabela rica enviam eventos TABLE_CHANGED em vez de eventos mais detalhados para indicar um tipo específico de alteração.</span><span class="sxs-lookup"><span data-stu-id="5ad66-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="5ad66-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="5ad66-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="5ad66-120">Ocorreu um erro, geralmente durante o processamento de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="5ad66-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="5ad66-121">Erros durante o processamento dos seguintes métodos podem gerar esse evento:</span><span class="sxs-lookup"><span data-stu-id="5ad66-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="5ad66-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="5ad66-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="5ad66-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="5ad66-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="5ad66-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="5ad66-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="5ad66-125">Após receber um evento TABLE_ERROR, um cliente não pode depender da precisão do conteúdo da tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="5ad66-126">Além disso, as notificações pendentes sobre outras alterações podem ser perdidas.</span><span class="sxs-lookup"><span data-stu-id="5ad66-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="5ad66-127">O método imApitable [:: GetLastError](imapitable-getlasterror.md) pode não fornecer informações adicionais sobre o erro, pois ele foi gerado em algum ponto anterior, não necessariamente da última chamada do método.</span><span class="sxs-lookup"><span data-stu-id="5ad66-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="5ad66-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="5ad66-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="5ad66-129">Os dados da tabela devem ser recarregados.</span><span class="sxs-lookup"><span data-stu-id="5ad66-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="5ad66-130">Os provedores de serviços enviam TABLE_RELOAD Quando, por exemplo, os dados subjacentes são armazenados em um banco de dados e o banco de dados é substituído.</span><span class="sxs-lookup"><span data-stu-id="5ad66-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="5ad66-131">Manipule esse evento supondo que nada sobre a tabela ainda seja válido e releia a tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="5ad66-132">Todos os indicadores, as teclas de instância, o status e as informações de posicionamento são inválidos.</span><span class="sxs-lookup"><span data-stu-id="5ad66-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="5ad66-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="5ad66-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="5ad66-134">Uma operação de restrição iniciada com uma chamada de método imApitable **:: Restrict** foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5ad66-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="5ad66-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="5ad66-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="5ad66-136">Uma nova linha foi adicionada à tabela e o objeto correspondente foi salvo.</span><span class="sxs-lookup"><span data-stu-id="5ad66-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="5ad66-137">Eventos TABLE_ROW_ADDED são gerados após uma chamada para o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad66-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="5ad66-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="5ad66-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="5ad66-139">Uma linha foi removida da tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-139">A row has been removed from the table.</span></span> <span data-ttu-id="5ad66-140">O membro **propPrior** está definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="5ad66-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="5ad66-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="5ad66-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="5ad66-142">Uma linha foi alterada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-142">A row has been changed.</span></span> <span data-ttu-id="5ad66-143">O membro **Row** contém as propriedades afetadas para a linha.</span><span class="sxs-lookup"><span data-stu-id="5ad66-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="5ad66-144">Vários eventos TABLE_ROW_MODIFIED são enviados na ordem em que aparecem no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="5ad66-145">Os eventos TABLE_ROW_MODIFIED são enviados após as alterações no objeto correspondente terem sido confirmadas com uma chamada para o método **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="5ad66-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="5ad66-146">Se a linha modificada agora for a primeira linha na tabela, o valor da marca de propriedade no membro **propPrior** será **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5ad66-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="5ad66-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="5ad66-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="5ad66-148">Uma operação de configuração de coluna iniciada com uma chamada de método imApitable **::** SetColumns foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5ad66-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="5ad66-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="5ad66-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="5ad66-150">Uma operação de classificação de tabela iniciada com uma chamada de método imApitable **:: SortTable** foi concluída.</span><span class="sxs-lookup"><span data-stu-id="5ad66-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="5ad66-151">**And**</span><span class="sxs-lookup"><span data-stu-id="5ad66-151">**hResult**</span></span>
  
> <span data-ttu-id="5ad66-152">Valor HRESULT para o erro que ocorreu, se o membro **ulTableEvent** estiver definido como TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="5ad66-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="5ad66-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="5ad66-153">**propIndex**</span></span>
  
> <span data-ttu-id="5ad66-154">Estrutura [SPropValue](spropvalue.md) para a propriedade **PR_INSTANCE_KEY** da linha afetada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="5ad66-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="5ad66-155">**propPrior**</span></span>
  
> <span data-ttu-id="5ad66-156">Estrutura **SPropValue** da propriedade **PR_INSTANCE_KEY** da linha antes da afetada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="5ad66-157">Se a linha afetada for a primeira linha na tabela, **propPrior** deverá ser definido como **PR_NULL** e não como zero.</span><span class="sxs-lookup"><span data-stu-id="5ad66-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="5ad66-158">Zero não é uma marca de propriedade válida.</span><span class="sxs-lookup"><span data-stu-id="5ad66-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="5ad66-159">**Row**</span><span class="sxs-lookup"><span data-stu-id="5ad66-159">**row**</span></span>
  
> <span data-ttu-id="5ad66-160">Estrutura [SRow](srow.md) descrevendo a linha afetada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="5ad66-161">Essa estrutura é preenchida para todos os eventos de notificação de tabela.</span><span class="sxs-lookup"><span data-stu-id="5ad66-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="5ad66-162">Para eventos de notificação de tabela que não passam dados de linha, o membro **cValues** da estrutura **SRow** é definido como zero e o membro **lpProps** é definido como nulo.</span><span class="sxs-lookup"><span data-stu-id="5ad66-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="5ad66-163">Como essa estrutura **SRow** é somente leitura; Os clientes devem fazer uma cópia deles se desejarem fazer modificações.</span><span class="sxs-lookup"><span data-stu-id="5ad66-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="5ad66-164">A função [ScDupPropset](scduppropset.md) pode ser usada para fazer a cópia.</span><span class="sxs-lookup"><span data-stu-id="5ad66-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5ad66-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="5ad66-165">Remarks</span></span>

<span data-ttu-id="5ad66-166">A estrutura de **notificação de\_tabela** é um dos membros da União de estruturas incluído no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="5ad66-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="5ad66-167">O membro **info** inclui uma estrutura de **notificação de\_tabela** quando o membro **ulEventType** da estrutura é definido como _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="5ad66-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="5ad66-168">A ordem e o tipo de colunas no membro da linha refletem a ordem e o tipo que estava em vigor no momento em que a notificação foi gerada.</span><span class="sxs-lookup"><span data-stu-id="5ad66-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="5ad66-169">A ordem e o tipo no momento em que a notificação foi gerada não é necessariamente o mesmo que quando a notificação foi entregue.</span><span class="sxs-lookup"><span data-stu-id="5ad66-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="5ad66-170">Para obter mais informações sobre notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5ad66-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="5ad66-171">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="5ad66-171">**Topic**</span></span>|<span data-ttu-id="5ad66-172">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="5ad66-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5ad66-173">Notificação de evento no MAPI</span><span class="sxs-lookup"><span data-stu-id="5ad66-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="5ad66-174">Visão geral dos eventos Notification e Notification.</span><span class="sxs-lookup"><span data-stu-id="5ad66-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="5ad66-175">Manipular notificações</span><span class="sxs-lookup"><span data-stu-id="5ad66-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="5ad66-176">Discussão sobre como os clientes devem lidar com notificações.</span><span class="sxs-lookup"><span data-stu-id="5ad66-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="5ad66-177">Notificação de evento de suporte</span><span class="sxs-lookup"><span data-stu-id="5ad66-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="5ad66-178">Discussão sobre como os provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="5ad66-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="5ad66-179">Como as notificações de tabela são assíncronas, os clientes podem receber a notificação de uma linha adicionada após aprender sobre a adição por outro meio.</span><span class="sxs-lookup"><span data-stu-id="5ad66-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="5ad66-180">É possível receber um evento TABLE_ERROR quando há um erro em um método imApitable: **: Sort**, IMAPITable: **: reStrict**ou imapitaBle:: SetColumns ou quando um processo subjacente tenta atualizar uma tabela com, por exemplo, novo ou \*\*\*\* linhas modificadas.</span><span class="sxs-lookup"><span data-stu-id="5ad66-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5ad66-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="5ad66-181">See also</span></span>

- [<span data-ttu-id="5ad66-182">NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="5ad66-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="5ad66-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="5ad66-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="5ad66-184">SRow</span><span class="sxs-lookup"><span data-stu-id="5ad66-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="5ad66-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="5ad66-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="5ad66-186">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="5ad66-186">MAPI Structures</span></span>](mapi-structures.md)

