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
ms.openlocfilehash: 21ea5faaccb81e763d6d062b6ff567db509d9d35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767287"
---
# <a name="imapisupportspoolernotify"></a><span data-ttu-id="9abf1-103">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="9abf1-103">IMAPISupport::SpoolerNotify</span></span>

  
  
<span data-ttu-id="9abf1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9abf1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9abf1-105">Notifica o MAPI spooler de uma alteração no status ou uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9abf1-105">Notifies the MAPI spooler of a change in status or a request for service.</span></span> 
  
```cpp
HRESULT SpoolerNotify(
ULONG ulFlags,
LPVOID lpvData
);
```

## <a name="parameters"></a><span data-ttu-id="9abf1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9abf1-106">Parameters</span></span>

 <span data-ttu-id="9abf1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9abf1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9abf1-108">[in] Uma bitmask dos sinalizadores que indica o tipo de notificação.</span><span class="sxs-lookup"><span data-stu-id="9abf1-108">[in] A bitmask of flags that indicates the type of notification.</span></span> <span data-ttu-id="9abf1-109">Provedores de transporte podem definir todos os sinalizadores, exceto NOTIFY_NEWMAIL_RECEIVED; apenas NOTIFY_NEWMAIL_RECEIVED e NOTIFY_READTOSEND são válidos para provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9abf1-109">Transport providers can set all of the flags except for NOTIFY_NEWMAIL_RECEIVED; only NOTIFY_NEWMAIL_RECEIVED and NOTIFY_READTOSEND are valid for message store providers.</span></span> <span data-ttu-id="9abf1-110">Sinalizadores a seguir são válidos para o parâmetro _ulFlags_ :</span><span class="sxs-lookup"><span data-stu-id="9abf1-110">The following flags are valid for the  _ulFlags_ parameter:</span></span> 
    
<span data-ttu-id="9abf1-111">NOTIFY_CONFIG_CHANGE</span><span class="sxs-lookup"><span data-stu-id="9abf1-111">NOTIFY_CONFIG_CHANGE</span></span> 
  
> <span data-ttu-id="9abf1-112">Registra uma solicitação para alterar a configuração do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9abf1-112">Registers a request to change the transport provider's configuration.</span></span> 
    
<span data-ttu-id="9abf1-113">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9abf1-113">NOTIFY_CRITICAL_ERROR</span></span> 
  
> <span data-ttu-id="9abf1-114">Um erro irreparável ocorreu para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9abf1-114">An unrecoverable error has occurred to the transport provider.</span></span> <span data-ttu-id="9abf1-115">Como NOTIFY_SENTDEFERRED e o NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ para chamadas de provedor de transporte, esses sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="9abf1-115">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter for transport provider calls, these flags are mutually exclusive.</span></span> 
    
<span data-ttu-id="9abf1-116">NOTIFY_CRITSEC</span><span class="sxs-lookup"><span data-stu-id="9abf1-116">NOTIFY_CRITSEC</span></span> 
  
> <span data-ttu-id="9abf1-117">Solicita uma seção crítica para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9abf1-117">Requests a critical section for the transport provider.</span></span> <span data-ttu-id="9abf1-118">O parâmetro _lpvData_ é indefinido e deve ser nula.</span><span class="sxs-lookup"><span data-stu-id="9abf1-118">The  _lpvData_ parameter is undefined and should be NULL.</span></span> 
    
<span data-ttu-id="9abf1-119">NOTIFY_NEWMAIL</span><span class="sxs-lookup"><span data-stu-id="9abf1-119">NOTIFY_NEWMAIL</span></span> 
  
> <span data-ttu-id="9abf1-120">O MAPI spooler deve baixar quaisquer mensagens recebidas recentemente no próximo horário disponível.</span><span class="sxs-lookup"><span data-stu-id="9abf1-120">The MAPI spooler should download any newly received messages at the next available time.</span></span> <span data-ttu-id="9abf1-121">O parâmetro _lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="9abf1-121">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9abf1-122">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="9abf1-122">NOTIFY_NEWMAIL_RECEIVED</span></span> 
  
