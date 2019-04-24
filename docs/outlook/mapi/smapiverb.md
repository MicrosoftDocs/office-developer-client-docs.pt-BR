---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309482"
---
# <a name="smapiverb"></a><span data-ttu-id="53b19-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="53b19-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="53b19-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53b19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53b19-105">Descreve um verbo MAPI.</span><span class="sxs-lookup"><span data-stu-id="53b19-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53b19-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="53b19-106">Header file:</span></span>  <br/> |<span data-ttu-id="53b19-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="53b19-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="53b19-108">Members</span><span class="sxs-lookup"><span data-stu-id="53b19-108">Members</span></span>

 <span data-ttu-id="53b19-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="53b19-109">**lVerb**</span></span>
  
> <span data-ttu-id="53b19-110">Código que representa o verbo que é passado para [IMAPIForm::D overb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="53b19-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="53b19-111">Os verbos padrão são definidos no arquivo de cabeçalho Exchform. h.</span><span class="sxs-lookup"><span data-stu-id="53b19-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="53b19-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="53b19-112">**szVerbname**</span></span>
  
> <span data-ttu-id="53b19-113">Exibe o nome do verbo como ele aparece no menu formulário.</span><span class="sxs-lookup"><span data-stu-id="53b19-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="53b19-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="53b19-114">**fuFlags**</span></span>
  
> <span data-ttu-id="53b19-115">Sinalizadores para o verbo.</span><span class="sxs-lookup"><span data-stu-id="53b19-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="53b19-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="53b19-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="53b19-117">Atributos do verbo.</span><span class="sxs-lookup"><span data-stu-id="53b19-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="53b19-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="53b19-118">**ulFlags**</span></span>
  
> <span data-ttu-id="53b19-119">Sinalizador que indica o formato do nome de exibição do verbo.</span><span class="sxs-lookup"><span data-stu-id="53b19-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="53b19-120">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="53b19-120">The following flag can be set:</span></span>
    
<span data-ttu-id="53b19-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="53b19-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="53b19-122">O nome para exibição está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="53b19-122">The display name is in Unicode format.</span></span> <span data-ttu-id="53b19-123">Se o sinalizador MAPI_UNICODE não estiver definido, o nome de exibição estará no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="53b19-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="53b19-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="53b19-124">Remarks</span></span>

<span data-ttu-id="53b19-125">A estrutura **SMAPIVerb** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="53b19-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="53b19-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="53b19-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="53b19-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="53b19-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="53b19-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="53b19-128">See also</span></span>



[<span data-ttu-id="53b19-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="53b19-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="53b19-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="53b19-130">MAPI Structures</span></span>](mapi-structures.md)

