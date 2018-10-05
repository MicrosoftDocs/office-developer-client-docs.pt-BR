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
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401500"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propriedade canônica PidTagAttachNumber

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
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

