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
ms.openlocfilehash: 79b6461ca4a796b292b86f0f3bdbd8a39ad65863
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575676"
---
# <a name="pidtagprofileserverversion-canonical-property"></a><span data-ttu-id="f219a-103">Propriedade canônica PidTagProfileServerVersion</span><span class="sxs-lookup"><span data-stu-id="f219a-103">PidTagProfileServerVersion Canonical Property</span></span>

  
  
<span data-ttu-id="f219a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f219a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f219a-105">Especifica informações sobre a versão do Microsoft Exchange Server ao qual contas em um perfil do Microsoft Outlook estão conectadas.</span><span class="sxs-lookup"><span data-stu-id="f219a-105">Specifies information about the version of Microsoft Exchange Server to which accounts in a Microsoft Outlook profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="f219a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f219a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f219a-107">PR_PROFILE_SERVER_VERSION</span><span class="sxs-lookup"><span data-stu-id="f219a-107">PR_PROFILE_SERVER_VERSION</span></span>  <br/> |
|<span data-ttu-id="f219a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f219a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f219a-109">0x661B</span><span class="sxs-lookup"><span data-stu-id="f219a-109">0x661B</span></span>  <br/> |
|<span data-ttu-id="f219a-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f219a-110">Property type:</span></span>  <br/> |<span data-ttu-id="f219a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f219a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f219a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f219a-112">Area:</span></span>  <br/> |<span data-ttu-id="f219a-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="f219a-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f219a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f219a-114">Remarks</span></span>

<span data-ttu-id="f219a-115">Um perfil pode especificar uma ou mais contas que se conectam ao servidor do Exchange, mas eles devem estar conectados ao mesmo servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="f219a-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="f219a-116">Versões do Outlook anteriores ao Microsoft Office Outlook 2007 podem gravar essa propriedade para armazenar informações sobre a versão do Exchange Server ao qual o perfil ativo está conectado.</span><span class="sxs-lookup"><span data-stu-id="f219a-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 can write to this property to store information about the version of Exchange Server to which the active profile is connected.</span></span> <span data-ttu-id="f219a-117">No entanto, o formato das informações de versão varia para versões diferentes do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f219a-117">However, the format of the version information varies for different versions of Exchange Server.</span></span> <span data-ttu-id="f219a-118">Por exemplo, repositórios do Outlook no **PR_PROFILE_SERVER_VERSION** o valor decimal 6944 para representar somente as principais número do identificador de versão de compilação **6.5.6944.3** para Microsoft Exchange Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f219a-118">For example, Outlook stores in **PR_PROFILE_SERVER_VERSION** the decimal value 6944 to represent only the major build number in the version identifier of **6.5.6944.3** for Microsoft Exchange Server 2003.</span></span> <span data-ttu-id="f219a-119">Para uma conexão do Exchange 2007, Outlook armazena o número de versão principal e número em uma representação hexadecimal concatenada desses números na propriedade da compilação do principal.</span><span class="sxs-lookup"><span data-stu-id="f219a-119">For an Exchange 2007 connection, Outlook stores the major version number and the major build number in a concatenated hexadecimal representation of these numbers in the property.</span></span> <span data-ttu-id="f219a-120">Um identificador de versão do Exchange 2007 de **8.0.685.24** tem um número de versão principal 8 e um número de compilação principais 685 em decimal.</span><span class="sxs-lookup"><span data-stu-id="f219a-120">An Exchange 2007 version identifier of **8.0.685.24** has a major version number 8 and a major build number 685 in decimal.</span></span> <span data-ttu-id="f219a-121">Conversão de ambos os números em hexadecimal, você obtém 0x8 e 0x2AD.</span><span class="sxs-lookup"><span data-stu-id="f219a-121">Converting both numbers to hexadecimal, you get 0x8 and 0x2AD.</span></span> <span data-ttu-id="f219a-122">Concatenando esses dois números, o Outlook armazena o valor 0x82AD em **PR_PROFILE_SERVER_VERSION** na representação hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="f219a-122">Concatenating these two numbers, Outlook stores the value 0x82AD in **PR_PROFILE_SERVER_VERSION** in hexadecimal representation.</span></span> 
  
<span data-ttu-id="f219a-123">O Outlook 2007 não ler ou gravar a essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f219a-123">Outlook 2007 does not read or write to this property.</span></span> <span data-ttu-id="f219a-124">Suporte a **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span><span class="sxs-lookup"><span data-stu-id="f219a-124">It supports **[PR_PROFILE_SERVER_FULL_VERSION](pidtagprofileserverfullversion-canonical-property.md)**.</span></span> 
  
<span data-ttu-id="f219a-125">Somente uma das **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** é provável que existam em um perfil, mas há nenhuma garantia de que um sempre existe em um perfil.</span><span class="sxs-lookup"><span data-stu-id="f219a-125">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="f219a-126">Outlook não gravar ou propriedade até que tenha se conectado com êxito ao servidor do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f219a-126">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="f219a-127">No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para localizar a versão do Exchange Server no qual a caixa de correio ativa está hospedada.</span><span class="sxs-lookup"><span data-stu-id="f219a-127">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f219a-128">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f219a-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f219a-129">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f219a-129">Protocol specifications</span></span>

<span data-ttu-id="f219a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f219a-130">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f219a-131">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f219a-131">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f219a-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f219a-132">Header files</span></span>

<span data-ttu-id="f219a-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f219a-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="f219a-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f219a-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="f219a-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f219a-135">Mapitags.h</span></span>
  
> <span data-ttu-id="f219a-136">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f219a-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f219a-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="f219a-137">See also</span></span>



[<span data-ttu-id="f219a-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f219a-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f219a-139">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f219a-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f219a-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f219a-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f219a-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f219a-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

