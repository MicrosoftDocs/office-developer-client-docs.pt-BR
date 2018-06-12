---
title: DTBLMVDDLBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVDDLBOX
api_type:
- COM
ms.assetid: 0e6283dc-9a08-460f-9400-03f0ceb4081c
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ede0a448a32565446e614fc2d14f2a72a9549dad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766482"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="c89a7-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="c89a7-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="c89a7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c89a7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c89a7-105">Descreve uma lista suspensa que será usada em uma caixa de diálogo que é construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="c89a7-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c89a7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c89a7-106">Header file:</span></span>  <br/> |<span data-ttu-id="c89a7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c89a7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="c89a7-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c89a7-108">Members</span></span>

 <span data-ttu-id="c89a7-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="c89a7-109">**ulFlags**</span></span>
  
> <span data-ttu-id="c89a7-110">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c89a7-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c89a7-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="c89a7-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="c89a7-112">Marca de propriedade para uma propriedade de valores múltiplos do tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="c89a7-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="c89a7-113">Os diferentes valores dessa propriedade são exibidos como distintas entradas na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="c89a7-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c89a7-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="c89a7-114">Remarks</span></span>

<span data-ttu-id="c89a7-115">Uma estrutura **DTBLMVDDLBOX** descreve uma lista suspensa de valores múltiplos uma lista de somente leitura de itens.</span><span class="sxs-lookup"><span data-stu-id="c89a7-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="c89a7-116">Usando uma lista suspensa de valores múltiplos, os valores são exibidos quando um usuário clica em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="c89a7-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="c89a7-117">Os dados que são exibidos provêm a propriedade identificada no membro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="c89a7-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="c89a7-118">Não há nenhum requisito para a interface de propriedade que está associada com a tabela de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="c89a7-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="c89a7-119">Além disso, como os usuários não são capazes de realizar seleções contra esses tipos de caixas de listagem, dados não são gravados na interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="c89a7-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="c89a7-120">Somente as propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos suspensa; Não há suporte para outros tipos de propriedade de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="c89a7-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="c89a7-121">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c89a7-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="c89a7-122">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="c89a7-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c89a7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c89a7-123">See also</span></span>



[<span data-ttu-id="c89a7-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="c89a7-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="c89a7-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="c89a7-125">MAPI Structures</span></span>](mapi-structures.md)

