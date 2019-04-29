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
ms.openlocfilehash: f14b8d7a9a73997f797f9cfa26a2e574222e839e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407442"
---
# <a name="sizeddtblpage"></a><span data-ttu-id="92ab5-103">SizedDtblPage</span><span class="sxs-lookup"><span data-stu-id="92ab5-103">SizedDtblPage</span></span>

<span data-ttu-id="92ab5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92ab5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92ab5-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLPAGE](dtblpage.md) para descrever um controle de página com guias, um rótulo de um tamanho especificado e uma entrada de arquivo de ajuda de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="92ab5-105">Creates a named structure that includes a [DTBLPAGE](dtblpage.md) structure for describing a tabbed page control, a label of a specified length, and a Help file entry of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="92ab5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="92ab5-106">Header file:</span></span>  <br/> |<span data-ttu-id="92ab5-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="92ab5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="92ab5-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="92ab5-108">Related structure:</span></span>  <br/> |<span data-ttu-id="92ab5-109">**DTBLPAGE**</span><span class="sxs-lookup"><span data-stu-id="92ab5-109">**DTBLPAGE**</span></span> <br/> |
   
```cpp
SizedDtblPage (n, n1, u)
```

## <a name="parameters"></a><span data-ttu-id="92ab5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92ab5-110">Parameters</span></span>

<span data-ttu-id="92ab5-111">_n_</span><span class="sxs-lookup"><span data-stu-id="92ab5-111">_n_</span></span>
  
> <span data-ttu-id="92ab5-112">Comprimento do rótulo da guia de página.</span><span class="sxs-lookup"><span data-stu-id="92ab5-112">Length of the label for the page tab.</span></span>
    
<span data-ttu-id="92ab5-113">_N1_</span><span class="sxs-lookup"><span data-stu-id="92ab5-113">_n1_</span></span>
  
> <span data-ttu-id="92ab5-114">Comprimento da entrada que aparece no arquivo MAPISVC. inf que identifica o arquivo de ajuda que será usado com o controle de página com guias.</span><span class="sxs-lookup"><span data-stu-id="92ab5-114">Length of the entry appearing in the Mapisvc.inf file identifying the Help file that will be used with the tabbed page control.</span></span>
    
<span data-ttu-id="92ab5-115">_u_</span><span class="sxs-lookup"><span data-stu-id="92ab5-115">_u_</span></span>
  
> <span data-ttu-id="92ab5-116">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="92ab5-116">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92ab5-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="92ab5-117">Remarks</span></span>

<span data-ttu-id="92ab5-118">A macro **SizedDtblPage** permite que você defina um controle de página com guias quando o número de caracteres no rótulo associado e entrada de arquivo de ajuda for conhecido.</span><span class="sxs-lookup"><span data-stu-id="92ab5-118">The **SizedDtblPage** macro lets you define a tabbed page control when the number of characters in the associated label and Help file entry is known.</span></span> <span data-ttu-id="92ab5-119">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="92ab5-119">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLPAGE dtblpage;
TCHAR lpszLabel[n];
TCHAR lpszComponent[n1];
```

<span data-ttu-id="92ab5-120">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblPage** como um ponteiro de estrutura **DTBLPAGE** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="92ab5-120">To use a pointer to the resulting structure from the **SizedDtblPage** macro as a **DTBLPAGE** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblPage = (LPDTBLPAGE) &SizedDtblPage;
```

## <a name="see-also"></a><span data-ttu-id="92ab5-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="92ab5-121">See also</span></span>

- [<span data-ttu-id="92ab5-122">DTBLPAGE</span><span class="sxs-lookup"><span data-stu-id="92ab5-122">DTBLPAGE</span></span>](dtblpage.md)
- [<span data-ttu-id="92ab5-123">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="92ab5-123">Macros Related to Structures</span></span>](macros-related-to-structures.md)