> <span data-ttu-id="9abf1-123">Uma nova mensagem foi recebida no repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9abf1-123">A new message has been received in the message store.</span></span> <span data-ttu-id="9abf1-124">O parâmetro _lpvData_ aponta para uma estrutura [NEWMAIL_NOTIFICATION](newmail_notification.md) que descreve a mensagem.</span><span class="sxs-lookup"><span data-stu-id="9abf1-124">The  _lpvData_ parameter points to a [NEWMAIL_NOTIFICATION](newmail_notification.md) structure that describes the message.</span></span> <span data-ttu-id="9abf1-125">Esse sinalizador é usado para provedores de armazenamento de mensagem que estejam intimamente ligadas a provedores de transporte e é ignorada se o provedor de repositório está conectado com o sinalizador MAPI_NO_MAIL definido.</span><span class="sxs-lookup"><span data-stu-id="9abf1-125">This flag is used for message store providers that are tightly coupled with transport providers and is ignored if the store provider is logged on with the MAPI_NO_MAIL flag set.</span></span> 
    
<span data-ttu-id="9abf1-126">NOTIFY_NONCRIT</span><span class="sxs-lookup"><span data-stu-id="9abf1-126">NOTIFY_NONCRIT</span></span> 
  
> <span data-ttu-id="9abf1-127">Libera uma seção crítica que foi obtida com uma chamada anterior a **SpoolerNotify** com _ulFlags_ definido como NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="9abf1-127">Releases a critical section that was obtained with a previous call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="9abf1-128">O parâmetro _lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="9abf1-128">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9abf1-129">NOTIFY_READYTOSEND</span><span class="sxs-lookup"><span data-stu-id="9abf1-129">NOTIFY_READYTOSEND</span></span> 
  
> <span data-ttu-id="9abf1-130">O provedor de repositórios de transporte ou de mensagem está pronto para enviar mensagens.</span><span class="sxs-lookup"><span data-stu-id="9abf1-130">The transport or message store provider is ready to send messages.</span></span> <span data-ttu-id="9abf1-131">O parâmetro _lpvData_ é indefinido e deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="9abf1-131">The  _lpvData_ parameter is undefined and should be set to NULL.</span></span> 
    
<span data-ttu-id="9abf1-132">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="9abf1-132">NOTIFY_SENTDEFERRED</span></span> 
  
