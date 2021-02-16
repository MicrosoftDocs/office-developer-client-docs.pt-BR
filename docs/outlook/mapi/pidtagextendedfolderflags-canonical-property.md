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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316349"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a><span data-ttu-id="dfc1c-103">Propriedade canônica PidTagExtendedFolderFlags</span><span class="sxs-lookup"><span data-stu-id="dfc1c-103">PidTagExtendedFolderFlags Canonical Property</span></span>
 
<span data-ttu-id="dfc1c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc1c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc1c-105">Contém sinalizadores estendidos sobre uma pasta.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-105">Contains extended flags about a folder.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc1c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dfc1c-107">PR_EXTENDED_FOLDER_FLAGS</span><span class="sxs-lookup"><span data-stu-id="dfc1c-107">PR_EXTENDED_FOLDER_FLAGS</span></span>  <br/> |
|<span data-ttu-id="dfc1c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dfc1c-109">0x36DA</span><span class="sxs-lookup"><span data-stu-id="dfc1c-109">0x36DA</span></span>  <br/> |
|<span data-ttu-id="dfc1c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-110">Data type:</span></span>  <br/> |<span data-ttu-id="dfc1c-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dfc1c-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dfc1c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-112">Area:</span></span>  <br/> |<span data-ttu-id="dfc1c-113">Contêiner MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc1c-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dfc1c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc1c-114">Remarks</span></span>

<span data-ttu-id="dfc1c-115">Essa propriedade é um fluxo binário que contém sub-propriedades codificadas para a pasta.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-115">This property is a binary stream that contains encoded sub-properties for the folder.</span></span> <span data-ttu-id="dfc1c-116">Ele é formatado como uma série de subsistros de comprimento variável.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-116">It is formatted as a series of variable length sub items.</span></span> <span data-ttu-id="dfc1c-117">Os primeiros 8 bits do sub item é um campo de ID, que indica que tipo de sinalizador o sub item representa.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-117">The first 8 bits of the sub item is an ID field, which indicates what kind of flag the sub item represents.</span></span> <span data-ttu-id="dfc1c-118">O segundo 8 bits é o número de bytes de dados a seguir.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-118">The second 8 bits is the number of bytes of data that follow.</span></span>
  
<span data-ttu-id="dfc1c-119">Os valores possíveis de ID incluem:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-119">Possible ID values include:</span></span>
  
- <span data-ttu-id="dfc1c-120">Invalid</span><span class="sxs-lookup"><span data-stu-id="dfc1c-120">Invalid</span></span>
    
   <span data-ttu-id="dfc1c-121">Não use esse valor</span><span class="sxs-lookup"><span data-stu-id="dfc1c-121">Do not use this value</span></span>
    
- <span data-ttu-id="dfc1c-122">ExtendedFlags</span><span class="sxs-lookup"><span data-stu-id="dfc1c-122">ExtendedFlags</span></span>
    
   <span data-ttu-id="dfc1c-123">Os dados são um valor de quatro byte formatado como:</span><span class="sxs-lookup"><span data-stu-id="dfc1c-123">The data is a four byte value formatted as:</span></span>
    
   |<span data-ttu-id="dfc1c-124">**Bits**</span><span class="sxs-lookup"><span data-stu-id="dfc1c-124">**Bits**</span></span>|<span data-ttu-id="dfc1c-125">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="dfc1c-125">**Description**</span></span>|
   |:-----|:-----|
   |<span data-ttu-id="dfc1c-126">0-1</span><span class="sxs-lookup"><span data-stu-id="dfc1c-126">0-1</span></span>  <br/> |<span data-ttu-id="dfc1c-127">Reservado.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-127">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="dfc1c-128">2 </span><span class="sxs-lookup"><span data-stu-id="dfc1c-128">2</span></span>  <br/> |<span data-ttu-id="dfc1c-129">De definida como 0 se o aplicativo deve mostrar uma descrição de política.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-129">Set to 0 if the application should show a policy description.</span></span>  <br/> |
   |<span data-ttu-id="dfc1c-130">3-5</span><span class="sxs-lookup"><span data-stu-id="dfc1c-130">3-5</span></span>  <br/> |<span data-ttu-id="dfc1c-131">Reservado.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-131">Reserved.</span></span>  <br/> |
   |<span data-ttu-id="dfc1c-132">6-7</span><span class="sxs-lookup"><span data-stu-id="dfc1c-132">6-7</span></span>  <br/> |<span data-ttu-id="dfc1c-133">Controla a exibição do número de mensagens na pasta.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-133">Controls the display of the number of messages in the folder.</span></span>  <br/> <span data-ttu-id="dfc1c-134">0 - Usar a configuração padrão</span><span class="sxs-lookup"><span data-stu-id="dfc1c-134">0 - Use the default setting</span></span>  <br/> <span data-ttu-id="dfc1c-135">1 - Usar o número de mensagens não lidas</span><span class="sxs-lookup"><span data-stu-id="dfc1c-135">1 - Use the number of unread messages</span></span>  <br/> <span data-ttu-id="dfc1c-136">3 - Usar o número total de mensagens</span><span class="sxs-lookup"><span data-stu-id="dfc1c-136">3 - Use the total number of messages</span></span>  <br/> |
   |<span data-ttu-id="dfc1c-137">8-31</span><span class="sxs-lookup"><span data-stu-id="dfc1c-137">8-31</span></span>  <br/> |<span data-ttu-id="dfc1c-138">Reservado.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-138">Reserved.</span></span>  <br/> |
   
