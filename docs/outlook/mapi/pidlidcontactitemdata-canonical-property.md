---
title: Propriedade canônica PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768351"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="39bb9-103">Propriedade canônica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="39bb9-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="39bb9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39bb9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39bb9-105">Usado para exibir as informações de contato.</span><span class="sxs-lookup"><span data-stu-id="39bb9-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="39bb9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="39bb9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="39bb9-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="39bb9-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="39bb9-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="39bb9-108">Property set:</span></span>  <br/> |<span data-ttu-id="39bb9-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="39bb9-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="39bb9-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="39bb9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="39bb9-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="39bb9-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="39bb9-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="39bb9-112">Data type:</span></span>  <br/> |<span data-ttu-id="39bb9-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="39bb9-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="39bb9-114">Área:</span><span class="sxs-lookup"><span data-stu-id="39bb9-114">Area:</span></span>  <br/> |<span data-ttu-id="39bb9-115">Contato</span><span class="sxs-lookup"><span data-stu-id="39bb9-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39bb9-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="39bb9-116">Remarks</span></span>

<span data-ttu-id="39bb9-117">Se presente, a propriedade deve ter seis entradas, cada um correspondendo a um campo visível na interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="39bb9-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="39bb9-118">**Baseado em um índice para a propriedade de valores múltiplos**</span><span class="sxs-lookup"><span data-stu-id="39bb9-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="39bb9-119">**O valor deve ser um dos seguintes**</span><span class="sxs-lookup"><span data-stu-id="39bb9-119">**The value must be one of the following**</span></span>|<span data-ttu-id="39bb9-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="39bb9-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="39bb9-121">1</span><span class="sxs-lookup"><span data-stu-id="39bb9-121">1</span></span>  <br/> |<span data-ttu-id="39bb9-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="39bb9-122">0x00000001</span></span>  <br/> |<span data-ttu-id="39bb9-123">O aplicativo deve exibir endereço residencial do contato.</span><span class="sxs-lookup"><span data-stu-id="39bb9-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="39bb9-124">1</span><span class="sxs-lookup"><span data-stu-id="39bb9-124">1</span></span>  <br/> |<span data-ttu-id="39bb9-125">0x00000002 ou 0x00000000</span><span class="sxs-lookup"><span data-stu-id="39bb9-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="39bb9-126">O aplicativo deve exibir comercial do contato.</span><span class="sxs-lookup"><span data-stu-id="39bb9-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="39bb9-127">1</span><span class="sxs-lookup"><span data-stu-id="39bb9-127">1</span></span>  <br/> |<span data-ttu-id="39bb9-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="39bb9-128">0x00000003</span></span>  <br/> |<span data-ttu-id="39bb9-129">O aplicativo deve exibir o contato do outro endereço.</span><span class="sxs-lookup"><span data-stu-id="39bb9-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="39bb9-130">2</span><span class="sxs-lookup"><span data-stu-id="39bb9-130">2</span></span>  <br/> |<span data-ttu-id="39bb9-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="39bb9-131">0x00008080</span></span>  <br/> |<span data-ttu-id="39bb9-132">O aplicativo deve exibir Email1.</span><span class="sxs-lookup"><span data-stu-id="39bb9-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="39bb9-133">2</span><span class="sxs-lookup"><span data-stu-id="39bb9-133">2</span></span>  <br/> |<span data-ttu-id="39bb9-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="39bb9-134">0x00008090</span></span>  <br/> |<span data-ttu-id="39bb9-135">O aplicativo deve exibir Email2.</span><span class="sxs-lookup"><span data-stu-id="39bb9-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="39bb9-136">2</span><span class="sxs-lookup"><span data-stu-id="39bb9-136">2</span></span>  <br/> |<span data-ttu-id="39bb9-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="39bb9-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="39bb9-138">O aplicativo deve exibir Email3.</span><span class="sxs-lookup"><span data-stu-id="39bb9-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="39bb9-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="39bb9-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="39bb9-140">PropertyID de qualquer uma das propriedades telefônica ou de qualquer um dos números de fax que foram especificados em [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="39bb9-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="39bb9-141">O aplicativo deve exibir a propriedade correspondente.</span><span class="sxs-lookup"><span data-stu-id="39bb9-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="39bb9-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="39bb9-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="39bb9-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="39bb9-143">Protocol specifications</span></span>

<span data-ttu-id="39bb9-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39bb9-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39bb9-145">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="39bb9-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="39bb9-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="39bb9-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="39bb9-147">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="39bb9-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="39bb9-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="39bb9-148">Header files</span></span>

<span data-ttu-id="39bb9-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="39bb9-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="39bb9-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="39bb9-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39bb9-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="39bb9-151">See also</span></span>



[<span data-ttu-id="39bb9-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="39bb9-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="39bb9-153">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="39bb9-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="39bb9-154">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="39bb9-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="39bb9-155">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="39bb9-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

