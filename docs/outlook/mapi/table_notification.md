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
# <a name="tablenotification"></a><span data-ttu-id="00a3d-103">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="00a3d-103">TABLE_NOTIFICATION</span></span>

<span data-ttu-id="00a3d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00a3d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00a3d-105">Descreve uma linha em uma tabela que foi afetada por algum tipo de evento, como uma alteração ou um erro.</span><span class="sxs-lookup"><span data-stu-id="00a3d-105">Describes a row in a table that has been affected by some type of event, such as a change or an error.</span></span> <span data-ttu-id="00a3d-106">Isso faz com que uma notificação de tabela a ser gerado.</span><span class="sxs-lookup"><span data-stu-id="00a3d-106">This causes a table notification to be generated.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="00a3d-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="00a3d-107">Header file:</span></span>  <br/> |<span data-ttu-id="00a3d-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00a3d-108">Mapidefs.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="00a3d-109">Members</span><span class="sxs-lookup"><span data-stu-id="00a3d-109">Members</span></span>

<span data-ttu-id="00a3d-110">**ulTableEvent**</span><span class="sxs-lookup"><span data-stu-id="00a3d-110">**ulTableEvent**</span></span>
  
> <span data-ttu-id="00a3d-111">Bitmask dos sinalizadores usado para representar o tipo de evento de tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-111">Bitmask of flags used to represent the table event type.</span></span> <span data-ttu-id="00a3d-112">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="00a3d-112">The following flags can be set:</span></span>
    
<span data-ttu-id="00a3d-113">TABLE_CHANGED</span><span class="sxs-lookup"><span data-stu-id="00a3d-113">TABLE_CHANGED</span></span> 
  
> <span data-ttu-id="00a3d-114">Indica nitidamente que algo sobre a tabela foi alterado.</span><span class="sxs-lookup"><span data-stu-id="00a3d-114">Indicates at a high level that something about the table has changed.</span></span> <span data-ttu-id="00a3d-115">Estado da tabela é como era antes do evento.</span><span class="sxs-lookup"><span data-stu-id="00a3d-115">The table's state is as it was before the event.</span></span> <span data-ttu-id="00a3d-116">Isso significa que todas as propriedades de **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), indicadores, posicionamento atual e seleções de interface do usuário são ainda válidas.</span><span class="sxs-lookup"><span data-stu-id="00a3d-116">This means that all **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) properties, bookmarks, current positioning, and user interface selections are still valid.</span></span> <span data-ttu-id="00a3d-117">Manipule esse evento, releitura a tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-117">Handle this event by rereading the table.</span></span> <span data-ttu-id="00a3d-118">Provedores de serviços que não deseja implementar notificações de tabela rich enviam eventos TABLE_CHANGED em vez de eventos mais detalhados para indicar um tipo específico de alteração.</span><span class="sxs-lookup"><span data-stu-id="00a3d-118">Service providers that do not want to implement rich table notifications send TABLE_CHANGED events instead of more detailed events to indicate a particular type of change.</span></span> 
    
<span data-ttu-id="00a3d-119">TABLE_ERROR</span><span class="sxs-lookup"><span data-stu-id="00a3d-119">TABLE_ERROR</span></span> 
  
