---
title: Propriedade canônica PidTagTnefCorrelationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTnefCorrelationKey
api_type:
- COM
ms.assetid: a7f05c8c-59b4-4d5b-8e70-ebcde5f2ed45
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e38cf93523c14d2d58c48e24a79249674298b4b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393842"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propriedade canônica PidTagTnefCorrelationKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que correlaciona um anexo TNEF Transport Neutral Encapsulation Format () com uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificador:  <br/> |0x007F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os sub-objetos do anexo TNEF exponham essa propriedade. Esta propriedade determina se ou não um arquivo TNEF entrado pertence à mensagem a que ela está anexada. Ele é usado principalmente pelos provedores de transporte e gateways.
  
Em uma mensagem de saída, o provedor de transporte deve compute um valor binário exclusivo para a mensagem ou use um valor existente que satisfaz o requisito de exclusividade, como um identificador de mensagem. O provedor de transporte deve armazenar esse valor nessa propriedade e, em seguida, chame o método de [ITnef::AddProps](itnef-addprops.md) para encapsulam a ele. O mesmo valor também deve ser armazenado no envelope transporte em um local definido pelo provedor, como o cabeçalho da mensagem. 
  
Em uma mensagem de entrada, o provedor de transporte deve chamar o método [ITnef::ExtractProps](itnef-extractprops.md) para decapsulate o anexo TNEF e, em seguida, essa propriedade em comparação com o valor armazenado no envelope da transporte. Se os valores coincidirem, TNEF deve ser processada normalmente, ou seja, todas as propriedades extraídas de anexo TNEF devem ser usadas. Se os valores não coincidirem, todas as propriedades do anexo TNEF devem ser ignoradas. Se essa propriedade não estiver definida, o arquivo TNEF deve ser considerado ao pertencem a esta mensagem e as outras propriedades extraídas de que ele devem ser usadas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos de mensagem e o anexo em uma representação de fluxo eficiente.
    
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

