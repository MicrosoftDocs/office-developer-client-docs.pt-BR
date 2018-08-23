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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 244087c41e33e470c42434e9d57cee7317bcb78c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571686"
---
# <a name="imapisupportnewuid"></a><span data-ttu-id="be530-103">IMAPISupport::NewUID</span><span class="sxs-lookup"><span data-stu-id="be530-103">IMAPISupport::NewUID</span></span>

  
  
<span data-ttu-id="be530-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be530-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be530-105">Cria uma nova estrutura [MAPIUID](mapiuid.md) a ser usado como um identificador exclusivo.</span><span class="sxs-lookup"><span data-stu-id="be530-105">Creates a new [MAPIUID](mapiuid.md) structure to be used as a unique identifier.</span></span> 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a><span data-ttu-id="be530-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="be530-106">Parameters</span></span>

 <span data-ttu-id="be530-107">_lpMuid_</span><span class="sxs-lookup"><span data-stu-id="be530-107">_lpMuid_</span></span>
  
> <span data-ttu-id="be530-108">Um ponteiro para a nova estrutura **MAPIUID** .</span><span class="sxs-lookup"><span data-stu-id="be530-108">A pointer to the new **MAPIUID** structure.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be530-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="be530-109">Return value</span></span>

<span data-ttu-id="be530-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="be530-110">S_OK</span></span> 
  
> <span data-ttu-id="be530-111">A nova estrutura **MAPIUID** foi criada.</span><span class="sxs-lookup"><span data-stu-id="be530-111">The new **MAPIUID** structure was created.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="be530-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="be530-112">Remarks</span></span>

<span data-ttu-id="be530-113">O método **IMAPISupport::NewUID** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="be530-113">The **IMAPISupport::NewUID** method is implemented for all support objects.</span></span> <span data-ttu-id="be530-114">Provedores de serviço e serviços de mensagem chamada **NewUID** sempre que precisam gerar um identificador exclusivo de longo prazo.</span><span class="sxs-lookup"><span data-stu-id="be530-114">Service providers and message services call **NewUID** whenever they need to generate a long-term unique identifier.</span></span> <span data-ttu-id="be530-115">Uma mensagem armazenar provedor, por exemplo, talvez chamada **NewUID** para obter um **MAPIUID** para colocar na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de uma mensagem recém-criado.</span><span class="sxs-lookup"><span data-stu-id="be530-115">A message store provider, for example, might call **NewUID** to obtain a **MAPIUID** to put in the **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) property of a newly created message.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="be530-116">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="be530-116">Notes to callers</span></span>

<span data-ttu-id="be530-117">Não confunda a estrutura **MAPIUID** que você registre na hora do logon com as estruturas de **MAPIUID** que o método **NewUID** cria.</span><span class="sxs-lookup"><span data-stu-id="be530-117">Do not confuse the **MAPIUID** structure that you register at logon time with the **MAPIUID** structures that the **NewUID** method creates.</span></span> <span data-ttu-id="be530-118">A estrutura **MAPIUID** que você registre quando você chama o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa seu catálogo de endereços ou mensagem armazenar provedor para MAPI e é usado para distinguir os identificadores de entrada que criar provedores diferentes.</span><span class="sxs-lookup"><span data-stu-id="be530-118">The **MAPIUID** structure that you register when you call the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method represents your address book or message store provider to MAPI and is used to distinguish entry identifiers that different providers create.</span></span> <span data-ttu-id="be530-119">Essa estrutura **MAPIUID** deve ser codificadas e não é obtida por meio de uma chamada para **NewUID**.</span><span class="sxs-lookup"><span data-stu-id="be530-119">This **MAPIUID** structure should be hard-coded and not obtained through a call to **NewUID**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="be530-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="be530-120">See also</span></span>



[<span data-ttu-id="be530-121">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="be530-121">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="be530-122">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="be530-122">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

