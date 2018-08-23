---
title: Centralizando o recebimento de NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579435"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="175d0-103">Centralizando o recebimento de NDRs</span><span class="sxs-lookup"><span data-stu-id="175d0-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="175d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="175d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="175d0-105">**Para fazer com que os relatórios de não entrega (NDRs) chegarem a um local central quando várias instâncias de seu cliente são executados simultaneamente**</span><span class="sxs-lookup"><span data-stu-id="175d0-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="175d0-106">Definir **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) com os valores apropriados para a conta que está para receber os relatórios.</span><span class="sxs-lookup"><span data-stu-id="175d0-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="175d0-107">Crie o identificador de entrada chamando [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) , se necessário.</span><span class="sxs-lookup"><span data-stu-id="175d0-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="175d0-108">Entenda que existem sistemas de mensagens que irá ignorar a conta que você solicitou para relatórios e enviá-las ao originador.</span><span class="sxs-lookup"><span data-stu-id="175d0-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="175d0-109">Reduza o impacto que isso terá sobre os administradores que precisarão percorrer os relatórios por:</span><span class="sxs-lookup"><span data-stu-id="175d0-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="175d0-110">Oferecendo uma classe de mensagem distinta, como IPM de sua mensagem original. Note.MSNNews.</span><span class="sxs-lookup"><span data-stu-id="175d0-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="175d0-111">Procure por mensagens de entrada com a classe Report.IPM.Note.MSNNews.NDR e encaminhá-las para a conta pretendido são fornecidos os relatórios.</span><span class="sxs-lookup"><span data-stu-id="175d0-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="175d0-112">Ao mesmo tempo, envie email para o sistema de mensagens que sua conta de relatório de não entrega para comunicar-se de que ele deve honram a propriedade **PR_REPORT_ENTRYID** de ignoradas.</span><span class="sxs-lookup"><span data-stu-id="175d0-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="175d0-113">Sistemas de mensagens mais que não respeitam **PR_REPORT_ENTRYID** não aceita as convenções de classe de mensagem MAPI ou.</span><span class="sxs-lookup"><span data-stu-id="175d0-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="175d0-114">Portanto, você receberá algo parecido com uma nota.</span><span class="sxs-lookup"><span data-stu-id="175d0-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="175d0-115">Este é um pouco mais difícil lidar com porque a entrada é então variável.</span><span class="sxs-lookup"><span data-stu-id="175d0-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="175d0-116">Examine o assunto e encaminhá-la, se você encontrar algo de uma lista de palavras significa que "não entregue" ou algo do seu assunto original.</span><span class="sxs-lookup"><span data-stu-id="175d0-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="175d0-117">Esteja preparado para ajustar essas listas ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="175d0-117">Be prepared to tune these lists over time.</span></span> 
    

