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
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355703"
---
# <a name="pidlidfileunderid-canonical-property"></a><span data-ttu-id="00bfa-103">Propriedade canônica PidLidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="00bfa-103">PidLidFileUnderId Canonical Property</span></span>

  
  
<span data-ttu-id="00bfa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00bfa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00bfa-105">Especifica como gerar e recalcular o valor da propriedade **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) quando outras propriedades de nome de contato são alteradas.</span><span class="sxs-lookup"><span data-stu-id="00bfa-105">Specifies how to generate and recompute the value of the **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) property when other contact name properties change.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00bfa-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="00bfa-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00bfa-107">dispidFileUnderId</span><span class="sxs-lookup"><span data-stu-id="00bfa-107">dispidFileUnderId</span></span>  <br/> |
|<span data-ttu-id="00bfa-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="00bfa-108">Property set:</span></span>  <br/> |<span data-ttu-id="00bfa-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="00bfa-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="00bfa-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="00bfa-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="00bfa-111">0x00008006</span><span class="sxs-lookup"><span data-stu-id="00bfa-111">0x00008006</span></span>  <br/> |
|<span data-ttu-id="00bfa-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="00bfa-112">Data type:</span></span>  <br/> |<span data-ttu-id="00bfa-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00bfa-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00bfa-114">Área:</span><span class="sxs-lookup"><span data-stu-id="00bfa-114">Area:</span></span>  <br/> |<span data-ttu-id="00bfa-115">Contato</span><span class="sxs-lookup"><span data-stu-id="00bfa-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00bfa-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="00bfa-116">Remarks</span></span>

<span data-ttu-id="00bfa-117">Se essa propriedade estiver ausente ou definida como um valor não detalhado na tabela abaixo ou em [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), o aplicativo poderá escolher sua própria lógica para recalcular o valor do **dispidFileUnder** à medida que outras propriedades de nome de contato forem alteradas.</span><span class="sxs-lookup"><span data-stu-id="00bfa-117">If this property is missing or set to a value not detailed in the table below or in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), the application can choose its own logic to recompute the value of the **dispidFileUnder** as other contact name properties change.</span></span> 
  
<span data-ttu-id="00bfa-118">Na tabela a seguir, a notação <PropertyName> é usada para especificar "o valor de PropertyName".</span><span class="sxs-lookup"><span data-stu-id="00bfa-118">In the following table, the notation <PropertyName> is used to specify "the value of PropertyName".</span></span> <span data-ttu-id="00bfa-119">Por exemplo, se o valor da propriedade **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) for "Smith" e o valor da propriedade **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) for "Ben", então "<PidTagGivenName> <PidTagSurname>" especifica a cadeia de caracteres "Ben Smith".</span><span class="sxs-lookup"><span data-stu-id="00bfa-119">For example, if the value of the **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) property is "Smith", and the value of the **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) property is "Ben", then "<PidTagGivenName> <PidTagSurname>" specifies the string "Ben Smith".</span></span> <span data-ttu-id="00bfa-120">Na tabela, "\r" especifica um caractere de retorno de carro, "\n" especifica um caractere de alimentação de linha <space> e representa um caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="00bfa-120">In the table, "\r" specifies a carriage return character, "\n" specifies a line-feed character, and <space> represents a space character.</span></span>
  
