---
title: SizedDtblLabel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblLabel
api_type:
- COM
ms.assetid: c7cb8cf9-7abd-4ee3-b88c-d61695f4ed31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8d960207e05b33efe55886166ff1322f7f4eedce
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586197"
---
# <a name="sizeddtbllabel"></a><span data-ttu-id="bf41b-103">SizedDtblLabel</span><span class="sxs-lookup"><span data-stu-id="bf41b-103">SizedDtblLabel</span></span>

<span data-ttu-id="bf41b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf41b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf41b-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLLABEL](dtbllabel.md) para descrever um controle label e o rótulo associado de um comprimento especificado.</span><span class="sxs-lookup"><span data-stu-id="bf41b-105">Creates a named structure that includes a [DTBLLABEL](dtbllabel.md) structure for describing a label control and the associated label of a specified length.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf41b-106">Especificados no arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="bf41b-106">Specified in header file:</span></span>  <br/> |<span data-ttu-id="bf41b-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="bf41b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="bf41b-108">Estrutura relacionada</span><span class="sxs-lookup"><span data-stu-id="bf41b-108">Related structure</span></span>  <br/> |<span data-ttu-id="bf41b-109">**DTBLLABEL**</span><span class="sxs-lookup"><span data-stu-id="bf41b-109">**DTBLLABEL**</span></span> <br/> |
   
```cpp
SizedDtblLabel (n, u)
```

## <a name="parameters"></a><span data-ttu-id="bf41b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf41b-110">Parameters</span></span>

<span data-ttu-id="bf41b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="bf41b-111">_n_</span></span>
  
> <span data-ttu-id="bf41b-112">Comprimento do rótulo.</span><span class="sxs-lookup"><span data-stu-id="bf41b-112">Length of the label.</span></span> <span data-ttu-id="bf41b-113">Isso inclui o caractere final de nulo.</span><span class="sxs-lookup"><span data-stu-id="bf41b-113">This includes the ending NULL character.</span></span> 
    
<span data-ttu-id="bf41b-114">_u_</span><span class="sxs-lookup"><span data-stu-id="bf41b-114">_u_</span></span>
  
> <span data-ttu-id="bf41b-115">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="bf41b-115">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf41b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf41b-116">Remarks</span></span>

<span data-ttu-id="bf41b-117">A macro **SizedDtblLabel** permite definir uma etiqueta de exibição tabela quando o número de caracteres no rótulo é conhecido.</span><span class="sxs-lookup"><span data-stu-id="bf41b-117">The **SizedDtblLabel** macro lets you define a display table label when the number of characters in the label is known.</span></span> <span data-ttu-id="bf41b-118">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="bf41b-118">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLLABEL dtbllabel;
TCHAR lpszLabelName[n];
```

<span data-ttu-id="bf41b-119">Para usar um ponteiro para a estrutura resultante de macro **SizedDtblLabel** como um ponteiro de estrutura **DTBLLABEL** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="bf41b-119">To use a pointer to the resulting structure from the **SizedDtblLabel** macro as a **DTBLLABEL** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblLabel = (LPDTBLLABEL) &SizedDtblLabel;
```

## <a name="see-also"></a><span data-ttu-id="bf41b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf41b-120">See also</span></span>

- [<span data-ttu-id="bf41b-121">DTBLLABEL</span><span class="sxs-lookup"><span data-stu-id="bf41b-121">DTBLLABEL</span></span>](dtbllabel.md)
- [<span data-ttu-id="bf41b-122">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="bf41b-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

