---
title: Propriedade canônica PidTagMailPermission
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMailPermission
api_type:
- HeaderDef
ms.assetid: f8270ef2-56d4-4b47-bdda-a39c966bbcba
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b396cd326dd25fd72346f9f8037e8a712b84a196
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430172"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="c757b-103">Propriedade canônica PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="c757b-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="c757b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c757b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c757b-105">Contém TRUE se o usuário de mensagens tem permissão para enviar e receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="c757b-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c757b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c757b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c757b-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="c757b-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="c757b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c757b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c757b-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="c757b-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="c757b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c757b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c757b-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c757b-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c757b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c757b-112">Area:</span></span>  <br/> |<span data-ttu-id="c757b-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="c757b-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c757b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c757b-114">Remarks</span></span>

<span data-ttu-id="c757b-115">Se essa propriedade não estiver definida, MAPI a tratará como tendo um valor VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="c757b-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="c757b-116">Definir essa propriedade como FALSE em um diretório corporativo onde algumas das entradas não estão habilitadas para email.</span><span class="sxs-lookup"><span data-stu-id="c757b-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c757b-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c757b-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c757b-118">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c757b-118">Header files</span></span>

<span data-ttu-id="c757b-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c757b-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="c757b-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c757b-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="c757b-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c757b-121">Mapitags.h</span></span>
  
> <span data-ttu-id="c757b-122">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c757b-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c757b-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c757b-123">See also</span></span>



[<span data-ttu-id="c757b-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c757b-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c757b-125">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c757b-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c757b-126">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c757b-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c757b-127">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c757b-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

