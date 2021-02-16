---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa a ID de entrada do armazenamento de entrega padrão da conta.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418894"
---
# <a name="prop_acct_delivery_store"></a><span data-ttu-id="d452f-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="d452f-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="d452f-104">Representa a ID de entrada do armazenamento de entrega padrão da conta.</span><span class="sxs-lookup"><span data-stu-id="d452f-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d452f-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="d452f-105">Quick info</span></span>

<span data-ttu-id="d452f-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="d452f-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d452f-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d452f-107">Identifier:</span></span>  <br/> |<span data-ttu-id="d452f-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="d452f-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="d452f-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d452f-109">Property type:</span></span>  <br/> |<span data-ttu-id="d452f-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d452f-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d452f-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d452f-111">Property tag:</span></span>  <br/> |<span data-ttu-id="d452f-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="d452f-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="d452f-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="d452f-113">Access:</span></span>  <br/> |<span data-ttu-id="d452f-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="d452f-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d452f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d452f-115">Remarks</span></span>

<span data-ttu-id="d452f-116">Obter ou definir essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d452f-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="d452f-117">Um dos efeitos colaterais da configuração de um armazenamento como o armazenamento de entrega padrão para uma conta é que, ao iniciar o Outlook, o Outlook cria pastas de pesquisa para esse armazenamento, caso ainda não existam, e lista o armazenamento na barra de To-Do.</span><span class="sxs-lookup"><span data-stu-id="d452f-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d452f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="d452f-118">See also</span></span>

- [<span data-ttu-id="d452f-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="d452f-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="d452f-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="d452f-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

