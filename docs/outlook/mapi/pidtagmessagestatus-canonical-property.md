---
title: Propriedade canônica PidTagMessageStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageStatus
api_type:
- HeaderDef
ms.assetid: e479e863-a8de-4f7e-9eae-3f721cd16e9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dacd759d978394a5f4ed028915ed1c717bf6efe5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355717"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="1ec5a-103">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1ec5a-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="1ec5a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ec5a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ec5a-105">Contém uma máscara de bits de 32 bits de sinalizadores que define o status de uma mensagem em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ec5a-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1ec5a-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1ec5a-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="1ec5a-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="1ec5a-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1ec5a-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1ec5a-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="1ec5a-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="1ec5a-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1ec5a-110">Data type:</span></span>  <br/> |<span data-ttu-id="1ec5a-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="1ec5a-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="1ec5a-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1ec5a-112">Area:</span></span>  <br/> |<span data-ttu-id="1ec5a-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="1ec5a-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ec5a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ec5a-114">Remarks</span></span>

<span data-ttu-id="1ec5a-115">Uma mensagem pode existir em um índice de conteúdo e em uma ou mais tabelas de resultados de pesquisa, e cada instância da mensagem pode ter um status diferente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="1ec5a-116">Essa propriedade não deve ser considerada uma propriedade em uma mensagem, mas uma coluna em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="1ec5a-117">Um aplicativo cliente pode definir um ou mais dos seguintes sinalizadores nesta propriedade:</span><span class="sxs-lookup"><span data-stu-id="1ec5a-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="1ec5a-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="1ec5a-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="1ec5a-119">A mensagem foi respondida.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="1ec5a-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="1ec5a-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="1ec5a-121">A mensagem foi marcada para exclusão subsequente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="1ec5a-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="1ec5a-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="1ec5a-123">A mensagem está no status de revisão de rascunho.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="1ec5a-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="1ec5a-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="1ec5a-125">A mensagem deve ser suprimida na exibição da pasta dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="1ec5a-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="1ec5a-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="1ec5a-127">A mensagem deve ser realçada nas exibições da pasta dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="1ec5a-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="1ec5a-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="1ec5a-129">A mensagem foi marcada para exclusão no armazenamento de mensagens remoto sem ser baixada para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="1ec5a-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="1ec5a-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="1ec5a-131">A mensagem foi marcada para download do armazenamento de mensagens remoto para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="1ec5a-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="1ec5a-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="1ec5a-133">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="1ec5a-134">Os **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED** e MSGSTATUS_TAGGED são  definidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="1ec5a-135">Os provedores de transporte e armazenamento passam esses bits sem qualquer ação.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="1ec5a-136">Os clientes podem interpretar esses valores de qualquer maneira que seja apropriado para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="1ec5a-137">Uma maneira pela qual muitos clientes usam essa propriedade é exibir mensagens marcadas para exclusão com um ícone representativo.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="1ec5a-138">Um cliente de visualizador remoto pode MSGSTATUS_REMOTE_DELETE ou **MSGSTATUS_REMOTE_DOWNLOAD** mensagens na pasta de header apresentadas a ele pelo provedor de transporte remoto. </span><span class="sxs-lookup"><span data-stu-id="1ec5a-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="1ec5a-139">O aplicativo cliente pode examinar cada header de mensagem nessa pasta para determinar se a mensagem deve ser baixada ou excluída no armazenamento de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="1ec5a-140">Em seguida, ele usa [o método IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para definir o sinalizador apropriado.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="1ec5a-141">**SetMessageStatus** é a única maneira de definir qualquer um dos sinalizadores nesta propriedade; o [método IMAPIProp::SetProps](imapiprop-setprops.md) não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="1ec5a-142">Para recuperar essa propriedade, os clientes chamam [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) em vez de [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="1ec5a-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="1ec5a-143">Os bits de 16 a 31 (0x10000 0x80000000) dessa propriedade estão disponíveis para uso pelo aplicativo cliente de mensagem interpersonal (IPM).</span><span class="sxs-lookup"><span data-stu-id="1ec5a-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="1ec5a-144">Todos os outros bits são reservados para uso por MAPI; aqueles não definidos na tabela anterior devem ser inicialmente definidos como zero e não alterados posteriormente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1ec5a-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1ec5a-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1ec5a-146">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1ec5a-146">Protocol specifications</span></span>

<span data-ttu-id="1ec5a-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ec5a-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ec5a-148">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1ec5a-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1ec5a-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1ec5a-150">Lida com a sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1ec5a-151">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="1ec5a-151">Header files</span></span>

<span data-ttu-id="1ec5a-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1ec5a-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="1ec5a-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="1ec5a-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1ec5a-154">Mapitags.h</span></span>
  
> <span data-ttu-id="1ec5a-155">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1ec5a-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1ec5a-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ec5a-156">See also</span></span>



[<span data-ttu-id="1ec5a-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="1ec5a-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="1ec5a-158">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1ec5a-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1ec5a-159">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="1ec5a-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1ec5a-160">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1ec5a-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1ec5a-161">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1ec5a-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

