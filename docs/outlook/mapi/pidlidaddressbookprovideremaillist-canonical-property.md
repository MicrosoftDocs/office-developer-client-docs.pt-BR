---
title: Propriedade canônica PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390356"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propriedade canônica PidLidAddressBookProviderEmailList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica quais propriedades de endereço eletrônico estão definidas no contato. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidABPEmailList  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008028  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Cada valor PT_LONG desta propriedade deve ser exclusiva na propriedade e deve ser definida como um dos valores na tabela a seguir. Se essa propriedade estiver definida, a propriedade **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) também deve ser definida. Essas duas propriedades devem ser mantidas sincronizadas entre si. Por exemplo, se um dos valores em **dispidABPEmailList** for "0x00000000", em seguida, **dispidABPArrayType** deve ter o bit "0x00000001" definido. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |Email1 é definida para o contato.  <br/> |
|0x00000001  <br/> |Email2 é definida para o contato.  <br/> |
|0x00000002  <br/> |Email3 é definida para o contato.  <br/> |
|0x00000003  <br/> |Fax comercial é definido para o contato.  <br/> |
|0x00000004  <br/> |Fax residencial é definida para o contato.  <br/> |
|0x00000005  <br/> |Fax principal é definida para o contato.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

