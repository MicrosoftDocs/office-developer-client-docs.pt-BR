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
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361065"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Propriedade canônica PidTagAttachTransportName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de um arquivo de anexo modificado para que possa ser associado a mensagens TNEF. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Identificador:  <br/> |0x370C  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

O TNEF e o provedor de transporte usam essas propriedades. Eles geralmente não estão disponíveis para aplicativos cliente. 
  
Essas propriedades são comumente usadas pelo TNEF quando o sistema de mensagens subjacente não dá suporte aos nomes de arquivo fornecidos. Por exemplo, eles são usados quando o usuário anexa vários arquivos com o mesmo nome, como cinco arquivos denominados CONFIG.SYS. O provedor de transporte deve modificar os nomes para garantir que sejam exclusivos. Cada nome modificado aparece nas propriedades PR_ATTACH_TRANSPORT_NAME **e** associadas do anexo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

