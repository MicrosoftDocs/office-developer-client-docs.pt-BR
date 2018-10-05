---
title: Liberar o provedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386219"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="432a0-103">Liberar o provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="432a0-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="432a0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="432a0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="432a0-105">Quando MAPI ou o MAPI spooler termina usando um objeto de logon de transporte:</span><span class="sxs-lookup"><span data-stu-id="432a0-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="432a0-106">MAPI ou o MAPI spooler chama o método de [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="432a0-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="432a0-107">O provedor de transporte invalida o objeto de status chamando o método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) .</span><span class="sxs-lookup"><span data-stu-id="432a0-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="432a0-108">Se o provedor de transporte invalida objetos de mensagem que estão sendo enviadas ou recebidas no momento da chamada **TransportLogoff** dependem os sinalizadores que foram passados ao **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="432a0-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="432a0-109">O provedor de transporte chama o suporte ao método do objeto [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) para remover a linha do provedor de transporte da tabela de status e remova qualquer identificadores exclusivos (UIDs) que foram definidos com o [IMAPISupport tabelas internas:: SetProviderUID](imapisupport-setprovideruid.md) método.</span><span class="sxs-lookup"><span data-stu-id="432a0-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="432a0-110">Ele diminui a contagem de objetos de logon conhecidos ativos neste objeto provedor.</span><span class="sxs-lookup"><span data-stu-id="432a0-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="432a0-111">Se a contagem chegar a zero, o MAPI chama o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) e a **versão** no objeto provedor.</span><span class="sxs-lookup"><span data-stu-id="432a0-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="432a0-112">Se este foi o último objeto fornecedor conhecido usando essa DLL sobre esse processo, MAPI chama a função de **FreeLibrary** na DLL mais tarde.</span><span class="sxs-lookup"><span data-stu-id="432a0-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="432a0-113">Memória para o objeto de suporte MAPI seja liberada e retorna o objeto de suporte ao método de **lançamento** .</span><span class="sxs-lookup"><span data-stu-id="432a0-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="432a0-114">O método **TransportLogoff** Retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="432a0-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="432a0-115">MAPI ou o MAPI spooler chama a **versão** no objeto de logon do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="432a0-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="432a0-116">A memória para o objeto é liberada.</span><span class="sxs-lookup"><span data-stu-id="432a0-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="432a0-117">MAPI ou o MAPI spooler chama **FreeLibrary** no provedor DLL.</span><span class="sxs-lookup"><span data-stu-id="432a0-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="432a0-118">Para robustez, os objetos de logon e o provedor devem ser capazes de lidar com chamadas de **versão** finais em si mesma sem ter que primeiro suas **TransportLogoff** ou os métodos de **desligamento** chamados.</span><span class="sxs-lookup"><span data-stu-id="432a0-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="432a0-119">Se a **versão** é chamado nesses casos, provedores de transporte devem tratar as chamadas como se **TransportLogoff** ou **desligamento** tivesse sido chamado com um argumento zero seguido de **lançamento**.</span><span class="sxs-lookup"><span data-stu-id="432a0-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

