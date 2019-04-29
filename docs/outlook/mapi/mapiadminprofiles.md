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
ms.openlocfilehash: e5043a614ccd94994fe86838f15aa1a43f22733e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412349"
---
# <a name="mapiadminprofiles"></a><span data-ttu-id="d150e-103">MAPIAdminProfiles</span><span class="sxs-lookup"><span data-stu-id="d150e-103">MAPIAdminProfiles</span></span>

  
  
<span data-ttu-id="d150e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d150e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d150e-105">Cria um objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="d150e-105">Creates a profile administration object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d150e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d150e-106">Header file:</span></span>  <br/> |<span data-ttu-id="d150e-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="d150e-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="d150e-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="d150e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d150e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d150e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d150e-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="d150e-110">Called by:</span></span>  <br/> |<span data-ttu-id="d150e-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="d150e-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT MAPIAdminProfiles(
  ULONG ulFlags,
  LPPROFADMIN FAR * lppProfAdmin
);
```

## <a name="parameters"></a><span data-ttu-id="d150e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d150e-112">Parameters</span></span>

 <span data-ttu-id="d150e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d150e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="d150e-114">no Bitmask de sinalizadores que indicam opções para a função de entrada de serviço.</span><span class="sxs-lookup"><span data-stu-id="d150e-114">[in] Bitmask of flags indicating options for the service entry function.</span></span> 
    
 <span data-ttu-id="d150e-115">_lppProfAdmin_</span><span class="sxs-lookup"><span data-stu-id="d150e-115">_lppProfAdmin_</span></span>
  
> <span data-ttu-id="d150e-116">bota Ponteiro para um ponteiro para o novo objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="d150e-116">[out] Pointer to a pointer to the new profile administration object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d150e-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d150e-117">Return value</span></span>

<span data-ttu-id="d150e-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d150e-118">S_OK</span></span> 
  
> <span data-ttu-id="d150e-119">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d150e-119">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="d150e-120">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d150e-120">MFCMAPI reference</span></span>

<span data-ttu-id="d150e-121">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d150e-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d150e-122">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="d150e-122">**File**</span></span>|<span data-ttu-id="d150e-123">**Função**</span><span class="sxs-lookup"><span data-stu-id="d150e-123">**Function**</span></span>|<span data-ttu-id="d150e-124">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="d150e-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d150e-125">MAPIObjects. cpp</span><span class="sxs-lookup"><span data-stu-id="d150e-125">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="d150e-126">CMapiObjects:: GetProfAdmin</span><span class="sxs-lookup"><span data-stu-id="d150e-126">CMapiObjects::GetProfAdmin</span></span>  <br/> |<span data-ttu-id="d150e-127">MFCMAPI usa o método **MAPIAdminProfiles** para obter o objeto de administração de perfil.</span><span class="sxs-lookup"><span data-stu-id="d150e-127">MFCMAPI uses the **MAPIAdminProfiles** method to get the profile administration object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d150e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="d150e-128">See also</span></span>



[<span data-ttu-id="d150e-129">IProfAdmin::CreateProfile</span><span class="sxs-lookup"><span data-stu-id="d150e-129">IProfAdmin::CreateProfile</span></span>](iprofadmin-createprofile.md)


[<span data-ttu-id="d150e-130">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="d150e-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

