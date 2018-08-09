---
title: HrCreateNewWrappedObject
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 780ade1c-88d0-04d2-ba7e-251c19c43438
description: Cria um objeto que um cliente pode acessar em um formato de caracteres preferencial.
ms.openlocfilehash: 187bcbce8fd1170e05f57c5c9147a8962669fea4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765811"
---
# <a name="hrcreatenewwrappedobject"></a><span data-ttu-id="92794-103">HrCreateNewWrappedObject</span><span class="sxs-lookup"><span data-stu-id="92794-103">HrCreateNewWrappedObject</span></span>

<span data-ttu-id="92794-104">Cria um objeto que um cliente pode acessar em um formato de caracteres preferencial.</span><span class="sxs-lookup"><span data-stu-id="92794-104">Creates an object that a client can access in a preferred character format.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="92794-105">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="92794-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92794-106">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="92794-106">Exported by:</span></span>  <br/> |<span data-ttu-id="92794-107">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="92794-107">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="92794-108">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="92794-108">Called by:</span></span>  <br/> |<span data-ttu-id="92794-109">Cliente</span><span class="sxs-lookup"><span data-stu-id="92794-109">Client</span></span>  <br/> |
|<span data-ttu-id="92794-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="92794-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="92794-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="92794-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrCreateNewWrappedObject( 
    LPVOID        pvUnwrapped, 
    ULONG         ulUnwrappedFlags, 
    ULONG         ulWrappedFlags, 
    const IID     *pIID, 
    const ULONG   *pulReserved, 
    BOOL          fCheckWrap, 
    LPVOID       *ppvWrapped 
);

