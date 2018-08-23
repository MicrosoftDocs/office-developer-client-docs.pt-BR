---
title: Renderizar um anexo em texto RTF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 26372539-e9fe-464d-95c7-90b58c20b98f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d8fc10f876408d616c5acefb664ba5d61c927a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22562971"
---
# <a name="rendering-an-attachment-in-rtf-text"></a>Renderizar um anexo em texto RTF

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Formato Rich Text (RTF)-clientes cientes podem recuperar informações de posição de renderização do texto da mensagem RTF observando a seguinte sequência de escape na propriedade de **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) da mensagem:
  
 `\objattph`
  
 **Para localizar as informações de renderização em texto formatado**
  
1. Chame **IMessage::GetAttachmentTable** para acessar a tabela de anexos da mensagem. Para obter mais informações, consulte [IMessage::GetAttachmentTable](imessage-getattachmenttable.md).
    
2. Construa uma restrição de propriedade que limita a tabela de linhas que possuem **PR_RENDERING_POSITION** não é igual a -1. Para obter mais informações, consulte **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)).
    
3. Chame **IMAPITable:: Restrict** para impor a restrição. Para obter mais informações, consulte [IMAPITable:: Restrict](imapitable-restrict.md).
    
4. Chame **IMAPITable:: SortTable** para classificar os anexos. Para obter mais informações, consulte [IMAPITable:: SortTable](imapitable-sorttable.md).
    
5. Chame **IMAPITable:: QueryRows** para recuperar as linhas apropriadas. Para obter mais informações, consulte [IMAPITable:: QueryRows](imapitable-queryrows.md).
    
6. Chame o método de **IMAPIProp::OpenProperty** da mensagem para recuperar **PR_RTF_COMPRESSED** com a interface **IStream** . Para obter mais informações, consulte [IMAPIProp::OpenProperty](imapiprop-openproperty.md) e **PR_RTF_COMPRESSED**.
    
7. Examinar o fluxo, procurando por espaço reservado renderização, `\objattph`. O caractere seguinte este espaço reservado é o local para o próximo anexo na tabela classificada.
    

