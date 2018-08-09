---
title: SMAPIFormPropEnumVal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropEnumVal
api_type:
- COM
ms.assetid: 694d40e9-cff2-435e-ad90-446044c306d2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bae750e7e940bc1417b3d225c9c81129e9da77b4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770446"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="a327c-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="a327c-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="a327c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a327c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a327c-105">Mapeia um valor inteiro enumeradas para um nome de exibição para o valor.</span><span class="sxs-lookup"><span data-stu-id="a327c-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a327c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a327c-106">Header file:</span></span>  <br/> |<span data-ttu-id="a327c-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a327c-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="a327c-108">Members</span><span class="sxs-lookup"><span data-stu-id="a327c-108">Members</span></span>

 <span data-ttu-id="a327c-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="a327c-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="a327c-110">Cadeia de caracteres que contém o nome de exibição para o valor especificado no membro **nVal** .</span><span class="sxs-lookup"><span data-stu-id="a327c-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="a327c-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="a327c-111">**nVal**</span></span>
  
> <span data-ttu-id="a327c-112">Um valor de enumeração para o nome de exibição apontado pelo membro **pszDisplayName** .</span><span class="sxs-lookup"><span data-stu-id="a327c-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a327c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a327c-113">Remarks</span></span>

<span data-ttu-id="a327c-114">Quando o usuário seleciona um nome de exibição a partir de um formulário, o valor de enumeração correspondente do nome é armazenado usando a implementação de interface de [IMAPIProp](imapipropiunknown.md) que está associada ao formulário.</span><span class="sxs-lookup"><span data-stu-id="a327c-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a327c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a327c-115">See also</span></span>



[<span data-ttu-id="a327c-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="a327c-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="a327c-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="a327c-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="a327c-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="a327c-118">MAPI Structures</span></span>](mapi-structures.md)

