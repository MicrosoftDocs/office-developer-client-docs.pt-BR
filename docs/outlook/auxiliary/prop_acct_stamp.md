---
title: PROP_ACCT_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70b6ecc8-6be3-0f05-3291-ac5b7f2ecfdb
description: Retorna o carimbo da conta.
ms.openlocfilehash: ec1824d8c8c61d392b4e11cdb5213a85100d971e
ms.sourcegitcommit: c55eec212ae794592c83bbf06b01eab5ca6bff6d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/25/2018
ms.locfileid: "19766068"
---
# <a name="propacctstamp"></a><span data-ttu-id="8dd34-103">PROP_ACCT_STAMP</span><span class="sxs-lookup"><span data-stu-id="8dd34-103">PROP_ACCT_STAMP</span></span>

<span data-ttu-id="8dd34-104">Retorna o carimbo da conta.</span><span class="sxs-lookup"><span data-stu-id="8dd34-104">Returns the account stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8dd34-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="8dd34-105">Quick info</span></span>

<span data-ttu-id="8dd34-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="8dd34-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8dd34-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8dd34-107">Identifier:</span></span>  <br/> |<span data-ttu-id="8dd34-108">0x000D</span><span class="sxs-lookup"><span data-stu-id="8dd34-108">0x000D</span></span>  <br/> |
|<span data-ttu-id="8dd34-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8dd34-109">Property type:</span></span>  <br/> |<span data-ttu-id="8dd34-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8dd34-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="8dd34-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="8dd34-111">Property tag:</span></span>  <br/> |<span data-ttu-id="8dd34-112">0x000D001F</span><span class="sxs-lookup"><span data-stu-id="8dd34-112">0x000D001F</span></span>  <br/> |
|<span data-ttu-id="8dd34-113">Access:</span><span class="sxs-lookup"><span data-stu-id="8dd34-113">Access:</span></span>  <br/> |<span data-ttu-id="8dd34-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="8dd34-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8dd34-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="8dd34-115">Remarks</span></span>

<span data-ttu-id="8dd34-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="8dd34-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="8dd34-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="8dd34-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8dd34-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="8dd34-118">See also</span></span>

- [<span data-ttu-id="8dd34-119">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="8dd34-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="8dd34-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="8dd34-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

