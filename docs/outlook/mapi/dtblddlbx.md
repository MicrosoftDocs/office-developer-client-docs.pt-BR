---
title: DTBLDDLBX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLDDLBX
api_type:
- COM
ms.assetid: cf60584c-4357-44c7-9d51-f30f7e510c0c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 244aaea4902d6be8eda4cdca176436af9b002ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438845"
---
# <a name="dtblddlbx"></a><span data-ttu-id="cef6a-103">DTBLDDLBX</span><span class="sxs-lookup"><span data-stu-id="cef6a-103">DTBLDDLBX</span></span>

  
  
<span data-ttu-id="cef6a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cef6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cef6a-105">Descreve um controle de lista suspensa que será usado em uma caixa de diálogo criada a partir de uma tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="cef6a-105">Describes a drop-down list control that will be used in a dialog box built from a display table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cef6a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="cef6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="cef6a-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="cef6a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _DTBLDDLBX
{
  ULONG ulFlags;
  ULONG ulPRDisplayProperty;
  ULONG ulPRSetProperty;
  ULONG ulPRTableName;
} DTBLDDLBX, FAR *LPDTBLDDLBX;

```

## <a name="members"></a><span data-ttu-id="cef6a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="cef6a-108">Members</span></span>

 <span data-ttu-id="cef6a-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="cef6a-109">**ulFlags**</span></span>
  
> <span data-ttu-id="cef6a-110">Reservado, deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="cef6a-110">Reserved, must be zero.</span></span> 
    
 <span data-ttu-id="cef6a-111">**ulPRDisplayProperty**</span><span class="sxs-lookup"><span data-stu-id="cef6a-111">**ulPRDisplayProperty**</span></span>
  
> <span data-ttu-id="cef6a-112">Marca de propriedade de uma propriedade do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="cef6a-112">Property tag for a property of type PT_TSTRING.</span></span> <span data-ttu-id="cef6a-113">Essa propriedade é uma das colunas na tabela identificadas pelo membro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="cef6a-113">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="cef6a-114">Os valores dessa propriedade são exibidos na lista.</span><span class="sxs-lookup"><span data-stu-id="cef6a-114">The values for this property are displayed in the list.</span></span> 
    
 <span data-ttu-id="cef6a-115">**ulPRSetProperty**</span><span class="sxs-lookup"><span data-stu-id="cef6a-115">**ulPRSetProperty**</span></span>
  
> <span data-ttu-id="cef6a-116">Marca de propriedade de uma propriedade de qualquer tipo.</span><span class="sxs-lookup"><span data-stu-id="cef6a-116">Property tag for a property of any type.</span></span> <span data-ttu-id="cef6a-117">Essa propriedade é uma das colunas na tabela identificadas pelo membro **ulPRTableName** .</span><span class="sxs-lookup"><span data-stu-id="cef6a-117">This property is one of the columns in the table identified by the **ulPRTableName** member.</span></span> <span data-ttu-id="cef6a-118">Quando o usuário da lista seleciona um valor de propriedade para o membro **ulPRDisplayProperty** das linhas da tabela identificadas pelo membro **ulPRTableName** , o membro **ulPRSetProperty** correspondente é definido.</span><span class="sxs-lookup"><span data-stu-id="cef6a-118">When the user of the list selects a property value for the **ulPRDisplayProperty** member from the rows of the table identified by the **ulPRTableName** member, the corresponding **ulPRSetProperty** member is set.</span></span> 
    
 <span data-ttu-id="cef6a-119">**ulPRTableName**</span><span class="sxs-lookup"><span data-stu-id="cef6a-119">**ulPRTableName**</span></span>
  
> <span data-ttu-id="cef6a-120">Marca de propriedade de uma propriedade de tabela do tipo PT_OBJECT que pode ser aberta usando \*\*\*\* uma chamada OpenProperty.</span><span class="sxs-lookup"><span data-stu-id="cef6a-120">Property tag for a table property of type PT_OBJECT that can be opened by using an **OpenProperty** call.</span></span> <span data-ttu-id="cef6a-121">A tabela deve ter duas colunas: **ulPRDisplayProperty** e **ulPRSetProperty**.</span><span class="sxs-lookup"><span data-stu-id="cef6a-121">The table should have two columns: **ulPRDisplayProperty** and **ulPRSetProperty**.</span></span> <span data-ttu-id="cef6a-122">As linhas da tabela devem corresponder aos itens na lista.</span><span class="sxs-lookup"><span data-stu-id="cef6a-122">The rows of the table should correspond to items in the list.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cef6a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="cef6a-123">Remarks</span></span>

<span data-ttu-id="cef6a-124">Uma estrutura **DTBLDDLBX** descreve um controle de lista suspensa que é exibido como um único item até que o usuário opte por expandi-lo.</span><span class="sxs-lookup"><span data-stu-id="cef6a-124">A **DTBLDDLBX** structure describes a drop-down list control that is displayed as a single item until the user elects to expand it.</span></span> 
  
<span data-ttu-id="cef6a-125">As três propriedades identificadas pelas marcas de propriedade funcionam juntas para exibir as informações na lista e definir uma propriedade relacionada.</span><span class="sxs-lookup"><span data-stu-id="cef6a-125">The three properties identified by the property tags work together to display the information in the list and set a related property.</span></span> <span data-ttu-id="cef6a-126">O membro **ulPRTableName** é um objeto Table que é acessado por meio de uma chamada a [IMAPIProp:: OpenProperty](imapiprop-openproperty.md).</span><span class="sxs-lookup"><span data-stu-id="cef6a-126">The **ulPRTableName** member is a table object that is accessed through a call to [IMAPIProp::OpenProperty](imapiprop-openproperty.md).</span></span> <span data-ttu-id="cef6a-127">A tabela tem duas colunas: uma coluna para a propriedade identificada pelo membro **ulPRDisplayProperty** e a outra para a propriedade identificada pelo membro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="cef6a-127">The table has two columns: one column for the property identified by the **ulPRDisplayProperty** member and the other for the property identified by the **ulPRSetProperty** member.</span></span> 
  
<span data-ttu-id="cef6a-128">A propriedade **ulPRDisplayProperty** orienta a exibição da lista.</span><span class="sxs-lookup"><span data-stu-id="cef6a-128">The **ulPRDisplayProperty** property drives the list display.</span></span> <span data-ttu-id="cef6a-129">Quando um usuário seleciona um dos valores da exibição, MAPI chama [IMAPIProp::](imapiprop-setprops.md) SetProps para definir a propriedade correspondente conforme identificado pelo membro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="cef6a-129">When a user selects one of the values from the display, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to set the corresponding property as identified by the **ulPRSetProperty** member.</span></span> <span data-ttu-id="cef6a-130">Isso significa que a propriedade na mesma linha que a propriedade de exibição selecionada.</span><span class="sxs-lookup"><span data-stu-id="cef6a-130">This means that the property in the same row as the selected display property.</span></span> <span data-ttu-id="cef6a-131">O membro **ulPRSetProperty** não pode ser definido como **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="cef6a-131">The **ulPRSetProperty** member cannot be set to **PR_NULL** ([PidTagNull](pidtagnull-canonical-property.md)).</span></span>
  
<span data-ttu-id="cef6a-132">Um valor inicial é exibido na lista se o MAPI tiver recuperado a propriedade representada pelo membro **ulPRSetProperty** por meio de uma chamada a [IMAPIProp::](imapiprop-getprops.md) GetProps e localizada uma linha na tabela com o valor do membro **ulPRSetProperty** .</span><span class="sxs-lookup"><span data-stu-id="cef6a-132">An initial value is displayed in the list if MAPI has retrieved the property represented by the **ulPRSetProperty** member through a call to [IMAPIProp::GetProps](imapiprop-getprops.md) and located a row in the table with the value for the **ulPRSetProperty** member.</span></span> <span data-ttu-id="cef6a-133">O valor inicial exibido é o conteúdo da coluna **ulPRDisplayProperty** dessa linha que corresponde à propriedade no membro **ulPRDisplayProperty** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="cef6a-133">The initial displayed value is the contents of the **ulPRDisplayProperty** column from that row that matches the property in the **ulPRDisplayProperty** member of the structure.</span></span> <span data-ttu-id="cef6a-134">O valor retornado por \*\*\*\* GetProps para a propriedade identificada pelo membro **ulPRDisplayProperty** se torna o valor inicial que é mostrado quando a lista é exibida pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="cef6a-134">The value returned by **GetProps** for the property identified by the **ulPRDisplayProperty** member becomes the initial value that is shown when the list is first displayed.</span></span> 
  
<span data-ttu-id="cef6a-135">Para obter uma visão geral das tabelas de exibição, consulte [Exibir tabelas](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="cef6a-135">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> <span data-ttu-id="cef6a-136">Para obter informações sobre como implementar uma tabela de exibição, consulte [implementando uma tabela de exibição](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="cef6a-136">For information about how to implement a display table, see [Implementing a Display Table](display-table-implementation.md).</span></span> <span data-ttu-id="cef6a-137">Para obter informações sobre tipos de propriedade, consulte [MAPI Property Type Overview](mapi-property-type-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cef6a-137">For information about property types, see [MAPI Property Type Overview](mapi-property-type-overview.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cef6a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cef6a-138">See also</span></span>



[<span data-ttu-id="cef6a-139">DTCTL</span><span class="sxs-lookup"><span data-stu-id="cef6a-139">DTCTL</span></span>](dtctl.md)
  
[<span data-ttu-id="cef6a-140">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="cef6a-140">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="cef6a-141">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="cef6a-141">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
  
[<span data-ttu-id="cef6a-142">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="cef6a-142">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)


[<span data-ttu-id="cef6a-143">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="cef6a-143">MAPI Structures</span></span>](mapi-structures.md)
  
[<span data-ttu-id="cef6a-144">Exibir a implementação da tabela</span><span class="sxs-lookup"><span data-stu-id="cef6a-144">Display Table Implementation</span></span>](display-table-implementation.md)
  
[<span data-ttu-id="cef6a-145">Exibir tabelas</span><span class="sxs-lookup"><span data-stu-id="cef6a-145">Display Tables</span></span>](display-tables.md)
  
[<span data-ttu-id="cef6a-146">Visão geral do tipo de propriedade MAPI</span><span class="sxs-lookup"><span data-stu-id="cef6a-146">MAPI Property Type Overview</span></span>](mapi-property-type-overview.md)

