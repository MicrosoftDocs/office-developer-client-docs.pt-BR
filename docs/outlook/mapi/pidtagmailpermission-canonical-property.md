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
ms.openlocfilehash: fb0b66cbf0de1ac351bb2026a48e0154de779206
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571189"
---
# <a name="pidtagmailpermission-canonical-property"></a><span data-ttu-id="1f834-103">Propriedade canônica PidTagMailPermission</span><span class="sxs-lookup"><span data-stu-id="1f834-103">PidTagMailPermission Canonical Property</span></span>

  
  
<span data-ttu-id="1f834-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f834-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f834-105">Conterá TRUE se o usuário de mensagens tem permissão para enviar e receber mensagens.</span><span class="sxs-lookup"><span data-stu-id="1f834-105">Contains TRUE if the messaging user is allowed to send and receive messages.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1f834-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1f834-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f834-107">PR_MAIL_PERMISSION</span><span class="sxs-lookup"><span data-stu-id="1f834-107">PR_MAIL_PERMISSION</span></span>  <br/> |
|<span data-ttu-id="1f834-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f834-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f834-109">0x3A0E</span><span class="sxs-lookup"><span data-stu-id="1f834-109">0x3A0E</span></span>  <br/> |
|<span data-ttu-id="1f834-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="1f834-110">Data type:</span></span>  <br/> |<span data-ttu-id="1f834-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="1f834-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="1f834-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f834-112">Area:</span></span>  <br/> |<span data-ttu-id="1f834-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="1f834-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f834-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f834-114">Remarks</span></span>

<span data-ttu-id="1f834-115">Se essa propriedade não estiver definida, MAPI a tratará como tendo um valor TRUE.</span><span class="sxs-lookup"><span data-stu-id="1f834-115">If this property is not set, MAPI treats it as having a TRUE value.</span></span> 
  
<span data-ttu-id="1f834-116">Defina essa propriedade como FALSE em um diretório corporativo, onde algumas das entradas não são habilitados para email.</span><span class="sxs-lookup"><span data-stu-id="1f834-116">Set this property to FALSE in a corporate directory where some of the entries are not email-enabled.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="1f834-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f834-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="1f834-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1f834-118">Header files</span></span>

<span data-ttu-id="1f834-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f834-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f834-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1f834-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f834-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f834-121">Mapitags.h</span></span>
  
> <span data-ttu-id="1f834-122">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="1f834-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f834-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f834-123">See also</span></span>



[<span data-ttu-id="1f834-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f834-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f834-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1f834-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f834-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f834-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f834-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1f834-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

