---
title: Propriedades do destinatário para todas as mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328438"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="a466e-103">Propriedades do destinatário para todas as mensagens</span><span class="sxs-lookup"><span data-stu-id="a466e-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="a466e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a466e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a466e-105">As propriedades a seguir geralmente estão presentes para todos os destinatários de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a466e-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="a466e-106">**PR_EMAIL_ADDRESS** e **PR_SEARCH_KEY** são opcionais; todas as outras propriedades são obrigatórias.</span><span class="sxs-lookup"><span data-stu-id="a466e-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="a466e-107">**Título da tabela**</span><span class="sxs-lookup"><span data-stu-id="a466e-107">**Table Title**</span></span>

|<span data-ttu-id="a466e-108">**Property**</span><span class="sxs-lookup"><span data-stu-id="a466e-108">**Property**</span></span>|<span data-ttu-id="a466e-109">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a466e-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a466e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-111">Contém o tipo de endereço de email do usuário de mensagens, como SMTP.</span><span class="sxs-lookup"><span data-stu-id="a466e-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="a466e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-113">Contém o nome para exibição de um determinado objeto MAPI.</span><span class="sxs-lookup"><span data-stu-id="a466e-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="a466e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-115">Contém um valor usado para associar um ícone a uma linha específica de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="a466e-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="a466e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-117">Contém o endereço de email do usuário de mensagens.</span><span class="sxs-lookup"><span data-stu-id="a466e-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="a466e-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-119">Contém um identificador de entrada MAPI usado para abrir e editar as propriedades de um objeto MAPI específico.</span><span class="sxs-lookup"><span data-stu-id="a466e-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="a466e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-121">Contém o tipo de um objeto.</span><span class="sxs-lookup"><span data-stu-id="a466e-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="a466e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="a466e-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="a466e-123">Contém uma chave comparável à binária que identifica objetos correlacionados para uma pesquisa.</span><span class="sxs-lookup"><span data-stu-id="a466e-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

