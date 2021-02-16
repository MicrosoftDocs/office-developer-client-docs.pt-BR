---
title: Endereços SMTP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 42015740-a94f-4628-bf32-b7fc2fdb9ff6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fb4402100891df8b27c8d26900a4acd05f4183e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419622"
---
# <a name="smtp-addresses"></a><span data-ttu-id="6fdf4-103">Endereços SMTP</span><span class="sxs-lookup"><span data-stu-id="6fdf4-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="6fdf4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fdf4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fdf4-105">O formato dos endereços de email SMTP é definido na RFC 822.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="6fdf4-106">Os componentes MAPI devem lidar com qualquer endereço que seja de acordo com esse padrão.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="6fdf4-107">No entanto, há uma forma específica de endereço RFC 822 que codifica melhor os endereços MAPI:</span><span class="sxs-lookup"><span data-stu-id="6fdf4-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="6fdf4-108">_display-name_ **\<** _email-address_**\>**</span><span class="sxs-lookup"><span data-stu-id="6fdf4-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="6fdf4-109">Os colchetes angulares são incluídos como literais.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="6fdf4-110">Espaços em branco são comuns em nomes de exibição; eles não precisam ser entre aspas.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="6fdf4-111">Um endereço típico pode se parecer com este, que pertence a um dos coautores da RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="6fdf4-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="6fdf4-112">Rúl Borenstein \< nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="6fdf4-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="6fdf4-113">Se o nome de exibição contiver caracteres que tenham significado especial em endereços SMTP, como ou @, todo o nome de exibição deverá estar entre \< aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="6fdf4-114">No email de saída, se o tamanho total do endereço de email mais o nome de exibição exceder 255 caracteres, o nome de exibição deverá ser descartado.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="6fdf4-115">As partes de um mapa de endereço SMTP em propriedades MAPI da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="6fdf4-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="6fdf4-116">**Componente de endereço SMTP**</span><span class="sxs-lookup"><span data-stu-id="6fdf4-116">**SMTP address component**</span></span>|<span data-ttu-id="6fdf4-117">**Propriedade MAPI**</span><span class="sxs-lookup"><span data-stu-id="6fdf4-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6fdf4-118">_display-name_ para todos os destinatários</span><span class="sxs-lookup"><span data-stu-id="6fdf4-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="6fdf4-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fdf4-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="6fdf4-120">_display-name_ for From field</span><span class="sxs-lookup"><span data-stu-id="6fdf4-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="6fdf4-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fdf4-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="6fdf4-122">_display-name_ para o campo Remetente</span><span class="sxs-lookup"><span data-stu-id="6fdf4-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="6fdf4-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fdf4-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="6fdf4-124">_email-address_</span><span class="sxs-lookup"><span data-stu-id="6fdf4-124">_email-address_</span></span> <br/> |<span data-ttu-id="6fdf4-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fdf4-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="6fdf4-126">implícito, sempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="6fdf4-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="6fdf4-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="6fdf4-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="6fdf4-128">Se não houver um nome de exibição para um endereço no email de entrada, todo o endereço de email deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="6fdf4-129">O tipo de endereço é sempre SMTP.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="6fdf4-130">As propriedades de destinatário são retiradas da tabela de destinatários da mensagem MAPI; as propriedades do remetente são retiradas da mensagem em si.</span><span class="sxs-lookup"><span data-stu-id="6fdf4-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

