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
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="62bee-103">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="62bee-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="62bee-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62bee-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62bee-105">Contém um bitmask de 32 bits de sinalizadores que define o status de uma mensagem em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="62bee-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="62bee-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="62bee-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="62bee-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="62bee-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="62bee-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="62bee-108">Identifier:</span></span>  <br/> |<span data-ttu-id="62bee-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="62bee-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="62bee-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="62bee-110">Data type:</span></span>  <br/> |<span data-ttu-id="62bee-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="62bee-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="62bee-112">Área:</span><span class="sxs-lookup"><span data-stu-id="62bee-112">Area:</span></span>  <br/> |<span data-ttu-id="62bee-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="62bee-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62bee-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="62bee-114">Remarks</span></span>

<span data-ttu-id="62bee-115">Uma mensagem pode existir em uma tabela de conteúdo e em uma ou mais tabelas de resultados de pesquisa, e cada instância da mensagem pode ter um status diferente.</span><span class="sxs-lookup"><span data-stu-id="62bee-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="62bee-116">Essa propriedade não deve ser considerada uma propriedade em uma mensagem, mas uma coluna em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="62bee-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="62bee-117">Um aplicativo cliente pode definir um ou mais dos seguintes sinalizadores nesta propriedade:</span><span class="sxs-lookup"><span data-stu-id="62bee-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="62bee-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="62bee-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="62bee-119">A mensagem foi respondida.</span><span class="sxs-lookup"><span data-stu-id="62bee-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="62bee-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="62bee-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="62bee-121">A mensagem foi marcada para exclusão subsequente.</span><span class="sxs-lookup"><span data-stu-id="62bee-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="62bee-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="62bee-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="62bee-123">A mensagem está no status de revisão de rascunho.</span><span class="sxs-lookup"><span data-stu-id="62bee-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="62bee-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="62bee-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="62bee-125">A mensagem deve ser suprimida da exibição da pasta destinatários.</span><span class="sxs-lookup"><span data-stu-id="62bee-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="62bee-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="62bee-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="62bee-127">A mensagem deve ser realçada na pasta de destinatários.</span><span class="sxs-lookup"><span data-stu-id="62bee-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="62bee-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="62bee-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="62bee-129">A mensagem foi marcada para exclusão no armazenamento remoto de mensagens sem baixar para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="62bee-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="62bee-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="62bee-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="62bee-131">A mensagem foi marcada para download no repositório de mensagens remotas para o cliente local.</span><span class="sxs-lookup"><span data-stu-id="62bee-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="62bee-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="62bee-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="62bee-133">A mensagem foi marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="62bee-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="62bee-134">Os sinalizadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**e **MSGSTATUS_TAGGED** são definidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="62bee-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="62bee-135">Provedores de transporte e de repositório passam esses bits sem qualquer ação.</span><span class="sxs-lookup"><span data-stu-id="62bee-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="62bee-136">Os clientes podem interpretar esses valores de qualquer forma que seja apropriada para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="62bee-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="62bee-137">Uma maneira de que muitos clientes usem essa propriedade é exibir mensagens marcadas para exclusão com um ícone representativo.</span><span class="sxs-lookup"><span data-stu-id="62bee-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="62bee-138">Um cliente do visualizador remoto pode definir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** em mensagens na pasta de cabeçalho apresentada pelo provedor de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="62bee-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="62bee-139">O aplicativo cliente pode examinar cada cabeçalho de mensagem nessa pasta para determinar se a mensagem deve ser baixada ou excluída no repositório de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="62bee-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="62bee-140">Em seguida, ele usa o método [IMAPIFolder:: SetMessageStatus](imapifolder-setmessagestatus.md) para definir o sinalizador apropriado.</span><span class="sxs-lookup"><span data-stu-id="62bee-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="62bee-141">**SetMessageStatus** é a única maneira de definir qualquer um dos sinalizadores nessa propriedade; o método [IMAPIProp::](imapiprop-setprops.md) SetProps não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="62bee-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="62bee-142">Para recuperar essa propriedade, os clientes chamam [IMAPIFolder:: GetMessageStatus](imapifolder-getmessagestatus.md) , em vez de [IMAPIProp::](imapiprop-getprops.md)GetProps.</span><span class="sxs-lookup"><span data-stu-id="62bee-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="62bee-143">Bits 16 a 31 (0x10000 a 0x80000000) desta propriedade estão disponíveis para uso pelo aplicativo cliente de mensagem interpessoal (IPM).</span><span class="sxs-lookup"><span data-stu-id="62bee-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="62bee-144">Todos os outros bits são reservados para uso por MAPI; aqueles não definidos na tabela anterior devem ser inicialmente definidos como zero e não alterados subsequentemente.</span><span class="sxs-lookup"><span data-stu-id="62bee-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="62bee-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="62bee-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="62bee-146">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="62bee-146">Protocol specifications</span></span>

<span data-ttu-id="62bee-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62bee-147">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62bee-148">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="62bee-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="62bee-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="62bee-149">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="62bee-150">Manipula a sincronização de dados do objeto Messaging entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="62bee-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="62bee-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="62bee-151">Header files</span></span>

<span data-ttu-id="62bee-152">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="62bee-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="62bee-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="62bee-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="62bee-154">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="62bee-154">Mapitags.h</span></span>
  
> <span data-ttu-id="62bee-155">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="62bee-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="62bee-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="62bee-156">See also</span></span>



[<span data-ttu-id="62bee-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="62bee-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="62bee-158">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="62bee-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="62bee-159">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="62bee-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="62bee-160">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="62bee-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="62bee-161">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="62bee-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

