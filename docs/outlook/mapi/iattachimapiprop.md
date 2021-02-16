---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409087"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mantém e fornece acesso às propriedades de anexos em mensagens. A interface **IAttach** não tem métodos exclusivos próprios. Para obter mais informações sobre como usar anexos, consulte [MapI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Exposto por:  <br/> |Objetos attachment  <br/> |
|Implementado por:  <br/> |Provedores de armazenamento de mensagens  <br/> |
|Chamado por:  <br/> |Aplicativos do cliente  <br/> |
|Identificador de interface:  <br/> |IID_IAttachment  <br/> |
|Tipo de ponteiro:  <br/> |LPATTACH  <br/> |
|Modelo de transação:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

Essa interface não tem métodos exclusivos.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

