---
title: SizedDtblComboBox
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedDtblComboBox
api_type:
- COM
ms.assetid: 1e5ea9f2-1029-4584-845a-890d3e956036
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8861c8f86eaab6defb270b673e0ee200446aedb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282821"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="50c0b-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="50c0b-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="50c0b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50c0b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50c0b-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLCOMBOBOX](dtblcombobox.md) para descrever um controle de caixa de combinação e o número máximo de caracteres que podem ser inseridos no controle de edição associado.</span><span class="sxs-lookup"><span data-stu-id="50c0b-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="50c0b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="50c0b-106">Header file:</span></span>  <br/> |<span data-ttu-id="50c0b-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="50c0b-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="50c0b-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="50c0b-108">Related structure:</span></span>  <br/> |<span data-ttu-id="50c0b-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="50c0b-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="50c0b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="50c0b-110">Parameters</span></span>

<span data-ttu-id="50c0b-111">_n_</span><span class="sxs-lookup"><span data-stu-id="50c0b-111">_n_</span></span>
  
> <span data-ttu-id="50c0b-112">Número de caracteres que podem ser inseridos no controle de edição da caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="50c0b-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="50c0b-113">_u_</span><span class="sxs-lookup"><span data-stu-id="50c0b-113">_u_</span></span>
  
> <span data-ttu-id="50c0b-114">Nome da nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="50c0b-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50c0b-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="50c0b-115">Remarks</span></span>

<span data-ttu-id="50c0b-116">A macro **SizedDtblComboBox** permite definir uma caixa de combinação quando o comprimento da cadeia de caracteres habilitada é conhecido.</span><span class="sxs-lookup"><span data-stu-id="50c0b-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="50c0b-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="50c0b-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="50c0b-118">Para usar um ponteiro para a estrutura resultante da macro **SizedDtblComboBox** como um ponteiro de estrutura **DTBLCOMBOBOX** , execute a seguinte conversão:</span><span class="sxs-lookup"><span data-stu-id="50c0b-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="50c0b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="50c0b-119">See also</span></span>

- [<span data-ttu-id="50c0b-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="50c0b-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="50c0b-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="50c0b-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

