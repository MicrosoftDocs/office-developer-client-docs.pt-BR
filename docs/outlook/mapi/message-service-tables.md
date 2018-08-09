---
title: Tabelas de serviços de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768144"
---
# <a name="message-service-tables"></a><span data-ttu-id="a63af-103">Tabelas de serviços de mensagens</span><span class="sxs-lookup"><span data-stu-id="a63af-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="a63af-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a63af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a63af-105">A tabela de serviço de mensagem contém informações sobre os serviços de mensagem no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="a63af-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="a63af-106">Há uma tabela de serviço de mensagem para cada sessão MAPI, implementada por MAPI e usado pelos aplicativos de cliente para fins especiais que oferecem suporte à configuração.</span><span class="sxs-lookup"><span data-stu-id="a63af-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="a63af-107">A tabela de serviço de mensagem é uma tabela estática.</span><span class="sxs-lookup"><span data-stu-id="a63af-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="a63af-108">Os clientes de acessar a tabela de serviços de mensagem chamando o método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="a63af-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="a63af-109">As seguintes propriedades compõem a coluna necessária definida na tabela de serviço de mensagem:</span><span class="sxs-lookup"><span data-stu-id="a63af-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a63af-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a63af-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a63af-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a63af-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a63af-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a63af-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="a63af-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a63af-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a63af-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="a63af-118">**PR_DISPLAY_NAME** é o nome para exibição para o serviço de mensagem e a coluna de chaves de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="a63af-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="a63af-119">**PR_INSTANCE_KEY** serve como a coluna de índice para a tabela, que identifica unicamente uma linha.</span><span class="sxs-lookup"><span data-stu-id="a63af-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="a63af-120">**PR_RESOURCE_FLAGS** descreve os recursos do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a63af-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="a63af-121">**PR_SERVICE_DLL_NAME** é o nome da DLL que contém a implementação do serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a63af-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="a63af-122">**PR_SERVICE_ENTRY_NAME** é o nome da função de ponto de entrada do serviço de mensagem que está em conformidade com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="a63af-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="a63af-123">**PR_SERVICE_NAME** é uma entrada necessária na seção **[Services]** em MAPISVC.</span><span class="sxs-lookup"><span data-stu-id="a63af-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="a63af-124">O valor dessa propriedade nunca será alterado ou localizado.</span><span class="sxs-lookup"><span data-stu-id="a63af-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="a63af-125">**PR_SERVICE_NAME** pode ser usado para identificar programaticamente o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a63af-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="a63af-126">**PR_SERVICE_SUPPORT_FILES** é uma lista dos arquivos que devem ser instalados com o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a63af-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="a63af-127">**PR_SERVICE_UID** é um identificador exclusivo para o serviço de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a63af-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a63af-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="a63af-128">See also</span></span>



[<span data-ttu-id="a63af-129">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="a63af-129">MAPI Tables</span></span>](mapi-tables.md)

