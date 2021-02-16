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
ms.openlocfilehash: 353bc574ca5987d71faf4841744de30a3d6c3f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435408"
---
# <a name="smapiformpropenumval"></a><span data-ttu-id="89ca0-103">SMAPIFormPropEnumVal</span><span class="sxs-lookup"><span data-stu-id="89ca0-103">SMAPIFormPropEnumVal</span></span>

  
  
<span data-ttu-id="89ca0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89ca0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89ca0-105">Mapeia um valor inteiro enumerado para um nome de exibição para esse valor.</span><span class="sxs-lookup"><span data-stu-id="89ca0-105">Maps an enumerated integer value to a display name for that value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="89ca0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="89ca0-106">Header file:</span></span>  <br/> |<span data-ttu-id="89ca0-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="89ca0-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct _SMAPIFormPropEnumVal
{
  LPSTR pszDisplayName;
  ULONG nVal;
} SMAPIFormPropEnumVal;

```

## <a name="members"></a><span data-ttu-id="89ca0-108">Members</span><span class="sxs-lookup"><span data-stu-id="89ca0-108">Members</span></span>

 <span data-ttu-id="89ca0-109">**pszDisplayName**</span><span class="sxs-lookup"><span data-stu-id="89ca0-109">**pszDisplayName**</span></span>
  
> <span data-ttu-id="89ca0-110">Cadeia de caracteres que contém o nome para exibição do valor especificado no **membro nVal.**</span><span class="sxs-lookup"><span data-stu-id="89ca0-110">String that contains the display name for the value specified in the **nVal** member.</span></span> 
    
 <span data-ttu-id="89ca0-111">**nVal**</span><span class="sxs-lookup"><span data-stu-id="89ca0-111">**nVal**</span></span>
  
> <span data-ttu-id="89ca0-112">Um valor de enumeração para o nome de exibição apontado pelo **membro pszDisplayName.**</span><span class="sxs-lookup"><span data-stu-id="89ca0-112">An enumeration value for the display name pointed to by the **pszDisplayName** member.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="89ca0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="89ca0-113">Remarks</span></span>

<span data-ttu-id="89ca0-114">Quando um usuário seleciona um nome de exibição de um formulário, o valor de enumeração correspondente do nome é armazenado usando a implementação da interface [IMAPIProp](imapipropiunknown.md) associada ao formulário.</span><span class="sxs-lookup"><span data-stu-id="89ca0-114">When a user selects a display name from a form, the name's corresponding enumeration value is stored by using the [IMAPIProp](imapipropiunknown.md) interface implementation that is associated with the form.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="89ca0-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="89ca0-115">See also</span></span>



[<span data-ttu-id="89ca0-116">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="89ca0-116">SMAPIFormProp</span></span>](smapiformprop.md)
  
[<span data-ttu-id="89ca0-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="89ca0-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="89ca0-118">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="89ca0-118">MAPI Structures</span></span>](mapi-structures.md)

