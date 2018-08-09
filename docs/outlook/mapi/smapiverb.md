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
ms.openlocfilehash: 4d060d62deb685b4691846c2b8e48a82ae3195ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770468"
---
# <a name="smapiverb"></a><span data-ttu-id="38227-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="38227-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="38227-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="38227-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="38227-105">Descreve um verbo MAPI.</span><span class="sxs-lookup"><span data-stu-id="38227-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38227-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="38227-106">Header file:</span></span>  <br/> |<span data-ttu-id="38227-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="38227-107">Mapiform.h</span></span>  <br/> |
   
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

## <a name="members"></a><span data-ttu-id="38227-108">Members</span><span class="sxs-lookup"><span data-stu-id="38227-108">Members</span></span>

 <span data-ttu-id="38227-109">**lVerb**</span><span class="sxs-lookup"><span data-stu-id="38227-109">**lVerb**</span></span>
  
> <span data-ttu-id="38227-110">Código que representa o verbo que é passado para [IMAPIForm::DoVerb](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="38227-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="38227-111">Verbos padrão são definidos no arquivo de cabeçalho Exchform.h.</span><span class="sxs-lookup"><span data-stu-id="38227-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="38227-112">**szVerbname**</span><span class="sxs-lookup"><span data-stu-id="38227-112">**szVerbname**</span></span>
  
> <span data-ttu-id="38227-113">Nome para exibição do verbo como ele aparece no menu formulário.</span><span class="sxs-lookup"><span data-stu-id="38227-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="38227-114">**fuFlags**</span><span class="sxs-lookup"><span data-stu-id="38227-114">**fuFlags**</span></span>
  
> <span data-ttu-id="38227-115">Sinalizadores para o verbo.</span><span class="sxs-lookup"><span data-stu-id="38227-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="38227-116">**grfAttribs**</span><span class="sxs-lookup"><span data-stu-id="38227-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="38227-117">Atributos do verbo.</span><span class="sxs-lookup"><span data-stu-id="38227-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="38227-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="38227-118">**ulFlags**</span></span>
  
> <span data-ttu-id="38227-119">Sinalizador que indica o formato de nome para exibição da verbo.</span><span class="sxs-lookup"><span data-stu-id="38227-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="38227-120">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="38227-120">The following flag can be set:</span></span>
    
<span data-ttu-id="38227-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="38227-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="38227-122">O nome de exibição está no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="38227-122">The display name is in Unicode format.</span></span> <span data-ttu-id="38227-123">Se o sinalizador MAPI_UNICODE não estiver definido, o nome de exibição é no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="38227-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="38227-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="38227-124">Remarks</span></span>

<span data-ttu-id="38227-125">A estrutura **SMAPIVerb** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="38227-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="38227-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="38227-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="38227-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="38227-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="38227-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="38227-128">See also</span></span>



[<span data-ttu-id="38227-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="38227-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="38227-130">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="38227-130">MAPI Structures</span></span>](mapi-structures.md)

