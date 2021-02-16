---
title: Propriedade canônica PidTagProfileServerVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d41a536-81ff-733c-2fd7-460798e057c8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 84ff229e9914ec9074d61023873279b110fb606a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286563"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="1e080-103">Propriedade canônica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="1e080-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="1e080-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e080-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e080-105">Especifica informações sobre a versão do Microsoft Exchange Server à qual as contas em um perfil do Microsoft Outlook estão conectadas.</span><span class="sxs-lookup"><span data-stu-id="1e080-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1e080-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1e080-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1e080-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="1e080-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="1e080-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1e080-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1e080-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="1e080-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="1e080-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="1e080-110">Property type:</span></span>  <br/> |<span data-ttu-id="1e080-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1e080-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1e080-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1e080-112">Area:</span></span>  <br/> |<span data-ttu-id="1e080-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1e080-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e080-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e080-114">Remarks</span></span>

<span data-ttu-id="1e080-115">Um perfil pode especificar uma ou mais contas que se conectam a um Exchange Server, mas devem estar conectadas ao mesmo Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1e080-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="1e080-116">Versões do Outlook anteriores ao Microsoft Office Outlook 2007 podem gravar nessa propriedade para armazenar informações sobre a versão do Exchange Server à qual o perfil ativo está conectado.</span><span class="sxs-lookup"><span data-stu-id="1e080-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="1e080-117">No entanto, o formato das informações de versão varia para diferentes versões do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1e080-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="1e080-118">Por exemplo, o Outlook armazena em **PR_PROFILE_SERVER_VERSION** o valor decimal 6944 para representar apenas o número de com build principal no identificador de versão **6.5.6944.3** do Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="1e080-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="1e080-119">Para uma conexão com o Exchange 2007, o Outlook armazena o número da versão principal e o número de build principal em uma representação hexadecimal concatenada desses números na propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e080-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="1e080-120">Um identificador de versão do Exchange 2007 de **8.0.685.24** tem um número de versão principal 8 e um número de com build principal 685 em decimal.</span><span class="sxs-lookup"><span data-stu-id="1e080-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="1e080-121">Convertendo ambos os números em hexadecimais, você 0x8 e 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="1e080-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="1e080-122">Concatenando esses dois números, o Outlook armazena o valor 0x82AD **em** PR_PROFILE_SERVER_VERSION em representação hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="1e080-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="1e080-123">O Outlook 2007 não lê nem escreve nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1e080-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="1e080-124">Ele dá suporte **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="1e080-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="1e080-125">Apenas um dos **PR_PROFILE_SERVER_VERSION** **ou PR_PROFILE_SERVER_FULL_VERSION** provavelmente existirá em um perfil, mas não há garantia de que sempre exista em um perfil.</span><span class="sxs-lookup"><span data-stu-id="1e080-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="1e080-126">O Outlook não gravará em nenhuma das propriedades até que tenha se conectado com êxito ao Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1e080-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="1e080-127">No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para encontrar a versão do Exchange Server na qual a caixa de correio ativa está hospedada.</span><span class="sxs-lookup"><span data-stu-id="1e080-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1e080-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e080-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1e080-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1e080-129">Protocol specifications</span></span>

<span data-ttu-id="1e080-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1e080-130">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1e080-131">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1e080-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1e080-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1e080-132">Header files</span></span>

<span data-ttu-id="1e080-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1e080-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="1e080-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1e080-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="1e080-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1e080-135">Mapitags.h</span></span>
  
> <span data-ttu-id="1e080-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1e080-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1e080-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e080-137">See also</span></span>



[<span data-ttu-id="1e080-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1e080-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1e080-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1e080-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1e080-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1e080-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1e080-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1e080-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

