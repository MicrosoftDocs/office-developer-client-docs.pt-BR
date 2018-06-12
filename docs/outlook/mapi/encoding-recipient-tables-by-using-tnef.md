---
title: Tabelas de destinatários de codificação usando TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8110eff9b38c76023621f34396d65714a4316d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766506"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="8fd88-103">Tabelas de destinatários de codificação usando TNEF</span><span class="sxs-lookup"><span data-stu-id="8fd88-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="8fd88-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8fd88-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8fd88-105">A codificação de uma tabela de destinatário no fluxo TNEF raramente é necessária como sistemas de mensagens mais suportam listas destinatários diretamente.</span><span class="sxs-lookup"><span data-stu-id="8fd88-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="8fd88-106">Em geral, as propriedades do destinatário são transmitidas no cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8fd88-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="8fd88-107">Quando a inclusão da tabela destinatário for necessário, o TNEF pode codificar tabela de destinatário, como parte do seu processamento normal.</span><span class="sxs-lookup"><span data-stu-id="8fd88-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="8fd88-108">Isso é feito durante a fase inicial do processamento de TNEF.</span><span class="sxs-lookup"><span data-stu-id="8fd88-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="8fd88-109">Provedor de transporte que pode incluir a tabela de destinatário da mensagem chamando o método [ITnef::AddProps](itnef-addprops.md) com a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada na lista de inclusão.</span><span class="sxs-lookup"><span data-stu-id="8fd88-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="8fd88-110">TNEF obtém uma tabela de destinatário da mensagem, consulta o conjunto de coluna e processa todas as linhas da tabela no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="8fd88-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="8fd88-111">Um método alternativo está disponível se o provedor de transporte precisa modificar a tabela de destinatário antes que ela é codificada.</span><span class="sxs-lookup"><span data-stu-id="8fd88-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="8fd88-112">O provedor de transporte pode construir a tabela necessária e então chamar o método [ITnef::EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="8fd88-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="8fd88-113">Se NULL é passada no parâmetro _lpRecipTable_ , a tabela de destinatários é executada diretamente a partir da mensagem conforme descrito para **ITnef::AddProps**.</span><span class="sxs-lookup"><span data-stu-id="8fd88-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

