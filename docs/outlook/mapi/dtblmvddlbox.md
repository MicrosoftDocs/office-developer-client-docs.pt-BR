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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33b4fd87f33c26db15e1a6a28f077c393168db91
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325757"
---
# <a name="dtblmvddlbox"></a><span data-ttu-id="521d6-103">DTBLMVDDLBOX</span><span class="sxs-lookup"><span data-stu-id="521d6-103">DTBLMVDDLBOX</span></span>

  
  
<span data-ttu-id="521d6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="521d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="521d6-105">Descreve uma lista suspensa que será usada em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="521d6-105">Describes a drop-down list that will be used in a dialog box that is built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="521d6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="521d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="521d6-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="521d6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLMVDDLBX
{
  ULONG ulFlags;
  ULONG ulMVPropTag;
} DTBLMVDDLBX, FAR * LPDTBLMVDDLBX;

```

## <a name="members"></a><span data-ttu-id="521d6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="521d6-108">Members</span></span>

 <span data-ttu-id="521d6-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="521d6-109">**ulFlags**</span></span>
  
> <span data-ttu-id="521d6-110">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="521d6-110">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="521d6-111">**ulMVPropTag**</span><span class="sxs-lookup"><span data-stu-id="521d6-111">**ulMVPropTag**</span></span>
  
> <span data-ttu-id="521d6-112">Marca de propriedade para uma propriedade de vários valores do tipo PT_MV_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="521d6-112">Property tag for a multi-valued property of type PT_MV_TSTRING.</span></span> <span data-ttu-id="521d6-113">Os valores diferentes dessa propriedade são exibidos como entradas distintas na lista suspensa.</span><span class="sxs-lookup"><span data-stu-id="521d6-113">The different values of this property are displayed as distinct entries in the drop-down list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="521d6-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="521d6-114">Remarks</span></span>

<span data-ttu-id="521d6-115">Uma estrutura **DTBLMVDDLBOX** descreve uma lista suspensa com vários valores uma lista de itens somente leitura.</span><span class="sxs-lookup"><span data-stu-id="521d6-115">A **DTBLMVDDLBOX** structure describes a multi-valued drop-down list a read-only list of items.</span></span> <span data-ttu-id="521d6-116">Usando uma lista suspensa com vários valores, os valores são exibidos quando um usuário clica em uma barra de rolagem.</span><span class="sxs-lookup"><span data-stu-id="521d6-116">By using a multi-valued drop-down list, values are displayed when a user clicks on a scroll bar.</span></span> 
  
<span data-ttu-id="521d6-117">Os dados exibidos vêm da propriedade identificada no membro **ulMVPropTag** .</span><span class="sxs-lookup"><span data-stu-id="521d6-117">The data that is displayed comes from the property identified in the **ulMVPropTag** member.</span></span> <span data-ttu-id="521d6-118">Não há nenhum requisito para ler a partir da interface de propriedade associada à tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="521d6-118">There is no requirement to read from the property interface that is associated with the display table.</span></span> <span data-ttu-id="521d6-119">Além disso, como os usuários não podem fazer seleções desses tipos de caixas de listagem, os dados não são gravados na interface de propriedade.</span><span class="sxs-lookup"><span data-stu-id="521d6-119">Also, because users are not able to make selections from these types of list boxes, data is not written to the property interface.</span></span> 
  
<span data-ttu-id="521d6-120">Somente as propriedades de cadeia de caracteres de valores múltiplos têm suporte para a lista suspensa de vários valores; Não há suporte para outros tipos de propriedades de valores múltiplos.</span><span class="sxs-lookup"><span data-stu-id="521d6-120">Only multi-valued string properties are supported for the multi-valued drop-down list; other multi-valued property types are not supported.</span></span> 
  
<span data-ttu-id="521d6-121">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="521d6-121">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="521d6-122">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="521d6-122">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="521d6-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="521d6-123">See also</span></span>



[<span data-ttu-id="521d6-124">DTCTL</span><span class="sxs-lookup"><span data-stu-id="521d6-124">DTCTL</span></span>](dtctl.md)


[<span data-ttu-id="521d6-125">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="521d6-125">MAPI Structures</span></span>](mapi-structures.md)

