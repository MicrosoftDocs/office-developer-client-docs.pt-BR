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
ms.openlocfilehash: 39854c320078d2e2ca2365244f094e28962380d0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593652"
---
# <a name="sizeddtblcombobox"></a><span data-ttu-id="039c5-103">SizedDtblComboBox</span><span class="sxs-lookup"><span data-stu-id="039c5-103">SizedDtblComboBox</span></span>
 
<span data-ttu-id="039c5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="039c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="039c5-105">Cria uma estrutura nomeada que inclui uma estrutura [DTBLCOMBOBOX](dtblcombobox.md) para descrever um controle de caixa de combinação e o número máximo de caracteres que podem ser inseridos no controle de edição associado.</span><span class="sxs-lookup"><span data-stu-id="039c5-105">Creates a named structure that includes a [DTBLCOMBOBOX](dtblcombobox.md) structure for describing a combo box control and the maximum number of characters that can be entered in the associated edit control.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="039c5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="039c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="039c5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="039c5-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="039c5-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="039c5-108">Related structure:</span></span>  <br/> |<span data-ttu-id="039c5-109">**DTBLCOMBOBOX**</span><span class="sxs-lookup"><span data-stu-id="039c5-109">**DTBLCOMBOBOX**</span></span> <br/> |
   
```cpp
SizedDtblComboBox (n, u)
```

## <a name="parameters"></a><span data-ttu-id="039c5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="039c5-110">Parameters</span></span>

<span data-ttu-id="039c5-111">_n_</span><span class="sxs-lookup"><span data-stu-id="039c5-111">_n_</span></span>
  
> <span data-ttu-id="039c5-112">Controle de edição de número de caracteres que podem ser inseridos na caixa de combinação.</span><span class="sxs-lookup"><span data-stu-id="039c5-112">Number of characters that can be entered in the combo box's edit control.</span></span> 
    
<span data-ttu-id="039c5-113">_u_</span><span class="sxs-lookup"><span data-stu-id="039c5-113">_u_</span></span>
  
> <span data-ttu-id="039c5-114">Nome para a nova estrutura.</span><span class="sxs-lookup"><span data-stu-id="039c5-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="039c5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="039c5-115">Remarks</span></span>

<span data-ttu-id="039c5-116">A macro **SizedDtblComboBox** permite definir uma caixa de combinação quando o comprimento da cadeia de caracteres habilitados é conhecido.</span><span class="sxs-lookup"><span data-stu-id="039c5-116">The **SizedDtblComboBox** macro lets you define a combo box when the length of the enabled character string is known.</span></span> <span data-ttu-id="039c5-117">A nova estrutura é criada com os seguintes membros:</span><span class="sxs-lookup"><span data-stu-id="039c5-117">The new structure is created with the following members:</span></span> 
  
```cpp
DTBLCOMBOBOX dtblcombobox;
TCHAR lpszCharsAllowed[n];

```

<span data-ttu-id="039c5-118">Para usar um ponteiro para a estrutura resultante de macro **SizedDtblComboBox** como um ponteiro de estrutura **DTBLCOMBOBOX** , execute a seguinte projeção:</span><span class="sxs-lookup"><span data-stu-id="039c5-118">To use a pointer to the resulting structure from the **SizedDtblComboBox** macro as a **DTBLCOMBOBOX** structure pointer, perform the following cast:</span></span> 
  
```cpp
lpDtblComboBox = (LPDTBLCOMBOBOX) &SizedDtblComboBox;

```

## <a name="see-also"></a><span data-ttu-id="039c5-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="039c5-119">See also</span></span>

- [<span data-ttu-id="039c5-120">DTBLCOMBOBOX</span><span class="sxs-lookup"><span data-stu-id="039c5-120">DTBLCOMBOBOX</span></span>](dtblcombobox.md)
- [<span data-ttu-id="039c5-121">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="039c5-121">Macros Related to Structures</span></span>](macros-related-to-structures.md)

