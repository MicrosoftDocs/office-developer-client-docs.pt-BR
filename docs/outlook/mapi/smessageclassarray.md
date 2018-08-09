---
title: SMessageClassArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMessageClassArray
api_type:
- COM
ms.assetid: 05f8c191-db2b-4174-8b3c-a9fdabfe6ac8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 01563e3655d42abc62ea88a12f2878e5d81129d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770467"
---
# <a name="smessageclassarray"></a><span data-ttu-id="78d7b-103">SMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="78d7b-103">SMessageClassArray</span></span>

  
  
<span data-ttu-id="78d7b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="78d7b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="78d7b-105">Contém uma matriz de ponteiros para cadeias de caracteres de classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="78d7b-105">Contains an array of pointers to message class strings.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="78d7b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="78d7b-106">Header file:</span></span>  <br/> |<span data-ttu-id="78d7b-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="78d7b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="78d7b-108">Macro relacionada:</span><span class="sxs-lookup"><span data-stu-id="78d7b-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="78d7b-109">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="78d7b-109">CbMessageClassArray</span></span>](cbmessageclassarray.md) <br/> |
   
```cpp
typedef struct 
{
  ULONG cValues;
  LPCSTR aMessageClass[MAPI_DIM];
} SMessageClassArray, FAR * LPSMESSAGECLASSARRAY;

```

## <a name="members"></a><span data-ttu-id="78d7b-110">Members</span><span class="sxs-lookup"><span data-stu-id="78d7b-110">Members</span></span>

 <span data-ttu-id="78d7b-111">**cValues**</span><span class="sxs-lookup"><span data-stu-id="78d7b-111">**cValues**</span></span>
  
> <span data-ttu-id="78d7b-112">Contagem de ponteiros de cadeia de caracteres de classe de mensagem na matriz.</span><span class="sxs-lookup"><span data-stu-id="78d7b-112">Count of message class string pointers in the array.</span></span>
    
 <span data-ttu-id="78d7b-113">**aMessageClass**</span><span class="sxs-lookup"><span data-stu-id="78d7b-113">**aMessageClass**</span></span>
  
> <span data-ttu-id="78d7b-114">Matriz de ponteiros para cadeias de caracteres de classe de mensagem.</span><span class="sxs-lookup"><span data-stu-id="78d7b-114">Array of pointers to message class strings.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78d7b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="78d7b-115">Remarks</span></span>

<span data-ttu-id="78d7b-116">A estrutura **SMessageClassArray** é passada como um parâmetro nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="78d7b-116">The **SMessageClassArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="78d7b-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="78d7b-117">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="78d7b-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="78d7b-118">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="78d7b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="78d7b-119">See also</span></span>



[<span data-ttu-id="78d7b-120">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="78d7b-120">MAPI Structures</span></span>](mapi-structures.md)

