---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa a identificação de entrada do repositório de entrega padrão para a conta.
ms.openlocfilehash: d803c539ec99da4d7fb31063f48237788f3ac3d9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327668"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="8b73a-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="8b73a-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="8b73a-104">Representa a identificação de entrada do repositório de entrega padrão para a conta.</span><span class="sxs-lookup"><span data-stu-id="8b73a-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8b73a-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8b73a-105">Quick info</span></span>

<span data-ttu-id="8b73a-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8b73a-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8b73a-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8b73a-107">Identifier:</span></span>  <br/> |<span data-ttu-id="8b73a-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="8b73a-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="8b73a-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8b73a-109">Property type:</span></span>  <br/> |<span data-ttu-id="8b73a-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8b73a-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8b73a-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8b73a-111">Property tag:</span></span>  <br/> |<span data-ttu-id="8b73a-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="8b73a-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="8b73a-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="8b73a-113">Access:</span></span>  <br/> |<span data-ttu-id="8b73a-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="8b73a-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8b73a-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b73a-115">Remarks</span></span>

<span data-ttu-id="8b73a-116">Obter ou definir essa propriedade usando [IOlkAccount:: GetProp](iolkaccount-getprop.md) ou [IOlkAccount:: SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8b73a-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="8b73a-117">Um dos efeitos colaterais da configuração de um repositório como o repositório de entrega padrão para uma conta é que, ao iniciar o Outlook, o Outlook cria pastas de pesquisa para esse repositório, caso ainda não existam, e liste o repositório na barra de tarefas pendentes.</span><span class="sxs-lookup"><span data-stu-id="8b73a-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8b73a-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b73a-118">See also</span></span>

- [<span data-ttu-id="8b73a-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="8b73a-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="8b73a-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="8b73a-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