|<span data-ttu-id="00bfa-121">\*\*Valor da propriedade \*\*dispidFileUnderId\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00bfa-121">**Value of the **dispidFileUnderId** property**</span></span>|<span data-ttu-id="00bfa-122">\*\*Descrição da propriedade \*\*dispidFileUnder\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="00bfa-122">**Description of the **dispidFileUnder** property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00bfa-123">0x00000000</span><span class="sxs-lookup"><span data-stu-id="00bfa-123">0x00000000</span></span>  <br/> |<span data-ttu-id="00bfa-124">PT_UNICODE vazio.</span><span class="sxs-lookup"><span data-stu-id="00bfa-124">Empty PT_UNICODE.</span></span>  <br/> |
|<span data-ttu-id="00bfa-125">0x00003001</span><span class="sxs-lookup"><span data-stu-id="00bfa-125">0x00003001</span></span>  <br/> |<span data-ttu-id="00bfa-126">"\<PidTagDisplayName\>"</span><span class="sxs-lookup"><span data-stu-id="00bfa-126">"\<PidTagDisplayName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-127">0x00003A06</span><span class="sxs-lookup"><span data-stu-id="00bfa-127">0x00003A06</span></span>  <br/> |<span data-ttu-id="00bfa-128">"\<PidTagGivenName\>"</span><span class="sxs-lookup"><span data-stu-id="00bfa-128">"\<PidTagGivenName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-129">0x00003A11</span><span class="sxs-lookup"><span data-stu-id="00bfa-129">0x00003A11</span></span>  <br/> |<span data-ttu-id="00bfa-130">"\<PidTagSurname\>"</span><span class="sxs-lookup"><span data-stu-id="00bfa-130">"\<PidTagSurname\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-131">0x00003A16</span><span class="sxs-lookup"><span data-stu-id="00bfa-131">0x00003A16</span></span>  <br/> |<span data-ttu-id="00bfa-132">"\<PidTagCompanyName\>"</span><span class="sxs-lookup"><span data-stu-id="00bfa-132">"\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-133">0x00008017</span><span class="sxs-lookup"><span data-stu-id="00bfa-133">0x00008017</span></span>  <br/> |<span data-ttu-id="00bfa-134">"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\<espaço\>"\<\></span><span class="sxs-lookup"><span data-stu-id="00bfa-134">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-135">0x00008018</span><span class="sxs-lookup"><span data-stu-id="00bfa-135">0x00008018</span></span>  <br/> |<span data-ttu-id="00bfa-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<\>\<\>espaço PidTagGivenName\<espaço\>PidTagMiddleName\>"\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-136">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-137">0x00008019</span><span class="sxs-lookup"><span data-stu-id="00bfa-137">0x00008019</span></span>  <br/> |<span data-ttu-id="00bfa-138">"\<PidTagSurname\>,\<espaço\>\<PidTagGivenName\>\>espaço PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-138">"\<PidTagSurname\>,\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-139">0x00008030</span><span class="sxs-lookup"><span data-stu-id="00bfa-139">0x00008030</span></span>  <br/> |<span data-ttu-id="00bfa-140">"\<PidTagSurname\>\<de\>\<espaço\>PidTagGivenName PidTagMiddleName\>"\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-140">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-141">0x00008031</span><span class="sxs-lookup"><span data-stu-id="00bfa-141">0x00008031</span></span>  <br/> |<span data-ttu-id="00bfa-142">"\<PidTagSurname\>\<\<espaço PidTagGivenName\>espaço\>PidTagMiddleName\>"\>\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-142">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-143">0x00008032</span><span class="sxs-lookup"><span data-stu-id="00bfa-143">0x00008032</span></span>  <br/> |<span data-ttu-id="00bfa-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espaço\>"\<\></span><span class="sxs-lookup"><span data-stu-id="00bfa-144">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-145">0x00008033</span><span class="sxs-lookup"><span data-stu-id="00bfa-145">0x00008033</span></span>  <br/> |<span data-ttu-id="00bfa-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<\<espaço PidTagGivenName\>espaço\>PidTagMiddleName\>"\>\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-146">"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-147">0x00008034</span><span class="sxs-lookup"><span data-stu-id="00bfa-147">0x00008034</span></span>  <br/> |<span data-ttu-id="00bfa-148">"\<PidTagSurname\>\<PidTagGivenName\>\>espaço PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-148">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-149">0x00008035</span><span class="sxs-lookup"><span data-stu-id="00bfa-149">0x00008035</span></span>  <br/> |<span data-ttu-id="00bfa-150">"\<PidTagSurname\>\<\<\>espaço PidTagGivenName\>espaço\>PidTagMiddleName\>\r\n\<PidTagCompanyName"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-150">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-151">0x00008036</span><span class="sxs-lookup"><span data-stu-id="00bfa-151">0x00008036</span></span>  <br/> |<span data-ttu-id="00bfa-152">"\<Espaço\>\<PidTagSurname\>\>\>PidTagGivenName\>\>espaço PidTagMiddleName\<espaço\>PidTagGeneration\<"\<\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-152">"\<PidTagSurname\>\<space\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-153">0x00008037</span><span class="sxs-lookup"><span data-stu-id="00bfa-153">0x00008037</span></span>  <br/> |<span data-ttu-id="00bfa-154">"\<Espaço\>\<PidTagGivenName\>\>\>PidTagMiddleName\>\>espaço PidTagSurname\<espaço\>PidTagGeneration\<"\<\<\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-154">"\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagSurname\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-155">0x00008038</span><span class="sxs-lookup"><span data-stu-id="00bfa-155">0x00008038</span></span>  <br/> |<span data-ttu-id="00bfa-156">"\<PidTagSurname\>\<espaço\>\<PidTagGivenName\>espaço\<PidTagMiddleName\>\>PidTagGeneration"\<\>\<</span><span class="sxs-lookup"><span data-stu-id="00bfa-156">"\<PidTagSurname\>\<PidTagGivenName\>\<space\>\<PidTagMiddleName\>\<space\>\<PidTagGeneration\>"</span></span>  <br/> |
|<span data-ttu-id="00bfa-157">0xfffffffd</span><span class="sxs-lookup"><span data-stu-id="00bfa-157">0xfffffffd</span></span>  <br/> |<span data-ttu-id="00bfa-158">Especifica que, ao exibir o contato, o aplicativo deve tentar usar o valor atual de **dispidFileUnder** e outras propriedades de contato para localizar uma "melhor correspondência" para o **dispidFileUnderId** para um dos valores anteriores desta tabela.</span><span class="sxs-lookup"><span data-stu-id="00bfa-158">Specifies that, when displaying the contact, the application should attempt to use the current value of **dispidFileUnder** and other contact properties to find a "best match" for **dispidFileUnderId** to one of the previous values in this table.</span></span>  <br/> |
|<span data-ttu-id="00bfa-159">0xFFFFFFFE</span><span class="sxs-lookup"><span data-stu-id="00bfa-159">0xfffffffe</span></span>  <br/> |<span data-ttu-id="00bfa-160">Especifica que, ao exibir o contato, o aplicativo deve escolher os valores padrão apropriados (de acordo com a localidade do idioma) para **dispidFileUnderId** e atualizar **dispidFileUnder** para corresponder à opção.</span><span class="sxs-lookup"><span data-stu-id="00bfa-160">Specifies that, when displaying the contact, the application should choose the appropriate default values (according to the language locale) for **dispidFileUnderId** and update **dispidFileUnder** to match the choice.</span></span>  <br/> |
|<span data-ttu-id="00bfa-161">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="00bfa-161">0xffffffff</span></span>  <br/> |<span data-ttu-id="00bfa-162">**dispidFileUnder** é um PT_UNICODE fornecido pelo usuário e não deve ser alterado quando outra propriedade de nome de contato é alterada.</span><span class="sxs-lookup"><span data-stu-id="00bfa-162">**dispidFileUnder** is a user-provided PT_UNICODE, and should not be changed when another contact name property changes.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="00bfa-163">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="00bfa-163">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00bfa-164">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="00bfa-164">Protocol specifications</span></span>

<span data-ttu-id="00bfa-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00bfa-165">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00bfa-166">Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="00bfa-166">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="00bfa-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00bfa-167">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00bfa-168">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="00bfa-168">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00bfa-169">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00bfa-169">Header files</span></span>

<span data-ttu-id="00bfa-170">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="00bfa-170">Mapidefs.h</span></span>
  
> <span data-ttu-id="00bfa-171">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00bfa-171">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00bfa-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="00bfa-172">See also</span></span>



[<span data-ttu-id="00bfa-173">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="00bfa-173">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00bfa-174">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="00bfa-174">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00bfa-175">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="00bfa-175">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00bfa-176">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="00bfa-176">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

