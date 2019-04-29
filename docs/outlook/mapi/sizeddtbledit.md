---
title: SizedDtblEdit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblEdit
api_type:
- COM
ms.assetid: a658d027-03a2-4cde-bf99-563e8521cb31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b5b9c42d944ad9d3ce92e99d08d29964944c8028
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437641"
---
# <a name="sizeddtbledit"></a><span data-ttu-id="c3aa4-103">SizedDtblEdit</span><span class="sxs-lookup"><span data-stu-id="c3aa4-103">SizedDtblEdit</span></span>

<span data-ttu-id="c3aa4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c3aa4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c3aa4-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLEDIT](dtbledit.md) para descrever um controle de edição e o número máximo de caracteres que podem ser inseridos no controle.</span><span class="sxs-lookup"><span data-stu-id="c3aa4-105">Creates a named structure that includes a [DTBLEDIT](dtbledit.md) structure for describing an edit control and the maximum number of characters that can be entered in the control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3aa4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c3aa4-106">Header file:</span></span>  <br/> |<span data-ttu-id="c3aa4-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c3aa4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="c3aa4-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="c3aa4-108">Related structure:</span></span>  <br/> |<span data-ttu-id="c3aa4-109">**DTBLEDIT**</span><span class="sxs-lookup"><span data-stu-id="c3aa4-109">**DTBLEDIT**</span></span> <br/> |
   
```cpp
SizedDtblEdit (n, u)
```

## <a name="parameters"></a><span data-ttu-id="c3aa4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3aa4-110">Parameters</span></span>

<span data-ttu-id="c3aa4-111">_n_</span><span class="sxs-lookup"><span data-stu-id="c3aa4-111">_n_</span></span>
  
> <span data-ttu-id="c3aa4-112">Número máximo de caracteres que podem ser inseridos no controle de edição.</span><span class="sxs-lookup"><span data-stu-id="c3aa4-112">Maximum number of characters that can be entered in the edit control.</span></span>
    
<span data-ttu-id="c3aa4-113">_u_</span><span class="sxs-lookup"><span data-stu-id="c3aa4-113">_u_</span></span>
  
> <span data-ttu-id="c3aa4-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="c3aa4-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c3aa4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3aa4-115">Remarks</span></span>

<span data-ttu-id="c3aa4-116">A macro **SizedDtblEdit** permite definir um controle de edição quando o número de caracteres habilitados é conhecido.</span><span class="sxs-lookup"><span data-stu-id="c3aa4-116">The **SizedDtblEdit** macro lets you define an edit control when the number of enabled characters is known.</span></span> <span data-ttu-id="c3aa4-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="c3aa4-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLEDIT dtbledit;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="c3aa4-118">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblEdit** como um ponteiro de estrutura **DTBLEDIT** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="c3aa4-118">To use a pointer to the resulting structure from the **SizedDtblEdit** macro as a **DTBLEDIT** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblEdit = (LPDTBLEDIT) &SizedDtblEdit;

```

## <a name="see-also"></a><span data-ttu-id="c3aa4-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3aa4-119">See also</span></span>

- [<span data-ttu-id="c3aa4-120">DTBLEDIT</span><span class="sxs-lookup"><span data-stu-id="c3aa4-120">DTBLEDIT</span></span>](dtbledit.md)
- [<span data-ttu-id="c3aa4-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="c3aa4-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

