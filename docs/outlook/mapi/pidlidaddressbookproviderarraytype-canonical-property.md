---
title: Propriedade canônica PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393086"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Propriedade canônica PidLidAddressBookProviderArrayType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica o estado de endereços de eletrônicos do contato e representa um conjunto de sinalizadores de bit.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidABPArrayType  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x00008029  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Comentários

O valor da propriedade **dispidABPArrayType** deve ser uma combinação de sinalizadores que especificam o estado do objeto de contato. Sinalizadores individuais são especificados na tabela a seguir. Se essa propriedade estiver definida, a propriedade **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) deve ser definida, também. Essas duas propriedades devem ser mantidas sincronizadas entre si. Por exemplo, se **dispidABPArrayType** tiver definido o bit "set 0x00000001", um dos valores de **dispidABPEmailList** deve ser "0x00000000". 
  
|**Bit**|**Descrição**|
|:-----|:-----|
|0x00000001  <br/> |Email1 é definida para o contato.  <br/> |
|0x00000002  <br/> |Email2 é definida para o contato.  <br/> |
|0x00000004  <br/> |Email3 é definida para o contato.  <br/> |
|0x00000008  <br/> |Fax comercial é definido para o contato.  <br/> |
|0x00000010  <br/> |Fax residencial é definida para o contato.  <br/> |
|0x00000020  <br/> |Fax principal é definida para o contato.  <br/> |
   
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

