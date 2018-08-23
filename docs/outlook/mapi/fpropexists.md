---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d016c83678d9c1c94ee4ad4b8e12723c03f7bda
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570433"
---
# <a name="fpropexists"></a><span data-ttu-id="0bf1d-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="0bf1d-103">FPropExists</span></span>

  
  
<span data-ttu-id="0bf1d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0bf1d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0bf1d-105">Procura uma marca de propriedade fornecida em uma interface de [IMAPIProp](imapipropiunknown.md) ou um derivado do **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="0bf1d-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0bf1d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0bf1d-106">Header file:</span></span>  <br/> |<span data-ttu-id="0bf1d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0bf1d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0bf1d-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0bf1d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0bf1d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0bf1d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0bf1d-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0bf1d-110">Called by:</span></span>  <br/> |<span data-ttu-id="0bf1d-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0bf1d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="0bf1d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0bf1d-112">Parameters</span></span>

 <span data-ttu-id="0bf1d-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="0bf1d-113">_pobj_</span></span>
  
> <span data-ttu-id="0bf1d-114">[in] Ponteiro para a interface **IMAPIProp** ou derivados **IMAPIProp** dentro do qual procurar a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="0bf1d-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="0bf1d-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="0bf1d-116">[in] Marca de propriedade a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0bf1d-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0bf1d-117">Return value</span></span>

<span data-ttu-id="0bf1d-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="0bf1d-118">TRUE</span></span> 
  
> <span data-ttu-id="0bf1d-119">Foi encontrada uma correspondência para a marca de propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="0bf1d-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="0bf1d-120">FALSE</span></span> 
  
> <span data-ttu-id="0bf1d-121">Não foi encontrada uma correspondência para a marca de propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0bf1d-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0bf1d-122">Remarks</span></span>

<span data-ttu-id="0bf1d-123">Se a marca de propriedade no parâmetro _ulPropTag_ tiver tipo PT_UNSPECIFIED, a função **FPropExists** procura por uma correspondência com base apenas no identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="0bf1d-124">Caso contrário, a correspondência diferencia para a marca de propriedade inteira, incluindo o tipo.</span><span class="sxs-lookup"><span data-stu-id="0bf1d-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

