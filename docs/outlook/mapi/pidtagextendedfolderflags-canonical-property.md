---
title: Propriedade canônica PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382656"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="53da9-103">Propriedade canônica PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="53da9-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="53da9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53da9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53da9-105">Contém os sinalizadores estendidos sobre uma pasta.</span><span class="sxs-lookup"><span data-stu-id="53da9-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="53da9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="53da9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="53da9-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="53da9-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="53da9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="53da9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="53da9-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="53da9-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="53da9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="53da9-110">Data type:</span></span>  <br/> |<span data-ttu-id="53da9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="53da9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="53da9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="53da9-112">Area:</span></span>  <br/> |<span data-ttu-id="53da9-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="53da9-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53da9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="53da9-114">Remarks</span></span>

<span data-ttu-id="53da9-115">Essa propriedade é um fluxo binário que contém propriedades sub-recurso codificadas para a pasta.</span><span class="sxs-lookup"><span data-stu-id="53da9-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="53da9-116">Ele é formatado como uma série de itens de sub de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="53da9-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="53da9-117">Os primeiros 8 bits do item sub é um campo de ID, que indica que tipo de sinalizador o item de sub representa.</span><span class="sxs-lookup"><span data-stu-id="53da9-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="53da9-118">Os segundo 8 bits é o número de bytes de dados que seguem.</span><span class="sxs-lookup"><span data-stu-id="53da9-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="53da9-119">Os valores de ID possíveis incluem:</span><span class="sxs-lookup"><span data-stu-id="53da9-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="53da9-120">Inválido</span><span class="sxs-lookup"><span data-stu-id="53da9-120">Invalid</span></span>
    
   <span data-ttu-id="53da9-121">Não use esse valor</span><span class="sxs-lookup"><span data-stu-id="53da9-121">Do not use this value</span></span>
    
- <span data-ttu-id="53da9-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="53da9-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="53da9-123">Os dados são um valor de quatro bytes formatado como:</span><span class="sxs-lookup"><span data-stu-id="53da9-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="53da9-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="53da9-124">**Bits**</span></span>|<span data-ttu-id="53da9-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="53da9-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="53da9-126">0-1</span><span class="sxs-lookup"><span data-stu-id="53da9-126">0-1</span></span>  <br/> |<span data-ttu-id="53da9-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="53da9-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="53da9-128">2</span><span class="sxs-lookup"><span data-stu-id="53da9-128">2</span></span>  <br/> |<span data-ttu-id="53da9-129">Defina como 0 se o aplicativo deve mostrar uma descrição da política.</span><span class="sxs-lookup"><span data-stu-id="53da9-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="53da9-130">3 a 5</span><span class="sxs-lookup"><span data-stu-id="53da9-130">3-5</span></span>  <br/> |<span data-ttu-id="53da9-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="53da9-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="53da9-132">6 e 7</span><span class="sxs-lookup"><span data-stu-id="53da9-132">6-7</span></span>  <br/> |<span data-ttu-id="53da9-133">Controla a exibição do número de mensagens na pasta.</span><span class="sxs-lookup"><span data-stu-id="53da9-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="53da9-134">0 - use a configuração padrão</span><span class="sxs-lookup"><span data-stu-id="53da9-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="53da9-135">1 - use o número de mensagens não lidas</span><span class="sxs-lookup"><span data-stu-id="53da9-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="53da9-136">3 - use o número total de mensagens</span><span class="sxs-lookup"><span data-stu-id="53da9-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="53da9-137">8-31</span><span class="sxs-lookup"><span data-stu-id="53da9-137">8-31</span></span>  <br/> |<span data-ttu-id="53da9-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="53da9-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="53da9-139">Itens reservados podem ser ignorados, mas os valores existentes devem ser preservados.</span><span class="sxs-lookup"><span data-stu-id="53da9-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="53da9-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="53da9-140">SearchFolderID</span></span>
    
   <span data-ttu-id="53da9-141">O campo de dados é um campo de 16 bytes.</span><span class="sxs-lookup"><span data-stu-id="53da9-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="53da9-142">Quando o aplicativo cria uma pasta de pesquisa persistente, defina esse campo na pasta para o mesmo valor que o **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) uma propriedade binária na mensagem de pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="53da9-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="53da9-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="53da9-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="53da9-144">O campo de dados é um campo de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="53da9-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="53da9-145">Quando o aplicativo cria a pasta de pesquisa de tarefas pendentes, ele deve definir o valor desse campo na pasta para o valor inteiro de pouca-endian da "0x000c0000":</span><span class="sxs-lookup"><span data-stu-id="53da9-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="53da9-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="53da9-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="53da9-147">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="53da9-147">Protocol specifications</span></span>

<span data-ttu-id="53da9-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53da9-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53da9-149">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="53da9-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="53da9-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53da9-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53da9-151">Especifica o local e as propriedades de dados de configuração de cliente e servidor, como listas de categoria compartilhada e o horário de trabalho.</span><span class="sxs-lookup"><span data-stu-id="53da9-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="53da9-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="53da9-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="53da9-153">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="53da9-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="53da9-154">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="53da9-154">Header files</span></span>

<span data-ttu-id="53da9-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="53da9-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="53da9-156">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="53da9-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="53da9-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="53da9-157">Mapitags.h</span></span>
  
> <span data-ttu-id="53da9-158">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="53da9-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53da9-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="53da9-159">See also</span></span>

- [<span data-ttu-id="53da9-160">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="53da9-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="53da9-161">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="53da9-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="53da9-162">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="53da9-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="53da9-163">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="53da9-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

