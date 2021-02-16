---
title: Sincronizando texto e formatação
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d7e166f0-1214-4571-b9a8-366960772a7a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 852ef988566ade8fca6551bea0d618199319d1d4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435100"
---
# <a name="synchronizing-text-and-formatting"></a>Sincronizando texto e formatação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O principal desafio ao enviar mensagens RTF (Rich Text Format) é manter o texto sincronizado com a formatação. Para garantir que, quando as mensagens chegarem ao seu destino, elas sejam como seus originores pretendido e que o texto e a formatação estejam sincronizados, o MAPI fornece a função [RTFSync.](rtfsync.md) **O RTFSync** normalmente é chamado por clientes com conhecimento de RTF antes de exibir mensagens de entrada e pelo spooler MAPI ao baixar mensagens para um provedor de transporte. Os chamadores especificam a área de discrepância possível passando um ou dois sinalizadores para **RTFSync:**
  
- RTF_SYNC_BODY_CHANGED para indicar uma modificação no texto da mensagem.
    
- RTF_SYNC_RTF_CHANGED para indicar uma modificação na formatação da mensagem.
    
O processo de sincronização que ocorre no **RTFSync** é uma verificação cíclica sofisticada de redundância (CRC) do texto da mensagem que ignora alguns caracteres e converte outros. Os caracteres que provavelmente foram adicionados por provedores de transporte são ignorados. MAPI define várias propriedades para trabalhar com RTF conforme descrito na tabela a seguir. 
  
|**Propriedade RTF**|**Descrição**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indica o início do texto real da mensagem.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contém o resultado da verificação de redundância cíclica do texto da mensagem.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contém o número de caracteres em **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |De definida como TRUE quando o texto e a formatação da mensagem foram sincronizados.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contém o número de caracteres não-whitespace que antes do texto da mensagem.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contém o número de caracteres não-whitespace que segue o texto da mensagem.  <br/> |
   

