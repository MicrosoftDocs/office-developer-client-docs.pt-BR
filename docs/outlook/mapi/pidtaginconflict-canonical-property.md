---
title: Propriedade canônica PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 573e0ba37d4117d85193933a3a5045b5060fbd3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769350"
---
# <a name="pidtaginconflict-canonical-property"></a><span data-ttu-id="1b3b1-103">Propriedade canônica PidTagInConflict</span><span class="sxs-lookup"><span data-stu-id="1b3b1-103">PidTagInConflict Canonical Property</span></span>

  
  
<span data-ttu-id="1b3b1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b3b1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b3b1-105">Contém TRUE quando o anexo representa uma réplica alternativa.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-105">Contains TRUE when the attachment represents an alternate replica.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1b3b1-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1b3b1-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1b3b1-107">PR_IN_CONFLICT</span><span class="sxs-lookup"><span data-stu-id="1b3b1-107">PR_IN_CONFLICT</span></span>  <br/> |
|<span data-ttu-id="1b3b1-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1b3b1-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1b3b1-109">0x666C</span><span class="sxs-lookup"><span data-stu-id="1b3b1-109">0x666C</span></span>  <br/> |
|<span data-ttu-id="1b3b1-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1b3b1-110">Data type:</span></span>  <br/> |<span data-ttu-id="1b3b1-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1b3b1-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1b3b1-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1b3b1-112">Area:</span></span>  <br/> |<span data-ttu-id="1b3b1-113">Observação de conflito</span><span class="sxs-lookup"><span data-stu-id="1b3b1-113">Conflict note</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1b3b1-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b3b1-114">Remarks</span></span>

<span data-ttu-id="1b3b1-115">O cliente de email e o servidor devem gerar uma mensagem de resolução de conflito quando detectar um conflito contra a versão atual de uma mensagem na réplica durante a sincronização.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-115">The email client and server must generate a conflict resolve message when detecting a conflict against the current version of a message in the replica during synchronization.</span></span> <span data-ttu-id="1b3b1-116">É importante entender o que é possível que a versão atual da mensagem na réplica local foi transmitida durante a operação de sincronização atual.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-116">It is important to understand that it is possible that the current version of the message in the local replica was transmitted during the current synchronization operation.</span></span> <span data-ttu-id="1b3b1-117">Isso acontecerá quando o conflito já existe no servidor antes de qualquer uma das mensagens conflitantes foram baixados para a réplica local.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-117">This will happen when the conflict already exists on the server before any of the conflicting messages were downloaded to the local replica.</span></span> <span data-ttu-id="1b3b1-118">Um conflito resolver mensagem deve ser sincronizada como independentes réplicas com PCLs conflitantes.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-118">A conflict resolve message must be synchronized as independent replicas with conflicting PCLs.</span></span> <span data-ttu-id="1b3b1-119">O conflito resolver mensagem propriamente dita não deve ser sincronizada entre cliente e servidor; somente as réplicas independentes que devem ser trocadas.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-119">The conflict resolve message itself must not be synchronized between client and server; only the independent replicas should be exchanged.</span></span> <span data-ttu-id="1b3b1-120">O parceiro de sincronização deve gerar uma nova mensagem que corresponda à estrutura da mensagem de conflito.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-120">The synchronization partner must then generate a new message that matches the structure of the conflict message.</span></span> <span data-ttu-id="1b3b1-121">Portanto, é importante que o cliente e servidor usam o mesmo algoritmo para detectar o item "prêmio".</span><span class="sxs-lookup"><span data-stu-id="1b3b1-121">Therefore, it is important that client and server use the same algorithm to detect the "winner" item.</span></span> <span data-ttu-id="1b3b1-122">As regras a seguir devem ser aplicadas para detectar o "prêmio":</span><span class="sxs-lookup"><span data-stu-id="1b3b1-122">The following rules must be applied to detect the "winner":</span></span>
  
1. <span data-ttu-id="1b3b1-123">Hora da última modificação.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-123">Last modification time.</span></span>
    
2. <span data-ttu-id="1b3b1-124">Superior CN GUID (usando a comparação de memória) para quebrar tie.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-124">Higher CN GUID (using memory compare) to break tie.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="1b3b1-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b3b1-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="1b3b1-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1b3b1-126">Protocol specifications</span></span>

<span data-ttu-id="1b3b1-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b3b1-127">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b3b1-128">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1b3b1-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1b3b1-129">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1b3b1-130">Trata-se de sincronização de dados de objeto de mensagens entre um servidor e um cliente.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-130">Handles synchronizing messaging object data between a server and a client.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1b3b1-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1b3b1-131">Header files</span></span>

<span data-ttu-id="1b3b1-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1b3b1-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="1b3b1-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="1b3b1-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1b3b1-134">Mapitags.h</span></span>
  
> <span data-ttu-id="1b3b1-135">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="1b3b1-135">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b3b1-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b3b1-136">See also</span></span>



[<span data-ttu-id="1b3b1-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3b1-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1b3b1-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1b3b1-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1b3b1-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1b3b1-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1b3b1-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1b3b1-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

