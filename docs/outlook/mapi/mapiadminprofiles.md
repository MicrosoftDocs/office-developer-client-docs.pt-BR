---
title: MAPIAdminProfiles
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAdminProfiles
api_type:
- HeaderDef
ms.assetid: 82a9e379-39e4-4257-8cba-a6758f431cdc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3cd1a19b23a3c4d3ff8a297881eb2b959585eb17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767988"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="38db3-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="38db3-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="38db3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38db3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38db3-105">Cria um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="38db3-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38db3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="38db3-106">Header file:</span></span>  <br/> |<span data-ttu-id="38db3-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="38db3-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="38db3-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="38db3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="38db3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="38db3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="38db3-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="38db3-110">Called by:</span></span>  <br/> |<span data-ttu-id="38db3-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="38db3-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="38db3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="38db3-112">Parameters</span></span>

 <span data-ttu-id="38db3-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="38db3-113">_ulFlags_</span></span>
  
> <span data-ttu-id="38db3-114">[in] Bitmask dos sinalizadores indicando opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="38db3-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="38db3-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="38db3-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="38db3-116">[out] Ponteiro para um ponteiro para o novo objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="38db3-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="38db3-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="38db3-117">Return value</span></span>

<span data-ttu-id="38db3-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="38db3-118">S_OK</span></span> 
  
> <span data-ttu-id="38db3-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="38db3-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="38db3-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="38db3-120">MFCMAPI reference</span></span>

<span data-ttu-id="38db3-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="38db3-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="38db3-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="38db3-122">**File**</span></span>|<span data-ttu-id="38db3-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="38db3-123">**Function**</span></span>|<span data-ttu-id="38db3-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="38db3-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38db3-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="38db3-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="38db3-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="38db3-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="38db3-127">MFCMAPI usa o método **MAPIAdminProfiles** para obter o objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="38db3-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="38db3-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="38db3-128">See also</span></span>



[<span data-ttu-id="38db3-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="38db3-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="38db3-130">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="38db3-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

