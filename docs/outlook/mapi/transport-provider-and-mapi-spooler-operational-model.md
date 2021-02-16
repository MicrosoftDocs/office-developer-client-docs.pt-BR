---
title: Provedor de Transporte e Modelo Operacional do Spooler MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5987111844f087801c63989b905992900ff6909c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426622"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a><span data-ttu-id="2d4c5-103">Provedor de Transporte e Modelo Operacional do Spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="2d4c5-103">Transport Provider and MAPI Spooler Operational Model</span></span>

  
  
<span data-ttu-id="2d4c5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d4c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d4c5-105">A inicialização, a inicialização, o processamento, o desligamento e a inicialização do provedor de transporte são realizadas por uma série de chamadas do spooler MAPI para o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-105">Transport provider initialization, startup, processing, shutdown and deinitialization are accomplished by a series of calls from the MAPI spooler to the transport provider.</span></span> <span data-ttu-id="2d4c5-106">As chamadas são sequenciadas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="2d4c5-106">The calls are sequenced as follows:</span></span>
  
1. <span data-ttu-id="2d4c5-107">O spooler MAPI chama a função [XPProviderInit,](xpproviderinit.md) passa um objeto de suporte, obtém o objeto do provedor e verifica se o provedor de transporte e o spooler MAPI suportam um intervalo compatível de números de versão MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-107">The MAPI spooler calls the [XPProviderInit](xpproviderinit.md) function, passes a support object, gets the provider object, and checks that the transport provider and MAPI spooler support a compatible range of MAPI version numbers.</span></span> 
    
2. <span data-ttu-id="2d4c5-108">O spooler MAPI chama o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) da interface [IXPProvider : IUnknown.](ixpprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="2d4c5-108">The MAPI spooler calls the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method of the [IXPProvider : IUnknown](ixpprovideriunknown.md) interface.</span></span> <span data-ttu-id="2d4c5-109">Uma sessão é estabelecida entre o spooler MAPI e o provedor de transporte com as credenciais na seção atual do perfil.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-109">A session is established between the MAPI spooler and the transport provider with the credentials in the current section of the profile.</span></span> <span data-ttu-id="2d4c5-110">O provedor de transporte retorna um objeto de logon.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-110">The transport provider returns a logon object.</span></span> 
    
3. <span data-ttu-id="2d4c5-111">O spooler MAPI chama o [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md)</span><span class="sxs-lookup"><span data-stu-id="2d4c5-111">The MAPI spooler calls the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> <span data-ttu-id="2d4c5-112">O provedor de transporte retorna uma lista dos identificadores exclusivos (UIDs) e tipos de endereço de email que ele aceitará.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-112">The transport provider returns a list of the unique identifiers (UIDs) and email address types it will accept.</span></span> 
    
4. <span data-ttu-id="2d4c5-113">O provedor de transporte chama o [método IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar sua linha na tabela de status MAPI.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-113">The transport provider calls the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to create its row in the MAPI status table.</span></span> 
    
5. <span data-ttu-id="2d4c5-114">O spooler MAPI chama o [método IXPLogon::TransportNotify](ixplogon-transportnotify.md) para habilitar a transmissão e a recepção de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-114">The MAPI spooler calls the [IXPLogon::TransportNotify](ixplogon-transportnotify.md) method to enable message transmission and reception.</span></span> 
    
6. <span data-ttu-id="2d4c5-115">Se solicitado pelo provedor de transporte em seu retorno para a chamada **TransportLogon,** o spooler MAPI chama periodicamente o método [IXPLogon::Idle.](ixplogon-idle.md)</span><span class="sxs-lookup"><span data-stu-id="2d4c5-115">If requested by the transport provider in its return for the **TransportLogon** call, the MAPI spooler periodically calls the [IXPLogon::Idle](ixplogon-idle.md) method.</span></span> <span data-ttu-id="2d4c5-116">O processamento ocioso será útil se o provedor de transporte precisar sondar o sistema de mensagens subjacente em busca de novas mensagens ou realizar outras tarefas de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-116">Idle processing is useful if the transport provider needs to poll the underlying messaging system for new messages or perform other low-priority tasks.</span></span> 
    
7. <span data-ttu-id="2d4c5-117">O spooler MAPI e o provedor de transporte enviam e recebem mensagens.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-117">The MAPI spooler and transport provider send and receive messages.</span></span> <span data-ttu-id="2d4c5-118">Para obter mais informações, consulte [Modelo de Envio de Mensagem](message-submission-model.md) e Modelo de Recepção de [Mensagens.](message-reception-model.md)</span><span class="sxs-lookup"><span data-stu-id="2d4c5-118">For more information, see [Message Submission Model](message-submission-model.md) and [Message Reception Model](message-reception-model.md).</span></span> <span data-ttu-id="2d4c5-119">O spooler mapi serviços de transporte solicitações e chamadas em objetos de suporte, mensagem e anexo.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-119">The MAPI spooler services transport requests and calls on support, message, and attachment objects.</span></span>
    
8. <span data-ttu-id="2d4c5-120">O spooler MAPI chama o **método TransportNotify** para desabilitar a transmissão e a recepção de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-120">The MAPI spooler calls the **TransportNotify** method to disable message transmission and reception.</span></span> 
    
9. <span data-ttu-id="2d4c5-121">O spooler MAPI libera os objetos de logon e provedor.</span><span class="sxs-lookup"><span data-stu-id="2d4c5-121">The MAPI spooler releases the logon and provider objects.</span></span> <span data-ttu-id="2d4c5-122">Para obter mais informações, consulte o [método IXPProvider::Shutdown.](ixpprovider-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="2d4c5-122">For more information, see the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method.</span></span> 
    

