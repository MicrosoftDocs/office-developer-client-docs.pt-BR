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
ms.openlocfilehash: 626bd945851155c20850ee7f367ec6073ad57bc1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570384"
---
# <a name="pidtagmessagestatus-canonical-property"></a><span data-ttu-id="0b850-103">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="0b850-103">PidTagMessageStatus Canonical Property</span></span>

  
  
<span data-ttu-id="0b850-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0b850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0b850-105">Contém uma bitmask de 32 bits dos sinalizadores que define o status de uma mensagem em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0b850-105">Contains a 32-bit bitmask of flags that defines the status of a message in a contents table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b850-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0b850-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0b850-107">PR_MSG_STATUS</span><span class="sxs-lookup"><span data-stu-id="0b850-107">PR_MSG_STATUS</span></span>  <br/> |
|<span data-ttu-id="0b850-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0b850-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0b850-109">0x0E17</span><span class="sxs-lookup"><span data-stu-id="0b850-109">0x0E17</span></span>  <br/> |
|<span data-ttu-id="0b850-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0b850-110">Data type:</span></span>  <br/> |<span data-ttu-id="0b850-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="0b850-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="0b850-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0b850-112">Area:</span></span>  <br/> |<span data-ttu-id="0b850-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="0b850-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b850-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b850-114">Remarks</span></span>

<span data-ttu-id="0b850-115">Uma mensagem pode existir em uma tabela de conteúdo e em uma ou mais tabelas de resultados de pesquisa, e cada instância da mensagem pode ter um status diferente.</span><span class="sxs-lookup"><span data-stu-id="0b850-115">A message can exist in a contents table and in one or more search-results tables, and each instance of the message can have a different status.</span></span> <span data-ttu-id="0b850-116">Essa propriedade não deve ser considerada uma propriedade em uma mensagem, mas uma coluna em uma tabela de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0b850-116">This property should not be considered a property on a message but a column in a contents table.</span></span> 
  
<span data-ttu-id="0b850-117">Um aplicativo cliente pode definir um ou mais dos seguintes sinalizadores nessa propriedade:</span><span class="sxs-lookup"><span data-stu-id="0b850-117">A client application can set one or more of the following flags in this property:</span></span> 
  
<span data-ttu-id="0b850-118">MSGSTATUS_ANSWERED</span><span class="sxs-lookup"><span data-stu-id="0b850-118">MSGSTATUS_ANSWERED</span></span> 
  
> <span data-ttu-id="0b850-119">A mensagem foi respondida.</span><span class="sxs-lookup"><span data-stu-id="0b850-119">The message has been replied to.</span></span> 
    
<span data-ttu-id="0b850-120">MSGSTATUS_DELMARKED</span><span class="sxs-lookup"><span data-stu-id="0b850-120">MSGSTATUS_DELMARKED</span></span> 
  
> <span data-ttu-id="0b850-121">A mensagem foi marcada para exclusão subsequente.</span><span class="sxs-lookup"><span data-stu-id="0b850-121">The message has been marked for subsequent deletion.</span></span> 
    
<span data-ttu-id="0b850-122">MSGSTATUS_DRAFT</span><span class="sxs-lookup"><span data-stu-id="0b850-122">MSGSTATUS_DRAFT</span></span> 
  
> <span data-ttu-id="0b850-123">A mensagem está no status de revisão de rascunho.</span><span class="sxs-lookup"><span data-stu-id="0b850-123">The message is in draft revision status.</span></span> 
    
<span data-ttu-id="0b850-124">MSGSTATUS_HIDDEN</span><span class="sxs-lookup"><span data-stu-id="0b850-124">MSGSTATUS_HIDDEN</span></span> 
  
> <span data-ttu-id="0b850-125">A mensagem deve ser suprimida da exibe de pasta dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="0b850-125">The message is to be suppressed from recipients' folder displays.</span></span> 
    
<span data-ttu-id="0b850-126">MSGSTATUS_HIGHLIGHTED</span><span class="sxs-lookup"><span data-stu-id="0b850-126">MSGSTATUS_HIGHLIGHTED</span></span> 
  
> <span data-ttu-id="0b850-127">A mensagem é realçado em exibições de pasta dos destinatários.</span><span class="sxs-lookup"><span data-stu-id="0b850-127">The message is to be highlighted in recipients' folder displays.</span></span> 
    
<span data-ttu-id="0b850-128">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="0b850-128">MSGSTATUS_REMOTE_DELETE</span></span> 
  
> <span data-ttu-id="0b850-129">A mensagem foi marcada para exclusão na loja remota de mensagens sem baixar no cliente local.</span><span class="sxs-lookup"><span data-stu-id="0b850-129">The message has been marked for deletion at the remote message store without downloading to the local client.</span></span> 
    
<span data-ttu-id="0b850-130">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="0b850-130">MSGSTATUS_REMOTE_DOWNLOAD</span></span> 
  
> <span data-ttu-id="0b850-131">A mensagem foi marcada para download a partir do armazenamento de mensagens remoto no cliente local.</span><span class="sxs-lookup"><span data-stu-id="0b850-131">The message has been marked for downloading from the remote message store to the local client.</span></span> 
    
<span data-ttu-id="0b850-132">MSGSTATUS_TAGGED</span><span class="sxs-lookup"><span data-stu-id="0b850-132">MSGSTATUS_TAGGED</span></span> 
  
