---
title: Codificar tabelas de destinatários usando TNEF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cd2f595f-4dd0-4704-b670-6857d6c843ca
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1ed047424e4a6d64c08b511a15769c081a0d8c4e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417956"
---
# <a name="encoding-recipient-tables-by-using-tnef"></a><span data-ttu-id="df747-103">Codificar tabelas de destinatários usando TNEF</span><span class="sxs-lookup"><span data-stu-id="df747-103">Encoding Recipient Tables by Using TNEF</span></span>

  
  
<span data-ttu-id="df747-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df747-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df747-105">A codificação de uma tabela de destinatários para o fluxo de TNEF é raramente necessária, pois a maioria dos sistemas de mensagens dão suporte a listas de destinatários diretamente.</span><span class="sxs-lookup"><span data-stu-id="df747-105">The encoding of a recipient table into the TNEF stream is rarely necessary since most messaging systems support recipient lists directly.</span></span> <span data-ttu-id="df747-106">Em geral, as propriedades do destinatário são transmitidas no cabeçalho da mensagem.</span><span class="sxs-lookup"><span data-stu-id="df747-106">In general, the recipient properties are transmitted in the message header.</span></span> <span data-ttu-id="df747-107">Quando a inclusão da tabela de destinatários é necessária, o TNEF pode codificar a tabela de destinatários como parte de seu processamento normal.</span><span class="sxs-lookup"><span data-stu-id="df747-107">When inclusion of the recipient table is necessary, TNEF can encode the recipient table as a part of its usual processing.</span></span> <span data-ttu-id="df747-108">Isso é feito durante a fase inicial do processamento TNEF.</span><span class="sxs-lookup"><span data-stu-id="df747-108">This is done during the initial phase of TNEF processing.</span></span> <span data-ttu-id="df747-109">O provedor de transporte pode incluir a tabela de destinatários da mensagem chamando o método [ITnef::](itnef-addprops.md) addprops com a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) especificada na lista de inclusão.</span><span class="sxs-lookup"><span data-stu-id="df747-109">The transport provider can include the message's recipient table by calling the [ITnef::AddProps](itnef-addprops.md) method with the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property specified in the inclusion list.</span></span> <span data-ttu-id="df747-110">O TNEF Obtém a tabela de destinatários da mensagem, consulta o conjunto de colunas e processa todas as linhas da tabela no fluxo TNEF.</span><span class="sxs-lookup"><span data-stu-id="df747-110">TNEF gets the recipient table from the message, queries the column set, and processes every row of the table into the TNEF stream.</span></span>
  
<span data-ttu-id="df747-111">Um método alternativo estará disponível se o provedor de transporte precisar modificar a tabela de destinatários antes de ser codificada.</span><span class="sxs-lookup"><span data-stu-id="df747-111">An alternate method is available if the transport provider needs to modify the recipient table before it is encoded.</span></span> <span data-ttu-id="df747-112">O provedor de transporte pode construir a tabela necessária e, em seguida, chamar o método [ITnef:: EncodeRecips](itnef-encoderecips.md) .</span><span class="sxs-lookup"><span data-stu-id="df747-112">The transport provider can construct the necessary table and then call the [ITnef::EncodeRecips](itnef-encoderecips.md) method.</span></span> <span data-ttu-id="df747-113">Se NULL for passado no parâmetro _lpRecipTable_ , a tabela de destinatários será obtida diretamente da mensagem, conforme descrito para **ITnef::** addprops.</span><span class="sxs-lookup"><span data-stu-id="df747-113">If NULL is passed in the  _lpRecipTable_ parameter, then the recipient table is taken directly from the message as described for **ITnef::AddProps**.</span></span>
  

