---
title: Propriedade canônica PidLidEmail2OriginalDisplayName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b3f59633fcea0b895cd024dbbbc106c8d492bf0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768373"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>Propriedade canônica PidLidEmail2OriginalDisplayName

  
  
**Aplica-se a**: Outlook 
  
Especifica o nome de exibição segundo que corresponde ao endereço de email especificado para o contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008094  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Se o valor da propriedade **dispidEmail2AddrType** ([PidLidEmail2AddressType](pidlidemail2addresstype-canonical-property.md)) for "SMTP", o valor da propriedade **PidLidEmail2OriginalDisplayName** respectivo será igual ao valor de **os respectivos dispidEmail2EmailAddress** propriedade ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)). A finalidade dessa propriedade é para exibir um endereço alternativo de fácil utilização que é equivalente ao **dispidEmail2EmailAddress**especificado no.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

