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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344559"
---
# <a name="smtp-addresses"></a><span data-ttu-id="b8152-103">Endereços SMTP</span><span class="sxs-lookup"><span data-stu-id="b8152-103">SMTP Addresses</span></span>

  
  
<span data-ttu-id="b8152-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8152-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8152-105">O formato dos endereços de email SMTP é definido na RFC 822.</span><span class="sxs-lookup"><span data-stu-id="b8152-105">The format of SMTP email addresses is defined in RFC 822.</span></span> <span data-ttu-id="b8152-106">Os componentes MAPI devem lidar com qualquer endereço compatível com o padrão.</span><span class="sxs-lookup"><span data-stu-id="b8152-106">MAPI components should handle any address that complies with that standard.</span></span> <span data-ttu-id="b8152-107">No enTanto, há uma forma específica de endereço RFC 822 que melhor codifica endereços MAPI:</span><span class="sxs-lookup"><span data-stu-id="b8152-107">However, there is a particular form of RFC 822 address that best encodes MAPI addresses:</span></span>
  
 <span data-ttu-id="b8152-108">_Display-Name_ **\<** _email-endereço_**\>**</span><span class="sxs-lookup"><span data-stu-id="b8152-108">_display-name_ **\<** _email-address_ **\>**</span></span>
  
<span data-ttu-id="b8152-109">Os colchetes angulares são incluídos como literais.</span><span class="sxs-lookup"><span data-stu-id="b8152-109">The angle brackets are included as literals.</span></span> <span data-ttu-id="b8152-110">Os espaços em branco são comuns em nomes para exibição; Eles não precisam ser colocados entre aspas.</span><span class="sxs-lookup"><span data-stu-id="b8152-110">Blanks are common in display names; they need not be quoted.</span></span> <span data-ttu-id="b8152-111">Um endereço típico pode ter a seguinte aparência, que pertence a um dos coautores da RFC 1521:</span><span class="sxs-lookup"><span data-stu-id="b8152-111">A typical address might look like this one, which belongs to one of the coauthors of RFC 1521:</span></span>
  
<span data-ttu-id="b8152-112">Nathaniel Borenstein \<NSB@bellcore.com\></span><span class="sxs-lookup"><span data-stu-id="b8152-112">Nathaniel Borenstein \<nsb@bellcore.com\></span></span>
  
<span data-ttu-id="b8152-113">Se o nome de exibição contiver caracteres com significado especial nos endereços SMTP, como \< ou @, o nome de exibição inteiro deverá ser colocado entre aspas duplas.</span><span class="sxs-lookup"><span data-stu-id="b8152-113">If the display name contains characters that have special meaning in SMTP addresses, such as \< or @, the entire display name should be enclosed in double quotes.</span></span> <span data-ttu-id="b8152-114">No email de saída, se o comprimento total do endereço de email e o nome de exibição exceder 255 caracteres, o nome para exibição deverá ser Descartado.</span><span class="sxs-lookup"><span data-stu-id="b8152-114">On outbound mail, if the total length of the email address plus display name exceeds 255 characters, the display name should be dropped.</span></span>
  
<span data-ttu-id="b8152-115">As partes de um endereço SMTP mapeiam as propriedades MAPI da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="b8152-115">The parts of an SMTP address map into MAPI properties as follows:</span></span>
  
|<span data-ttu-id="b8152-116">**Componente de endereço SMTP**</span><span class="sxs-lookup"><span data-stu-id="b8152-116">**SMTP address component**</span></span>|<span data-ttu-id="b8152-117">**Propriedade MAPI**</span><span class="sxs-lookup"><span data-stu-id="b8152-117">**MAPI property**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b8152-118">_Display-Name_ para todos os destinatários</span><span class="sxs-lookup"><span data-stu-id="b8152-118">_display-name_ for all recipients</span></span>  <br/> |<span data-ttu-id="b8152-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8152-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b8152-120">_exibir nome_ do campo de</span><span class="sxs-lookup"><span data-stu-id="b8152-120">_display-name_ for From field</span></span>  <br/> |<span data-ttu-id="b8152-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8152-121">**PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b8152-122">_Display-nome_ para o campo de remetente</span><span class="sxs-lookup"><span data-stu-id="b8152-122">_display-name_ for Sender field</span></span>  <br/> |<span data-ttu-id="b8152-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8152-123">**PR_SENT_REPRESENTING_NAME** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))</span></span>  <br/> |
| <span data-ttu-id="b8152-124">_email-endereço_</span><span class="sxs-lookup"><span data-stu-id="b8152-124">_email-address_</span></span> <br/> |<span data-ttu-id="b8152-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8152-125">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |
|<span data-ttu-id="b8152-126">implícito, sempre "SMTP"</span><span class="sxs-lookup"><span data-stu-id="b8152-126">implicit, always "SMTP"</span></span>  <br/> |<span data-ttu-id="b8152-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="b8152-127">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |
   
<span data-ttu-id="b8152-128">Se não houver um nome de exibição para um endereço no email de entrada, o endereço de email inteiro deverá ser usado em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="b8152-128">If there is no display name for an address on inbound mail, the entire email address should be used instead.</span></span> <span data-ttu-id="b8152-129">O tipo de endereço é sempre SMTP.</span><span class="sxs-lookup"><span data-stu-id="b8152-129">The address type is always SMTP.</span></span>
  
<span data-ttu-id="b8152-130">As propriedades de destinatário são obtidas da tabela de destinatários da mensagem MAPI; as propriedades do remetente são obtidas da própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="b8152-130">Recipient properties are taken from the MAPI message's recipient table; sender properties are taken from the message itself.</span></span>
  

