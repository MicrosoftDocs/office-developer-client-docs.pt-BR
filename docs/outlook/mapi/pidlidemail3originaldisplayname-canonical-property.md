---
title: Propriedade canônica PidLidEmail3OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail3OriginalDisplayName
api_type:
- COM
ms.assetid: f3fa392a-c3b1-46dd-bf9b-5ce310719542
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e69bcde35bcfec7746893ee18423aca3a24a6c4a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338070"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>Propriedade canônica PidLidEmail3OriginalDisplayName

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o terceiro nome para exibição que corresponde ao endereço de email especificado para o contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x000080A4  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se o valor da propriedade **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) for "SMTP", o valor da respectiva **propriedade dispidEmail3OriginalDisplayName** deve ser igual ao valor do respectivo **dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)). O objetivo dessa propriedade é exibir um endereço amigável alternativo que seja equivalente ao endereço no **dispidEmail3EmailAddress**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