<span data-ttu-id="dfc1c-139">Os itens reservados podem ser ignorados, mas os valores existentes devem ser preservados.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-139">Reserved items can be ignored, but existing values must be preserved.</span></span>
    
- <span data-ttu-id="dfc1c-140">SearchFolderID</span><span class="sxs-lookup"><span data-stu-id="dfc1c-140">SearchFolderID</span></span>
    
   <span data-ttu-id="dfc1c-141">O campo de dados é um campo de 16 byte.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-141">The data field is a 16-byte field.</span></span> <span data-ttu-id="dfc1c-142">Quando o aplicativo cria uma pasta de pesquisa persistente, ele deve definir esse campo na pasta com o mesmo valor que a propriedade binária **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) na Mensagem da Pasta de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-142">When the application creates a persistent search folder, it must set this field on the folder to the same value as the **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) binary property on the Search Folder Message.</span></span>
    
- <span data-ttu-id="dfc1c-143">ToDoFolderVersion</span><span class="sxs-lookup"><span data-stu-id="dfc1c-143">ToDoFolderVersion</span></span>
    
   <span data-ttu-id="dfc1c-144">O campo de dados é um campo de 4 byte.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-144">The data field is a 4-byte field.</span></span> <span data-ttu-id="dfc1c-145">Quando o aplicativo cria a pasta de pesquisa de fazer, ele deve definir o valor desse campo na pasta como o valor inteiro little-endian de" 0x000c0000":</span><span class="sxs-lookup"><span data-stu-id="dfc1c-145">When the application creates the to-do search folder, it must set the value of this field on the folder to the little-endian integer value of" 0x000c0000":</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="dfc1c-146">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dfc1c-146">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="dfc1c-147">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="dfc1c-147">Protocol specifications</span></span>

<span data-ttu-id="dfc1c-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfc1c-148">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfc1c-149">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-149">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="dfc1c-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfc1c-150">[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfc1c-151">Especifica o local e as propriedades dos dados de configuração do cliente e do servidor, como listas de categorias compartilhadas e horas de trabalho.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-151">Specifies the location and properties of client and server configuration data, such as shared category lists and working hours.</span></span>
    
<span data-ttu-id="dfc1c-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="dfc1c-152">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="dfc1c-153">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-153">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="dfc1c-154">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="dfc1c-154">Header files</span></span>

<span data-ttu-id="dfc1c-155">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="dfc1c-155">Mapidefs.h</span></span>
  
> <span data-ttu-id="dfc1c-156">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-156">Provides data type definitions.</span></span>
    
<span data-ttu-id="dfc1c-157">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="dfc1c-157">Mapitags.h</span></span>
  
> <span data-ttu-id="dfc1c-158">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="dfc1c-158">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dfc1c-159">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc1c-159">See also</span></span>

- [<span data-ttu-id="dfc1c-160">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc1c-160">MAPI Properties</span></span>](mapi-properties.md)
- [<span data-ttu-id="dfc1c-161">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc1c-161">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
- [<span data-ttu-id="dfc1c-162">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc1c-162">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
- [<span data-ttu-id="dfc1c-163">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dfc1c-163">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

