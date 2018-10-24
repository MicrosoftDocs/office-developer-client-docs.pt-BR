---
title: Usar objetos livres de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 49a94b785a51b4b0c3082832145250eec0745a19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580975"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="90fa7-103">Usar objetos livres de threads</span><span class="sxs-lookup"><span data-stu-id="90fa7-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="90fa7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90fa7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90fa7-105">Aplicativos cliente podem assumir que os objetos usados diretamente ou como retornos de chamada são sempre thread-safe, exceto nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="90fa7-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="90fa7-106">Objeto de status de um provedor de transporte obtido por meio de uma chamada de cliente para [IMAPISession::OpenEntry](imapisession-openentry.md) com um identificador de entrada de linha de tabela de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="90fa7-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="90fa7-107">Obtidos por meio de uma chamada de cliente para [MAPIOpenFormMgr](mapiopenformmgr.md)todos os objetos de formulário MAPI.</span><span class="sxs-lookup"><span data-stu-id="90fa7-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="90fa7-108">Objetos de formulário cumprir regras de modelo apartment e os clientes devem usá-los e todos os objetos contidos por eles somente no segmento que foram criados.</span><span class="sxs-lookup"><span data-stu-id="90fa7-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="90fa7-109">Quando um cliente acessa a linha de um provedor de transporte na tabela de status que inclui o identificador de entrada do objeto status associado, o cliente pode chamar **OpenEntry** com esse identificador de entrada para abrir o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="90fa7-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="90fa7-110">Este objeto de status não é thread-safe porque os provedores de transporte executado no contexto do spooler MAPI e não mantêm um contexto separado para seu objeto de status.</span><span class="sxs-lookup"><span data-stu-id="90fa7-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="90fa7-111">O objeto status obedeça a regras de modelo apartment e os clientes devem usar somente no segmento que criou a ele.</span><span class="sxs-lookup"><span data-stu-id="90fa7-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="90fa7-112">Um cliente também deve chamar [MAPIInitialize](mapiinitialize.md) em cada segmento antes de usar quaisquer objetos MAPI e [MAPIUninitialize](mapiuninitialize.md) quando que usam for concluído.</span><span class="sxs-lookup"><span data-stu-id="90fa7-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="90fa7-113">Essas chamadas devem ser feitas, mesmo se os objetos a serem usados são passados para o thread de uma fonte externa.</span><span class="sxs-lookup"><span data-stu-id="90fa7-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="90fa7-114">**MAPIInitialize** e **MAPIUninitialize** podem ser chamado de qualquer lugar, exceto de dentro de uma função do Win32 **DllMain** , uma função que é invocada pelo sistema quando threads e processos são inicializados e encerradas, ou mediante chamadas para o \*\* LoadLibrary\*\* e **FreeLibrary** funções.</span><span class="sxs-lookup"><span data-stu-id="90fa7-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="90fa7-115">Usar indiretas objetos nunca devem ser considerados thread-safe.</span><span class="sxs-lookup"><span data-stu-id="90fa7-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="90fa7-116">Usar indiretas objetos são retornados por métodos que requeiram ponteiros de interface de destino como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="90fa7-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="90fa7-117">Exemplos de tais métodos são **IMAPIProp::CopyTo** e **CopyProps**, **IMAPIFolder::CopyFolder** e **CopyMessage**e **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="90fa7-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="90fa7-118">Se quiser que um provedor de serviços para um objeto desse tipo de chamada de um thread diferente em que ele foi passado, o provedor é responsável por marshaling explicitamente o objeto.</span><span class="sxs-lookup"><span data-stu-id="90fa7-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

