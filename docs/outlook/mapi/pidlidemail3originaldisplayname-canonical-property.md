---
title: Propriedade canônico de PidLidEmail3OriginalDisplayName
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 3ac90910e143d05c17b73aa6a1062cd0999b0d3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768398"
---
# <a name="pidlidemail3originaldisplayname-canonical-property"></a>Propriedade canônico de PidLidEmail3OriginalDisplayName

  
  
**Aplica-se a**: Outlook 
  
Especifica o nome de exibição de terceiro que corresponde ao endereço de email especificado para o contato.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidEmail3OriginalDisplayName  <br/> |
|Propriedade definida:  <br/> |PSETID_Address  <br/> |
|ID de longo (LID):  <br/> |0x000080A4  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Contato  <br/> |
   
## <a name="remarks"></a>Coment�rios

Se o valor da propriedade **dispidEmail3AddrType** ([PidLidEmail3AddressType](pidlidemail3addresstype-canonical-property.md)) for "SMTP", o valor da propriedade respectivos **dispidEmail3OriginalDisplayName** será igual ao valor de **os respectivos dispidEmail3EmailAddress** ([PidLidEmail3EmailAddress](pidlidemail3emailaddress-canonical-property.md)). A finalidade dessa propriedade é para exibir um endereço alternativo de fácil utilização que é equivalente ao **dispidEmail3EmailAddress**especificado no.
  
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
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

