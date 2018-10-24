---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 357ace3267f22d751a20a12c96f108ee2f8ae1e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595199"
---
# <a name="tchar"></a><span data-ttu-id="5f11e-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="5f11e-103">TCHAR</span></span>

  
  
<span data-ttu-id="5f11e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5f11e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5f11e-105">Uma cadeia de caracteres Win32 que pode ser usada para descrever as cadeias de caracteres ANSI, Unicode ou DBCS.</span><span class="sxs-lookup"><span data-stu-id="5f11e-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="5f11e-106">Para plataformas ANSI e DBCS, TCHAR é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="5f11e-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="5f11e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f11e-107">Remarks</span></span>

<span data-ttu-id="5f11e-108">Plataformas de Unicode, TCHAR é definido como o tipo WCHAR um sinônimo.</span><span class="sxs-lookup"><span data-stu-id="5f11e-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="5f11e-109">Clientes MAPI podem usar o tipo de dados TCHAR para representar uma cadeia de caracteres de tipo de WCHAR ou char.</span><span class="sxs-lookup"><span data-stu-id="5f11e-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="5f11e-110">Certifique-se definir o UNICODE constante simbólico e limitar a plataforma quando for solicitado.</span><span class="sxs-lookup"><span data-stu-id="5f11e-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="5f11e-111">MAPI irá interpretar as informações de plataforma e internamente traduzir TCHAR para a cadeia de caracteres apropriada.</span><span class="sxs-lookup"><span data-stu-id="5f11e-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="5f11e-112">O tipo de propriedade MAPI, PT_TSTRING, funciona como o tipo de dados TCHAR.</span><span class="sxs-lookup"><span data-stu-id="5f11e-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="5f11e-113">Quando a plataforma oferece suporte a Unicode, propriedades do tipo PT_TSTRING recebem o tipo PT_UNICODE em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="5f11e-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="5f11e-114">Quando a plataforma não oferece suporte a Unicode, essas propriedades recebem o tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="5f11e-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="5f11e-115">Para obter mais informações sobre essa funcionalidade, consulte [Conjuntos de caracteres](mapi-character-sets.md) e a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="5f11e-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5f11e-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f11e-116">See also</span></span>



[<span data-ttu-id="5f11e-117">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="5f11e-117">MAPI Data Types</span></span>](mapi-data-types.md)

