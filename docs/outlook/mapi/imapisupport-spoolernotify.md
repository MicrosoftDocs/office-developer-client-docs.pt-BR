---
title: IMAPISupportSpoolerNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SpoolerNotify
api_type:
- COM
ms.assetid: d4f153b2-939f-4153-85fb-dc510193848c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 99377d63b4b5cf8731809446b70770f0c24231ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423766"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="c2441-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="c2441-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="c2441-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2441-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2441-105">Notifica o spooler MAPI sobre uma alteração no status ou uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c2441-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="c2441-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2441-106">Parameters</span></span>

 <span data-ttu-id="c2441-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2441-107">_ulFlags_</span></span>
  
> <span data-ttu-id="c2441-108">[in] Uma máscara de bits de sinalizadores que indica o tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="c2441-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="c2441-109">Os provedores de transporte podem definir todos os sinalizadores, exceto NOTIFY_NEWMAIL_RECEIVED; somente NOTIFY_NEWMAIL_RECEIVED e NOTIFY_READTOSEND são válidos para provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2441-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="c2441-110">Os sinalizadores a seguir são válidos para o _parâmetro ulFlags:_</span><span class="sxs-lookup"><span data-stu-id="c2441-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="c2441-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="c2441-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="c2441-112">Registra uma solicitação para alterar a configuração do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c2441-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="c2441-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="c2441-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="c2441-114">Ocorreu um erro irrecuperável para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c2441-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="c2441-115">Como os NOTIFY_SENTDEFERRED e NOTIFY_CRITICAL_ERROR usam o parâmetro  _lpvData_ para chamadas de provedor de transporte, esses sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c2441-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="c2441-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="c2441-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="c2441-117">Solicita uma seção crítica para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="c2441-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="c2441-118">O  _parâmetro lpvData_ é indefinido e deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="c2441-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="c2441-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="c2441-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="c2441-120">O spooler MAPI deve baixar as mensagens recém-recebidas no próximo horário disponível.</span><span class="sxs-lookup"><span data-stu-id="c2441-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="c2441-121">O  _parâmetro lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="c2441-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c2441-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="c2441-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="c2441-123">Uma nova mensagem foi recebida no armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2441-123">A new message has been received in the message store.</span></span> <span data-ttu-id="c2441-124">O  _parâmetro lpvData_ aponta para uma [NEWMAIL_NOTIFICATION](newmail_notification.md) estrutura que descreve a mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2441-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="c2441-125">Esse sinalizador é usado para provedores de armazenamento de mensagens que estão fortemente conectados aos provedores de transporte e será ignorado se o provedor de armazenamento estiver conectado com o sinalizador MAPI_NO_MAIL definido.</span><span class="sxs-lookup"><span data-stu-id="c2441-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="c2441-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="c2441-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="c2441-127">Libera uma seção crítica que foi obtida com uma chamada anterior para **SpoolerNotify** com  _ulFlags_ definido como NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="c2441-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="c2441-128">O  _parâmetro lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="c2441-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c2441-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="c2441-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="c2441-130">O provedor de transporte ou de armazenamento de mensagens está pronto para enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2441-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="c2441-131">O  _parâmetro lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="c2441-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="c2441-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c2441-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="c2441-133">Uma mensagem adiada anteriormente deve ser enviada, e o provedor de transporte deve ser notificado quando a mensagem estiver pronta para ser entregue usando uma chamada para o método [IXPLogon::SubmitMessage.](ixplogon-submitmessage.md)</span><span class="sxs-lookup"><span data-stu-id="c2441-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="c2441-134">O identificador de entrada da mensagem adiada está contido em uma [estrutura SBinary](sbinary.md) apontada por  _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="c2441-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="c2441-135">Como os NOTIFY_SENTDEFERRED e NOTIFY_CRITICAL_ERROR usam o parâmetro  _lpvData,_ esses sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="c2441-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="c2441-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="c2441-136">_lpvData_</span></span>
  
> <span data-ttu-id="c2441-137">[in] Um ponteiro para os dados associados aplicáveis a uma notificação.</span><span class="sxs-lookup"><span data-stu-id="c2441-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="c2441-138">O  _parâmetro lpvData_ aponta para dados válidos somente quando os sinalizadores a seguir são definidos (_lpvData_ é NULL quando  _ulFlags_ é definido para os outros tipos de notificação):</span><span class="sxs-lookup"><span data-stu-id="c2441-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="c2441-139">**_Configuração ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="c2441-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="c2441-140">**_Valor lpvData_**</span><span class="sxs-lookup"><span data-stu-id="c2441-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c2441-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="c2441-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="c2441-142">Informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="c2441-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="c2441-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="c2441-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="c2441-144">Uma **NEWMAIL_NOTIFICATION** que contém informações sobre a mensagem recém-entregue.</span><span class="sxs-lookup"><span data-stu-id="c2441-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="c2441-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="c2441-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="c2441-146">Uma **estrutura SBinary** que contém o identificador de entrada da mensagem adiada.</span><span class="sxs-lookup"><span data-stu-id="c2441-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="c2441-147">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c2441-147">Return value</span></span>

