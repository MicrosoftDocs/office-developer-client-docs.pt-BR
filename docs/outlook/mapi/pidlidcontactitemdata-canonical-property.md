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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319506"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="636eb-103">Propriedade canônica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="636eb-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="636eb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="636eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="636eb-105">Usado para exibir as informações de contato.</span><span class="sxs-lookup"><span data-stu-id="636eb-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="636eb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="636eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="636eb-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="636eb-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="636eb-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="636eb-108">Property set:</span></span>  <br/> |<span data-ttu-id="636eb-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="636eb-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="636eb-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="636eb-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="636eb-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="636eb-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="636eb-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="636eb-112">Data type:</span></span>  <br/> |<span data-ttu-id="636eb-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="636eb-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="636eb-114">Área:</span><span class="sxs-lookup"><span data-stu-id="636eb-114">Area:</span></span>  <br/> |<span data-ttu-id="636eb-115">Contato</span><span class="sxs-lookup"><span data-stu-id="636eb-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="636eb-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="636eb-116">Remarks</span></span>

<span data-ttu-id="636eb-117">Se presente, a propriedade deve ter seis entradas, cada uma correspondendo a um campo visível na interface do usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="636eb-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="636eb-118">**Índice baseado em um na propriedade de vários valores**</span><span class="sxs-lookup"><span data-stu-id="636eb-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="636eb-119">**O valor deve ser um dos seguintes:**</span><span class="sxs-lookup"><span data-stu-id="636eb-119">**The value must be one of the following**</span></span>|<span data-ttu-id="636eb-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="636eb-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="636eb-121">1</span><span class="sxs-lookup"><span data-stu-id="636eb-121">1</span></span>  <br/> |<span data-ttu-id="636eb-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="636eb-122">0x00000001</span></span>  <br/> |<span data-ttu-id="636eb-123">O aplicativo deve exibir o endereço residencial do contato.</span><span class="sxs-lookup"><span data-stu-id="636eb-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="636eb-124">1 </span><span class="sxs-lookup"><span data-stu-id="636eb-124">1</span></span>  <br/> |<span data-ttu-id="636eb-125">0x00000002 ou 0x00000000</span><span class="sxs-lookup"><span data-stu-id="636eb-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="636eb-126">O aplicativo deve exibir o trabalho do contato.</span><span class="sxs-lookup"><span data-stu-id="636eb-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="636eb-127">1 </span><span class="sxs-lookup"><span data-stu-id="636eb-127">1</span></span>  <br/> |<span data-ttu-id="636eb-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="636eb-128">0x00000003</span></span>  <br/> |<span data-ttu-id="636eb-129">O aplicativo deve exibir o outro endereço do contato.</span><span class="sxs-lookup"><span data-stu-id="636eb-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="636eb-130">2 </span><span class="sxs-lookup"><span data-stu-id="636eb-130">2</span></span>  <br/> |<span data-ttu-id="636eb-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="636eb-131">0x00008080</span></span>  <br/> |<span data-ttu-id="636eb-132">O aplicativo deve exibir Email1.</span><span class="sxs-lookup"><span data-stu-id="636eb-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="636eb-133">2 </span><span class="sxs-lookup"><span data-stu-id="636eb-133">2</span></span>  <br/> |<span data-ttu-id="636eb-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="636eb-134">0x00008090</span></span>  <br/> |<span data-ttu-id="636eb-135">O aplicativo deve exibir Email2.</span><span class="sxs-lookup"><span data-stu-id="636eb-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="636eb-136">2 </span><span class="sxs-lookup"><span data-stu-id="636eb-136">2</span></span>  <br/> |<span data-ttu-id="636eb-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="636eb-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="636eb-138">O aplicativo deve exibir Email3.</span><span class="sxs-lookup"><span data-stu-id="636eb-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="636eb-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="636eb-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="636eb-140">PropertyID de qualquer uma das propriedades de telefone ou qualquer um dos números de fax especificados em [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="636eb-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="636eb-141">O aplicativo deve exibir a propriedade correspondente.</span><span class="sxs-lookup"><span data-stu-id="636eb-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="636eb-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="636eb-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="636eb-143">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="636eb-143">Protocol specifications</span></span>

<span data-ttu-id="636eb-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="636eb-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="636eb-145">Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="636eb-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="636eb-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="636eb-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="636eb-147">Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.</span><span class="sxs-lookup"><span data-stu-id="636eb-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="636eb-148">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="636eb-148">Header files</span></span>

<span data-ttu-id="636eb-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="636eb-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="636eb-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="636eb-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="636eb-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="636eb-151">See also</span></span>



[<span data-ttu-id="636eb-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="636eb-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="636eb-153">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="636eb-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="636eb-154">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="636eb-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="636eb-155">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="636eb-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

