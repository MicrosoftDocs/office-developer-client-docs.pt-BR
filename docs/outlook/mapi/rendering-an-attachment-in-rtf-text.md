---
title: Renderização de um anexo em texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b2a1a23f073d05e85c8203826e3407c5ae193f19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439790"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Renderização de um anexo em texto RTF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Clientes com conhecimento em RTF (Rich Text Format) podem recuperar informações de posição de renderização do texto da mensagem RTF procurando a seguinte sequência de escape na propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem:
  
 `\objattph`
  
 **Para localizar informações de renderização em texto formatado**
  
1. Chame **IMessage::GetAttachmentTable** para acessar a tabela de anexos da mensagem. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Crie uma restrição de propriedade que limite a tabela a linhas que não **PR_RENDERING_POSITION** igual a -1. Para obter mais informações, **consulte PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Chame **IMAPITable::Restrict** para impor a restrição. Para obter mais informações, consulte [IMAPITable::Restrict](imapitable-restrict.md).
    
4. Chame **IMAPITable::SortTable** para classificar os anexos. Para obter mais informações, consulte [IMAPITable::SortTable](imapitable-sorttable.md).
    
5. Chame **IMAPITable::QueryRows** para recuperar as linhas apropriadas. Para obter mais informações, [consulte IMAPITable::QueryRows](imapitable-queryrows.md).
    
6. Chame o método **IMAPIProp::OpenProperty** da mensagem para recuperar PR_RTF_COMPRESSED **com** a interface **IStream.** Para obter mais informações, [consulte IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.
    
7. Digitalizar o fluxo, procurando o espaço reservado de renderização,  `\objattph` . O caractere após esse espaço reservado é o lugar para o próximo anexo na tabela ordenada.
    

