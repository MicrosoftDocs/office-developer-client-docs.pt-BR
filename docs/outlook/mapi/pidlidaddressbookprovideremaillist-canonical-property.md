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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348479"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propriedade canônica PidLidAddressBookProviderEmailList

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica quais propriedades de endereço eletrônico estão definidas no contato. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidABPEmailList  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008028  <br/> |
|Tipo de dados:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

Cada valor de PT_LONG nessa propriedade deve ser exclusivo na propriedade e deve ser definido como um dos valores na tabela a seguir. Se essa propriedade for definida, a propriedade **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) também deverá ser definida. Essas duas propriedades devem ser mantidas sincronizadas umas com as outras. Por exemplo, se um dos valores de **dispidABPEmailList** for "0x00000000", **dispidABPArrayType** deverá ter o bit "0x00000001" definido. 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|0x00000000  <br/> |Email1 é definido para o contato.  <br/> |
|0x00000001  <br/> |EMAIL2 é definido para o contato.  <br/> |
|0x00000002  <br/> |Email3 é definido para o contato.  <br/> |
|0x00000003  <br/> |O fax comercial é definido para o contato.  <br/> |
|0x00000004  <br/> |O fax residencial é definido para o contato.  <br/> |
|0x00000005  <br/> |O fax principal é definido para o contato.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