> <span data-ttu-id="9abf1-133">Uma mensagem adiada anteriormente agora deve ser enviada e o provedor de transporte deve ser notificado quando a mensagem está pronta para ser entregues por meio de uma chamada ao método [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="9abf1-133">A previously deferred message should now be sent, and the transport provider should be notified when the message is ready to be delivered by using a call to the [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) method.</span></span> <span data-ttu-id="9abf1-134">O identificador de entrada da mensagem adiada está contido em uma estrutura de [SBinary](sbinary.md) apontada pela _lpvData_.</span><span class="sxs-lookup"><span data-stu-id="9abf1-134">The entry identifier of the deferred message is contained in an [SBinary](sbinary.md) structure pointed to by  _lpvData_.</span></span> <span data-ttu-id="9abf1-135">Como NOTIFY_SENTDEFERRED e o NOTIFY_CRITICAL_ERROR usam o parâmetro _lpvData_ , esses sinalizadores são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="9abf1-135">Because both NOTIFY_SENTDEFERRED and NOTIFY_CRITICAL_ERROR use the  _lpvData_ parameter, these flags are mutually exclusive.</span></span> 
    
 <span data-ttu-id="9abf1-136">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="9abf1-136">_lpvData_</span></span>
  
> <span data-ttu-id="9abf1-137">[in] Um ponteiro para os dados associados aplicáveis a uma notificação.</span><span class="sxs-lookup"><span data-stu-id="9abf1-137">[in] A pointer to associated data applicable to a notification.</span></span> <span data-ttu-id="9abf1-138">O parâmetro _lpvData_ aponta para dados válido somente quando os seguintes sinalizadores estão definidos (_lpvData_ é NULL quando _ulFlags_ estiver definido como os outros tipos de notificação):</span><span class="sxs-lookup"><span data-stu-id="9abf1-138">The  _lpvData_ parameter points to valid data only when the following flags are set (_lpvData_ is NULL when  _ulFlags_ is set to the other notification types):</span></span> 
    
|<span data-ttu-id="9abf1-139">**configuração de _ulFlags_**</span><span class="sxs-lookup"><span data-stu-id="9abf1-139">**_ulFlags_ setting**</span></span>|<span data-ttu-id="9abf1-140">**valor de _lpvData_**</span><span class="sxs-lookup"><span data-stu-id="9abf1-140">**_lpvData_ value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9abf1-141">NOTIFY_CRITICAL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9abf1-141">NOTIFY_CRITICAL_ERROR</span></span>  <br/> |<span data-ttu-id="9abf1-142">Informações sobre o erro.</span><span class="sxs-lookup"><span data-stu-id="9abf1-142">Information about the error.</span></span>  <br/> |
|<span data-ttu-id="9abf1-143">NOTIFY_NEWMAIL_RECEIVED</span><span class="sxs-lookup"><span data-stu-id="9abf1-143">NOTIFY_NEWMAIL_RECEIVED</span></span>  <br/> |<span data-ttu-id="9abf1-144">Uma estrutura **NEWMAIL_NOTIFICATION** que contém informações sobre a mensagem entregue recentemente.</span><span class="sxs-lookup"><span data-stu-id="9abf1-144">A **NEWMAIL_NOTIFICATION** structure that contains information about the newly delivered message.</span></span>  <br/> |
|<span data-ttu-id="9abf1-145">NOTIFY_SENTDEFERRED</span><span class="sxs-lookup"><span data-stu-id="9abf1-145">NOTIFY_SENTDEFERRED</span></span>  <br/> |<span data-ttu-id="9abf1-146">Uma estrutura de **SBinary** que contém o identificador de entrada de mensagem adiada.</span><span class="sxs-lookup"><span data-stu-id="9abf1-146">An **SBinary** structure that contains the entry identifier of deferred message.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="9abf1-147">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9abf1-147">Return value</span></span>

<span data-ttu-id="9abf1-148">S_OK</span><span class="sxs-lookup"><span data-stu-id="9abf1-148">S_OK</span></span> 
  
> <span data-ttu-id="9abf1-149">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9abf1-149">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9abf1-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="9abf1-150">Remarks</span></span>

<span data-ttu-id="9abf1-151">O método **IMAPISupport::SpoolerNotify** é implementado para mensagem armazenar e objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="9abf1-151">The **IMAPISupport::SpoolerNotify** method is implemented for message store and transport provider support objects.</span></span> <span data-ttu-id="9abf1-152">Esses provedores chamarem **SpoolerNotify** para notificar o MAPI spooler de uma alteração no status ou uma solicitação de serviço.</span><span class="sxs-lookup"><span data-stu-id="9abf1-152">These providers call **SpoolerNotify** to notify the MAPI spooler of a change in status or a request for service.</span></span> <span data-ttu-id="9abf1-153">**SpoolerNotify** é chamado principalmente pelos provedores de transporte e pode ser chamado a qualquer momento durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="9abf1-153">**SpoolerNotify** is called primarily by transport providers and may be called at any time during the session.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="9abf1-154">Observações para provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="9abf1-154">Notes to Transport Providers</span></span>

<span data-ttu-id="9abf1-155">Se você tiver alterado sua configuração de provedor de transporte, chame **SpoolerNotify** e defina _ulFlags_ como NOTIFY_CONFIG_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="9abf1-155">If you have changed your transport provider configuration, call **SpoolerNotify** and set  _ulFlags_ to NOTIFY_CONFIG_CHANGED.</span></span> <span data-ttu-id="9abf1-156">**SpoolerNotify** responde chamando o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) a consulta para uma alteração de tipos de endereço com suporte.</span><span class="sxs-lookup"><span data-stu-id="9abf1-156">**SpoolerNotify** responds by calling the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method to query for a change in supported address types.</span></span> 
  
