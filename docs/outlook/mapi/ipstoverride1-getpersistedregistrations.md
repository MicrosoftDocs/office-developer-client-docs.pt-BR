---
title: IPSTOVERRIDE1GetPersistedRegistrations
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTOVERRIDE1.GetPersistedRegistrations
api_type:
- COM
ms.assetid: 027092f0-f2d6-49e8-a8d0-8926824953a2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 822b4164737aa6010ccce108b544410104ac023d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415128"
---
# <a name="ipstoverride1getpersistedregistrations"></a><span data-ttu-id="1574a-103">IPSTOVERRIDE1::GetPersistedRegistrations</span><span class="sxs-lookup"><span data-stu-id="1574a-103">IPSTOVERRIDE1::GetPersistedRegistrations</span></span>

  
  
<span data-ttu-id="1574a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1574a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1574a-105">Recupera a lista de registros do arquivo de Pastas Particulares (.pst).</span><span class="sxs-lookup"><span data-stu-id="1574a-105">Retrieves the list of registrations for the Personal Folders (.pst) file.</span></span>
  
```cpp
HRESULT GetPersistedRegistration(SPropValue **ppmval);
```

## <a name="parameters"></a><span data-ttu-id="1574a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1574a-106">Parameters</span></span>

 <span data-ttu-id="1574a-107">_ppmval_</span><span class="sxs-lookup"><span data-stu-id="1574a-107">_ppmval_</span></span>
  
> <span data-ttu-id="1574a-108">[in] Um ponteiro para um ponteiro para uma [estrutura SPropValue.](spropvalue.md)</span><span class="sxs-lookup"><span data-stu-id="1574a-108">[in] A pointer to a pointer to an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="1574a-109">O membro ulPropTag dessa estrutura é do tipo PT_MV_UNICODE, e o membro de valor MVszW será uma matriz de cadeias de caracteres Unicode terminadas por caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="1574a-109">The ulPropTag member of this structure is of the type PT_MV_UNICODE, and the MVszW value member will be an array of null-terminated Unicode strings.</span></span> <span data-ttu-id="1574a-110">Essas cadeias de caracteres são caminhos para DLLs para os quais o registro foi persistente.</span><span class="sxs-lookup"><span data-stu-id="1574a-110">These strings are paths to DLLs for which registration has been persisted.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1574a-111">O suporte ao .pst para ANSI não foi implementado.</span><span class="sxs-lookup"><span data-stu-id="1574a-111">.pst support for ANSI is not implemented.</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="1574a-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1574a-112">Return value</span></span>

<span data-ttu-id="1574a-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1574a-113">S_OK</span></span> 
  
> <span data-ttu-id="1574a-114">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1574a-114">The function call was successful.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1574a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1574a-115">See also</span></span>



[<span data-ttu-id="1574a-116">IPSTOVERRIDE1 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1574a-116">IPSTOVERRIDE1 : IUnknown</span></span>](ipstoverride1iunknown.md)
  
[<span data-ttu-id="1574a-117">IPSTOVERRIDEREQ : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1574a-117">IPSTOVERRIDEREQ : IUnknown</span></span>](ipstoverridereqiunknown.md)

