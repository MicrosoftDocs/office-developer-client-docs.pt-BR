---
title: Propriedade canônica PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c4a46710311f2c4d26ec3d667c7bf535df69f595
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768980"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propriedade canônica PidTagAttachNumber

  
  
**Aplica-se a**: Outlook 
  
Contém um número que identifica exclusivamente o anexo dentro de sua mensagem pai. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_NUM  <br/> |
|Identificador:  <br/> |0x0E21  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Os armazenamentos de mensagem geram e manter essa propriedade. O número de anexo é a chave de classificação secundária, após a posição de renderização, na tabela de anexo. 
  
 **PR_ATTACH_NUM** é usado para abrir o anexo com o método [IMessage::OpenAttach](imessage-openattach.md) . Dentro da sessão de um aplicativo cliente, a propriedade **PR_ATTACH_NUM** de anexo de uma mensagem permanece constante desde que a tabela de anexo está aberta. 
  
O armazenamento de mensagens propaga as alterações na tabela usando os métodos **IMessage::CreateAttach** e **IMessage::DeleteAttach** . A seu critério o armazenamento de mensagens pode gerar notificações de tabela em tabelas abrir anexo para que os clientes podem sincronizar para essas alterações. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

