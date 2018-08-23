---
title: DTBLMVLISTBOX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLMVLISTBOX
api_type:
- COM
ms.assetid: 1c22f842-d0e7-44f0-a7d5-c9c2aa6b8820
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f7c1241f2ad31dee8277f3b3b77ac02137067a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576306"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="3667f-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="3667f-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="3667f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3667f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3667f-105">Descreve uma lista de valores múltiplos que será exibida em uma caixa de diálogo que é construída a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="3667f-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3667f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3667f-106">Header file:</span></span>  <br/> |<span data-ttu-id="3667f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3667f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="3667f-108">Members</span><span class="sxs-lookup"><span data-stu-id="3667f-108">Members</span></span>

 <span data-ttu-id="3667f-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="3667f-109">**ulFlags**</span></span>
  
> <span data-ttu-id="3667f-110">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="3667f-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3667f-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="3667f-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="3667f-112">Marca de propriedade para uma propriedade de valores múltiplos do tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="3667f-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3667f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3667f-113">Remarks</span></span>

<span data-ttu-id="3667f-114">Uma estrutura **DTBLMVLISTBOX** descreve uma lista de valores múltiplos padrão que tem uma lista de itens de somente leitura.</span><span class="sxs-lookup"><span data-stu-id="3667f-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="3667f-115">Usando uma lista de valores múltiplos padrão, os valores são exibidos imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3667f-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="3667f-116">Os dados que são exibidos provêm a propriedade identificada no membro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="3667f-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="3667f-117">Não há nenhum requisito para a interface de propriedade que está associada com a tabela de exibição de leitura.</span><span class="sxs-lookup"><span data-stu-id="3667f-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="3667f-118">Além disso, como os usuários não são capazes de realizar seleções desses tipos de listas, dados não são gravados na interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="3667f-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="3667f-119">Somente as propriedades de cadeia de caracteres de valores múltiplos são suportadas para a lista de valores múltiplos; Não há suporte para outros tipos de propriedade de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="3667f-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="3667f-120">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3667f-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="3667f-121">Para obter informações sobre como implementar uma tabela de exibição, consulte [Implementando uma tabela exibir](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="3667f-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3667f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="3667f-122">See also</span></span>



[<span data-ttu-id="3667f-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="3667f-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="3667f-124">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="3667f-124">MAPI Structures</span></span>](mapi-structures.md)

