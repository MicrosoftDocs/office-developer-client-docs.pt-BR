---
title: Liberando o provedor de transporte
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: '�ltima altera��o: segunda-feira, 7 de dezembro de 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328382"
---
# <a name="releasing-the-transport-provider"></a><span data-ttu-id="39bd1-103">Liberando o provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="39bd1-103">Releasing the Transport Provider</span></span>

 
  
<span data-ttu-id="39bd1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39bd1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39bd1-105">Quando o Spooler MAPI ou MAPI termina de usar um objeto de logon de transporte:</span><span class="sxs-lookup"><span data-stu-id="39bd1-105">When MAPI or the MAPI spooler finishes using a transport logon object:</span></span>
  
1. <span data-ttu-id="39bd1-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span><span class="sxs-lookup"><span data-stu-id="39bd1-106">MAPI or the MAPI spooler calls the transport provider's [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) method.</span></span> 
    
2. <span data-ttu-id="39bd1-107">O provedor de transporte invalida o objeto de status chamando o [método IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md)</span><span class="sxs-lookup"><span data-stu-id="39bd1-107">The transport provider invalidates the status object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method.</span></span> <span data-ttu-id="39bd1-108">Se o provedor de transporte invalida os objetos de mensagem que estão sendo enviados ou recebidos no momento da chamada **TransportLogoff** depende dos sinalizadores que foram passados para **TransportLogoff**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-108">Whether the transport provider invalidates message objects that are being sent or received at the time of the **TransportLogoff** call depends on the flags that were passed to **TransportLogoff**.</span></span>
    
3. <span data-ttu-id="39bd1-109">O provedor de transporte chama o método [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) do objeto de suporte para remover a linha do provedor de transporte da tabela de status e remover das tabelas internas quaisquer identificadores exclusivos (UIDs) que foram definidos com o método [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="39bd1-109">The transport provider calls the support object's [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) method to remove the transport provider's row from the status table and remove from internal tables any unique identifiers (UIDs) that were set with the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="39bd1-110">Ele diminui a contagem de objetos de logon conhecidos ativos neste objeto de provedor.</span><span class="sxs-lookup"><span data-stu-id="39bd1-110">It decrements the count of known logon objects active on this provider object.</span></span> <span data-ttu-id="39bd1-111">Se a contagem atingir zero, o MAPI chamará o método [IXPProvider::Shutdown](ixpprovider-shutdown.md) e **Release** no objeto do provedor.</span><span class="sxs-lookup"><span data-stu-id="39bd1-111">If the count reaches zero, MAPI calls the [IXPProvider::Shutdown](ixpprovider-shutdown.md) method and **Release** on the provider object.</span></span> <span data-ttu-id="39bd1-112">Se esse for o último objeto de provedor conhecido que usa essa DLL nesse processo, o MAPI chamará a **função FreeLibrary** na DLL posteriormente.</span><span class="sxs-lookup"><span data-stu-id="39bd1-112">If this was the last known provider object using this DLL on this process, MAPI calls the **FreeLibrary** function on the DLL at a later time.</span></span> <span data-ttu-id="39bd1-113">A memória para o objeto de suporte MAPI é liberada e o método **Release** do objeto de suporte retorna.</span><span class="sxs-lookup"><span data-stu-id="39bd1-113">Memory for the MAPI support object is freed and the support object **Release** method returns.</span></span> 
    
4. <span data-ttu-id="39bd1-114">O **método TransportLogoff** retorna S_OK.</span><span class="sxs-lookup"><span data-stu-id="39bd1-114">The **TransportLogoff** method returns S_OK.</span></span> 
    
5. <span data-ttu-id="39bd1-115">MAPI or the MAPI spooler **calls Release** on the transport provider's logon object.</span><span class="sxs-lookup"><span data-stu-id="39bd1-115">MAPI or the MAPI spooler calls **Release** on the transport provider's logon object.</span></span> <span data-ttu-id="39bd1-116">A memória do objeto é liberada.</span><span class="sxs-lookup"><span data-stu-id="39bd1-116">The memory for the object is released.</span></span> 
    
6. <span data-ttu-id="39bd1-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span><span class="sxs-lookup"><span data-stu-id="39bd1-117">MAPI or the MAPI spooler calls **FreeLibrary** on the provider DLL.</span></span> 
    
<span data-ttu-id="39bd1-118">Para robustez, os objetos de logon e provedor devem ser capazes de lidar com chamadas finais **de** Versão por conta própria sem antes ter seus métodos **TransportLogoff** ou **Shutdown** chamados.</span><span class="sxs-lookup"><span data-stu-id="39bd1-118">For robustness, the logon and provider objects should be able to handle final **Release** calls on themselves without first having their **TransportLogoff** or **Shutdown** methods called.</span></span> <span data-ttu-id="39bd1-119">Se **Release** for chamado nesses casos, os provedores de transporte deverão tratar as chamadas como se **TransportLogoff** ou **Shutdown** tivessem sido chamados com um argumento zero seguido de **Release**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-119">If **Release** is called in such cases, transport providers should treat the calls as if **TransportLogoff** or **Shutdown** had been called with a zero argument followed by **Release**.</span></span>
  

