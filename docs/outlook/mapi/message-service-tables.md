---
title: Tabelas de serviço de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422492"
---
# <a name="message-service-tables"></a><span data-ttu-id="cc41f-103">Tabelas de serviço de mensagens</span><span class="sxs-lookup"><span data-stu-id="cc41f-103">Message Service Tables</span></span>

  
  
<span data-ttu-id="cc41f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cc41f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cc41f-105">A tabela de serviço de mensagens contém informações sobre os serviços de mensagens no perfil atual.</span><span class="sxs-lookup"><span data-stu-id="cc41f-105">The message service table contains information about the message services in the current profile.</span></span> <span data-ttu-id="cc41f-106">Há uma tabela de serviço de mensagens para cada sessão MAPI, implementada por MAPI e usada por aplicativos clientes de propósito especial que oferecem suporte à configuração.</span><span class="sxs-lookup"><span data-stu-id="cc41f-106">There is one message service table for every MAPI session, implemented by MAPI and used by special purpose client applications that provide configuration support.</span></span> 
  
<span data-ttu-id="cc41f-107">A tabela de serviço de mensagens é uma tabela estática.</span><span class="sxs-lookup"><span data-stu-id="cc41f-107">The message service table is a static table.</span></span>
  
<span data-ttu-id="cc41f-108">Os clientes acessam a tabela de serviço de mensagens chamando o método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) .</span><span class="sxs-lookup"><span data-stu-id="cc41f-108">Clients access the message service table by calling the [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) method.</span></span> 
  
<span data-ttu-id="cc41f-109">As propriedades a seguir compõem o conjunto de colunas necessárias na tabela de serviço de mensagens:</span><span class="sxs-lookup"><span data-stu-id="cc41f-109">The following properties make up the required column set in the message service table:</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cc41f-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-110">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cc41f-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-111">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="cc41f-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-112">**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cc41f-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-113">**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="cc41f-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-114">**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cc41f-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-115">**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="cc41f-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-116">**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="cc41f-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="cc41f-117">**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))</span></span>  <br/> |
   
 <span data-ttu-id="cc41f-118">**PR_DISPLAY_NAME** é o nome de exibição para o serviço de mensagem e a coluna de chave de classificação padrão.</span><span class="sxs-lookup"><span data-stu-id="cc41f-118">**PR_DISPLAY_NAME** is the displayable name for the message service and the default sort key column.</span></span> 
  
 <span data-ttu-id="cc41f-119">**PR_INSTANCE_KEY** serve como a coluna de índice para a tabela, identificando exclusivamente uma linha.</span><span class="sxs-lookup"><span data-stu-id="cc41f-119">**PR_INSTANCE_KEY** serves as the index column for the table, uniquely identifying a row.</span></span> 
  
 <span data-ttu-id="cc41f-120">**PR_RESOURCE_FLAGS** descreve os recursos do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cc41f-120">**PR_RESOURCE_FLAGS** describes the message service's capabilities.</span></span> 
  
 <span data-ttu-id="cc41f-121">**PR_SERVICE_DLL_NAME** é o nome da dll que contém a implementação do serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cc41f-121">**PR_SERVICE_DLL_NAME** is the name of the DLL that contains the message service implementation.</span></span> 
  
 <span data-ttu-id="cc41f-122">**PR_SERVICE_ENTRY_NAME** é o nome da função de ponto de entrada do serviço de mensagens que está de acordo com o protótipo do [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="cc41f-122">**PR_SERVICE_ENTRY_NAME** is the name of the message service's entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> 
  
 <span data-ttu-id="cc41f-123">**PR_SERVICE_NAME** é uma entrada necessária na seção **[serviços]** no MAPISVC. inf.</span><span class="sxs-lookup"><span data-stu-id="cc41f-123">**PR_SERVICE_NAME** is a required entry in the **[Services]** section in MAPISVC.INF.</span></span> <span data-ttu-id="cc41f-124">O valor dessa propriedade nunca será alterado ou localizado.</span><span class="sxs-lookup"><span data-stu-id="cc41f-124">The value for this property will never be changed or localized.</span></span> <span data-ttu-id="cc41f-125">O **PR_SERVICE_NAME** pode ser usado para identificar programaticamente o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cc41f-125">**PR_SERVICE_NAME** can be used to programmatically identify the message service.</span></span> 
  
 <span data-ttu-id="cc41f-126">**PR_SERVICE_SUPPORT_FILES** é uma lista de arquivos que devem ser instalados com o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cc41f-126">**PR_SERVICE_SUPPORT_FILES** is a list of files that must be installed with the message service.</span></span> 
  
 <span data-ttu-id="cc41f-127">**PR_SERVICE_UID** é um identificador exclusivo para o serviço de mensagens.</span><span class="sxs-lookup"><span data-stu-id="cc41f-127">**PR_SERVICE_UID** is a unique identifier for the message service.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cc41f-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="cc41f-128">See also</span></span>



[<span data-ttu-id="cc41f-129">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="cc41f-129">MAPI Tables</span></span>](mapi-tables.md)

