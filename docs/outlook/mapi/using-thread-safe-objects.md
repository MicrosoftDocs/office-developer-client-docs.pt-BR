---
title: Usando Thread-Safe objetos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e688db5e-d1a1-4afc-998f-b3d31eb6239b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 611e0a49f0fd8df8fe40205a33ed5501055c3d45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425166"
---
# <a name="using-thread-safe-objects"></a><span data-ttu-id="7bffd-103">Usando Thread-Safe objetos</span><span class="sxs-lookup"><span data-stu-id="7bffd-103">Using Thread-Safe Objects</span></span>

  
  
<span data-ttu-id="7bffd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7bffd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7bffd-105">Os aplicativos cliente podem presumir que os objetos usados diretamente ou como retornos de chamada sejam sempre thread-safe, exceto nos seguintes casos:</span><span class="sxs-lookup"><span data-stu-id="7bffd-105">Client applications can assume that objects used directly or as callbacks are always thread-safe except in the following cases:</span></span>
  
- <span data-ttu-id="7bffd-106">Objeto de status de um provedor de transporte obtido por meio de uma chamada de cliente para [IMAPISession::OpenEntry](imapisession-openentry.md) com um identificador de entrada da linha da tabela de status do provedor.</span><span class="sxs-lookup"><span data-stu-id="7bffd-106">A transport provider's status object obtained through a client call to [IMAPISession::OpenEntry](imapisession-openentry.md) with an entry identifier from the provider's status table row.</span></span> 
    
- <span data-ttu-id="7bffd-107">Todos os objetos de formulário MAPI obtidos por meio de uma chamada de cliente para [MAPIOpenFormMgr](mapiopenformmgr.md).</span><span class="sxs-lookup"><span data-stu-id="7bffd-107">All MAPI form objects obtained through a client call to [MAPIOpenFormMgr](mapiopenformmgr.md).</span></span> <span data-ttu-id="7bffd-108">Os objetos de formulário obedecerão às regras de modelo de apartment e os clientes devem usá-los e todos os objetos contidos neles somente no thread que os criou.</span><span class="sxs-lookup"><span data-stu-id="7bffd-108">Form objects obey apartment model rules and clients must use them and all objects contained by them only on the thread that created them.</span></span>
    
<span data-ttu-id="7bffd-109">Quando um cliente acessa a linha de um provedor de transporte na tabela de status que inclui o identificador de entrada do objeto de status associado, o cliente pode chamar **OpenEntry** com esse identificador de entrada para abrir o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="7bffd-109">When a client accesses a transport provider's row in the status table that includes the entry identifier of the associated status object, the client can call **OpenEntry** with that entry identifier to open the status object.</span></span> <span data-ttu-id="7bffd-110">Esse objeto de status não é thread-safe porque os provedores de transporte são executados no contexto do spooler MAPI e não mantêm um contexto separado para seu objeto de status.</span><span class="sxs-lookup"><span data-stu-id="7bffd-110">This status object is not thread-safe because transport providers run in the context of the MAPI spooler and do not maintain a separate context for their status object.</span></span> <span data-ttu-id="7bffd-111">O objeto de status segue as regras de modelo de apartment e os clientes devem usá-lo somente no thread que o criou.</span><span class="sxs-lookup"><span data-stu-id="7bffd-111">The status object obeys apartment model rules and clients must use it only on the thread that created it.</span></span> 
  
<span data-ttu-id="7bffd-112">Um cliente também deve invocar [MAPIInitialize](mapiinitialize.md) em cada thread antes de usar qualquer objeto MAPI [e MAPIUninitialize](mapiuninitialize.md) quando esse uso for concluído.</span><span class="sxs-lookup"><span data-stu-id="7bffd-112">A client must also invoke [MAPIInitialize](mapiinitialize.md) on every thread before using any MAPI objects and [MAPIUninitialize](mapiuninitialize.md) when that use is complete.</span></span> <span data-ttu-id="7bffd-113">Essas chamadas devem ser feitas mesmo se os objetos a serem usados são passados para o thread de uma fonte externa.</span><span class="sxs-lookup"><span data-stu-id="7bffd-113">These calls should be made even if the objects to be used are passed to the thread from an external source.</span></span> <span data-ttu-id="7bffd-114">**MAPIInitialize** e **MAPIUninitialize** podem ser chamados de qualquer lugar, exceto de dentro de uma função **DllMain** Win32, uma função que é invocada pelo sistema quando processos e threads são inicializados e encerrados, ou em chamadas para as funções **LoadLibrary** e **FreeLibrary.**</span><span class="sxs-lookup"><span data-stu-id="7bffd-114">**MAPIInitialize** and **MAPIUninitialize** can be called from anywhere except from within a Win32 **DllMain** function, a function that is invoked by the system when processes and threads are initialized and terminated, or upon calls to the **LoadLibrary** and **FreeLibrary** functions.</span></span> 
  
<span data-ttu-id="7bffd-115">Os objetos de uso indireto nunca devem ser assumidos como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="7bffd-115">Indirect use objects should never be assumed to be thread-safe.</span></span> <span data-ttu-id="7bffd-116">Objetos de uso indireto são retornados por métodos que exigem ponteiros de interface de destino como parâmetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="7bffd-116">Indirect use objects are returned by methods that require destination interface pointers as input parameters.</span></span> <span data-ttu-id="7bffd-117">Exemplos de tais métodos são **IMAPIProp::CopyTo** e **CopyProps**, **IMAPIFolder::CopyFolder** e **CopyMessage** e **IMsgServiceAdmin::CopyMsgService**.</span><span class="sxs-lookup"><span data-stu-id="7bffd-117">Examples of such methods are **IMAPIProp::CopyTo** and **CopyProps**, **IMAPIFolder::CopyFolder** and **CopyMessage**, and **IMsgServiceAdmin::CopyMsgService**.</span></span> <span data-ttu-id="7bffd-118">Se um provedor de serviços quiser chamar esse objeto de um thread diferente do que foi passado, o provedor será responsável por empacotar explicitamente o objeto.</span><span class="sxs-lookup"><span data-stu-id="7bffd-118">If a service provider wants to call such an object from a thread other than the one on which it was passed, the provider is responsible for explicitly marshaling the object.</span></span>
  

