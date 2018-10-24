---
title: Provedor de transporte e modelo operacional do spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 26d9982248fde015a584eb79cc248bafc5afc6bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594030"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="fdfda-103">Provedor de transporte e modelo operacional do spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="fdfda-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="fdfda-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fdfda-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fdfda-105">Inicialização do provedor de transporte, inicialização, processamento, desligamento e deinitialization são realizadas por uma série de chamadas do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="fdfda-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="fdfda-106">As chamadas são sequenciadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="fdfda-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="fdfda-107">O MAPI spooler chama a função [XPProviderInit](xpproviderinit.md) , passa um objeto de suporte, obtém o objeto de provedor e verifica se o provedor de transporte e o spooler MAPI suportam um números de versão do intervalo compatível de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdfda-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="fdfda-108">O MAPI spooler chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) do [IXPProvider: IUnknown](ixpprovideriunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="fdfda-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="fdfda-109">Uma sessão é estabelecida entre o spooler MAPI e o provedor de transporte com as credenciais da seção atual do perfil.</span><span class="sxs-lookup"><span data-stu-id="fdfda-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="fdfda-110">Provedor de transporte que retorna um objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="fdfda-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="fdfda-111">O MAPI spooler chama o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="fdfda-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="fdfda-112">O provedor de transporte retorna uma lista de identificadores exclusivos (UIDs) e tipos de endereço de email serão aceitas.</span><span class="sxs-lookup"><span data-stu-id="fdfda-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="fdfda-113">O provedor de transporte chama o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar sua linha na tabela de status de MAPI.</span><span class="sxs-lookup"><span data-stu-id="fdfda-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="fdfda-114">O MAPI spooler chama o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar o recebimento e transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fdfda-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="fdfda-115">Se solicitado pelo provedor de transporte em seu retorno para a chamada **TransportLogon** , o MAPI spooler periodicamente chama o método [IXPLogon::Idle](ixplogon-idle.md) .</span><span class="sxs-lookup"><span data-stu-id="fdfda-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="fdfda-116">Processamento ocioso é útil se o provedor de transporte precisa sondar o sistema de mensagens subjacente para novas mensagens ou realize outras tarefas de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="fdfda-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="fdfda-117">O spooler MAPI e o provedor de transporte enviar e recebem mensagens.</span><span class="sxs-lookup"><span data-stu-id="fdfda-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="fdfda-118">Para obter mais informações, consulte [Modelos de envio de mensagem](message-submission-model.md) e [recepção de mensagem](message-reception-model.md).</span><span class="sxs-lookup"><span data-stu-id="fdfda-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="fdfda-119">O MAPI spooler chama em objetos de suporte, a mensagem e o anexo e solicitações de transporte de serviços.</span><span class="sxs-lookup"><span data-stu-id="fdfda-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="fdfda-120">O MAPI spooler chama o método de **TransportNotify** para desabilitar o recebimento e transmissão de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fdfda-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="fdfda-121">O MAPI spooler libera os objetos de logon e o provedor.</span><span class="sxs-lookup"><span data-stu-id="fdfda-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="fdfda-122">Para obter mais informações, consulte o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) .</span><span class="sxs-lookup"><span data-stu-id="fdfda-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

