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
ms.openlocfilehash: 5a3a83153dc799154edc6a46946682684cad8a09
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593769"
---
# <a name="pidtagcontainerclass-canonical-property"></a><span data-ttu-id="fec5f-103">Propriedade canônica PidTagContainerClass</span><span class="sxs-lookup"><span data-stu-id="fec5f-103">PidTagContainerClass Canonical Property</span></span>

  
  
<span data-ttu-id="fec5f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fec5f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fec5f-105">Contém uma cadeia de caracteres de texto descrevendo o tipo de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="fec5f-105">Contains a text string describing the type of a folder.</span></span> <span data-ttu-id="fec5f-106">Embora esta propriedade é ignorada em geral, as versões do Microsoft® Exchange Server antes do Gerenciador de caixa de correio do Exchange Server 2003 esperam essa propriedade estar presentes.</span><span class="sxs-lookup"><span data-stu-id="fec5f-106">Although this property is generally ignored, versions of Microsoft® Exchange Server prior to Exchange Server 2003 Mailbox Manager expect this property to be present.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fec5f-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fec5f-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="fec5f-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="fec5f-108">PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="fec5f-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fec5f-109">Identifier:</span></span>  <br/> |<span data-ttu-id="fec5f-110">0x3613</span><span class="sxs-lookup"><span data-stu-id="fec5f-110">0x3613</span></span>  <br/> |
|<span data-ttu-id="fec5f-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fec5f-111">Data type:</span></span>  <br/> |<span data-ttu-id="fec5f-112">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fec5f-112">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fec5f-113">Área:</span><span class="sxs-lookup"><span data-stu-id="fec5f-113">Area:</span></span>  <br/> |<span data-ttu-id="fec5f-114">Container</span><span class="sxs-lookup"><span data-stu-id="fec5f-114">Container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fec5f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="fec5f-115">Remarks</span></span>

<span data-ttu-id="fec5f-116">Normalmente, essas propriedades não são usadas pelo Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fec5f-116">These properties are not normally used by Exchange Server.</span></span> <span data-ttu-id="fec5f-117">No entanto, Microsoft Office Outlook® anexa-los às pastas de caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="fec5f-117">However, Microsoft Office Outlook® attaches them to mailbox folders.</span></span> <span data-ttu-id="fec5f-118">Além disso, as versões do Exchange Server antes do Gerenciador de caixa de correio do Exchange Server 2003 incorretamente podem tratar de pastas que não tenham essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fec5f-118">In addition, versions of Exchange Server prior to Exchange Server 2003 Mailbox Manager might incorrectly handle folders that do not have these properties.</span></span>
  
<span data-ttu-id="fec5f-119">Os valores de cadeia de caracteres na tabela a seguir podem ser atribuídas a essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fec5f-119">These properties can be assigned the string values in the following table.</span></span>
  
|<span data-ttu-id="fec5f-120">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fec5f-120">**Value**</span></span>|<span data-ttu-id="fec5f-121">**Conteúdo da pasta**</span><span class="sxs-lookup"><span data-stu-id="fec5f-121">**Contents of Folder**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fec5f-122">FALHA DE PÁGINA INVÁLIDA. Compromisso</span><span class="sxs-lookup"><span data-stu-id="fec5f-122">IPF.Appointment</span></span>  <br/> |<span data-ttu-id="fec5f-123">Compromissos</span><span class="sxs-lookup"><span data-stu-id="fec5f-123">Appointments</span></span>  <br/> |
|<span data-ttu-id="fec5f-124">FALHA DE PÁGINA INVÁLIDA. Contato</span><span class="sxs-lookup"><span data-stu-id="fec5f-124">IPF.Contact</span></span>  <br/> |<span data-ttu-id="fec5f-125">Contatos</span><span class="sxs-lookup"><span data-stu-id="fec5f-125">Contacts</span></span>  <br/> |
|<span data-ttu-id="fec5f-126">FALHA DE PÁGINA INVÁLIDA. Diário</span><span class="sxs-lookup"><span data-stu-id="fec5f-126">IPF.Journal</span></span>  <br/> |<span data-ttu-id="fec5f-127">Entradas de diário do Outlook</span><span class="sxs-lookup"><span data-stu-id="fec5f-127">Outlook Journal entries</span></span>  <br/> |
|<span data-ttu-id="fec5f-128">FALHA DE PÁGINA INVÁLIDA. Observação</span><span class="sxs-lookup"><span data-stu-id="fec5f-128">IPF.Note</span></span>  <br/> |<span data-ttu-id="fec5f-129">Mensagens de email e notas</span><span class="sxs-lookup"><span data-stu-id="fec5f-129">Mail Messages and notes</span></span>  <br/> |
|<span data-ttu-id="fec5f-130">FALHA DE PÁGINA INVÁLIDA. StickyNote</span><span class="sxs-lookup"><span data-stu-id="fec5f-130">IPF.StickyNote</span></span>  <br/> |<span data-ttu-id="fec5f-131">Notas Autoadesivas do Outlook</span><span class="sxs-lookup"><span data-stu-id="fec5f-131">Outlook Sticky Notes</span></span>  <br/> |
|<span data-ttu-id="fec5f-132">FALHA DE PÁGINA INVÁLIDA. Tarefa</span><span class="sxs-lookup"><span data-stu-id="fec5f-132">IPF.Task</span></span>  <br/> |<span data-ttu-id="fec5f-133">Tarefas do Outlook</span><span class="sxs-lookup"><span data-stu-id="fec5f-133">Outlook Tasks</span></span>  <br/> |
   
<span data-ttu-id="fec5f-134">Para pastas que contêm mensagens de email, essas propriedades devem ser definidas como falha de página inválida. Nota.</span><span class="sxs-lookup"><span data-stu-id="fec5f-134">For folders that contain mail messages, these properties should be set to IPF.Note.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fec5f-135">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fec5f-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fec5f-136">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fec5f-136">Protocol specifications</span></span>

<span data-ttu-id="fec5f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fec5f-137">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fec5f-138">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="fec5f-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fec5f-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fec5f-139">[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fec5f-140">Especifica as propriedades e operações para a criação e a localização de pastas especiais em uma caixa de correio.</span><span class="sxs-lookup"><span data-stu-id="fec5f-140">Specifies the properties and operations for creating and locating the special folders in a mailbox.</span></span>
    
<span data-ttu-id="fec5f-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fec5f-141">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fec5f-142">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="fec5f-142">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="fec5f-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fec5f-143">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fec5f-144">Especifica as propriedades e operações que são permitidas para contato e objetos de lista de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="fec5f-144">Specifies the properties and operations that are permissible for contact and personal distribution list objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fec5f-145">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fec5f-145">Header files</span></span>

<span data-ttu-id="fec5f-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fec5f-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="fec5f-147">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fec5f-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="fec5f-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fec5f-148">Mapitags.h</span></span>
  
> <span data-ttu-id="fec5f-149">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fec5f-149">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fec5f-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="fec5f-150">See also</span></span>



[<span data-ttu-id="fec5f-151">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fec5f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fec5f-152">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fec5f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fec5f-153">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fec5f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fec5f-154">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fec5f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

