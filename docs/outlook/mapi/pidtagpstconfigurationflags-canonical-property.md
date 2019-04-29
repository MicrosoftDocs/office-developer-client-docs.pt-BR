---
title: Propriedade canônica PidTagPstConfigurationFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: e4234ddf-d9dc-4dc9-8eda-dbbee151b5d7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e881c8eeffa29706591e07113d70a3670606f2be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408940"
---
# <a name="pidtagpstconfigurationflags-canonical-property"></a><span data-ttu-id="3c871-103">Propriedade canônica PidTagPstConfigurationFlags</span><span class="sxs-lookup"><span data-stu-id="3c871-103">PidTagPstConfigurationFlags Canonical Property</span></span>
  
<span data-ttu-id="3c871-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c871-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c871-105">Especifica sinalizadores de configuração de uma tabela de armazenamento pessoal (arquivo. pst).</span><span class="sxs-lookup"><span data-stu-id="3c871-105">Specfies configuration flags for a personal storage table (.pst file).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3c871-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3c871-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3c871-107">PR_PST_CONFIG_FLAGS</span><span class="sxs-lookup"><span data-stu-id="3c871-107">PR_PST_CONFIG_FLAGS</span></span>  <br/> |
|<span data-ttu-id="3c871-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3c871-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3c871-109">0x6770</span><span class="sxs-lookup"><span data-stu-id="3c871-109">0x6770</span></span>  <br/> |
|<span data-ttu-id="3c871-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3c871-110">Data type:</span></span>  <br/> |<span data-ttu-id="3c871-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="3c871-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="3c871-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3c871-112">Area:</span></span>  <br/> |<span data-ttu-id="3c871-113">Tabela de armazenamento pessoal (. pst) interna</span><span class="sxs-lookup"><span data-stu-id="3c871-113">Personal storage table (.pst) internal</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c871-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3c871-114">Remarks</span></span>

<span data-ttu-id="3c871-115">Estes são os valores válidos para esta propriedade:</span><span class="sxs-lookup"><span data-stu-id="3c871-115">The following are valid values for this property:</span></span>
  
<span data-ttu-id="3c871-116">PST_CONFIG_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3c871-116">PST_CONFIG_UNICODE</span></span>
  
> <span data-ttu-id="3c871-117">Indica um arquivo. pst Unicode.</span><span class="sxs-lookup"><span data-stu-id="3c871-117">Indicates a Unicode .pst file.</span></span> 
    
   `#define PST_CONFIG_UNICODE 0x80000000`
    
<span data-ttu-id="3c871-118">PST_CONFIG_CREATE_NOWARN</span><span class="sxs-lookup"><span data-stu-id="3c871-118">PST_CONFIG_CREATE_NOWARN</span></span>
  
> <span data-ttu-id="3c871-119">Quando definido nos sinalizadores de cliente para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) , trata **ConfigureMsgService** como uma chamada [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) e ignora o "este serviço de informações não foi configurado" Cuidado.</span><span class="sxs-lookup"><span data-stu-id="3c871-119">When set from the client flags to the [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) method, treats **ConfigureMsgService** like a [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) call and skips the "This information service has not been configured" warning.</span></span> 
    
   `#define PST_CONFIG_CREATE_NOWARN 0x00000001`
    
<span data-ttu-id="3c871-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="3c871-120">PST_CONFIG_PRESERVE_DISPLAY_NAME</span></span>
  
> <span data-ttu-id="3c871-121">Informa ao **ConfigureMsgService** para não alterar o valor da propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), mesmo que ela tenha sido fornecida.</span><span class="sxs-lookup"><span data-stu-id="3c871-121">Tells **ConfigureMsgService** to not change the value of the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, even though it was supplied.</span></span> <span data-ttu-id="3c871-122">Nesse caso, ele foi fornecido apenas para os novos arquivos. pst.</span><span class="sxs-lookup"><span data-stu-id="3c871-122">In that case, it was supplied only for new .pst files.</span></span>
    
   `#define PST_CONFIG_PRESERVE_DISPLAY_NAME 0x00000002`
    
<span data-ttu-id="3c871-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span><span class="sxs-lookup"><span data-stu-id="3c871-123">OST_CONFIG_POLICY_DELAY_IGNORE_OST</span></span>
  
> <span data-ttu-id="3c871-124">Instrui o código de configuração a exibir primeiro uma caixa de diálogo para confirmar se um arquivo de pasta offline (. ost) foi encontrado e, dependendo da resposta do usuário, usar a pasta offline encontrada ou permitir que o usuário navegue para outra pasta offline.</span><span class="sxs-lookup"><span data-stu-id="3c871-124">Tells the configuration code to first display a dialog box to confirm whether an Offline Folder (.ost) file was found and, depending on the user's response, either use the found Offline Folder or enable the user to browse for another Offline Folder.</span></span>
    
   `#define OST_CONFIG_POLICY_DELAY_IGNORE_OST 0x00000008`
    
<span data-ttu-id="3c871-125">OST_CONFIG_CREATE_NEW_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="3c871-125">OST_CONFIG_CREATE_NEW_DEFAULT</span></span>
  
> <span data-ttu-id="3c871-126">Copia o arquivo. ost com um novo nome exclusivo e descarta o nome atual.</span><span class="sxs-lookup"><span data-stu-id="3c871-126">Copies the .ost file with a new unique name and discards the current name.</span></span> <span data-ttu-id="3c871-127">O arquivo. ost existente permanece no computador, mas não é mais usado neste perfil.</span><span class="sxs-lookup"><span data-stu-id="3c871-127">The existing .ost file remains on the computer but is no longer used in this profile.</span></span> <span data-ttu-id="3c871-128">Isso geralmente ocorre quando o Microsoft Outlook não permite mais um arquivo. ost específico, e as políticas de registro não permitem que o usuário renomeie o arquivo.</span><span class="sxs-lookup"><span data-stu-id="3c871-128">This typically occurs when Microsoft Outlook no longer permits a particular .ost file, and registry policies do not allow the user to rename the file.</span></span> 
    
   `#define OST_CONFIG_CREATE_NEW_DEFAULT_OST 0x00000010`
    
## <a name="related-resources"></a><span data-ttu-id="3c871-129">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c871-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="3c871-130">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="3c871-130">Protocol specifications</span></span>

<span data-ttu-id="3c871-131">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="3c871-131">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="3c871-132">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="3c871-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="3c871-133">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3c871-133">Header files</span></span>

<span data-ttu-id="3c871-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="3c871-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="3c871-135">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3c871-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="3c871-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="3c871-136">Mapitags.h</span></span>
  
> <span data-ttu-id="3c871-137">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="3c871-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3c871-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3c871-138">See also</span></span>



[<span data-ttu-id="3c871-139">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3c871-139">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3c871-140">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="3c871-140">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3c871-141">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3c871-141">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3c871-142">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3c871-142">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

