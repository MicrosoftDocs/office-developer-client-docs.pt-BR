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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e7b3774d8dce446f0e87f041f11dac607f464680
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770594"
---
# <a name="tchar"></a><span data-ttu-id="8e121-103">TCHAR</span><span class="sxs-lookup"><span data-stu-id="8e121-103">TCHAR</span></span>

  
  
<span data-ttu-id="8e121-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8e121-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8e121-105">Uma cadeia de caracteres Win32 que pode ser usada para descrever as cadeias de caracteres ANSI, Unicode ou DBCS.</span><span class="sxs-lookup"><span data-stu-id="8e121-105">A Win32 character string that can be used to describe ANSI, DBCS, or Unicode strings.</span></span> <span data-ttu-id="8e121-106">Para plataformas ANSI e DBCS, TCHAR é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8e121-106">For ANSI and DBCS platforms, TCHAR is defined as follows:</span></span>
  
```cpp
typedef char TCHAR;

```

## <a name="remarks"></a><span data-ttu-id="8e121-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8e121-107">Remarks</span></span>

<span data-ttu-id="8e121-108">Plataformas de Unicode, TCHAR é definido como o tipo WCHAR um sinônimo.</span><span class="sxs-lookup"><span data-stu-id="8e121-108">For Unicode platforms, TCHAR is defined as synonymous with the WCHAR type.</span></span> 
  
<span data-ttu-id="8e121-109">Clientes MAPI podem usar o tipo de dados TCHAR para representar uma cadeia de caracteres de tipo de WCHAR ou char.</span><span class="sxs-lookup"><span data-stu-id="8e121-109">MAPI clients can use the TCHAR data type to represent a string of either the WCHAR or char type.</span></span> <span data-ttu-id="8e121-110">Certifique-se definir o UNICODE constante simbólico e limitar a plataforma quando for solicitado.</span><span class="sxs-lookup"><span data-stu-id="8e121-110">Be sure to define the symbolic constant UNICODE and limit the platform when it is required.</span></span> <span data-ttu-id="8e121-111">MAPI irá interpretar as informações de plataforma e internamente traduzir TCHAR para a cadeia de caracteres apropriada.</span><span class="sxs-lookup"><span data-stu-id="8e121-111">MAPI will interpret the platform information and internally translate TCHAR to the appropriate string.</span></span> <span data-ttu-id="8e121-112">O tipo de propriedade MAPI, PT_TSTRING, funciona como o tipo de dados TCHAR.</span><span class="sxs-lookup"><span data-stu-id="8e121-112">The MAPI property type, PT_TSTRING, works just like the TCHAR data type.</span></span> <span data-ttu-id="8e121-113">Quando a plataforma oferece suporte a Unicode, propriedades do tipo PT_TSTRING recebem o tipo PT_UNICODE em tempo de compilação.</span><span class="sxs-lookup"><span data-stu-id="8e121-113">When the platform supports Unicode, properties of type PT_TSTRING are assigned the type PT_UNICODE at compile time.</span></span> <span data-ttu-id="8e121-114">Quando a plataforma não oferece suporte a Unicode, essas propriedades recebem o tipo PT_STRING8.</span><span class="sxs-lookup"><span data-stu-id="8e121-114">When the platform does not support Unicode, these properties are assigned the type PT_STRING8.</span></span>
  
<span data-ttu-id="8e121-115">Para obter mais informações sobre essa funcionalidade, consulte [Conjuntos de caracteres](mapi-character-sets.md) e a [Lista de tipos de propriedade](property-types.md).</span><span class="sxs-lookup"><span data-stu-id="8e121-115">For more information about this functionality, see [Character Sets](mapi-character-sets.md) and [List of Property Types](property-types.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8e121-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="8e121-116">See also</span></span>



[<span data-ttu-id="8e121-117">Tipos de dados MAPI</span><span class="sxs-lookup"><span data-stu-id="8e121-117">MAPI Data Types</span></span>](mapi-data-types.md)

