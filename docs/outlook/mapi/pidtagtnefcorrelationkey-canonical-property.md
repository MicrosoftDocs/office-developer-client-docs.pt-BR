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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341948"
---
# <a name="pidtagtnefcorrelationkey-canonical-property"></a>Propriedade canônica PidTagTnefCorrelationKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que correlaciona um anexo TNEF (Transport neutral Encapsulation Format) com uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_TNEF_CORRELATION_KEY  <br/> |
|Identificador:  <br/> |0x007F  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os subobjetos de anexo TNEF exponham essa propriedade. Essa propriedade determina se um arquivo TNEF de entrada pertence ou não à mensagem à qual está anexado. É usado principalmente por provedores de transporte e gateways.
  
Em uma mensagem de saída, o provedor de transporte deve calcular um valor binário exclusivo para essa mensagem ou usar um valor existente que satisfaça o requisito de exclusividade, como um identificador de mensagem. O provedor de transporte deve armazenar esse valor nessa propriedade e, em seguida, chamar o método [ITnef::](itnef-addprops.md) addprops para encapsulá-lo. O mesmo valor também deve ser armazenado no envelope de transporte em um local definido pelo provedor, como o cabeçalho da mensagem. 
  
Em uma mensagem de entrada, o provedor de transporte deve chamar o método [ITnef:: ExtractProps](itnef-extractprops.md) para decapsulate o anexo TNEF e comparar essa propriedade com o valor armazenado no envelope de transporte. Se os valores forem correspondentes, o TNEF deverá ser processado normalmente, ou seja, todas as propriedades extraídas do anexo TNEF deverão ser usadas. Se os valores não corresponderem, todas as propriedades do anexo TNEF deverão ser ignoradas. Se essa propriedade não for definida, o arquivo TNEF deverá ser considerado como pertencer a essa mensagem, e as outras propriedades extraídas dela deverão ser usadas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte as convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
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

