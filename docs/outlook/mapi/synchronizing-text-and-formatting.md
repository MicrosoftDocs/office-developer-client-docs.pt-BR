---
title: Sincronizar texto e formatação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 40d7a45ab97e0d2f8e9d3db1e1d38eb3bdb75158
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770579"
---
# <a name="synchronizing-text-and-formatting"></a><span data-ttu-id="712d0-103">Sincronizar texto e formatação</span><span class="sxs-lookup"><span data-stu-id="712d0-103">Synchronizing Text and Formatting</span></span>

  
  
<span data-ttu-id="712d0-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="712d0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="712d0-105">O principal desafio na enviando mensagens de formato Rich Text (RTF) é manter o sincronizada com a formatação de texto.</span><span class="sxs-lookup"><span data-stu-id="712d0-105">The main challenge in sending Rich Text Format (RTF) messages is keeping the text synchronized with the formatting.</span></span> <span data-ttu-id="712d0-106">Para garantir que quando as mensagens chegam ao seu destino estão como seus criadores foi projetados e que a formatação de texto e são sincronizados, MAPI fornece a função [RTFSync](rtfsync.md) .</span><span class="sxs-lookup"><span data-stu-id="712d0-106">To ensure that when messages arrive at their destination they are as their originators intended and that the text and formatting are synchronized, MAPI provides the [RTFSync](rtfsync.md) function.</span></span> <span data-ttu-id="712d0-107">**RTFSync** é geralmente chamado por clientes RTF ciente antes de exibir mensagens de entrada e pelo spooler MAPI quando ele baixa mensagens a um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="712d0-107">**RTFSync** is typically called by RTF-aware clients before displaying incoming messages and by the MAPI spooler when it downloads messages to a transport provider.</span></span> <span data-ttu-id="712d0-108">Os chamadores especificam a área de possível discrepância, passando um ou dois sinalizadores para **RTFSync**:</span><span class="sxs-lookup"><span data-stu-id="712d0-108">Callers specify the area of possible discrepancy by passing one or two flags to **RTFSync**:</span></span>
  
- <span data-ttu-id="712d0-109">RTF_SYNC_BODY_CHANGED para indicar uma modificação no texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="712d0-109">RTF_SYNC_BODY_CHANGED to indicate a modification in message text.</span></span>
    
- <span data-ttu-id="712d0-110">RTF_SYNC_RTF_CHANGED para indicar uma modificação na formatação da mensagem.</span><span class="sxs-lookup"><span data-stu-id="712d0-110">RTF_SYNC_RTF_CHANGED to indicate a modification in message formatting.</span></span>
    
<span data-ttu-id="712d0-111">O processo de sincronização que ocorre em **RTFSync** é uma verificação de sofisticados de redundância cíclica (CRC) do texto da mensagem que ignora alguns caracteres e converte a outras pessoas.</span><span class="sxs-lookup"><span data-stu-id="712d0-111">The synchronization process that occurs in **RTFSync** is a sophisticated cyclic redundancy check (CRC) of the message text that ignores some characters and converts others.</span></span> <span data-ttu-id="712d0-112">Caracteres que provavelmente foram adicionados por provedores de transporte são ignorados.</span><span class="sxs-lookup"><span data-stu-id="712d0-112">Characters that most likely were added by transport providers are ignored.</span></span> <span data-ttu-id="712d0-113">MAPI define várias propriedades para trabalhar com RTF, conforme descrito na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="712d0-113">MAPI defines several properties for working with RTF as described in the following table.</span></span> 
  
|<span data-ttu-id="712d0-114">**Propriedade RTF**</span><span class="sxs-lookup"><span data-stu-id="712d0-114">**RTF property**</span></span>|<span data-ttu-id="712d0-115">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="712d0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="712d0-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-116">**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-117">Indica o início do texto da mensagem real.</span><span class="sxs-lookup"><span data-stu-id="712d0-117">Indicates the beginning of the real message text.</span></span>  <br/> |
|<span data-ttu-id="712d0-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-118">**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-119">Contém o resultado da verificação de redundância cíclica do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="712d0-119">Contains the result of the cyclic redundancy check of the message text.</span></span>  <br/> |
|<span data-ttu-id="712d0-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-120">**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-121">Contém o número de caracteres em **PR_RTF_SYNC_BODY_CRC**.</span><span class="sxs-lookup"><span data-stu-id="712d0-121">Contains the number of characters in **PR_RTF_SYNC_BODY_CRC**.</span></span>  <br/> |
|<span data-ttu-id="712d0-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-122">**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-123">Defina como TRUE quando a mensagem de texto e a formatação foram sincronizadas.</span><span class="sxs-lookup"><span data-stu-id="712d0-123">Set to TRUE when the message text and formatting have been synchronized.</span></span>  <br/> |
|<span data-ttu-id="712d0-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-124">**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-125">Contém o número de caracteres nonwhitespace que preceder o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="712d0-125">Contains the number of nonwhitespace characters that preceed the message text.</span></span>  <br/> |
|<span data-ttu-id="712d0-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="712d0-126">**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="712d0-127">Contém o número de caracteres nonwhitespace rastros o texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="712d0-127">Contains the number of nonwhitespace characters that trail the message text.</span></span>  <br/> |
   
