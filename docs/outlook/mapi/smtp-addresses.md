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
ms.openlocfilehash: 655d48d1ea937659f85e0ef7379425759ea7e256
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591356"
---
# <a name="smtp-addresses"></a><span data-ttu-id="d344a-103">Endereços SMTP</span><span class="sxs-lookup"><span data-stu-id="d344a-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="d344a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d344a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d344a-105">O formato dos endereços de email SMTP é definido no RFC 822.</span><span class="sxs-lookup"><span data-stu-id="d344a-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="d344a-106">Componentes MAPI devem lidar com qualquer endereço compatível com esse padrão.</span><span class="sxs-lookup"><span data-stu-id="d344a-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="d344a-107">No entanto, há um determinado formato de endereço de RFC 822 que melhor codifica endereços MAPI:</span><span class="sxs-lookup"><span data-stu-id="d344a-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="d344a-108">_nome para exibição_ **\<** _endereço de email_**\>**</span><span class="sxs-lookup"><span data-stu-id="d344a-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="d344a-109">Os colchetes angulares são incluídos como literais.</span><span class="sxs-lookup"><span data-stu-id="d344a-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="d344a-110">Espaços em branco são comuns em nomes de exibição; eles não precisam ser citados.</span><span class="sxs-lookup"><span data-stu-id="d344a-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="d344a-111">Um endereço típico pode parecer como este, que pertence a um dos coauthors do RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="d344a-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="d344a-112">Nathaniel Borenstein \<nsb@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="d344a-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="d344a-113">Se o nome de exibição contém caracteres que têm um significado especial em endereços SMTP, tais como \< ou @, o nome para exibição inteira deve estar entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="d344a-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="d344a-114">Em mensagens de saída, se o comprimento total do endereço de email mais exibir nome exceda 255 caracteres, o nome para exibição deve ser descartado.</span><span class="sxs-lookup"><span data-stu-id="d344a-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="d344a-115">As partes de um endereço SMTP ser mapeadas para propriedades MAPI da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d344a-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="d344a-116">**Componente de endereço de SMTP**</span><span class="sxs-lookup"><span data-stu-id="d344a-116">**SMTP address component**</span></span>|<span data-ttu-id="d344a-117">**Propriedade MAPI**</span><span class="sxs-lookup"><span data-stu-id="d344a-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d344a-118">_nome de exibição_ para todos os destinatários</span><span class="sxs-lookup"><span data-stu-id="d344a-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="d344a-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d344a-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d344a-120">_nome de exibição_ para do campo</span><span class="sxs-lookup"><span data-stu-id="d344a-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="d344a-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d344a-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d344a-122">_nome de exibição_ para o campo de remetente</span><span class="sxs-lookup"><span data-stu-id="d344a-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="d344a-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d344a-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="d344a-124">_endereço de email_</span><span class="sxs-lookup"><span data-stu-id="d344a-124">_email-address_</span></span> <br/> |<span data-ttu-id="d344a-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d344a-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="d344a-126">implícita, sempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="d344a-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="d344a-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d344a-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="d344a-128">Se não houver nenhum nome de exibição para um endereço de email de entrada, o endereço de email inteira deve ser usado.</span><span class="sxs-lookup"><span data-stu-id="d344a-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="d344a-129">O tipo de endereço é sempre SMTP.</span><span class="sxs-lookup"><span data-stu-id="d344a-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="d344a-130">Propriedades de destinatário são obtidas da tabela de destinatário da mensagem MAPI; Propriedades do remetente são utilizadas da própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="d344a-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

