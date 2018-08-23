---
title: Propriedade canônica PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3899f7000bfa1365228864d97b4410833b774bed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570777"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propriedade canônica PidTagAttachTransportName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de um arquivo de anexo modificado de modo que ela pode ser associada a mensagens TNEF. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificador:  <br/> |0x370C  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

TNEF e o provedor de transporte utilizar essas propriedades. Eles geralmente não estão disponíveis para os aplicativos cliente. 
  
Essas propriedades são usadas pelo TNEF quando o sistema de mensagens subjacente não oferece suporte a nomes de arquivo fornecido. Por exemplo, eles são usados quando o usuário anexa vários arquivos com o mesmo nome, como arquivos de cinco chamado CONFIG. SYS. O provedor de transporte deve modificar os nomes para garantir que eles sejam exclusivos. Cada nome modificado aparece no **PR_ATTACH_TRANSPORT_NAME** de seu anexo e propriedades associadas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

