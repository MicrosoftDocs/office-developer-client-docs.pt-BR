---
title: Propriedade canônica PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768482"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="215aa-103">Propriedade canônica PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="215aa-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="215aa-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="215aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="215aa-105">Especifica como gerar e recalcular o valor da propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) quando alterar propriedades de nome de outro contato.</span><span class="sxs-lookup"><span data-stu-id="215aa-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="215aa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="215aa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="215aa-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="215aa-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="215aa-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="215aa-108">Property set:</span></span>  <br/> |<span data-ttu-id="215aa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="215aa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="215aa-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="215aa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="215aa-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="215aa-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="215aa-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="215aa-112">Data type:</span></span>  <br/> |<span data-ttu-id="215aa-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="215aa-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="215aa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="215aa-114">Area:</span></span>  <br/> |<span data-ttu-id="215aa-115">Contato</span><span class="sxs-lookup"><span data-stu-id="215aa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="215aa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="215aa-116">Remarks</span></span>

<span data-ttu-id="215aa-117">Se essa propriedade estiver faltando ou definida como um valor que não são detalhado na tabela a seguir ou em [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), o aplicativo pode escolher sua própria lógica recalcular o valor do **dispidFileUnder** como outra alteração de propriedades do nome do contato.</span><span class="sxs-lookup"><span data-stu-id="215aa-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="215aa-118">Na tabela a seguir, a notação <PropertyName> é usado para especificar "o valor de PropertyName".</span><span class="sxs-lookup"><span data-stu-id="215aa-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="215aa-119">Por exemplo, se o valor da propriedade **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) é "Smith", e o valor da propriedade **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) é "Ben", em seguida, "<PidTagGivenName> <PidTagSurname>" Especifica a cadeia de caracteres "Ben Smith".</span><span class="sxs-lookup"><span data-stu-id="215aa-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="215aa-120">Na tabela, "\r" Especifica um caractere de retorno de carro, "\n." Especifica um caractere de alimentação de linha, e <space> representa um caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="215aa-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="215aa-121">**Valor da propriedade **dispidFileUnderId****</span><span class="sxs-lookup"><span data-stu-id="215aa-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="215aa-122">**Descrição da propriedade **dispidFileUnder****</span><span class="sxs-lookup"><span data-stu-id="215aa-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="215aa-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="215aa-123">0x00000000</span></span>  <br/> |<span data-ttu-id="215aa-124">PT_UNICODE vazia.</span><span class="sxs-lookup"><span data-stu-id="215aa-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="215aa-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="215aa-125">0x00003001</span></span>  <br/> |<span data-ttu-id="215aa-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="215aa-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="215aa-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="215aa-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="215aa-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="215aa-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="215aa-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="215aa-133">0x00008017</span></span>  <br/> |<span data-ttu-id="215aa-134">"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="215aa-135">0x00008018</span></span>  <br/> |<span data-ttu-id="215aa-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="215aa-137">0x00008019</span></span>  <br/> |<span data-ttu-id="215aa-138">"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="215aa-139">0x00008030</span></span>  <br/> |<span data-ttu-id="215aa-140">"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="215aa-141">0x00008031</span></span>  <br/> |<span data-ttu-id="215aa-142">"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="215aa-143">0x00008032</span></span>  <br/> |<span data-ttu-id="215aa-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="215aa-145">0x00008033</span></span>  <br/> |<span data-ttu-id="215aa-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="215aa-147">0x00008034</span></span>  <br/> |<span data-ttu-id="215aa-148">"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="215aa-149">0x00008035</span></span>  <br/> |<span data-ttu-id="215aa-150">"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="215aa-151">0x00008036</span></span>  <br/> |<span data-ttu-id="215aa-152">"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="215aa-153">0x00008037</span></span>  <br/> |<span data-ttu-id="215aa-154">"\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagSurname\>\<espaço\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="215aa-155">0x00008038</span></span>  <br/> |<span data-ttu-id="215aa-156">"\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>\<PidTagMiddleName\>\<espaço\>\<PidTagGeneration\>"</span><span class="sxs-lookup"><span data-stu-id="215aa-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="215aa-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="215aa-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="215aa-158">Especifica que, ao exibir o contato, o aplicativo deve tentar usar o valor atual do **dispidFileUnder** e outras propriedades de contato para encontrar uma "melhor correspondência" para **dispidFileUnderId** para um dos valores anteriores nesta tabela.</span><span class="sxs-lookup"><span data-stu-id="215aa-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="215aa-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="215aa-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="215aa-160">Especifica que, ao exibir o contato, o aplicativo deve escolher os valores padrão adequado (de acordo com a localidade do idioma) para **dispidFileUnderId** e **dispidFileUnder** para coincidir com a opção de atualização.</span><span class="sxs-lookup"><span data-stu-id="215aa-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="215aa-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="215aa-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="215aa-162">**dispidFileUnder** é um PT_UNICODE fornecido pelo usuário e não deve ser alterado quando outra propriedade de nome do contato é alterada.</span><span class="sxs-lookup"><span data-stu-id="215aa-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="215aa-163">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="215aa-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="215aa-164">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="215aa-164">Protocol specifications</span></span>

<span data-ttu-id="215aa-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="215aa-165">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="215aa-166">Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="215aa-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="215aa-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="215aa-167">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="215aa-168">Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="215aa-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="215aa-169">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="215aa-169">Header files</span></span>

<span data-ttu-id="215aa-170">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="215aa-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="215aa-171">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="215aa-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="215aa-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="215aa-172">See also</span></span>



[<span data-ttu-id="215aa-173">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="215aa-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="215aa-174">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="215aa-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="215aa-175">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="215aa-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="215aa-176">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="215aa-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
