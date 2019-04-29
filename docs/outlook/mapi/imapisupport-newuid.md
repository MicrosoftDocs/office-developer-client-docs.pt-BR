---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406994"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="e86b9-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="e86b9-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="e86b9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e86b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e86b9-105">Cria uma nova estrutura [MAPIUID](mapiuid.md) a ser usada como um identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="e86b9-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="e86b9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e86b9-106">Parameters</span></span>

 <span data-ttu-id="e86b9-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="e86b9-107">_lpMuid_</span></span>
  
> <span data-ttu-id="e86b9-108">Um ponteiro para a nova estrutura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="e86b9-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e86b9-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e86b9-109">Return value</span></span>

<span data-ttu-id="e86b9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e86b9-110">S_OK</span></span> 
  
> <span data-ttu-id="e86b9-111">A nova estrutura **MAPIUID** foi criada.</span><span class="sxs-lookup"><span data-stu-id="e86b9-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e86b9-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e86b9-112">Remarks</span></span>

<span data-ttu-id="e86b9-113">O método **IMAPISupport:: NewUID** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="e86b9-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="e86b9-114">Os provedores de serviço e os serviços de mensagens chamam o **NewUID** sempre que precisam gerar um identificador único de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="e86b9-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="e86b9-115">Um provedor de repositório de mensagens, por exemplo, pode chamar **NewUID** para obter um **MAPIUID** a ser colocado na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de uma mensagem recém-criada.</span><span class="sxs-lookup"><span data-stu-id="e86b9-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e86b9-116">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e86b9-116">Notes to callers</span></span>

<span data-ttu-id="e86b9-117">Não confunda a estrutura **MAPIUID** que você registra no momento do logon com as estruturas **MAPIUID** que o método **NewUID** cria.</span><span class="sxs-lookup"><span data-stu-id="e86b9-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="e86b9-118">A estrutura **MAPIUID** que você registra ao chamar o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) representa seu catálogo de endereços ou provedor de repositório de mensagens para MAPI e é usado para distinguir identificadores de entrada criados por provedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="e86b9-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="e86b9-119">Essa estrutura **MAPIUID** deve ser codificada e não obtida por meio de uma chamada para **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="e86b9-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e86b9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="e86b9-120">See also</span></span>



[<span data-ttu-id="e86b9-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="e86b9-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="e86b9-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e86b9-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

