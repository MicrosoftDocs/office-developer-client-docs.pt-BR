---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Retorna o accountsendstamp.
ms.openlocfilehash: 948855f32ecd83334e2ab2af0926fedb0e6d7f84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766049"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="2e148-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="2e148-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="2e148-104">Retorna o carimbo de conta "Enviar".</span><span class="sxs-lookup"><span data-stu-id="2e148-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="2e148-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="2e148-105">Quick info</span></span>

<span data-ttu-id="2e148-106">Consulte [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="2e148-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e148-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="2e148-107">Identifier:</span></span>  <br/> |<span data-ttu-id="2e148-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="2e148-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="2e148-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="2e148-109">Property type:</span></span>  <br/> |<span data-ttu-id="2e148-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2e148-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="2e148-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="2e148-111">Property tag:</span></span>  <br/> |<span data-ttu-id="2e148-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="2e148-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="2e148-113">Access:</span><span class="sxs-lookup"><span data-stu-id="2e148-113">Access:</span></span>  <br/> |<span data-ttu-id="2e148-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e148-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e148-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2e148-115">Remarks</span></span>

<span data-ttu-id="2e148-116">Obtenha essa propriedade usando [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="2e148-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="2e148-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="2e148-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e148-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e148-118">See also</span></span>

- [<span data-ttu-id="2e148-119">Sobre a API de gerenciamento de conta</span><span class="sxs-lookup"><span data-stu-id="2e148-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="2e148-120">Constantes (API de gerenciamento de conta)</span><span class="sxs-lookup"><span data-stu-id="2e148-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

