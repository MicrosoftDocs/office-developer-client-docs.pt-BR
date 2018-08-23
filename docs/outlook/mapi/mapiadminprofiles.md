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
ms.openlocfilehash: 843eed06f30dcca530cf4306c9e03bbffbb05af5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581283"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="4c113-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="4c113-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="4c113-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c113-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c113-105">Cria um objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="4c113-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c113-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4c113-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c113-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="4c113-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="4c113-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4c113-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c113-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c113-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c113-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4c113-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c113-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="4c113-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="4c113-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c113-112">Parameters</span></span>

 <span data-ttu-id="4c113-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4c113-113">_ulFlags_</span></span>
  
> <span data-ttu-id="4c113-114">[in] Bitmask dos sinalizadores indicando opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="4c113-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="4c113-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="4c113-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="4c113-116">[out] Ponteiro para um ponteiro para o novo objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="4c113-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4c113-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4c113-117">Return value</span></span>

<span data-ttu-id="4c113-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="4c113-118">S_OK</span></span> 
  
> <span data-ttu-id="4c113-119">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="4c113-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="4c113-120">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="4c113-120">MFCMAPI reference</span></span>

<span data-ttu-id="4c113-121">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="4c113-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4c113-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="4c113-122">**File**</span></span>|<span data-ttu-id="4c113-123">**Function**</span><span class="sxs-lookup"><span data-stu-id="4c113-123">**Function**</span></span>|<span data-ttu-id="4c113-124">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4c113-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4c113-125">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="4c113-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="4c113-126">CMapiObjects::GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="4c113-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="4c113-127">MFCMAPI usa o método **MAPIAdminProfiles** para obter o objeto de administração do perfil.</span><span class="sxs-lookup"><span data-stu-id="4c113-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4c113-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="4c113-128">See also</span></span>



[<span data-ttu-id="4c113-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="4c113-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="4c113-130">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="4c113-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

