---
title: Propriedade canônica PidTagAttachPayloadProviderGuidString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPayloadProviderGuidString
api_type:
- HeaderDef
ms.assetid: c9d4b561-53b3-492b-9324-9376dd7abddf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5051784ea08316477f3c8888ada9170e3d99c2b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361100"
---
# <a name="pidtagattachpayloadproviderguidstring-canonical-property"></a>Propriedade canônica PidTagAttachPayloadProviderGuidString

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o valor de um campo de cabeçalho MIME X-Payload-Provider-GUID.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_PAYLOAD_PROV_GUID_STR, PR_ATTACH_PAYLOAD_PROV_GUID_STR_A, PR_ATTACH_PAYLOAD_PROV_GUID_STR_W  <br/> |
|Identificador:  <br/> |0x3719  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Aplicativo do Outlook  <br/> |
   
## <a name="remarks"></a>Comentários

Para definir o valor dessas propriedades, os clientes MIME devem gravar um campo de cabeçalho X-Payload-Provider-GUID em uma entidade MIME que será analisada como um anexo.
  
Leitores MIME devem copiar esse valor de campo de cabeçalho para o valor da propriedade correspondente. Leitores MIME devem ignorar esse campo de cabeçalho quando ele aparecer em uma entidade MIME que é analisada como um corpo de mensagem ou mensagem, em vez de um anexo.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

