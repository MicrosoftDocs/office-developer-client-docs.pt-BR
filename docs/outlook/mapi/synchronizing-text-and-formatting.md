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
ms.openlocfilehash: d797932a9fd22944f1cfd78e7fb67cd3ddbf8632
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588815"
---
# <a name="synchronizing-text-and-formatting"></a>Sincronizar texto e formatação

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O principal desafio na enviando mensagens de formato Rich Text (RTF) é manter o sincronizada com a formatação de texto. Para garantir que quando as mensagens chegam ao seu destino estão como seus criadores foi projetados e que a formatação de texto e são sincronizados, MAPI fornece a função [RTFSync](rtfsync.md) . **RTFSync** é geralmente chamado por clientes RTF ciente antes de exibir mensagens de entrada e pelo spooler MAPI quando ele baixa mensagens a um provedor de transporte. Os chamadores especificam a área de possível discrepância, passando um ou dois sinalizadores para **RTFSync**:
  
- RTF_SYNC_BODY_CHANGED para indicar uma modificação no texto da mensagem.
    
- RTF_SYNC_RTF_CHANGED para indicar uma modificação na formatação da mensagem.
    
O processo de sincronização que ocorre em **RTFSync** é uma verificação de sofisticados de redundância cíclica (CRC) do texto da mensagem que ignora alguns caracteres e converte a outras pessoas. Caracteres que provavelmente foram adicionados por provedores de transporte são ignorados. MAPI define várias propriedades para trabalhar com RTF, conforme descrito na tabela a seguir. 
  
|**Propriedade RTF**|**Descrição**|
|:-----|:-----|
|**PR_RTF_SYNC_BODY_TAG** ([PidTagRtfSyncBodyTag](pidtagrtfsyncbodytag-canonical-property.md))  <br/> |Indica o início do texto da mensagem real.  <br/> |
|**PR_RTF_SYNC_BODY_CRC** ([PidTagRtfSyncBodyCrc](pidtagrtfsyncbodycrc-canonical-property.md))  <br/> |Contém o resultado da verificação de redundância cíclica do texto da mensagem.  <br/> |
|**PR_RTF_SYNC_BODY_COUNT** ([PidTagRtfSyncBodyCount](pidtagrtfsyncbodycount-canonical-property.md))  <br/> |Contém o número de caracteres em **PR_RTF_SYNC_BODY_CRC**.  <br/> |
|**PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md))  <br/> |Defina como TRUE quando a mensagem de texto e a formatação foram sincronizadas.  <br/> |
|**PR_RTF_SYNC_PREFIX_COUNT** ([PidTagRtfSyncPrefixCount](pidtagrtfsyncprefixcount-canonical-property.md))  <br/> |Contém o número de caracteres nonwhitespace que preceder o texto da mensagem.  <br/> |
|**PR_RTF_SYNC_TRAILING_COUNT** ([PidTagRtfSyncTrailingCount](pidtagrtfsynctrailingcount-canonical-property.md))  <br/> |Contém o número de caracteres nonwhitespace rastros o texto da mensagem.  <br/> |
   