<span data-ttu-id="9abf1-157">Se você precisar de uma seção crítica para garantir o processamento ininterrupto, chame **SpoolerNotify** com _ulFlags_ definido como NOTIFY_CRITSEC.</span><span class="sxs-lookup"><span data-stu-id="9abf1-157">If you need a critical section to ensure uninterrupted processing, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_CRITSEC.</span></span> <span data-ttu-id="9abf1-158">Defina esse sinalizador informa o MAPI spooler que ele não deve chamar os métodos [IXPLogon::Idle](ixplogon-idle.md) e [IXPLogon::Poll](ixplogon-poll.md) .</span><span class="sxs-lookup"><span data-stu-id="9abf1-158">Setting this flag informs the MAPI spooler that it should not call the [IXPLogon::Idle](ixplogon-idle.md) and [IXPLogon::Poll](ixplogon-poll.md) methods.</span></span> <span data-ttu-id="9abf1-159">Enquanto uma seção crítica aberto, retorne MAPI_E_BUSY sempre que o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="9abf1-159">While you have a critical section open, return MAPI_E_BUSY whenever the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method is called.</span></span> <span data-ttu-id="9abf1-160">Quando você terminar com a seção crítica, fazer outra chamada para **SpoolerNotify** com _ulFlags_ definido como NOTIFY_NONCRIT.</span><span class="sxs-lookup"><span data-stu-id="9abf1-160">When you are finished with the critical section, make another call to **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NONCRIT.</span></span> 
  
<span data-ttu-id="9abf1-161">Por exemplo, se seu provedor de transporte remoto estiver no processo de carregamento de mensagens, você precisará permitir que o usuário insira um número de telefone para estabelecer a conexão remota.</span><span class="sxs-lookup"><span data-stu-id="9abf1-161">For example, if your remote transport provider is in the process of uploading messages, you might need to allow a user to enter a telephone number to establish the remote connection.</span></span> <span data-ttu-id="9abf1-162">Antes de você percorrer o procedimento da caixa de diálogo, você deve declarar uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="9abf1-162">Before you loop through the dialog box procedure, you should declare a critical section.</span></span> <span data-ttu-id="9abf1-163">Quando o usuário fechar a caixa de diálogo, encerrando o procedimento da caixa de diálogo, você deve liberar a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="9abf1-163">When the user closes the dialog box, terminating the dialog box procedure, you should release the critical section.</span></span>
  
<span data-ttu-id="9abf1-164">Quando você definir _ulFlags_ como NOTIFY_CRITICAL_ERROR, o spooler MAPI não faz nenhuma chamada adicional para o provedor, exceto ao liberá-la.</span><span class="sxs-lookup"><span data-stu-id="9abf1-164">When you set  _ulFlags_ to NOTIFY_CRITICAL_ERROR, the MAPI spooler makes no further calls to the provider except to release it.</span></span> <span data-ttu-id="9abf1-165">Se você chamar **SpoolerNotify** com NOTIFY_CRITICAL_ERROR definir a partir dos métodos [IXPLogon::StartMessage](ixplogon-startmessage.md) ou [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) , retornar com um valor de erro apropriado do **StartMessage** ou * * SubmitMessage * * chamada imediatamente após a chamada **SpoolerNotify** .</span><span class="sxs-lookup"><span data-stu-id="9abf1-165">If you call **SpoolerNotify** with NOTIFY_CRITICAL_ERROR set from the [IXPLogon::StartMessage](ixplogon-startmessage.md) or [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) methods, return with an appropriate error value from the **StartMessage** or ** SubmitMessage ** call immediately after the **SpoolerNotify** call.</span></span> 
  
