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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396173"
---
# <a name="pidtagprofileserverfullversion-canonical-property"></a><span data-ttu-id="f5365-103">Propriedade canônica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="f5365-103">PidTagProfileServerFullVersion Canonical Property</span></span>

  
  
<span data-ttu-id="f5365-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5365-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5365-105">Especifica as informações de versão e compilação completas sobre o Microsoft Exchange Server ao qual contas em um perfil estão conectadas.</span><span class="sxs-lookup"><span data-stu-id="f5365-105">Specifies complete version and build information about the Microsoft Exchange Server to which accounts in a profile are connected.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="f5365-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f5365-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f5365-107">PR_PROFILE_SERVER_FULL_VERSION</span><span class="sxs-lookup"><span data-stu-id="f5365-107">PR_PROFILE_SERVER_FULL_VERSION</span></span>  <br/> |
|<span data-ttu-id="f5365-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f5365-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f5365-109">0x663B</span><span class="sxs-lookup"><span data-stu-id="f5365-109">0x663B</span></span>  <br/> |
|<span data-ttu-id="f5365-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="f5365-110">Property type:</span></span>  <br/> |<span data-ttu-id="f5365-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="f5365-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="f5365-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f5365-112">Area:</span></span>  <br/> |<span data-ttu-id="f5365-113">Configuração de perfil MAPI</span><span class="sxs-lookup"><span data-stu-id="f5365-113">MAPI profile configuration</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f5365-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f5365-114">Remarks</span></span>

<span data-ttu-id="f5365-115">Um perfil pode especificar uma ou mais contas que se conectam ao servidor do Exchange, mas eles devem estar conectados ao mesmo servidor Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5365-115">A profile can specify one or more accounts that connect to an Exchange Server, but they must be connected to the same Exchange Server.</span></span>
  
<span data-ttu-id="f5365-116">Versões do Outlook anteriores ao Microsoft Office Outlook 2007 não têm suporte para essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="f5365-116">Versions of Outlook earlier than Microsoft Office Outlook 2007 do not support this property.</span></span> <span data-ttu-id="f5365-117">Para as versões do Outlook, verifique a existência de **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** no perfil.</span><span class="sxs-lookup"><span data-stu-id="f5365-117">For those versions of Outlook, check for the existence of **[PR_PROFILE_SERVER_VERSION](pidtagprofileserverversion-canonical-property.md)** in the profile.</span></span> 
  
<span data-ttu-id="f5365-118">Geralmente, se a caixa de correio ativa estiver conectada a um servidor Exchange, o Outlook 2007 armazena informações de versão completas do Exchange Server na propriedade **PR_PROFILE_SERVER_FULL_VERSION** no perfil ativo.</span><span class="sxs-lookup"><span data-stu-id="f5365-118">Generally, if the active mailbox is connected to an Exchange Server, Outlook 2007 stores complete Exchange Server version information in the **PR_PROFILE_SERVER_FULL_VERSION** property in the active profile.</span></span> <span data-ttu-id="f5365-119">Outlook armazena as informações em uma estrutura **EXCHANGE_STORE_VERSION_NUM** que contém os números da versão principal e secundária e os números de compilação principais e secundárias.</span><span class="sxs-lookup"><span data-stu-id="f5365-119">Outlook stores the information in an **EXCHANGE_STORE_VERSION_NUM** structure that contains the major and minor version numbers and the major and minor build numbers.</span></span> <span data-ttu-id="f5365-120">Por exemplo, para armazenar o identificador de versão do Exchange Server do **8.0.685.24**, o número de versão principal é 8 e número da versão secundária é 0 e o número de compilação principais é 685 e número da versão secundária está 24.</span><span class="sxs-lookup"><span data-stu-id="f5365-120">For example, to store the Exchange Server version identifier of **8.0.685.24**, the major version number is 8 and minor version number is 0, and the major build number is 685 and minor build number is 24.</span></span>
  
<span data-ttu-id="f5365-121">Somente uma das **PR_PROFILE_SERVER_VERSION** ou **PR_PROFILE_SERVER_FULL_VERSION** é provável que existam em um perfil, mas há nenhuma garantia de que um sempre existe em um perfil.</span><span class="sxs-lookup"><span data-stu-id="f5365-121">Only one of **PR_PROFILE_SERVER_VERSION** or **PR_PROFILE_SERVER_FULL_VERSION** is likely to exist in a profile, but there is no guarantee that either always exists in a profile.</span></span> <span data-ttu-id="f5365-122">Outlook não gravar ou propriedade até que tenha se conectado com êxito ao servidor do Exchange.</span><span class="sxs-lookup"><span data-stu-id="f5365-122">Outlook does not write to either property until it has successfully connected to the Exchange Server.</span></span> 
  
<span data-ttu-id="f5365-123">No modelo de objeto do Outlook, você pode usar a propriedade **ExchangeMailboxServerVersion** do objeto **NameSpace** para localizar a versão do Exchange Server no qual a caixa de correio ativa está hospedada.</span><span class="sxs-lookup"><span data-stu-id="f5365-123">In the Outlook object model, you can use the **ExchangeMailboxServerVersion** property of the **NameSpace** object to find the version of Exchange Server on which the active mailbox is hosted.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="f5365-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5365-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f5365-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f5365-125">Protocol specifications</span></span>

<span data-ttu-id="f5365-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f5365-126">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f5365-127">Fornece as definições do conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f5365-127">Provides property set definitions.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f5365-128">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f5365-128">Header files</span></span>

<span data-ttu-id="f5365-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5365-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="f5365-130">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f5365-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="f5365-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f5365-131">Mapitags.h</span></span>
  
> <span data-ttu-id="f5365-132">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f5365-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f5365-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f5365-133">See also</span></span>



[<span data-ttu-id="f5365-134">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f5365-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f5365-135">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f5365-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f5365-136">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f5365-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f5365-137">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f5365-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

