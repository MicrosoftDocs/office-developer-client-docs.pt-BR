---
title: PROP_ACCT_IS_EXCH
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 599bfc7d-7b62-7cc1-69ff-6db04c96a49b
description: True se a conta for uma conta do Exchange.
ms.openlocfilehash: db9f5ae46096d221ac3636a44f588c6a90ce146e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766045"
---
# <a name="propacctisexch"></a><span data-ttu-id="0e984-103">PROP_ACCT_IS_EXCH</span><span class="sxs-lookup"><span data-stu-id="0e984-103">PROP_ACCT_IS_EXCH</span></span>

<span data-ttu-id="0e984-104">True se a conta for uma conta do Exchange.</span><span class="sxs-lookup"><span data-stu-id="0e984-104">True if the account is an Exchange account.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0e984-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="0e984-105">Quick info</span></span>

<span data-ttu-id="0e984-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="0e984-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0e984-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0e984-107">Identifier:</span></span>  <br/> |<span data-ttu-id="0e984-108">0x0014</span><span class="sxs-lookup"><span data-stu-id="0e984-108">0x0014</span></span>  <br/> |
|<span data-ttu-id="0e984-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="0e984-109">Property type:</span></span>  <br/> |<span data-ttu-id="0e984-110">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0e984-110">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0e984-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="0e984-111">Property tag:</span></span>  <br/> |<span data-ttu-id="0e984-112">0x00140003</span><span class="sxs-lookup"><span data-stu-id="0e984-112">0x00140003</span></span>  <br/> |
|<span data-ttu-id="0e984-113">Access:</span><span class="sxs-lookup"><span data-stu-id="0e984-113">Access:</span></span>  <br/> |<span data-ttu-id="0e984-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0e984-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e984-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="0e984-115">Remarks</span></span>

<span data-ttu-id="0e984-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="0e984-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="0e984-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="0e984-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0e984-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e984-118">See also</span></span>

- [<span data-ttu-id="0e984-119">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="0e984-119">About the Account Management API</span></span>](about-the-account-management-api.md) 
- [<span data-ttu-id="0e984-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="0e984-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

