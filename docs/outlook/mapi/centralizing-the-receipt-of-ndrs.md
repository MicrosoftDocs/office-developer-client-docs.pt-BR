---
title: Centralizar recebimentos de NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332659"
---
# <a name="centralizing-the-receipt-of-ndrs"></a><span data-ttu-id="edc2f-103">Centralizar recebimentos de NDRs</span><span class="sxs-lookup"><span data-stu-id="edc2f-103">Centralizing the receipt of NDRs</span></span>

<span data-ttu-id="edc2f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc2f-105">**Para que os relatórios de não entrega (NDRs) cheguem a um local central quando várias instâncias do seu cliente estão sendo executadas simultaneamente**</span><span class="sxs-lookup"><span data-stu-id="edc2f-105">**To have nondelivery reports (NDRs) arrive at a central location when multiple instances of your client are running simultaneously**</span></span>
  
1. <span data-ttu-id="edc2f-106">Defina **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) para os valores apropriados para a conta que será recebida os relatórios.</span><span class="sxs-lookup"><span data-stu-id="edc2f-106">Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)), and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports.</span></span> <span data-ttu-id="edc2f-107">Crie o identificador de entrada chamando [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) , se necessário.</span><span class="sxs-lookup"><span data-stu-id="edc2f-107">Create the entry identifier by calling [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) if necessary.</span></span> 
    
2. <span data-ttu-id="edc2f-108">Entenda que há sistemas de mensagens que ignorarão a conta solicitada por relatórios e as enviarão ao originador.</span><span class="sxs-lookup"><span data-stu-id="edc2f-108">Understand that there are messaging systems that will ignore the account you've requested for reports and send them to the originator.</span></span> <span data-ttu-id="edc2f-109">Reduza o impacto que isso terá em relação aos administradores que precisarão mover relatórios por:</span><span class="sxs-lookup"><span data-stu-id="edc2f-109">Reduce the impact that this will have on administrators that will need to move reports around by:</span></span>
    
- <span data-ttu-id="edc2f-110">Dando à sua mensagem original uma classe de mensagem distinta, como IPM. Note. MSNNews.</span><span class="sxs-lookup"><span data-stu-id="edc2f-110">Giving your original message a distinct message class, such as IPM.Note.MSNNews.</span></span> <span data-ttu-id="edc2f-111">Procure mensagens de entrada com o relatório de classe. IPM. Note. MSNNews. NDR e encaminhe-os para a conta que você pretendia que os relatórios.</span><span class="sxs-lookup"><span data-stu-id="edc2f-111">Look for incoming messages with class Report.IPM.Note.MSNNews.NDR and forward them to the account you intended reports to come to.</span></span> <span data-ttu-id="edc2f-112">Ao mesmo tempo, envie um email para o sistema de mensagens que ignorou sua conta de relatório de não-entrega para se comunicar que deve honrar a propriedade **PR_REPORT_ENTRYID** .</span><span class="sxs-lookup"><span data-stu-id="edc2f-112">At the same time, send email to the messaging system that ignored your nondelivery report account to communicate that it should honor the **PR_REPORT_ENTRYID** property.</span></span> 
    
- <span data-ttu-id="edc2f-113">A maioria dos sistemas de mensagens que não honra o **PR_REPORT_ENTRYID** não honrará as convenções de classe da mensagem MAPI.</span><span class="sxs-lookup"><span data-stu-id="edc2f-113">Most messaging systems which do not honor **PR_REPORT_ENTRYID** will not honor the MAPI message class conventions either.</span></span> <span data-ttu-id="edc2f-114">Portanto, você receberá algo parecido com uma observação.</span><span class="sxs-lookup"><span data-stu-id="edc2f-114">Therefore, you'll receive something that looks like a note.</span></span> <span data-ttu-id="edc2f-115">Isso é um pouco mais difícil de lidar porque a entrada é tão variável.</span><span class="sxs-lookup"><span data-stu-id="edc2f-115">This is a little harder to deal with because the input is so variable.</span></span> <span data-ttu-id="edc2f-116">Examine o assunto e encaminhe-o se encontrar algo de uma lista de palavras que signifique "não pode ser entregue" ou algo de seu assunto original.</span><span class="sxs-lookup"><span data-stu-id="edc2f-116">Look at the subject and forward it if you find either something from a list of words that mean "undeliverable" or something from your original subject.</span></span> <span data-ttu-id="edc2f-117">Esteja preparado para ajustar essas listas ao longo do tempo.</span><span class="sxs-lookup"><span data-stu-id="edc2f-117">Be prepared to tune these lists over time.</span></span> 
    

