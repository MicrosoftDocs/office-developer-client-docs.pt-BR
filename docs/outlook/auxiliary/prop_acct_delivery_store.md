---
title: PROP_ACCT_DELIVERY_STORE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f5db43e9-687b-d467-1be1-3737e3f91c27
description: Representa a identificação de entrada do repositório de entrega padrão para a conta.
ms.openlocfilehash: 72c5325e70a6e8b42ee433d8d674c2b2ea0c8398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766048"
---
# <a name="propacctdeliverystore"></a><span data-ttu-id="cb7b8-103">PROP_ACCT_DELIVERY_STORE</span><span class="sxs-lookup"><span data-stu-id="cb7b8-103">PROP_ACCT_DELIVERY_STORE</span></span>

<span data-ttu-id="cb7b8-104">Representa a identificação de entrada do repositório de entrega padrão para a conta.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-104">Represents the Entry ID of the default delivery store for the account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb7b8-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="cb7b8-105">Quick info</span></span>

<span data-ttu-id="cb7b8-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="cb7b8-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cb7b8-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-107">Identifier:</span></span>  <br/> |<span data-ttu-id="cb7b8-108">0x0018</span><span class="sxs-lookup"><span data-stu-id="cb7b8-108">0x0018</span></span>  <br/> |
|<span data-ttu-id="cb7b8-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-109">Property type:</span></span>  <br/> |<span data-ttu-id="cb7b8-110">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="cb7b8-110">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="cb7b8-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-111">Property tag:</span></span>  <br/> |<span data-ttu-id="cb7b8-112">0x00180102</span><span class="sxs-lookup"><span data-stu-id="cb7b8-112">0x00180102</span></span>  <br/> |
|<span data-ttu-id="cb7b8-113">Access:</span><span class="sxs-lookup"><span data-stu-id="cb7b8-113">Access:</span></span>  <br/> |<span data-ttu-id="cb7b8-114">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="cb7b8-114">Read/write</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cb7b8-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="cb7b8-115">Remarks</span></span>

<span data-ttu-id="cb7b8-116">Obter ou definir essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md) ou [IOlkAccount::SetProp](iolkaccount-setprop.md), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-116">Get or set this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md) or [IOlkAccount::SetProp](iolkaccount-setprop.md), respectively.</span></span>
  
<span data-ttu-id="cb7b8-117">Um dos efeitos colaterais do definindo um repositório como repositório de entrega padrão para uma conta é que ao iniciar o Outlook, o Outlook cria as pastas de pesquisa para esse repositório se elas existirem e listar o repositório na barra de tarefas pendentes.</span><span class="sxs-lookup"><span data-stu-id="cb7b8-117">One of the side effects of setting a store as the default delivery store for an account is that when starting Outlook, Outlook creates search folders for that store if they do not already exist, and list the store in the To-Do Bar.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb7b8-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb7b8-118">See also</span></span>

- [<span data-ttu-id="cb7b8-119">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="cb7b8-119">About the Account Management API</span></span>](about-the-account-management-api.md)
- [<span data-ttu-id="cb7b8-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="cb7b8-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

