---
title: Modelo de recebimento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d85d269e-2251-4399-9159-a2f47a85e3d1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cecdb2c30d6c9df2aafbeed43714269b863ebc48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19768126"
---
# <a name="message-reception-model"></a><span data-ttu-id="d4af9-103">Modelo de recebimento de mensagens</span><span class="sxs-lookup"><span data-stu-id="d4af9-103">Message Reception Model</span></span>

  
  
<span data-ttu-id="d4af9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4af9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4af9-105">O provedor de transporte controla se o MAPI spooler deve sondá-lo para email de entrada ou se ele realiza uma chamada de volta para o MAPI spooler quando chegar novo email.</span><span class="sxs-lookup"><span data-stu-id="d4af9-105">The transport provider controls whether the MAPI spooler must poll it for incoming mail or whether it performs a call back to the MAPI spooler when new mail arrives.</span></span> <span data-ttu-id="d4af9-106">O provedor de transporte define o sinalizador SP_LOGON_POLL quando ela retorna de [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para solicitar sondagem.</span><span class="sxs-lookup"><span data-stu-id="d4af9-106">The transport provider sets the SP_LOGON_POLL flag when it returns from [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) to request polling.</span></span> <span data-ttu-id="d4af9-107">Caso contrário, o provedor de transporte usa [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) quando o email de entrada estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="d4af9-107">Otherwise, the transport provider uses [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) when incoming mail is available.</span></span> <span data-ttu-id="d4af9-108">Depois que o email de entrada está disponível de aprendizagem, o MAPI spooler abre uma nova mensagem e solicita o provedor de transporte para armazenar as propriedades da mensagem recebida na mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af9-108">After learning that incoming mail is available, the MAPI spooler opens a new message and asks the transport provider to store the received message properties into the message.</span></span> 
  
<span data-ttu-id="d4af9-109">Esse processo funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d4af9-109">This process works as follows:</span></span>
  
1. <span data-ttu-id="d4af9-110">Mensagens disponíveis são indicadas pelo provedor de transporte chamar **IMAPISupport::SpoolerNotify** ou pelo spooler MAPI chamar [IXPLogon::Poll](ixplogon-poll.md).</span><span class="sxs-lookup"><span data-stu-id="d4af9-110">Available messages are indicated by either the transport provider calling **IMAPISupport::SpoolerNotify** or by the MAPI spooler calling [IXPLogon::Poll](ixplogon-poll.md).</span></span>
    
2. <span data-ttu-id="d4af9-111">O MAPI spooler chama [IXPLogon::StartMessage](ixplogon-startmessage.md) para iniciar o processo.</span><span class="sxs-lookup"><span data-stu-id="d4af9-111">The MAPI spooler calls [IXPLogon::StartMessage](ixplogon-startmessage.md) to initiate the process.</span></span> 
    
3. <span data-ttu-id="d4af9-112">O provedor de transporte coloca um valor de referência no local referenciado na **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="d4af9-112">The transport provider places a reference value in the location referenced in **StartMessage**.</span></span> <span data-ttu-id="d4af9-113">Esses valores de referência permitem que o provedor de transporte e o spooler MAPI controlar qual mensagem está sendo processada quando há várias mensagens para fornecer.</span><span class="sxs-lookup"><span data-stu-id="d4af9-113">These reference values allow the transport provider and the MAPI spooler to keep track of which message is being processed when there are multiple messages to deliver.</span></span>
    
4. <span data-ttu-id="d4af9-114">Provedor de transporte que armazena os dados de mensagem no passado. [IMessage: IMAPIProp](imessageimapiprop.md) instância.</span><span class="sxs-lookup"><span data-stu-id="d4af9-114">The transport provider stores the message data into the passed [IMessage : IMAPIProp](imessageimapiprop.md) instance.</span></span> 
    
5. <span data-ttu-id="d4af9-115">O provedor de transporte chama o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) na instância **IMessage** e retorna a partir de **StartMessage**.</span><span class="sxs-lookup"><span data-stu-id="d4af9-115">The transport provider calls the [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method on the **IMessage** instance and returns from **StartMessage**.</span></span>
    
6. <span data-ttu-id="d4af9-116">O MAPI spooler chama [IXPLogon::TransportNotify](ixplogon-transportnotify.md) se ele deve parar a entrega da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af9-116">The MAPI spooler calls [IXPLogon::TransportNotify](ixplogon-transportnotify.md) if it must stop message delivery.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="d4af9-117">Se um provedor de transporte deve fornecer um grande número de mensagens e o provedor de transporte está usando **IMAPISupport::SpoolerNotify** em vez de **IXPLogon::Poll**, tome cuidado não para chamar **SpoolerNotify** muito frequentemente na ordem não fazer impedir que outros provedores de transporte do tempo da CPU.</span><span class="sxs-lookup"><span data-stu-id="d4af9-117">If a transport provider must deliver a large number of messages and the transport provider is using **IMAPISupport::SpoolerNotify** instead of **IXPLogon::Poll**, care should be taken not to call **SpoolerNotify** too frequently in order not to deprive other transport providers of CPU time.</span></span> <span data-ttu-id="d4af9-118">O MAPI spooler possuem lógica para evitar que isso aconteça, mas, em geral, o intervalo entre chamadas **SpoolerNotify** deve ser maior que o tempo que leva seu provedor de transporte para processar uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af9-118">The MAPI spooler does have logic to prevent this from happening, but in general the interval between **SpoolerNotify** calls should be longer than the time it takes your transport provider to process one message.</span></span> <span data-ttu-id="d4af9-119">> Além disso, o MAPI spooler talvez não processar uma mensagem de entrada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d4af9-119">> Also, the MAPI spooler may not process an incoming message immediately.</span></span> <span data-ttu-id="d4af9-120">O MAPI spooler pode solicitar que o provedor de transporte para executar outras tarefas antes de ele recebe a mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="d4af9-120">The MAPI spooler may ask the transport provider to perform other tasks before it receives the incoming message.</span></span> 
  

