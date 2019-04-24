---
title: Sincronização de texto e formatação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346596"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="36eb0-103">Sincronização de texto e formatação</span><span class="sxs-lookup"><span data-stu-id="36eb0-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="36eb0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36eb0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36eb0-105">O principal desafio no envio de mensagens no formato Rich Text (RTF) é manter o texto sincronizado com a formatação.</span><span class="sxs-lookup"><span data-stu-id="36eb0-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="36eb0-106">Para garantir que, quando as mensagens chegarem ao seu destino, elas sejam como originadores pretendidos e que o texto e a formatação estejam sincronizados, o MAPI fornece a função [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="36eb0-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="36eb0-107">**RTFSync** normalmente é chamado por clientes com reconhecimento de RTF antes de exibir mensagens de entrada e pelo spooler MAPI quando ele baixa mensagens para um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="36eb0-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="36eb0-108">Os chamadores especificam a área de possível discrepância passando um ou dois sinalizadores para **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="36eb0-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="36eb0-109">RTF_SYNC_BODY_CHANGED para indicar uma modificação no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="36eb0-110">RTF_SYNC_RTF_CHANGED para indicar uma modificação na formatação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="36eb0-111">O processo de sincronização que ocorre no **RTFSync** é uma CRC (verificação de redundância cíclica) sofisticada do texto da mensagem que ignora alguns caracteres e converte outros.</span><span class="sxs-lookup"><span data-stu-id="36eb0-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="36eb0-112">Os caracteres que mais provavelmente foram adicionados por provedores de transporte são ignorados.</span><span class="sxs-lookup"><span data-stu-id="36eb0-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="36eb0-113">MAPI define várias propriedades para trabalhar com RTF, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="36eb0-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="36eb0-114">**Propriedade RTF**</span><span class="sxs-lookup"><span data-stu-id="36eb0-114">**RTF property**</span></span>|<span data-ttu-id="36eb0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="36eb0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="36eb0-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-117">Indica o início do texto real da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="36eb0-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-119">Contém o resultado da verificação de redundância cíclica do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="36eb0-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-121">Contém o número de caracteres em **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="36eb0-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="36eb0-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-123">Defina como TRUE quando o texto e a formatação da mensagem tiverem sido sincronizados.</span><span class="sxs-lookup"><span data-stu-id="36eb0-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="36eb0-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-125">Contém o número de caracteres não-espaço em branco que precedem o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="36eb0-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="36eb0-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="36eb0-127">Contém o número de caracteres não-espaço em branco que trilham o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="36eb0-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   

