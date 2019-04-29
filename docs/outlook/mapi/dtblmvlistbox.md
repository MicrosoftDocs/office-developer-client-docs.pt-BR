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
ms.openlocfilehash: ae8f3ab28837bf0579549ead46c28477f815f35c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439699"
---
# <a name="dtblmvlistbox"></a><span data-ttu-id="e89ed-103">DTBLMVLISTBOX</span><span class="sxs-lookup"><span data-stu-id="e89ed-103">DTBLMVLISTBOX</span></span>

  
  
<span data-ttu-id="e89ed-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e89ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e89ed-105">Descreve uma lista de vários valores que será exibida em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e89ed-105">Describes a multi-valued list that will be displayed in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e89ed-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e89ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="e89ed-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e89ed-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVLISTBOX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVLISTBOX, FAR * LPDTBLMVLISTBOX;

```

## <a name="members"></a><span data-ttu-id="e89ed-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e89ed-108">Members</span></span>

 <span data-ttu-id="e89ed-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e89ed-109">**ulFlags**</span></span>
  
> <span data-ttu-id="e89ed-110">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e89ed-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e89ed-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="e89ed-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="e89ed-112">Marca de propriedade para uma propriedade de vários valores do tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e89ed-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e89ed-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e89ed-113">Remarks</span></span>

<span data-ttu-id="e89ed-114">Uma estrutura **DTBLMVLISTBOX** descreve uma lista de valores múltiplos padrão que tem uma lista de itens somente leitura.</span><span class="sxs-lookup"><span data-stu-id="e89ed-114">A **DTBLMVLISTBOX** structure describes a standard multi-valued list that has a read-only list of items.</span></span> <span data-ttu-id="e89ed-115">Usando uma lista de vários valores padrão, os valores são exibidos imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e89ed-115">By using a standard multi-valued list, the values are displayed immediately.</span></span> 
  
<span data-ttu-id="e89ed-116">Os dados exibidos vêm da propriedade identificada no membro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="e89ed-116">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="e89ed-117">Não há nenhum requisito para ler a partir da interface de propriedade associada à tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="e89ed-117">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="e89ed-118">Além disso, como os usuários não podem fazer seleções desses tipos de listas, os dados não são gravados na interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e89ed-118">Also, because users are not able to make selections from these types of lists, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="e89ed-119">Somente as propriedades de cadeia de caracteres de valores múltiplos têm suporte para a lista de vários valores; Não há suporte para outros tipos de propriedades de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="e89ed-119">Only multi-valued string properties are supported for the multi-valued list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="e89ed-120">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="e89ed-120">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="e89ed-121">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e89ed-121">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e89ed-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e89ed-122">See also</span></span>



[<span data-ttu-id="e89ed-123">DTCTL</span><span class="sxs-lookup"><span data-stu-id="e89ed-123">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="e89ed-124">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e89ed-124">MAPI Structures</span></span>](mapi-structures.md)

