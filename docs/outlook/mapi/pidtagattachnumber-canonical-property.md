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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327248"
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

Os armazenamentos de mensagens geram e mantêm essa propriedade. O número do anexo é a chave de classificação secundária, após a posição de renderização, na tabela de anexos. 
  
 **PR_ATTACH_NUM** é usado para abrir o anexo com o [método IMessage::OpenAttach.](imessage-openattach.md) Dentro da sessão de um aplicativo cliente, a PR_ATTACH_NUM **propriedade** de um anexo de mensagem permanece constante enquanto a tabela de anexos está aberta. 
  
O armazenamento de mensagens propaga alterações na tabela usando os métodos **IMessage::CreateAttach** e **IMessage::D eleteAttach.** Em sua opção, o armazenamento de mensagens pode gerar notificações de tabela em tabelas de anexo abertas para que os clientes possam sincronizar de forma ressincroniza para essas alterações. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