> <span data-ttu-id="0b850-133">A mensagem foram marcada para uma finalidade definida pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="0b850-133">The message has been tagged for a client-defined purpose.</span></span>
    
<span data-ttu-id="0b850-134">Os sinalizadores **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**e **MSGSTATUS_TAGGED** são definidos pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="0b850-134">The **MSGSTATUS_DELMARKED**, **MSGSTATUS_HIDDEN**, **MSGSTATUS_HIGHLIGHTED**, and **MSGSTATUS_TAGGED** flags are defined by the client.</span></span> <span data-ttu-id="0b850-135">Provedores de transporte e o repositório passam esses bits sem qualquer ação.</span><span class="sxs-lookup"><span data-stu-id="0b850-135">Transport and store providers pass these bits without any action.</span></span> 
  
<span data-ttu-id="0b850-136">Os clientes podem interpretar esses valores de qualquer forma que é apropriada para seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="0b850-136">Clients can interpret these values in any way that is appropriate for their applications.</span></span> <span data-ttu-id="0b850-137">Uma maneira que muitos clientes usam essa propriedade é para exibir mensagens marcadas para exclusão com um ícone de representante.</span><span class="sxs-lookup"><span data-stu-id="0b850-137">One way that many clients use this property is to display messages marked for deletion with a representative icon.</span></span> 
  
<span data-ttu-id="0b850-138">Um cliente remoto visualizador pode definir **MSGSTATUS_REMOTE_DELETE** ou **MSGSTATUS_REMOTE_DOWNLOAD** em mensagens na pasta cabeçalho apresentada a ele pelo provedor de transporte remoto.</span><span class="sxs-lookup"><span data-stu-id="0b850-138">A remote viewer client can set **MSGSTATUS_REMOTE_DELETE** or **MSGSTATUS_REMOTE_DOWNLOAD** on messages in the header folder presented to it by the remote transport provider.</span></span> <span data-ttu-id="0b850-139">O aplicativo cliente pode examinar cada cabeçalho da mensagem nesta pasta para determinar se a mensagem deve ser baixada ou excluída ao armazenamento de mensagens remoto.</span><span class="sxs-lookup"><span data-stu-id="0b850-139">The client application can examine each message header in this folder to determine whether the message should be downloaded or deleted at the remote message store.</span></span> <span data-ttu-id="0b850-140">Ele usa o método [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) para definir o sinalizador apropriado.</span><span class="sxs-lookup"><span data-stu-id="0b850-140">It then uses the [IMAPIFolder::SetMessageStatus](imapifolder-setmessagestatus.md) method to set the appropriate flag.</span></span> <span data-ttu-id="0b850-141">**SetMessageStatus** é a única maneira para definir qualquer um dos sinalizadores nessa propriedade; o método [IMAPIProp::SetProps](imapiprop-setprops.md) não pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="0b850-141">**SetMessageStatus** is the only way to set any of the flags in this property; the [IMAPIProp::SetProps](imapiprop-setprops.md) method cannot be used.</span></span> <span data-ttu-id="0b850-142">Para recuperar essa propriedade, os clientes chamar [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) em vez de [IMAPIProp::GetProps](imapiprop-getprops.md).</span><span class="sxs-lookup"><span data-stu-id="0b850-142">To retrieve this property, clients call [IMAPIFolder::GetMessageStatus](imapifolder-getmessagestatus.md) rather than [IMAPIProp::GetProps](imapiprop-getprops.md).</span></span>
  
<span data-ttu-id="0b850-143">Bits 16 a 31 (0x10000 por meio de 0x80000000) dessa propriedade estarão disponíveis para uso pelo aplicativo cliente interpessoais mensagens (IPM).</span><span class="sxs-lookup"><span data-stu-id="0b850-143">Bits 16 through 31 (0x10000 through 0x80000000) of this property are available for use by the interpersonal message (IPM) client application.</span></span> <span data-ttu-id="0b850-144">Todos os outros bits são reservados para uso pelo MAPI; aqueles não definido na tabela anterior devem ser definidas inicialmente como zero e subsequentemente não foi alteradas.</span><span class="sxs-lookup"><span data-stu-id="0b850-144">All other bits are reserved for use by MAPI; those not defined in the preceding table should be initially set to zero and not altered subsequently.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0b850-145">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b850-145">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0b850-146">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="0b850-146">Protocol specifications</span></span>

<span data-ttu-id="0b850-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b850-147">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b850-148">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="0b850-148">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0b850-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0b850-149">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0b850-150">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="0b850-150">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0b850-151">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0b850-151">Header files</span></span>

<span data-ttu-id="0b850-152">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0b850-152">Mapidefs.h</span></span>
  
> <span data-ttu-id="0b850-153">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0b850-153">Provides data type definitions.</span></span>
    
<span data-ttu-id="0b850-154">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0b850-154">Mapitags.h</span></span>
  
> <span data-ttu-id="0b850-155">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0b850-155">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0b850-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b850-156">See also</span></span>



[<span data-ttu-id="0b850-157">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="0b850-157">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)


[<span data-ttu-id="0b850-158">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0b850-158">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0b850-159">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0b850-159">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0b850-160">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0b850-160">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0b850-161">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0b850-161">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