```

## <a name="parameters"></a><span data-ttu-id="92794-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92794-112">Parameters</span></span>

<span data-ttu-id="92794-113">_pvUnwrapped_</span><span class="sxs-lookup"><span data-stu-id="92794-113">_pvUnwrapped_</span></span>
  
> <span data-ttu-id="92794-114">[in] O objeto do Outlook desfeito inicial.</span><span class="sxs-lookup"><span data-stu-id="92794-114">[in] The initial unwrapped Outlook object.</span></span> <span data-ttu-id="92794-115">Deve implementar uma das seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="92794-115">Must implement one of the following interfaces:</span></span>
    
   - <span data-ttu-id="92794-116">[IMailUser: IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder: IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage: IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore: IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon: IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), ou [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="92794-116">[IMailUser : IMAPIProp](http://msdn.microsoft.com/library/74c25870-62d9-484a-9a99-4dc35c52479e%28Office.15%29.aspx), [IMAPIFolder : IMAPIContainer](http://msdn.microsoft.com/library/bc2e8d17-7687-43c2-8f01-b677703f7288%28Office.15%29.aspx), [IMessage : IMAPIProp](http://msdn.microsoft.com/library/7e244d40-595e-432c-aa8c-f9f62ca3c138%28Office.15%29.aspx), [IMsgStore : IMAPIProp](http://msdn.microsoft.com/library/20090114-b183-4767-8971-a304a9aa47e6%28Office.15%29.aspx), [IMSLogon : IUnknown](http://msdn.microsoft.com/library/d87093dc-f705-465f-ab3c-944ca0cd3e54%28Office.15%29.aspx), or [IOSTX](http://msdn.microsoft.com/library/f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f%28Office.15%29.aspx).</span></span>
    
<span data-ttu-id="92794-117">_ulUnwrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="92794-117">_ulUnwrappedFlags_</span></span>
  
> <span data-ttu-id="92794-118">[in] Sinalizadores que caracterizam o objeto inicial desfeito.</span><span class="sxs-lookup"><span data-stu-id="92794-118">[in] Flags that characterize the unwrapped initial object.</span></span> <span data-ttu-id="92794-119">Deve ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92794-119">Must be one or more of the following values:</span></span>
    
   - <span data-ttu-id="92794-120">DDLWRAP_FLAG_ANSI — o objeto de Unwrapped é ANSI.</span><span class="sxs-lookup"><span data-stu-id="92794-120">DDLWRAP_FLAG_ANSI—Unwrapped object is ANSI.</span></span>
    
   - <span data-ttu-id="92794-121">DDLWRAP_FLAG_UNICODE — o objeto de Unwrapped é UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92794-121">DDLWRAP_FLAG_UNICODE—Unwrapped object is UNICODE.</span></span>
    
<span data-ttu-id="92794-122">_ulWrappedFlags_</span><span class="sxs-lookup"><span data-stu-id="92794-122">_ulWrappedFlags_</span></span>
  
>  <span data-ttu-id="92794-123">[in] Sinalizadores para o formato de caracteres preferencial.</span><span class="sxs-lookup"><span data-stu-id="92794-123">[in] Flags for the preferred character format.</span></span> <span data-ttu-id="92794-124">Deve ser um ou mais dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="92794-124">Must be one or more of the following values:</span></span> 
    
   - <span data-ttu-id="92794-125">DDLWRAP_FLAG_ANSI — objeto Wrapped será exposto como ANSI.</span><span class="sxs-lookup"><span data-stu-id="92794-125">DDLWRAP_FLAG_ANSI—Wrapped object will be exposed as ANSI.</span></span>
    
   - <span data-ttu-id="92794-126">DDLWRAP_FLAG_UNICODE — objeto Wrapped será exposto como UNICODE.</span><span class="sxs-lookup"><span data-stu-id="92794-126">DDLWRAP_FLAG_UNICODE—Wrapped object will be exposed as UNICODE.</span></span>
    
<span data-ttu-id="92794-127">_pIID_</span><span class="sxs-lookup"><span data-stu-id="92794-127">_pIID_</span></span>
  
>  <span data-ttu-id="92794-128">[in] O identificador da interface suportado pelo objeto desfeito; Defina-la como NULL se isso for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="92794-128">[in] The identifier of the interface supported by the unwrapped object; set it to NULL if this is unknown.</span></span> 
    
<span data-ttu-id="92794-129">_pulReserved_</span><span class="sxs-lookup"><span data-stu-id="92794-129">_pulReserved_</span></span>
  
>  <span data-ttu-id="92794-130">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="92794-130">[in] This parameter is not used.</span></span> <span data-ttu-id="92794-131">Ela deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="92794-131">It must be NULL.</span></span> 
    
<span data-ttu-id="92794-132">_fCheckWrap_</span><span class="sxs-lookup"><span data-stu-id="92794-132">_fCheckWrap_</span></span>
  
>  <span data-ttu-id="92794-133">[in] Defina este parâmetro como **true** se _pvUnwrapped_ devem ser verificadas para seu formato de disposição; Defina-a **false** se o objeto deve ser quebrado sem verificação.</span><span class="sxs-lookup"><span data-stu-id="92794-133">[in] Set this parameter to **true** if  _pvUnwrapped_ should be checked for its format before wrapping; set it to **false** if the object should be wrapped without checking.</span></span> 
    
<span data-ttu-id="92794-134">_ppvWrapped_</span><span class="sxs-lookup"><span data-stu-id="92794-134">_ppvWrapped_</span></span>
  
>  <span data-ttu-id="92794-135">[out] Um ponteiro para o objeto solicitado, quebrado automaticamente no formato de caractere solicitada.</span><span class="sxs-lookup"><span data-stu-id="92794-135">[out] A pointer to the requested object, wrapped in the requested character format.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="92794-136">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="92794-136">Return values</span></span>

<span data-ttu-id="92794-137">S_OK se a chamada foi bem-sucedida; Caso contrário, um código de erro.</span><span class="sxs-lookup"><span data-stu-id="92794-137">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92794-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="92794-138">Remarks</span></span>

<span data-ttu-id="92794-139">Passagem em um objeto com quebra com _fCheckWrap_ definido como **true** resultará em um objeto desfeito.</span><span class="sxs-lookup"><span data-stu-id="92794-139">Passing in a wrapped object with  _fCheckWrap_ set to **true** will result in an unwrapped object.</span></span> <span data-ttu-id="92794-140">Independentemente de estarem ou não o objeto retornado é disposto, o cliente é responsável por liberando a referência de objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="92794-140">Regardless of whether or not the returned object is wrapped, the client is responsible for releasing the reference on the returned object.</span></span> 
  
<span data-ttu-id="92794-141">Ao usar o **GetProcAddress** para procurar o endereço desta função no Msmapi32, especifique **HrCreateNewWrappedObject@28** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="92794-141">When using **GetProcAddress** to look for the address of this function in msmapi32.dll, specify **HrCreateNewWrappedObject@28** as the procedure name.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92794-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="92794-142">See also</span></span>

- [<span data-ttu-id="92794-143">Sobre a camada de redução de dados API</span><span class="sxs-lookup"><span data-stu-id="92794-143">About the Data Degradation Layer API</span></span>](about-the-data-degradation-layer-api.md)
- [<span data-ttu-id="92794-144">Constantes (camada de dados degradação API)</span><span class="sxs-lookup"><span data-stu-id="92794-144">Constants (Data degradation layer API)</span></span>](constants-data-degradation-layer-api.md)

