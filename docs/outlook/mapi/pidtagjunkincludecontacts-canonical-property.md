---
title: Propriedade canônica PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387017"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propriedade canônica PidTagJunkIncludeContacts

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica se os endereços de email dos contatos na pasta Contatos são tratados especialmente em relação ao filtro de spam.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificador:  <br/> |0x6100  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentários

Se definido como "0x00000001", esses endereços de email devem popular a parte de endereço de e-mail de contato "confiáveis" da restrição de regra de lixo eletrônico, de forma que os emails desses endereços é tratado como "não é lixo eletrônico". Se definido como "0x00000000", endereços de email da pasta Contatos não devem ser adicionados a regra de lixo eletrônico e a seção da regra deve ser NULL.
  
Se essa propriedade estiver presente com um valor de "0x00000001" e se o contato adicionado tem os endereços de email que não ainda foram incluídos na seção contatos confiáveis da regra lixo eletrônico, esses endereços de email devem ser adicionados para a restrição. Se essa propriedade for "0x00000000", nenhuma ação é necessária.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite a manipulação das listas de permitir/bloquear e a determinação das mensagens de lixo eletrônico.
    
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