<span data-ttu-id="c2441-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2441-148">S_OK</span></span> 
  
> <span data-ttu-id="c2441-149">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c2441-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2441-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2441-150">Remarks</span></span>

<span data-ttu-id="c2441-151">O **método IMAPISupport::SpoolerNotify** é implementado para objetos de suporte do provedor de transporte e do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2441-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="c2441-152">Esses provedores chamam **SpoolerNotify** para notificar o spooler MAPI de uma alteração no status ou uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="c2441-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="c2441-153">**SpoolerNotify** é chamado principalmente por provedores de transporte e pode ser chamado a qualquer momento durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="c2441-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="c2441-154">Observações para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="c2441-154">Notes to Transport Providers</span></span>

<span data-ttu-id="c2441-155">Se você tiver alterado a configuração do provedor de transporte, chame **SpoolerNotify** e defina  _ulFlags_ como NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="c2441-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="c2441-156">**SpoolerNotify** responde chamando o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) para consultar uma alteração nos tipos de endereço com suporte.</span><span class="sxs-lookup"><span data-stu-id="c2441-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="c2441-157">Se você precisar de uma seção crítica para garantir o processamento ininterrupto, chame **SpoolerNotify** com  _ulFlags_ definido como NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="c2441-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="c2441-158">A definição desse sinalizador informa ao spooler MAPI que ele não deve chamar os métodos [IXPLogon::Idle](ixplogon-idle.md) e [IXPLogon::P oll.](ixplogon-poll.md)</span><span class="sxs-lookup"><span data-stu-id="c2441-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="c2441-159">Enquanto uma seção crítica estiver aberta, retorne MAPI_E_BUSY sempre que o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) for chamado.</span><span class="sxs-lookup"><span data-stu-id="c2441-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="c2441-160">Quando terminar a seção crítica, faça outra chamada para **SpoolerNotify** com  _ulFlags_ definido como NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="c2441-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="c2441-161">Por exemplo, se seu provedor de transporte remoto estiver no processo de carregamento de mensagens, talvez seja necessário permitir que um usuário insira um número de telefone para estabelecer a conexão remota.</span><span class="sxs-lookup"><span data-stu-id="c2441-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="c2441-162">Antes de fazer um loop pelo procedimento da caixa de diálogo, você deve declarar uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="c2441-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="c2441-163">Quando o usuário fechar a caixa de diálogo, encerrando o procedimento da caixa de diálogo, você deverá liberar a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="c2441-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="c2441-164">Quando você configura  _ulFlags_ como NOTIFY_CRITICAL_ERROR, o spooler MAPI não faz mais chamadas para o provedor, exceto para liberá-lo.</span><span class="sxs-lookup"><span data-stu-id="c2441-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="c2441-165">Se você chamar **SpoolerNotify** com NOTIFY_CRITICAL_ERROR definido dos métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage,](ixplogon-submitmessage.md) retorne com um valor de erro apropriado da chamada **StartMessage** ou \*\* SubmitMessage \*\* imediatamente após a chamada **SpoolerNotify.**</span><span class="sxs-lookup"><span data-stu-id="c2441-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or \*\* SubmitMessage \*\* call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="c2441-166">Se o provedor de transporte se recuperou de uma condição que anteriormente causou sua falha, chame **SpoolerNotify** com  _ulFlags_ definido como NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="c2441-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="c2441-167">Esse sinalizador indica que o provedor está novamente pronto para lidar com mensagens.</span><span class="sxs-lookup"><span data-stu-id="c2441-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="c2441-168">Observações para provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="c2441-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="c2441-169">Chame **SpoolerNotify**, passando o sinalizador NOTIFY_READYTOSEND em  _ulFlags_, antes de fazer sua primeira chamada para [IMAPISupport::P repareSubmit](imapisupport-preparesubmit.md) **em IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="c2441-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="c2441-170">Essa chamada para **SpoolerNotify** precisa ser feita apenas uma vez por sessão.</span><span class="sxs-lookup"><span data-stu-id="c2441-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="c2441-171">Se seu provedor de armazenamento de mensagens estiver fortemente unido a um provedor de transporte e você chamar **SpoolerNotify** com  _ulFlags_ definido como NOTIFY_NEWMAIL_RECEIVED, o spooler MAPI abrirá a nova mensagem e começará a processar a nova função de gancho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2441-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="c2441-172">Quando o processamento é concluído, o spooler MAPI chama o método [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informá-lo sobre sua própria nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="c2441-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="c2441-173">Para obter mais informações sobre como **chamar SpoolerNotify,** consulte um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="c2441-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="c2441-174">Implementando o método FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c2441-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="c2441-175">Interagindo com o Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="c2441-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="c2441-176">Modelo de Recepção de Mensagens</span><span class="sxs-lookup"><span data-stu-id="c2441-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="c2441-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2441-177">See also</span></span>



[<span data-ttu-id="c2441-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="c2441-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="c2441-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="c2441-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="c2441-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="c2441-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="c2441-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2441-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

