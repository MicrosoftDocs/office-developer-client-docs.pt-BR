---
title: PROP_ACCT_SEND_STAMP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b86242f3-dfd7-398e-a054-93db85b69752
description: Retorna o accountsendstamp.
ms.openlocfilehash: d860a117e4ab5470f84ff1807cb6246cd852d24b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327605"
---
# <a name="propacctsendstamp"></a><span data-ttu-id="a9db2-103">PROP_ACCT_SEND_STAMP</span><span class="sxs-lookup"><span data-stu-id="a9db2-103">PROP_ACCT_SEND_STAMP</span></span>

<span data-ttu-id="a9db2-104">Retorna o carimbo "enviar" da conta.</span><span class="sxs-lookup"><span data-stu-id="a9db2-104">Returns the account "send" stamp.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a9db2-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="a9db2-105">Quick info</span></span>

<span data-ttu-id="a9db2-106">Confira [IOlkAccount](iolkaccount.md).</span><span class="sxs-lookup"><span data-stu-id="a9db2-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a9db2-107">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a9db2-107">Identifier:</span></span>  <br/> |<span data-ttu-id="a9db2-108">0x000E</span><span class="sxs-lookup"><span data-stu-id="a9db2-108">0x000E</span></span>  <br/> |
|<span data-ttu-id="a9db2-109">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a9db2-109">Property type:</span></span>  <br/> |<span data-ttu-id="a9db2-110">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a9db2-110">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a9db2-111">Marca de propriedade:</span><span class="sxs-lookup"><span data-stu-id="a9db2-111">Property tag:</span></span>  <br/> |<span data-ttu-id="a9db2-112">0x000E001F</span><span class="sxs-lookup"><span data-stu-id="a9db2-112">0x000E001F</span></span>  <br/> |
|<span data-ttu-id="a9db2-113">Acesso:</span><span class="sxs-lookup"><span data-stu-id="a9db2-113">Access:</span></span>  <br/> |<span data-ttu-id="a9db2-114">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9db2-114">Read-only</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9db2-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9db2-115">Remarks</span></span>

<span data-ttu-id="a9db2-116">Use essa propriedade por meio [IOlkAccount::GetProp](iolkaccount-getprop.md).</span><span class="sxs-lookup"><span data-stu-id="a9db2-116">Get this property by using [IOlkAccount::GetProp](iolkaccount-getprop.md).</span></span> <span data-ttu-id="a9db2-117">Se o cliente tentar definir essa propriedade, essa propriedade retornará **E_OLK_PROP_READ_ONLY**.</span><span class="sxs-lookup"><span data-stu-id="a9db2-117">If the client attempts to set this property, this property returns **E_OLK_PROP_READ_ONLY**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a9db2-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9db2-118">See also</span></span>

- [<span data-ttu-id="a9db2-119">Sobre a API de gerenciamento de contas</span><span class="sxs-lookup"><span data-stu-id="a9db2-119">About the Account Management API</span></span>](about-the-account-management-api.md)  
- [<span data-ttu-id="a9db2-120">Constantes (API de gerenciamento de contas)</span><span class="sxs-lookup"><span data-stu-id="a9db2-120">Constants (Account management API)</span></span>](constants-account-management-api.md)

