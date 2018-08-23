---
title: SizedDtblPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblPage
api_type:
- COM
ms.assetid: 47b2a69d-e902-429f-8b31-166b51aeaf7f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ae3f84c6b219c7becb88737f0d6c9fcb9722ea34
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584965"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="5657f-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="5657f-103">SizedDtblPage</span></span>

<span data-ttu-id="5657f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5657f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5657f-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLPAGE](dtblpage.md) para descrever a um controle de páginas com guias, um rótulo de um comprimento especificado e uma entrada de arquivo de ajuda de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="5657f-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5657f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5657f-106">Header file:</span></span>  <br/> |<span data-ttu-id="5657f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5657f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5657f-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="5657f-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5657f-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="5657f-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="5657f-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5657f-110">Parameters</span></span>

<span data-ttu-id="5657f-111">_n_</span><span class="sxs-lookup"><span data-stu-id="5657f-111">_n_</span></span>
  
> <span data-ttu-id="5657f-112">Comprimento do rótulo para a guia página.</span><span class="sxs-lookup"><span data-stu-id="5657f-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="5657f-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="5657f-113">_n1_</span></span>
  
> <span data-ttu-id="5657f-114">Comprimento da entrada que aparecem no arquivo Mapisvc que identifica o arquivo de Ajuda que será usado com o controle de página com guias.</span><span class="sxs-lookup"><span data-stu-id="5657f-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="5657f-115">_u_</span><span class="sxs-lookup"><span data-stu-id="5657f-115">_u_</span></span>
  
> <span data-ttu-id="5657f-116">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="5657f-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5657f-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5657f-117">Remarks</span></span>

<span data-ttu-id="5657f-118">A macro **SizedDtblPage** permite definir um controle de páginas com guias quando o número de caracteres no rótulo associado e entrada de arquivo de Ajuda é conhecido.</span><span class="sxs-lookup"><span data-stu-id="5657f-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="5657f-119">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="5657f-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="5657f-120">Para usar um ponteiro para a estrutura resultante de macro **SizedDtblPage** como um ponteiro de estrutura **DTBLPAGE** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="5657f-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="5657f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="5657f-121">See also</span></span>

- [<span data-ttu-id="5657f-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="5657f-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="5657f-123">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="5657f-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