<span data-ttu-id="9abf1-166">Se o seu provedor de transporte recuperados de uma condição que anteriormente deixá-lo falhar, chame **SpoolerNotify** com _ulFlags_ definido como NOTIFY_READYTOSEND.</span><span class="sxs-lookup"><span data-stu-id="9abf1-166">If your transport provider recovered from a condition that previously caused it to fail, call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_READYTOSEND.</span></span> <span data-ttu-id="9abf1-167">Esse sinalizador indica que o provedor está pronto para lidar com as mensagens novamente.</span><span class="sxs-lookup"><span data-stu-id="9abf1-167">This flag indicates that the provider is again ready to handle messages.</span></span> 
  
## <a name="notes-to-message-store-providers"></a><span data-ttu-id="9abf1-168">Observações para provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="9abf1-168">Notes to Message Store Providers</span></span>

<span data-ttu-id="9abf1-169">Chame **SpoolerNotify**, passando o sinalizador NOTIFY_READYTOSEND _ulFlags_, antes de fazer a chamada primeira para [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) no **IMessage::SubmitMessage**.</span><span class="sxs-lookup"><span data-stu-id="9abf1-169">Call **SpoolerNotify**, passing the NOTIFY_READYTOSEND flag in  _ulFlags_, before you make your first call to [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) in **IMessage::SubmitMessage**.</span></span> <span data-ttu-id="9abf1-170">Essa chamada para **SpoolerNotify** deve ser feita apenas uma vez por sessão.</span><span class="sxs-lookup"><span data-stu-id="9abf1-170">This call to **SpoolerNotify** needs to be made only once per session.</span></span> 
  
<span data-ttu-id="9abf1-171">Se o seu provedor de armazenamento de mensagem está intimamente ligado com um transporte provedor e você chamar **SpoolerNotify** com _ulFlags_ definido para NOTIFY_NEWMAIL_RECEIVED, o MAPI spooler abre a nova mensagem e inicia o processamento a nova função de gancho de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9abf1-171">If your message store provider is tightly coupled with a transport provider and you call **SpoolerNotify** with  _ulFlags_ set to NOTIFY_NEWMAIL_RECEIVED, the MAPI spooler opens the new message and begins processing the new message hook function.</span></span> <span data-ttu-id="9abf1-172">Quando o processamento estiver concluído, o MAPI spooler chama o método de [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) para informar sua própria mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="9abf1-172">When processing is complete, the MAPI spooler calls the [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) method to inform you of your own new message.</span></span> 
  
<span data-ttu-id="9abf1-173">Para obter mais informações sobre como chamar **SpoolerNotify**, consulte qualquer um dos seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="9abf1-173">For more information about calling **SpoolerNotify**, see any of the following topics:</span></span>
  
- [<span data-ttu-id="9abf1-174">Implementar método FlushQueues</span><span class="sxs-lookup"><span data-stu-id="9abf1-174">Implementing the FlushQueues Method</span></span>](implementing-the-flushqueues-method.md)
    
- [<span data-ttu-id="9abf1-175">Interagir com um spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="9abf1-175">Interacting with the MAPI Spooler</span></span>](interacting-with-the-mapi-spooler.md)
    
- [<span data-ttu-id="9abf1-176">Modelo de recebimento de mensagens</span><span class="sxs-lookup"><span data-stu-id="9abf1-176">Message Reception Model</span></span>](message-reception-model.md)
    
## <a name="see-also"></a><span data-ttu-id="9abf1-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="9abf1-177">See also</span></span>



[<span data-ttu-id="9abf1-178">IMsgStore::NotifyNewMail</span><span class="sxs-lookup"><span data-stu-id="9abf1-178">IMsgStore::NotifyNewMail</span></span>](imsgstore-notifynewmail.md)
  
[<span data-ttu-id="9abf1-179">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="9abf1-179">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="9abf1-180">IXPLogon::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="9abf1-180">IXPLogon::SubmitMessage</span></span>](ixplogon-submitmessage.md)
  
[<span data-ttu-id="9abf1-181">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9abf1-181">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

