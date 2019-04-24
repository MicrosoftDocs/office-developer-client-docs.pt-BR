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
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="833bf-103">Propriedade canônica PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="833bf-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="833bf-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="833bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="833bf-105">Usado para exibir as informações de contato.</span><span class="sxs-lookup"><span data-stu-id="833bf-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="833bf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="833bf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="833bf-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="833bf-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="833bf-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="833bf-108">Property set:</span></span>  <br/> |<span data-ttu-id="833bf-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="833bf-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="833bf-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="833bf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="833bf-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="833bf-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="833bf-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="833bf-112">Data type:</span></span>  <br/> |<span data-ttu-id="833bf-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="833bf-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="833bf-114">Área:</span><span class="sxs-lookup"><span data-stu-id="833bf-114">Area:</span></span>  <br/> |<span data-ttu-id="833bf-115">Contato</span><span class="sxs-lookup"><span data-stu-id="833bf-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="833bf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="833bf-116">Remarks</span></span>

<span data-ttu-id="833bf-117">Se presente, a propriedade deve ter seis entradas, cada uma delas correspondente a um campo visível na interface de usuário do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="833bf-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="833bf-118">**Um índice com base na propriedade de vários valores**</span><span class="sxs-lookup"><span data-stu-id="833bf-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="833bf-119">**O valor deve ser um dos seguintes**</span><span class="sxs-lookup"><span data-stu-id="833bf-119">**The value must be one of the following**</span></span>|<span data-ttu-id="833bf-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="833bf-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="833bf-121">1</span><span class="sxs-lookup"><span data-stu-id="833bf-121">1</span></span>  <br/> |<span data-ttu-id="833bf-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="833bf-122">0x00000001</span></span>  <br/> |<span data-ttu-id="833bf-123">O aplicativo deve exibir o endereço residencial do contato.</span><span class="sxs-lookup"><span data-stu-id="833bf-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="833bf-124">1</span><span class="sxs-lookup"><span data-stu-id="833bf-124">1</span></span>  <br/> |<span data-ttu-id="833bf-125">0x00000002 ou 0x00000000</span><span class="sxs-lookup"><span data-stu-id="833bf-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="833bf-126">O aplicativo deve exibir o trabalho do contato.</span><span class="sxs-lookup"><span data-stu-id="833bf-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="833bf-127">1</span><span class="sxs-lookup"><span data-stu-id="833bf-127">1</span></span>  <br/> |<span data-ttu-id="833bf-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="833bf-128">0x00000003</span></span>  <br/> |<span data-ttu-id="833bf-129">O aplicativo deve exibir o outro endereço do contato.</span><span class="sxs-lookup"><span data-stu-id="833bf-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="833bf-130">duas</span><span class="sxs-lookup"><span data-stu-id="833bf-130">2</span></span>  <br/> |<span data-ttu-id="833bf-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="833bf-131">0x00008080</span></span>  <br/> |<span data-ttu-id="833bf-132">O aplicativo deve exibir email1.</span><span class="sxs-lookup"><span data-stu-id="833bf-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="833bf-133">duas</span><span class="sxs-lookup"><span data-stu-id="833bf-133">2</span></span>  <br/> |<span data-ttu-id="833bf-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="833bf-134">0x00008090</span></span>  <br/> |<span data-ttu-id="833bf-135">O aplicativo deve exibir EMAIL2.</span><span class="sxs-lookup"><span data-stu-id="833bf-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="833bf-136">duas</span><span class="sxs-lookup"><span data-stu-id="833bf-136">2</span></span>  <br/> |<span data-ttu-id="833bf-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="833bf-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="833bf-138">O aplicativo deve exibir Email3.</span><span class="sxs-lookup"><span data-stu-id="833bf-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="833bf-139">3, 4, 5, 6</span><span class="sxs-lookup"><span data-stu-id="833bf-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="833bf-140">PropertyId de qualquer uma das propriedades telefônicas ou de qualquer número de fax especificado em [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="833bf-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="833bf-141">O aplicativo deve exibir a propriedade correspondente.</span><span class="sxs-lookup"><span data-stu-id="833bf-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="833bf-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="833bf-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="833bf-143">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="833bf-143">Protocol specifications</span></span>

<span data-ttu-id="833bf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="833bf-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="833bf-145">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="833bf-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="833bf-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="833bf-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="833bf-147">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="833bf-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="833bf-148">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="833bf-148">Header files</span></span>

<span data-ttu-id="833bf-149">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="833bf-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="833bf-150">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="833bf-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="833bf-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="833bf-151">See also</span></span>



[<span data-ttu-id="833bf-152">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="833bf-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="833bf-153">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="833bf-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="833bf-154">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="833bf-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="833bf-155">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="833bf-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

