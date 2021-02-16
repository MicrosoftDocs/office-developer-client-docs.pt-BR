---
title: Propriedade canônica PidTagProfileServerFullVersion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c88a625-da57-3b1d-9887-0a898b722766
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9456178e9426d7a5fe17382d876f507daa0251f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341598"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="1370f-103">Propriedade canônica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="1370f-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="1370f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1370f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1370f-105">Especifica informações completas de versão e build sobre o Microsoft Exchange Server às quais as contas em um perfil estão conectadas.</span><span class="sxs-lookup"><span data-stu-id="1370f-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1370f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1370f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1370f-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="1370f-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="1370f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1370f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1370f-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="1370f-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="1370f-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="1370f-110">Property type:</span></span>  <br/> |<span data-ttu-id="1370f-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="1370f-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="1370f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1370f-112">Area:</span></span>  <br/> |<span data-ttu-id="1370f-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="1370f-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1370f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1370f-114">Remarks</span></span>

<span data-ttu-id="1370f-115">Um perfil pode especificar uma ou mais contas que se conectam a um Exchange Server, mas devem estar conectadas ao mesmo Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1370f-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="1370f-116">As versões do Outlook anteriores ao Microsoft Office Outlook 2007 não são suportadas por essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="1370f-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="1370f-117">Para essas versões do Outlook, verifique a existência **[de PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** no perfil.</span><span class="sxs-lookup"><span data-stu-id="1370f-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="1370f-118">Geralmente, se **a** caixa de correio ativa estiver conectada a um Exchange Server, o Outlook 2007 armazenará informações completas da versão do Exchange Server na PR_PROFILE_SERVER_FULL_VERSION no perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="1370f-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="1370f-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span><span class="sxs-lookup"><span data-stu-id="1370f-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="1370f-120">Por exemplo, para armazenar o identificador de versão do Exchange Server de **8.0.685.24**, o número da versão principal é 8 e o número da versão secundária é 0, e o número de com build principal é 685 e o número de com build secundário é 24.</span><span class="sxs-lookup"><span data-stu-id="1370f-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="1370f-121">Apenas um dos **PR_PROFILE_SERVER_VERSION** **ou PR_PROFILE_SERVER_FULL_VERSION** provavelmente existirá em um perfil, mas não há garantia de que sempre exista em um perfil.</span><span class="sxs-lookup"><span data-stu-id="1370f-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="1370f-122">O Outlook não gravará em nenhuma das propriedades até que tenha se conectado com êxito ao Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1370f-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="1370f-123">No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para encontrar a versão do Exchange Server na qual a caixa de correio ativa está hospedada.</span><span class="sxs-lookup"><span data-stu-id="1370f-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1370f-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1370f-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1370f-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1370f-125">Protocol specifications</span></span>

<span data-ttu-id="1370f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1370f-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1370f-127">Fornece definições de conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="1370f-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1370f-128">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1370f-128">Header files</span></span>

<span data-ttu-id="1370f-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1370f-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="1370f-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1370f-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="1370f-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1370f-131">Mapitags.h</span></span>
  
> <span data-ttu-id="1370f-132">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1370f-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1370f-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1370f-133">See also</span></span>



[<span data-ttu-id="1370f-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1370f-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1370f-135">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1370f-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1370f-136">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1370f-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1370f-137">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1370f-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