> <span data-ttu-id="00a3d-120">Ocorreu um erro, geralmente durante o processamento de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="00a3d-120">An error has occurred, usually during the processing of an asynchronous operation.</span></span> <span data-ttu-id="00a3d-121">Erros durante o processamento dos métodos a seguir podem gerar esse evento:</span><span class="sxs-lookup"><span data-stu-id="00a3d-121">Errors during the processing of the following methods can generate this event:</span></span> 
    
   - [<span data-ttu-id="00a3d-122">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="00a3d-122">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
    
   - [<span data-ttu-id="00a3d-123">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="00a3d-123">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
    
   - [<span data-ttu-id="00a3d-124">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="00a3d-124">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
    
   <span data-ttu-id="00a3d-125">Após receber um evento TABLE_ERROR, um cliente não pode depender a precisão do conteúdo da tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-125">After receiving a TABLE_ERROR event, a client cannot rely on the accuracy of the table contents.</span></span> <span data-ttu-id="00a3d-126">Além disso, notificações sobre outras alterações pendentes podem ser perdidas.</span><span class="sxs-lookup"><span data-stu-id="00a3d-126">Also, pending notifications about other changes might be lost.</span></span> <span data-ttu-id="00a3d-127">O método [IMAPITable::GetLastError](imapitable-getlasterror.md) não pode fornecer informações adicionais sobre o erro porque ela foi gerada em algum momento anterior, não necessariamente da última chamada de método.</span><span class="sxs-lookup"><span data-stu-id="00a3d-127">The [IMAPITable::GetLastError](imapitable-getlasterror.md) method might not provide any additional information about the error because it was generated at some previous point, not necessarily from the last method call.</span></span> 
    
<span data-ttu-id="00a3d-128">TABLE_RELOAD</span><span class="sxs-lookup"><span data-stu-id="00a3d-128">TABLE_RELOAD</span></span> 
  
> <span data-ttu-id="00a3d-129">Os dados na tabela devem ser recarregados.</span><span class="sxs-lookup"><span data-stu-id="00a3d-129">The data in the table should be reloaded.</span></span> <span data-ttu-id="00a3d-130">Provedores de serviços enviam TABLE_RELOAD quando, por exemplo, os dados subjacentes são armazenados em um banco de dados e o banco de dados foi substituído.</span><span class="sxs-lookup"><span data-stu-id="00a3d-130">Service providers send TABLE_RELOAD when, for example, the underlying data is stored in a database and the database is replaced.</span></span> <span data-ttu-id="00a3d-131">Manipule esse evento por supondo que nada sobre a tabela ainda é válido e por releitura a tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-131">Handle this event by assuming that nothing about the table is still valid and by rereading the table.</span></span> <span data-ttu-id="00a3d-132">Todos os indicadores, chaves da instância, status e informações de posicionamento são inválidos.</span><span class="sxs-lookup"><span data-stu-id="00a3d-132">All bookmarks, instance keys, status and positioning information are invalid.</span></span>
    
<span data-ttu-id="00a3d-133">TABLE_RESTRICT_DONE</span><span class="sxs-lookup"><span data-stu-id="00a3d-133">TABLE_RESTRICT_DONE</span></span> 
  
> <span data-ttu-id="00a3d-134">Uma operação de restrição iniciada com uma chamada de método **IMAPITable:: Restrict** foi concluída.</span><span class="sxs-lookup"><span data-stu-id="00a3d-134">A restriction operation initiated with an **IMAPITable::Restrict** method call has completed.</span></span> 
    
<span data-ttu-id="00a3d-135">TABLE_ROW_ADDED</span><span class="sxs-lookup"><span data-stu-id="00a3d-135">TABLE_ROW_ADDED</span></span> 
  
> <span data-ttu-id="00a3d-136">Foi adicionada uma nova linha à tabela de e o objeto correspondente salvo.</span><span class="sxs-lookup"><span data-stu-id="00a3d-136">A new row has been added to the table and the corresponding object saved.</span></span> <span data-ttu-id="00a3d-137">Eventos TABLE_ROW_ADDED são gerados após uma chamada para o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) .</span><span class="sxs-lookup"><span data-stu-id="00a3d-137">TABLE_ROW_ADDED events are generated after a call to the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> 
    
<span data-ttu-id="00a3d-138">TABLE_ROW_DELETED</span><span class="sxs-lookup"><span data-stu-id="00a3d-138">TABLE_ROW_DELETED</span></span> 
  
> <span data-ttu-id="00a3d-139">Uma linha foi removida da tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-139">A row has been removed from the table.</span></span> <span data-ttu-id="00a3d-140">O membro **propPrior** é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="00a3d-140">The **propPrior** member is set to NULL.</span></span> 
    
<span data-ttu-id="00a3d-141">TABLE_ROW_MODIFIED</span><span class="sxs-lookup"><span data-stu-id="00a3d-141">TABLE_ROW_MODIFIED</span></span> 
  
> <span data-ttu-id="00a3d-142">Uma linha foi alterada.</span><span class="sxs-lookup"><span data-stu-id="00a3d-142">A row has been changed.</span></span> <span data-ttu-id="00a3d-143">O membro de **linha** contém as propriedades afetadas para a linha.</span><span class="sxs-lookup"><span data-stu-id="00a3d-143">The **row** member contains the affected properties for the row.</span></span> <span data-ttu-id="00a3d-144">Vários eventos TABLE_ROW_MODIFIED são enviados na ordem em que eles aparecem no modo de exibição de tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-144">Multiple TABLE_ROW_MODIFIED events are sent in the order that they appear in the table view.</span></span> 
    
  <span data-ttu-id="00a3d-145">Eventos TABLE_ROW_MODIFIED são enviados depois que forem confirmadas com uma chamada ao método **IMAPIProp::SaveChanges** alterações ao objeto correspondente.</span><span class="sxs-lookup"><span data-stu-id="00a3d-145">TABLE_ROW_MODIFIED events are sent after changes to the corresponding object have been committed with a call to the **IMAPIProp::SaveChanges** method.</span></span> <span data-ttu-id="00a3d-146">Se a linha modificada agora for a primeira linha da tabela, o valor da propriedade marca no membro **propPrior** é **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="00a3d-146">If the modified row is now the first row in the table, the value of the property tag in the **propPrior** member is **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
    
<span data-ttu-id="00a3d-147">TABLE_SETCOL_DONE</span><span class="sxs-lookup"><span data-stu-id="00a3d-147">TABLE_SETCOL_DONE</span></span> 
  
> <span data-ttu-id="00a3d-148">Uma operação de configuração de coluna iniciada com uma chamada de método **IMAPITable::SetColumns** foi concluída.</span><span class="sxs-lookup"><span data-stu-id="00a3d-148">A column setting operation initiated with an **IMAPITable::SetColumns** method call has completed.</span></span> 
    
<span data-ttu-id="00a3d-149">TABLE_SORT_DONE</span><span class="sxs-lookup"><span data-stu-id="00a3d-149">TABLE_SORT_DONE</span></span> 
  
> <span data-ttu-id="00a3d-150">Uma operação iniciada com uma chamada de método **IMAPITable:: SortTable** de classificação de tabela foi concluída.</span><span class="sxs-lookup"><span data-stu-id="00a3d-150">A table sorting operation initiated with an **IMAPITable::SortTable** method call has completed.</span></span> 
    
<span data-ttu-id="00a3d-151">**hResult**</span><span class="sxs-lookup"><span data-stu-id="00a3d-151">**hResult**</span></span>
  
> <span data-ttu-id="00a3d-152">Valor HRESULT para o erro que ocorreu, se o membro **ulTableEvent** for definido como TABLE_ERROR.</span><span class="sxs-lookup"><span data-stu-id="00a3d-152">HRESULT value for the error that has occurred, if the **ulTableEvent** member is set to TABLE_ERROR.</span></span> 
    
<span data-ttu-id="00a3d-153">**propIndex**</span><span class="sxs-lookup"><span data-stu-id="00a3d-153">**propIndex**</span></span>
  
> <span data-ttu-id="00a3d-154">Estrutura de [SPropValue](spropvalue.md) para a propriedade **PR_INSTANCE_KEY** da linha afetada.</span><span class="sxs-lookup"><span data-stu-id="00a3d-154">[SPropValue](spropvalue.md) structure for the **PR_INSTANCE_KEY** property of the affected row.</span></span> 
    
<span data-ttu-id="00a3d-155">**propPrior**</span><span class="sxs-lookup"><span data-stu-id="00a3d-155">**propPrior**</span></span>
  
> <span data-ttu-id="00a3d-156">Estrutura de **SPropValue** para a propriedade **PR_INSTANCE_KEY** da linha antes daquela afetado.</span><span class="sxs-lookup"><span data-stu-id="00a3d-156">**SPropValue** structure for the **PR_INSTANCE_KEY** property of the row before the affected one.</span></span> <span data-ttu-id="00a3d-157">Se a linha afetada for a primeira linha na tabela, **propPrior** deve ser definida para **PR_NULL** e não a zero.</span><span class="sxs-lookup"><span data-stu-id="00a3d-157">If the affected row is the first row in the table, **propPrior** must be set to **PR_NULL** and not zero.</span></span> <span data-ttu-id="00a3d-158">Zero não é uma marca de propriedade válido.</span><span class="sxs-lookup"><span data-stu-id="00a3d-158">Zero is not a valid property tag.</span></span> 
    
<span data-ttu-id="00a3d-159">**row**</span><span class="sxs-lookup"><span data-stu-id="00a3d-159">**row**</span></span>
  
> <span data-ttu-id="00a3d-160">Estrutura de [SRow](srow.md) descrevendo na linha afetada.</span><span class="sxs-lookup"><span data-stu-id="00a3d-160">[SRow](srow.md) structure describing the affected row.</span></span> <span data-ttu-id="00a3d-161">Essa estrutura é preenchida para todos os eventos de notificação de tabela.</span><span class="sxs-lookup"><span data-stu-id="00a3d-161">This structure is filled for all table notification events.</span></span> <span data-ttu-id="00a3d-162">Para eventos de notificação de tabela que não transmitir dados de linha, o membro **cValues** da estrutura **SRow** está definido como zero e o membro **lpProps** é definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="00a3d-162">For table notification events that do not pass row data, the **cValues** member of the **SRow** structure is set to zero and the **lpProps** member is set to NULL.</span></span> <span data-ttu-id="00a3d-163">Como essa estrutura **SRow** é somente leitura; os clientes devem fazer uma cópia dela se desejam fazer modificações.</span><span class="sxs-lookup"><span data-stu-id="00a3d-163">Because this **SRow** structure is read-only; clients must make a copy of it if they want to make modifications.</span></span> <span data-ttu-id="00a3d-164">A função de [ScDupPropset](scduppropset.md) pode ser usada para fazer a cópia.</span><span class="sxs-lookup"><span data-stu-id="00a3d-164">The [ScDupPropset](scduppropset.md) function can be used to make the copy.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00a3d-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="00a3d-165">Remarks</span></span>

<span data-ttu-id="00a3d-166">O **tabela\_notificação** estrutura é um dos membros da união de estruturas incluídos no membro **info** da estrutura de [notificação](notification.md) .</span><span class="sxs-lookup"><span data-stu-id="00a3d-166">The **TABLE\_NOTIFICATION** structure is one of the members of the union of structures included in the **info** member of the [NOTIFICATION](notification.md) structure.</span></span> <span data-ttu-id="00a3d-167">O membro **info** inclui um **tabela\_notificação** estruturar quando o membro **ulEventType** da estrutura é definido como _fnevTableModified_.</span><span class="sxs-lookup"><span data-stu-id="00a3d-167">The **info** member includes a **TABLE\_NOTIFICATION** structure when the **ulEventType** member of the structure is set to  _fnevTableModified_.</span></span>
  
<span data-ttu-id="00a3d-168">A ordem e o tipo das colunas no membro da linha refletem a ordem e o tipo que estava em vigor no momento em que a notificação foi gerada.</span><span class="sxs-lookup"><span data-stu-id="00a3d-168">The order and type of columns in the row member reflect the order and type that was in effect at the time that the notification was generated.</span></span> <span data-ttu-id="00a3d-169">A ordem e o tipo no momento em que a notificação foi gerada não é necessariamente o mesmo quando a notificação foi entregue.</span><span class="sxs-lookup"><span data-stu-id="00a3d-169">The order and type at the time that the notification was generated is not necessarily the same as when the notification was delivered.</span></span> 
  
<span data-ttu-id="00a3d-170">Para obter mais informações sobre a notificação, consulte os tópicos descritos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="00a3d-170">For more information about notification, see the topics described in the following table.</span></span>
  
|<span data-ttu-id="00a3d-171">**Tópico**</span><span class="sxs-lookup"><span data-stu-id="00a3d-171">**Topic**</span></span>|<span data-ttu-id="00a3d-172">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="00a3d-172">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00a3d-173">Notificações de eventos no MAPI</span><span class="sxs-lookup"><span data-stu-id="00a3d-173">Event Notification in MAPI</span></span>](event-notification-in-mapi.md) <br/> |<span data-ttu-id="00a3d-174">Visão geral de notificação e eventos de notificação.</span><span class="sxs-lookup"><span data-stu-id="00a3d-174">General overview of notification and notification events.</span></span>  <br/> |
|[<span data-ttu-id="00a3d-175">Lidar com notificações</span><span class="sxs-lookup"><span data-stu-id="00a3d-175">Handling Notifications</span></span>](handling-notifications.md) <br/> |<span data-ttu-id="00a3d-176">Discussão sobre como os clientes devem manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="00a3d-176">Discussion of how clients should handle notifications.</span></span>  <br/> |
|[<span data-ttu-id="00a3d-177">Suporte à notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="00a3d-177">Supporting Event Notification</span></span>](supporting-event-notification.md) <br/> |<span data-ttu-id="00a3d-178">Discussão sobre como provedores de serviços podem usar o método **IMAPISupport** para gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="00a3d-178">Discussion of how service providers can use the **IMAPISupport** method to generate notifications.</span></span>  <br/> |
   
<span data-ttu-id="00a3d-179">Como notificações de tabela são assíncronas, os clientes podem receber notificações de uma linha adicionada depois de conhecer a adição por outros meios.</span><span class="sxs-lookup"><span data-stu-id="00a3d-179">Because table notifications are asynchronous, clients can receive notification of an added row after learning about the addition through another means.</span></span> <span data-ttu-id="00a3d-180">É possível receber um evento TABLE_ERROR quando houver um erro em um método de **IMAPITable::Sort**, **IMAPITable:: Restrict**ou **IMAPITable::SetColumns** ou quando uma base de processo tenta atualizar uma tabela com, por exemplo, a nova funcionalidade ou linhas modificadas.</span><span class="sxs-lookup"><span data-stu-id="00a3d-180">It is possible to receive a TABLE_ERROR event when there is an error in an **IMAPITable::Sort**, **IMAPITable::Restrict**, or **IMAPITable::SetColumns** method or when an underlying process attempts to update a table with, for example, new or modified rows.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="00a3d-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="00a3d-181">See also</span></span>

- [<span data-ttu-id="00a3d-182">NOTIFICAÇÃO</span><span class="sxs-lookup"><span data-stu-id="00a3d-182">NOTIFICATION</span></span>](notification.md) 
- [<span data-ttu-id="00a3d-183">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="00a3d-183">ScDupPropset</span></span>](scduppropset.md)
- [<span data-ttu-id="00a3d-184">SRow</span><span class="sxs-lookup"><span data-stu-id="00a3d-184">SRow</span></span>](srow.md)
- [<span data-ttu-id="00a3d-185">SPropValue</span><span class="sxs-lookup"><span data-stu-id="00a3d-185">SPropValue</span></span>](spropvalue.md)
- [<span data-ttu-id="00a3d-186">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="00a3d-186">MAPI Structures</span></span>](mapi-structures.md)

