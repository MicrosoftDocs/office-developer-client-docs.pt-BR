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
ms.openlocfilehash: ce9c8b189991e4102fcc9d17b88747d4ce55efec
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570909"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mantém e fornece acesso às propriedades de anexos em mensagens. A interface **IAttach** não possui exclusivos métodos sua própria conta. Para obter mais informações sobre como usar os anexos, consulte [As tabelas de anexo](attachment-tables.md)e [Anexos de MAPI](mapi-attachments.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de anexo  <br/> |
|Implementada por:  <br/> |Provedores de armazenamento de mensagem  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IAttachment  <br/> |
|Tipo de ponteiro:  <br/> |LPATTACH  <br/> |
|Modelo de transação:  <br/> |Transacionadas  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

Essa interface não tem quaisquer métodos exclusivos.
  
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
   
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

