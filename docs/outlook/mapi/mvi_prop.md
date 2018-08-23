---
title: MVI_PROP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MVI_PROP
api_type:
- COM
ms.assetid: d7f07524-6935-4a60-aaf3-3f753ea8d86a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6a3d0d79d190b318d36fd9be8a3ec39d6aa7ad29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593974"
---
# <a name="mviprop"></a><span data-ttu-id="260c6-103">MVI_PROP</span><span class="sxs-lookup"><span data-stu-id="260c6-103">MVI_PROP</span></span>

  
  
<span data-ttu-id="260c6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="260c6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="260c6-105">Define o MVI_FLAG para uma propriedade especificada.</span><span class="sxs-lookup"><span data-stu-id="260c6-105">Sets the MVI_FLAG for a specified property.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="260c6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="260c6-106">Header file:</span></span>  <br/> |<span data-ttu-id="260c6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="260c6-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="260c6-108">Estrutura relacionada:</span><span class="sxs-lookup"><span data-stu-id="260c6-108">Related structure:</span></span>  <br/> |[<span data-ttu-id="260c6-109">SPropValue</span><span class="sxs-lookup"><span data-stu-id="260c6-109">SPropValue</span></span>](spropvalue.md) <br/> |
   
```cpp
MVI_PROP (tag)
```

## <a name="parameters"></a><span data-ttu-id="260c6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="260c6-110">Parameters</span></span>

 <span data-ttu-id="260c6-111">_marca_</span><span class="sxs-lookup"><span data-stu-id="260c6-111">_tag_</span></span>
  
> <span data-ttu-id="260c6-112">A marca de propriedade a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="260c6-112">The property tag to be modified.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="260c6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="260c6-113">Remarks</span></span>

<span data-ttu-id="260c6-114">O MVI_FLAG combina a configuração da MV_FLAG, que identifica uma propriedade como valores múltiplos e MV_INSTANCE, solicitando que uma propriedade de valores múltiplos exibida em uma tabela em várias linhas.</span><span class="sxs-lookup"><span data-stu-id="260c6-114">The MVI_FLAG combines the setting of MV_FLAG, identifying a property as multi-valued, and MV_INSTANCE, requesting that a multi-valued property be displayed in a table in multiple rows.</span></span> <span data-ttu-id="260c6-115">O tipo de propriedade da propriedade afetado é modificado, mas o identificador permanecerá inalterado.</span><span class="sxs-lookup"><span data-stu-id="260c6-115">The property type of the affected property is modified, but the identifier remains unchanged.</span></span> 
  
<span data-ttu-id="260c6-116">Por exemplo, quando a macro MVI_PROP é aplicada a uma propriedade do tipo PT_FLOAT, seu tipo é alterado para PT_MV_FLOAT.</span><span class="sxs-lookup"><span data-stu-id="260c6-116">For example, when the MVI_PROP macro is applied to a property of type PT_FLOAT, its type is changed to PT_MV_FLOAT.</span></span> <span data-ttu-id="260c6-117">Quando incluído em uma tabela, várias linhas são usadas para representar a propriedade que tem uma linha para cada valor.</span><span class="sxs-lookup"><span data-stu-id="260c6-117">When included in a table, multiple rows are used to represent the property that has one row for each value.</span></span> <span data-ttu-id="260c6-118">As propriedades das outras colunas são repetidas.</span><span class="sxs-lookup"><span data-stu-id="260c6-118">The properties for the other columns are repeated.</span></span> 
  
<span data-ttu-id="260c6-119">Para obter mais informações sobre esses sinalizadores, consulte [Visão geral do tipo de propriedade de MAPI](mapi-property-type-overview.md) e [trabalhar com vários valores de colunas](working-with-multivalued-columns.md).</span><span class="sxs-lookup"><span data-stu-id="260c6-119">For more information about these flags, see [MAPI Property Type Overview](mapi-property-type-overview.md) and [Working with Multivalued Columns](working-with-multivalued-columns.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="260c6-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="260c6-120">See also</span></span>



[<span data-ttu-id="260c6-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="260c6-121">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="260c6-122">Macros relacionadas a estruturas</span><span class="sxs-lookup"><span data-stu-id="260c6-122">Macros Related to Structures</span></span>](macros-related-to-structures.md)

