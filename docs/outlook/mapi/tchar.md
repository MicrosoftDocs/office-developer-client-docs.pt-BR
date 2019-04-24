---
title: TCHAR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
api_name:
- MAPI.TCHAR
api_type:
- COM
ms.assetid: 7a92060b-4c30-4eba-993f-36f5f9231a4b
description: 'Última modificação: 23 de julho de 2011'
localization_priority: Priority
ms.openlocfilehash: 2b04ebe6d05cd72a59fe6d44c9138468fd7ddec1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269990"
---
# <a name="tchar"></a><span data-ttu-id="8b0ab-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="8b0ab-103">TCHAR</span></span>

  
  
<span data-ttu-id="8b0ab-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b0ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b0ab-105">Uma cadeia de caracteres do Win32 que pode ser usada para descrever cadeias de caracteres ANSI, DBCS ou Unicode.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="8b0ab-106">Para plataformas ANSI e DBCS, o TCHAR é definido da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="8b0ab-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="8b0ab-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b0ab-107">Remarks</span></span>

<span data-ttu-id="8b0ab-108">Para plataformas Unicode, o TCHAR é definido como sinônimo do tipo WCHAR.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="8b0ab-109">Os clientes MAPI podem usar o tipo de dados TCHAR para representar uma cadeia de caracteres do tipo WCHAR ou char.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="8b0ab-110">Certifique-se de definir o UNICODE da constante simbólica e limite a plataforma quando for necessário.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="8b0ab-111">O MAPI interpretará as informações da plataforma e traduzirá internamente o TCHAR para a cadeia de caracteres apropriada.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="8b0ab-112">O tipo de propriedade MAPI, PT_TSTRING, funciona exatamente como o tipo de dados TCHAR.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="8b0ab-113">Quando a plataforma suporta Unicode, as propriedades do tipo PT_TSTRING são atribuídas ao tipo PT_UNICODE no tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="8b0ab-114">Quando a plataforma não oferece suporte a Unicode, essas propriedades são atribuídas ao tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="8b0ab-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="8b0ab-115">Confira mais informações sobre essa em [Conjuntos de Caracteres](mapi-character-sets.md) e [Lista de Tipos de Propriedades](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8b0ab-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b0ab-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b0ab-116">See also</span></span>



[<span data-ttu-id="8b0ab-117">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="8b0ab-117">MAPI Data Types</span></span>](mapi-data-types.md)

