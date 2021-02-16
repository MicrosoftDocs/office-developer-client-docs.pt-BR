---
title: Propriedade canônica PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283146"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="a3039-103">Propriedade canônica PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="a3039-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="a3039-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3039-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3039-105">Contém uma cadeia de caracteres de texto que descreve o tipo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="a3039-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="a3039-106">Embora essa propriedade seja geralmente ignorada, as versões do Microsoft® Exchange Server anteriores ao Gerenciador de Caixa de Correio do Exchange Server 2003 esperam que essa propriedade estará presente.</span><span class="sxs-lookup"><span data-stu-id="a3039-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3039-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a3039-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="a3039-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="a3039-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="a3039-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a3039-109">Identifier:</span></span>  <br/> |<span data-ttu-id="a3039-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="a3039-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="a3039-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a3039-111">Data type:</span></span>  <br/> |<span data-ttu-id="a3039-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a3039-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="a3039-113">Área:</span><span class="sxs-lookup"><span data-stu-id="a3039-113">Area:</span></span>  <br/> |<span data-ttu-id="a3039-114">Contêiner</span><span class="sxs-lookup"><span data-stu-id="a3039-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a3039-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a3039-115">Remarks</span></span>

<span data-ttu-id="a3039-116">Essas propriedades normalmente não são usadas pelo Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a3039-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="a3039-117">No entanto, o Microsoft Office Outlook ® anexa-os a pastas de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a3039-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="a3039-118">Além disso, as versões do Exchange Server anteriores ao Gerenciador de Caixa de Correio do Exchange Server 2003 podem lidar incorretamente com pastas que não têm essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a3039-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="a3039-119">Essas propriedades podem ser atribuídas aos valores de cadeia de caracteres na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="a3039-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="a3039-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a3039-120">**Value**</span></span>|<span data-ttu-id="a3039-121">**Conteúdo da pasta**</span><span class="sxs-lookup"><span data-stu-id="a3039-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a3039-122">IPF. Compromisso</span><span class="sxs-lookup"><span data-stu-id="a3039-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="a3039-123">Compromissos</span><span class="sxs-lookup"><span data-stu-id="a3039-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="a3039-124">IPF. Contato</span><span class="sxs-lookup"><span data-stu-id="a3039-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="a3039-125">Contatos</span><span class="sxs-lookup"><span data-stu-id="a3039-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="a3039-126">IPF. Diário</span><span class="sxs-lookup"><span data-stu-id="a3039-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="a3039-127">Entradas de Diário do Outlook</span><span class="sxs-lookup"><span data-stu-id="a3039-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="a3039-128">IPF. Observação</span><span class="sxs-lookup"><span data-stu-id="a3039-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="a3039-129">Mensagens de Email e anotações</span><span class="sxs-lookup"><span data-stu-id="a3039-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="a3039-130">IPF. StickyNote</span><span class="sxs-lookup"><span data-stu-id="a3039-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="a3039-131">Observações Desaderentadas do Outlook</span><span class="sxs-lookup"><span data-stu-id="a3039-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="a3039-132">IPF. Tarefa</span><span class="sxs-lookup"><span data-stu-id="a3039-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="a3039-133">Tarefas do Outlook</span><span class="sxs-lookup"><span data-stu-id="a3039-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="a3039-134">Para pastas que contêm mensagens de email, essas propriedades devem ser definidas como IPF. Observação.</span><span class="sxs-lookup"><span data-stu-id="a3039-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a3039-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3039-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a3039-136">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a3039-136">Protocol specifications</span></span>

<span data-ttu-id="a3039-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3039-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3039-138">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a3039-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a3039-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3039-139">[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3039-140">Especifica as propriedades e operações para criar e localizar as pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="a3039-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="a3039-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3039-141">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3039-142">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="a3039-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="a3039-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a3039-143">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a3039-144">Especifica as propriedades e operações que são permitidas para contatos e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="a3039-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a3039-145">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="a3039-145">Header files</span></span>

<span data-ttu-id="a3039-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a3039-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="a3039-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a3039-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="a3039-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a3039-148">Mapitags.h</span></span>
  
> <span data-ttu-id="a3039-149">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a3039-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3039-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3039-150">See also</span></span>



[<span data-ttu-id="a3039-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a3039-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a3039-152">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="a3039-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a3039-153">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a3039-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a3039-154">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a3039-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

