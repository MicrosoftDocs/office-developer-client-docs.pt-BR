---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437536"
---
# <a name="imapisupportsetprovideruid"></a><span data-ttu-id="b3474-103">IMAPISupport::SetProviderUID</span><span class="sxs-lookup"><span data-stu-id="b3474-103">IMAPISupport::SetProviderUID</span></span>

  
  
<span data-ttu-id="b3474-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3474-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3474-105">Registra uma estrutura [MAPIUID](mapiuid.md) que representa exclusivamente o provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="b3474-105">Registers a [MAPIUID](mapiuid.md) structure that uniquely represents the service provider.</span></span> 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b3474-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3474-106">Parameters</span></span>

 <span data-ttu-id="b3474-107">_lpProviderID_</span><span class="sxs-lookup"><span data-stu-id="b3474-107">_lpProviderID_</span></span>
  
> <span data-ttu-id="b3474-108">no Um ponteiro para a estrutura **MAPIUID** que identifica o catálogo de endereços ou o provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3474-108">[in] A pointer to the **MAPIUID** structure that identifies the address book or message store provider.</span></span> 
    
 <span data-ttu-id="b3474-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3474-109">_ulFlags_</span></span>
  
> <span data-ttu-id="b3474-110">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="b3474-110">Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b3474-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b3474-111">Return value</span></span>

<span data-ttu-id="b3474-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3474-112">S_OK</span></span> 
  
> <span data-ttu-id="b3474-113">A estrutura **MAPIUID** foi registrada com êxito.</span><span class="sxs-lookup"><span data-stu-id="b3474-113">The **MAPIUID** structure was successfully registered.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b3474-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b3474-114">Remarks</span></span>

<span data-ttu-id="b3474-115">O método **IMAPISupport:: SetProviderUID** é implementado para o catálogo de endereços e os objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="b3474-115">The **IMAPISupport::SetProviderUID** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="b3474-116">Esses provedores chamam **SetProviderUID** para registrar um identificador exclusivo descrito na estrutura **MAPIUID** indicada por _lpProviderID_.</span><span class="sxs-lookup"><span data-stu-id="b3474-116">These providers call **SetProviderUID** to register a unique identifier described in the **MAPIUID** structure that is pointed to by  _lpProviderID_.</span></span> <span data-ttu-id="b3474-117">Os provedores incluem esse identificador em todos os identificadores de entrada criados por eles.</span><span class="sxs-lookup"><span data-stu-id="b3474-117">Providers include this identifier in all of the entry identifiers that they create.</span></span> 
  
<span data-ttu-id="b3474-118">MAPI usa a estrutura **MAPIUID** quando ele envia mensagens de saída para o spooler MAPI e para determinar o provedor apropriado para lidar com solicitações de cliente.</span><span class="sxs-lookup"><span data-stu-id="b3474-118">MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests.</span></span> <span data-ttu-id="b3474-119">Por exemplo, quando um cliente chama o método [IMAPISession:: OpenEntry](imapisession-openentry.md) , o MAPI examina a parte **MAPIUID** do identificador de entrada, mapeia-o para o provedor que o aprovou para **SetProviderUID**e chama o **OpenEntry** do provedor .</span><span class="sxs-lookup"><span data-stu-id="b3474-119">For example, when a client calls the [IMAPISession::OpenEntry](imapisession-openentry.md) method, MAPI examines the **MAPIUID** portion of the entry identifier, maps it to the provider that passed it to **SetProviderUID**, and calls that provider's **OpenEntry**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b3474-120">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b3474-120">Notes to callers</span></span>

<span data-ttu-id="b3474-121">Chame **SetProviderUID** no momento do logon para registrar sua estrutura do **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="b3474-121">Call **SetProviderUID** at logon time to register your **MAPIUID** structure.</span></span> <span data-ttu-id="b3474-122">MAPI permite que o catálogo de endereços e provedores de repositório de mensagens registrem vários identificadores.</span><span class="sxs-lookup"><span data-stu-id="b3474-122">MAPI allows address book and message store providers to register multiple identifiers.</span></span> <span data-ttu-id="b3474-123">Quando você faz várias chamadas para o **SetProviderUID**, ela sempre adiciona a estrutura **MAPIUID** ao conjunto de estruturas **MAPIUID** do provedor, mesmo que o **MAPIUID** seja uma duplicata.</span><span class="sxs-lookup"><span data-stu-id="b3474-123">When you make multiple calls to **SetProviderUID**, it always adds the **MAPIUID** structure to the provider's set of **MAPIUID** structures, even if the **MAPIUID** is a duplicate.</span></span> <span data-ttu-id="b3474-124">**SetProviderUID** não pode remover um **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="b3474-124">**SetProviderUID** cannot remove a **MAPIUID**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3474-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3474-125">See also</span></span>



[<span data-ttu-id="b3474-126">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="b3474-126">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="b3474-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3474-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

